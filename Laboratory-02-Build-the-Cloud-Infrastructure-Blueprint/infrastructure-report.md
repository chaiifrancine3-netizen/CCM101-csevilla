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

## 🧪 Investigation Summary

The KillerCoda environment is a virtualized Linux server running **Ubuntu 24.04 LTS (Noble)**. During my investigation, I found that it has **1 vCPU**, around **1.9 GiB of RAM**, and a **19 GiB root disk**.

The system is running with the **KVM hypervisor** and has different mounted filesystems used for the operating system, boot files, temporary storage, and shared memory.

For networking, the main interface is `enp1s0`, which has the private IP address `172.30.1.2/24`. I also found a Docker bridge with the address `172.17.0.1/16`, which is used for container networking.

This investigation helped me become more familiar with using Linux commands to check a server's resources and configuration. I learned how to identify the operating system, CPU, RAM, disk storage, mounted filesystems, hostname, and IP address. It also helped me understand the basic components that make up a cloud server and why checking these details is important before deploying infrastructure.

```text
Interface: enp1s0
IP Address: 172.30.1.2/24
