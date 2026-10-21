# Docker Compose Guide

This guide explains the `docker-compose.yml` blueprint used to deploy the
two-tier Nextcloud stack: a MariaDB **database tier** and a Nextcloud
**web/application tier**.

---

## The Full Blueprint

```yaml
version: '3'

services:
  database:
    image: mariadb:10.6
    environment:
      - MYSQL_ROOT_PASSWORD=cloudnova_root
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user

  app:
    image: nextcloud
    ports:
      - 8080:80
    environment:
      - MYSQL_PASSWORD=cloudnova_pass
      - MYSQL_DATABASE=nextcloud_db
      - MYSQL_USER=nextcloud_user
      - MYSQL_HOST=database
```

Two services, one `version:` declaration. That's the whole deployment.

---

## 1. What does the `services:` block do?

The `services:` block is the **top-level declaration of every container**
that Compose will build, start, and wire together. It is the heart of any
Compose file — remove it and nothing runs.

Inside it, each child key is a **service name**:

- `database:` — the MariaDB service
- `app:` — the Nextcloud service

Each service is **not** a container. It is a **description** of what
container(s) to create:

- `image:` — which Docker image to pull and run
- `environment:` — variables injected into the container
- `ports:` — host-to-container port mappings
- `volumes:`, `networks:`, `depends_on:` — optional wiring

When you run `docker-compose up -d`, Compose parses `services:`, creates a
default bridge network, then **starts each service as a container** with its
configuration injected. Service names become **DNS names** inside the
network — which is exactly how the app finds the database (see section 2).

---

## 2. How does the `app` container find the `database` container?

The answer is three lines in the YAML working together:

```yaml
  app:
    environment:
      - MYSQL_HOST=database
```

and

```yaml
  database:
    ...
```

### The mechanism, step by step

1. `MYSQL_HOST=database` sets an **environment variable** in the `app`
   container. The value is not an IP address — it is the literal string
   `database`.

2. `database` is the **service name** declared in the `services:` block.
   Compose uses service names as **hostnames** on the network it creates.

3. When Compose starts the stack, it creates a **default bridge network**
   (named `nextcloud-deployment_default` if your project folder is
   `nextcloud-deployment`) and attaches **both** containers to it.

4. Compose also runs an **embedded DNS server** on that network
   (at `127.0.0.11`). When the app container resolves `database`, this DNS
   answers with the database container's **current IP**.

5. Nextcloud's PHP code reads `MYSQL_HOST`, opens a MySQL connection to
   `database:3306`, and Docker's DNS resolves it transparently.

### Why this is powerful

- No IP addresses are hardcoded — if the database container restarts and
  gets a new IP, the app still connects via the name `database`.
- No `/etc/hosts` editing, no manual network configuration.
- The two containers are **isolated** — the `database` container is not
  published to the host (`ports:` is only on `app`), so only the app tier
  can reach the database.

If you had used `MYSQL_HOST=localhost`, the app would look for MariaDB
**inside its own container** and fail. That is the single most common
Compose mistake.

---

## 3. `docker run` vs. `docker-compose up -d`

Mission 4 used `docker run` to launch a **single** container. Mission 6 uses
`docker-compose up -d` to launch **the whole stack**. The difference is not
just convenience — it changes how the deployment is designed.

| Aspect | `docker run` | `docker-compose up -d` |
|---|---|---|
| **Scope** | One container per command | Every service in `docker-compose.yml` at once |
| **Config** | Flags on the command line (`-e`, `-p`, `-v`, `--network`) | Declared in YAML, version-controlled |
| **Networking** | Manually `docker network create` + attach each container | Compose auto-creates a default network for all services |
| **Discovery** | Hardcode container names or IPs | Services reach each other **by service name** |
| **Order** | Start containers in the right order by hand | `depends_on:` defines startup order |
| **Repeatability** | Easy to typo; each command is one-off | Same file → same result on any machine |
| **Teardown** | `docker stop` + `docker rm` per container | `docker-compose down` removes containers **and** network |
| **Best for** | Quick tests, single containers | Multi-container apps, dev, CI/CD, production-like stacks |

### The `-d` flag

`-d` means **detached**. `docker-compose up` attaches to the containers'
logs and blocks your terminal; `docker-compose up -d` runs them in the
**background** and returns your prompt — ideal for long-running services
like a web app and a database.

### In short

`docker run` is the **single-container primitive**. `docker-compose` is the
**orchestration layer** — the same Docker engine, but declarative,
repeatable, and aware of multiple services. For a two-tier deployment,
`docker run` would require: creating a network, starting MariaDB, waiting for
it, finding its IP or name, then starting Nextcloud with that host configured
— every command typed by hand. Compose encodes all of that in one file and
one command.

---

## Quick Reference

| Compose command | What it does |
|---|---|
| `docker-compose up -d` | Pull, create, and start all services detached |
| `docker-compose ps` | Show status of services in this project |
| `docker-compose logs -f app` | Follow the app service's logs |
| `docker-compose restart app` | Restart one service |
| `docker-compose down` | Stop and remove all containers **and** the network |
| `docker-compose config` | Validate and print the normalized config |
