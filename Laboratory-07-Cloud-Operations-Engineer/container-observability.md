# Container Observability

---

## Application Logging with Nginx

### Overview

The `client-website` Nginx container was deployed on port 8080 and received traffic simulating a user visiting the site. Application logs were retrieved using the Docker CLI to inspect how the server handled each request.

### Command Used

```bash
docker logs client-website

---

## Real-Time Container Metrics

Command used: `docker stats`

| Metric | Value |
|--------|-------|
| Memory Usage | 2.746MiB |
| CPU % | 0.00% |

At the time of the screenshot, the `client-website` container was consuming **2.746MiB** of memory (0.14% of its 1.859GiB limit) and **0.00%** CPU.
---
