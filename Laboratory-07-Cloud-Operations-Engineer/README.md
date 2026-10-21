# Laboratory-07: Cloud Operations Engineer

## Mission Overview

This laboratory simulates the day-to-day work of a Cloud Operations Engineer responsible for maintaining the health of a host server and the containers running on it. Starting from a bare KillerCoda Ubuntu Playground, I established a baseline of host resources, deployed an Nginx web server container, generated simulated user traffic (including a failed request), and then used Docker's logging and monitoring tools to observe how the application behaved. The exercise demonstrates that reliable operations depend on knowing both the host and the workload — and on having evidence, not assumptions, when something goes wrong.

## Objectives

- Establish a baseline of host system health by recording RAM, disk capacity, and CPU/process activity.
- Deploy a containerized Nginx web server with the correct name and port mapping.
- Generate realistic traffic, including a deliberate 404 error, to produce observable log data.
- Retrieve and interpret application logs using `docker logs`.
- Capture live container resource consumption using `docker stats`.
- Explain why logs and metrics serve different but complementary troubleshooting purposes.
- Document findings professionally and reflect on the operational lessons learned.

## Monitoring Commands Executed

| Command | Purpose |
|---------|---------|
| `free -h` | Display total, used, free, and available RAM in human-readable units |
| `df -h` | Show disk usage and total capacity of mounted filesystems, including root (`/`) |
| `top` | View active processes, CPU load, and memory usage in real time |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploy the Nginx container in the background on port 8080 |
| `docker ps` | Confirm the container is running and verify the port mapping |
| `curl http://localhost:8080` | Simulate a user visiting the website (HTTP 200) |
| `curl http://localhost:8080/hidden-admin-page` | Simulate a request for a non-existent page (HTTP 404) |
| `docker logs client-website` | Retrieve the application's HTTP access and error logs |
| `docker stats` | View live CPU, memory, and network I/O for running containers |

## Skills Learned

- **Host baseline assessment** — reading `free`, `df`, and `top` output to establish what "normal" looks like before load is applied.
- **Container deployment** — running a named, port-mapped Nginx container in detached mode and verifying it with `docker ps`.
- **Traffic simulation** — using `curl` to generate both successful and failing requests for observability testing.
- **Log analysis** — interpreting Nginx access logs (status codes, timestamps, client IPs) and error logs (missing file causes).
- **Metrics collection** — using `docker stats` to measure CPU and memory consumption against container limits.
- **Distinguishing logs from metrics** — understanding that logs explain *what happened* and metrics show *how much resource is being used*.
- **Operational documentation** — recording evidence and findings in a structured, reviewable format.
- **Troubleshooting discipline** — forming hypotheses and confirming them with commands rather than guessing.

## Repository Contents

- `README.md` — This document
- `system-baseline-report.md` — Host RAM, disk, and process baseline
- `container-observability.md` — Application logs and real-time container metrics
- `reflection.md` — Mission reflection
- `screenshots/` — Evidence captured during the laboratory
