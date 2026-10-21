# System Baseline Report

## Environment

- Platform: KillerCoda Ubuntu Playground
- Capture time (from `top`): 04:35:41, uptime 7 min
- Hostname prompt: `root@ubuntu`

## Host Baseline Metrics

| Metric | Value |
|--------|-------|
| Total RAM available | 1.9Gi (1903.2 MiB) |
| Total Storage capacity of root (/) | 19G (`/dev/vda1`) |

## Additional Baseline Observations

| Metric | Value |
|--------|-------|
| RAM used / free / available | 413Mi / 1.2Gi / 1.5Gi |
| Swap total / used | 1.0Gi / 0B |
| Root (/) used / available / use% | 5.5G / 13G / 30% |
| Load average (1m, 5m, 15m) | 0.00, 0.03, 0.01 |
| CPU idle | 100.0% |
| Processes (total / running / sleeping / zombie) | 129 / 1 / 128 / 0 |

## Why Check Disk Space Before a Traffic Surge

Checking disk space before a massive traffic surge is critical because logs, caches, and temporary files can grow rapidly under load, and a full root filesystem can prevent the server from writing logs, serving requests, or staying online — turning a traffic spike into a full outage.
