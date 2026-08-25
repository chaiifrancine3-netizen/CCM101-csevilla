# 🔎 Checkpoint 2 — Investigate the Cloud Server

## 🖥️ Cloud Server Investigation

Using the KillerCoda terminal, I investigated the Linux environment to identify its operating system, hardware resources, storage, networking configuration, and hostname.

## 📋 Infrastructure Findings

| Component | Finding |
|---|---|
| 🐧 **Operating System** | Ubuntu 24.04 LTS (Noble) |
| ⚙️ **Kernel Version** | `6.8.0-138-generic` |
| 💻 **CPU Model** | Intel Xeon E312xx (Sandy Bridge) |
| 🧠 **CPU Cores** | 1 vCPU |
| 💾 **Total RAM** | 1.9 GiB |
| 💿 **Disk Capacity** | 19 GiB |
| 📂 **Filesystem** | ext4 |
| 🖥️ **Hostname** | `ubuntu` |
| 🌐 **IP Address** | `172.30.1.2/24` |

## 📂 Mounted File Systems

| Mount Point | Device / Type | Size |
|---|---|---:|
| `/` | `/dev/vda1` — ext4 | 19 GiB |
| `/boot` | `/dev/vda16` — ext4 | 881M |
| `/boot/efi` | `/dev/vda15` — vfat | 105M |
| `/run` | tmpfs | 191M |
| `/dev/shm` | tmpfs | 952M |

The root filesystem (`/`) has approximately **13 GiB of available space**.

## 🌐 Network Information

### Primary Network Interface

```text
Interface: enp1s0
IP Address: 172.30.1.2/24
