# Container Observability

## Application Logging with Nginx

### Overview

The `client-website` Nginx container was deployed on port 8080 and received traffic simulating a user visiting the site. Application logs were retrieved using the Docker CLI to inspect how the server handled each request.

### Command Used

```bash
docker logs client-website
