
# Checkpoint 6 – Firewall Configuration

## 1. Allow SSH Access

Command:

```bash
sudo ufw allow ssh
```

This command allows SSH connections through port 22 so administrators can remotely manage the server.

## 2. Configure Default Deny Policy

Commands:

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

These commands block incoming connections by default while allowing outgoing connections from the server.

## 3. Enable Firewall

Command:

```bash
sudo ufw enable
```

This activates the firewall and applies the configured security rules.

## 4. Allow Port 8080

Command:

```bash
sudo ufw allow 8080/tcp
```

This allows TCP traffic through port 8080 so users can access the deployed web application.

## 5. Verify Firewall Rules

Commands:

```bash
sudo ufw status verbose
sudo ufw status numbered
```

These commands display the firewall status and configured rules.

## 6. Security Reminder

If `sudo ufw enable` is executed before `sudo ufw allow ssh`, SSH connections may be blocked by the default deny incoming policy, potentially locking remote administrators out of the server.

