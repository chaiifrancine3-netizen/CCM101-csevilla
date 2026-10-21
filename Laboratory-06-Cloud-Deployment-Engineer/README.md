# Laboratory 06 – Cloud Deployment Engineer

## Mission Overview

This laboratory mission documents the deployment of a **two-tier cloud
application** using Docker Compose. The stack consists of a **Nextcloud
web/application tier** and a **MariaDB database tier**, deployed as two
isolated containers on a private KillerCoda Ubuntu playground. The lab
covers the full lifecycle: researching multi-tier architecture, writing
the infrastructure as code, deploying the stack, accessing the private
cloud via a proxied port, and tearing it down gracefully.

The resulting deployment demonstrates the difference between ad-hoc
`docker run` commands and declarative `docker-compose` orchestration, and
shows how Docker's internal DNS lets containers find each other by service
name instead of hardcoded IPs.

## Objectives

- Research and document two-tier architecture (web/application tier vs.
  database tier) and justify separating them into different containers.
- Write a valid `docker-compose.yml` blueprint defining a Nextcloud
  application service and a MariaDB database service.
- Deploy the multi-container stack with `docker-compose up -d` and verify
  both containers are running.
- Access the Nextcloud web interface through KillerCoda's port proxy on
  port 8080.
- Gracefully tear down the infrastructure with `docker-compose down`.
- Produce technical documentation explaining each Compose concept to
  another engineer.

## Commands Executed

```bash
# 1. Create the project directory
mkdir nextcloud-deployment
cd nextcloud-deployment

# 2. Open nano to write the Compose blueprint
nano docker-compose.yml
# (pasted the YAML for the `database` and `app` services)

# 3. Deploy the full stack in the background
docker-compose up -d

# 4. Verify both containers are running
docker-compose ps

# 5. Access Nextcloud via KillerCoda's Traffic/Ports panel
#    → entered port 8080 → clicked "Access"
#    → Nextcloud setup screen appeared at /index.php

# 6. Gracefully shut down the entire infrastructure
docker-compose down

# 7. Verify the teardown
docker-compose ps
```

## Skills Learned

- **Multi-tier architecture**: distinguishing the web/application tier
  (serves UI, handles HTTP requests) from the database tier (persists
  data), and explaining why separation improves scaling, security, and
  maintainability.
- **Infrastructure as Code (IaC)**: writing declarative
  `docker-compose.yml` files instead of imperative `docker run` commands.
- **YAML syntax**: strict indentation rules, list items, top-level keys,
  and the consequences of a single misplaced space.
- **Docker Compose service discovery**: using the `MYSQL_HOST` environment
  variable and Compose's embedded DNS so containers resolve each other by
  **service name** rather than IP.
- **Container orchestration**: `services:`, `image:`, `environment:`,
  `ports:`, and the lifecycle of `up -d`, `ps`, and `down`.
- **Port forwarding in ephemeral playgrounds**: using KillerCoda's
  Traffic/Ports panel to expose a container port to a browser.
- **Graceful teardown**: understanding that `docker-compose down`
  removes containers **and** the auto-created network, while leaving
  images cached.
- **Technical documentation**: translating a working deployment into a
  reproducible guide another engineer can follow.

## Repository Contents

| File | Description |
|---|---|
| `multi-tier-architecture.md` | Two-tier architecture research |
| `docker-compose-guide.md` | Technical guide to the Compose blueprint |
| `docker-compose.yml` | The deployable Nextcloud + MariaDB blueprint |
| `reflection.md` | Personal reflection on the lab |
| `screenshots/` | Deployment, UI, and teardown proof |
