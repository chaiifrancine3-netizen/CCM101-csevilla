
# Checkpoint 6 – Technical Documentation

## 1. Backup Script Code

```bash
#!/bin/bash

# Automated Backup Script for CloudNova Technologies

SOURCE_DIR="app-data"
BACKUP_DIR="backups"
TIMESTAMP=$(date +"%Y%m%d_%H%M%S")

echo "Initiating automated backup..."

mkdir -p "$BACKUP_DIR"

tar -czf "$BACKUP_DIR/backup_$TIMESTAMP.tar.gz" "$SOURCE_DIR"

echo "Backup completed successfully at $TIMESTAMP!"
```

## 2. File Permissions

The `chmod +x backup.sh` command gives the Bash script permission to execute. Without this permission, Linux displays a Permission denied error when running the script directly.

## 3. Cron Job Configuration

The Cron expression used is:

```bash
0 2 * * * /root/backup.sh
```

### Cron Field Explanation

| Field | Value | Description |
|---|---|---|
| Minute | 0 | Runs at minute zero. |
| Hour | 2 | Runs at 2:00 AM. |
| Day of Month | * | Runs every day of the month. |
| Month | * | Runs every month. |
| Day of Week | * | Runs every day of the week. |

## 4. Result

The backup script successfully created a compressed `.tar.gz` file containing the application data. The Cron job was also installed and verified using `crontab -l`.

