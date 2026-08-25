# 🖥️ System Information

This document contains the system information collected from the **KillerCoda Ubuntu Linux environment** using basic Linux commands.

---

## 🐧 Linux Distribution

### Command

```bash
lsb_release -a

### Output

```text
Distributor ID: Ubuntu
Description: Ubuntu 24.04 LTS
Release: 24.04
Codename: noble
```

### 📋 Summary

| Information      | Value     |
| ---------------- | --------- |
| **Distribution** | Ubuntu    |
| **Version**      | 24.04 LTS |
| **Codename**     | Noble     |

---

## ⚙️ Kernel Version

### Command

```bash
uname -r
```

### Output

```text
6.8.0-136-generic
```

### 📋 Summary

| Information        | Value               |
| ------------------ | ------------------- |
| **Kernel Version** | `6.8.0-136-generic` |

---

## 💻 CPU Information

### Command

```bash
lscpu
```

### Important Findings

```text
Architecture:        x86_64
CPU(s):              1
Vendor ID:           GenuineIntel
Model name:          Intel Xeon E312xx (Sandy Bridge, IBRS update)
Thread(s) per core:  1
Core(s) per socket:  1
Socket(s):           1
Hypervisor vendor:   KVM
Virtualization type: full
```

### 📋 CPU Summary

| Information        | Value                            |
| ------------------ | -------------------------------- |
| **Architecture**   | x86_64                           |
| **CPU Cores**      | 1                                |
| **CPU Threads**    | 1                                |
| **CPU Model**      | Intel Xeon E312xx (Sandy Bridge) |
| **CPU Frequency**  | 2.0 GHz                          |
| **Hypervisor**     | KVM                              |
| **Virtualization** | Full virtualization              |

---

## 💾 Total Memory

### Command

```bash
free -h
```

### Output

```text
               total        used        free      shared  buff/cache   available
Mem:           1.9Gi       433Mi       768Mi       1.1Mi       876Mi       1.4Gi
Swap:          1.0Gi          0B       1.0Gi
```

### 📋 Memory Summary

| Resource |   Total |    Used |    Free | Available |
| -------- | ------: | ------: | ------: | --------: |
| **RAM**  | 1.9 GiB | 433 MiB | 768 MiB |   1.4 GiB |
| **Swap** | 1.0 GiB |     0 B | 1.0 GiB |   1.0 GiB |

---

## 💿 Available Disk Space

### Command

```bash
df -h
```

### Output

```text
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M  1012K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M  84K    952M   1% /dev/shm
tmpfs           5.0M     0    5.0M   0% /run/lock
/dev/vda16      881M  117M   703M  15% /boot
/dev/vda15      105M  6.2M    99M   6% /boot/efi
tmpfs           191M  8.0K   191M   1% /run/user/1001
```

### 📋 Storage Summary

| Filesystem   | Size |  Used | Available | Mount Point      |
| ------------ | ---: | ----: | --------: | ---------------- |
| `/dev/vda1`  |  19G |  5.4G |       13G | `/`              |
| `/dev/vda16` | 881M |  117M |      703M | `/boot`          |
| `/dev/vda15` | 105M |  6.2M |       99M | `/boot/efi`      |
| `tmpfs`      | 191M | 1012K |      190M | `/run`           |
| `tmpfs`      | 952M |   84K |      952M | `/dev/shm`       |
| `tmpfs`      | 5.0M |     0 |      5.0M | `/run/lock`      |
| `tmpfs`      | 191M |  8.0K |      191M | `/run/user/1001` |

---

## 📊 System Overview

| Component                     | Finding                          |
| ----------------------------- | -------------------------------- |
| 🐧 **Operating System**       | Ubuntu 24.04 LTS                 |
| ⚙️ **Kernel**                 | `6.8.0-136-generic`              |
| 💻 **CPU**                    | Intel Xeon E312xx (Sandy Bridge) |
| 🧠 **CPU Cores**              | 1                                |
| 💾 **RAM**                    | 1.9 GiB                          |
| 🔄 **Swap**                   | 1.0 GiB                          |
| 💿 **Root Disk**              | 19 GiB                           |
| 📂 **Available Root Storage** | 13 GiB                           |
| 🖥️ **Hypervisor**            | KVM                              |
| 🏗️ **Architecture**          | x86_64                           |

---

## 🧪 Summary

The KillerCoda environment is a **virtualized Ubuntu 24.04 LTS server** running on the KVM hypervisor. It provides **1 virtual CPU core**, **1.9 GiB of RAM**, and a **19 GiB root filesystem**, with approximately **13 GiB of available storage**.

Using commands such as `lsb_release`, `uname`, `lscpu`, `free`, and `df`, I was able to inspect the main hardware and software resources of the cloud environment. This helped me understand how Linux commands can be used to collect important infrastructure information and perform a basic system audit.

```
```
