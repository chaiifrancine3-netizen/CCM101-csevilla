
# Laboratory Activity 8

## Mission 8: The Cloud Security Engineer

### Mission Overview

This laboratory activity focuses on securing a Linux server using the UFW firewall. It involves deploying an Nginx web application, checking network access, configuring firewall rules, and allowing only necessary traffic.

### Objectives

- Understand the Principle of Least Privilege.
- Identify the attack surface of a server.
- Understand the Default Deny Policy.
- Deploy an Nginx web server using Docker.
- Configure UFW firewall rules.
- Allow SSH and HTTP application traffic.
- Monitor and verify firewall configurations.

### Commands Executed

| Command | Description |
|---|---|
| `docker run -d --name secure-web-app -p 8080:80 nginx` | Deploys Nginx container. |
| `docker ps` | Displays running containers. |
| `curl http://localhost:8080` | Tests the web application. |
| `sudo ufw allow ssh` | Allows SSH access. |
| `sudo ufw default deny incoming` | Blocks incoming traffic by default. |
| `sudo ufw default allow outgoing` | Allows outgoing traffic. |
| `sudo ufw enable` | Activates the firewall. |
| `sudo ufw status verbose` | Displays firewall status. |
| `sudo ufw allow 8080/tcp` | Allows TCP traffic on port 8080. |
| `sudo ufw status numbered` | Displays numbered firewall rules. |

### Skills Learned

- Linux Server Security
- UFW Firewall Configuration
- Docker Container Deployment
- Network Port Management
- Attack Surface Reduction
- Principle of Least Privilege
- Firewall Monitoring

### Screenshots

- `vulnerable-app-running.png` – Shows the running Nginx application.
- `firewall-activated.png` – Shows the active firewall and default deny policy.
- `firewall-port-allowed.png` – Shows the configured firewall rules and successful application test.

### Mission Status

**Completed** – Successfully deployed a web application and configured UFW firewall rules to secure the server.

