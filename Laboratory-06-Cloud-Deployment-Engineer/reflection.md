# Reflection

## 1. How does writing a `docker-compose.yml` file make a cloud engineer's job easier?

A Compose file turns a fragile, multi-step manual process into a single
repeatable command. With `docker run`, I had to remember every flag —
network creation, port mappings, environment variables, correct start
order — and retype them correctly each time. One typo and the app
couldn't find the database. With `docker-compose.yml`, all of that is
declared once, version-controlled in Git, and reproducible on any machine
by running `docker-compose up -d`. It's the difference between a recipe
written from memory and a recipe written down.

## 2. What happens if you make an indentation error (like using a Tab instead of Spaces) in a YAML file?

YAML fails fast. Docker Compose will refuse to parse the file and throw an
error like `found character '\t' that cannot start any token` or
`did not find expected key`, pointing to the offending line. Unlike a
runtime bug, an indentation mistake doesn't partially work — the file
simply won't load. That's actually a good thing: it forces me to fix the
problem before anything deploys, and `docker-compose config` lets me
validate the syntax before touching a live stack.

## 3. Why did we use environment variables (like `MYSQL_PASSWORD`) in the Compose file?

Environment variables separate **configuration from code**. The same
`nextcloud` and `mariadb` images work in development, staging, and
production — only the injected values change. Using `MYSQL_PASSWORD`,
`MYSQL_DATABASE`, and `MYSQL_HOST` lets the two containers agree on
credentials and connection details without hardcoding them into an image.
It also keeps secrets out of the container itself, so I can rotate a
password by editing one line (or better, an untracked `.env` file) instead
of rebuilding anything.

## 4. How did it feel to deploy a fully functional enterprise cloud storage system in just a few minutes?

Honestly, a little surreal. Nextcloud is the kind of tool I'd expect to
take an afternoon of Apache configuration, PHP extensions, and database
setup. Instead, `docker-compose up -d` pulled two images and, within a
couple of minutes, I was staring at the real Nextcloud setup screen in my
browser. The complexity was still there — it was just hidden behind a
well-written blueprint.

## 5. How has your understanding of Cloud Computing evolved since Mission 1?

In Mission 1 I thought of the cloud as "someone else's servers." Now I
see it as **composable infrastructure defined by code**. Containers,
service discovery, environment-based configuration, and declarative
orchestration are the building blocks — the same ideas behind Kubernetes,
ECS, and every major cloud platform. The shift from imperative commands to
declarative files is the same shift the whole industry made, and this lab
made that click for me.
