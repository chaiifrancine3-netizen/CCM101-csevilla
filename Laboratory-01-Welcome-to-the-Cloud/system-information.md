# 🖥️ System Information

This document contains the system information collected from the **KillerCoda Ubuntu Linux environment** using basic Linux commands.

---

## 🐧 Linux Distribution

### Command

```bash
lsb_release -a
```

### Output

```text
Distributor ID: Ubuntu
Description: Ubuntu 24.04 LTS
Release: 24.04
Codename: noble
```

### 📋 Summary

| Information | Value |
|---|---|
| **Distribution** | Ubuntu |
| **Version** | 24.04 LTS |
| **Codename** | Noble |

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

| Information | Value |
|---|---|
| **Kernel Version** | `6.8.0-136-generic` |

---

## 💻 CPU Information

### Command

```bash
lscpu
```

### Output

```text
Architecture:                x86_64
  CPU op-mode(s):            32-bit, 64-bit
  Address sizes:             39 bits physical, 48 bits virtual
  Byte Order:                Little Endian
CPU(s):                      1
  On-line CPU(s) list:       0
Vendor ID:                   GenuineIntel
  BIOS Vendor ID:            Red Hat
  Model name:                Intel Xeon E312xx (Sandy Bridge, IBRS update)
    BIOS Model name:         RHEL-9.6.0 PC (Q35 + ICH9, 2009)  CPU @ 2.0GHz
    BIOS CPU family:         1
    CPU family:              6
    Model:                   42
    Thread(s) per core:      1
    Core(s) per socket:      1
    Socket(s):               1
    Stepping:                1
    BogoMIPS:                7391.99
    Flags:                   fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 syscall nx rdtscp lm constant_tsc rep_good nopl xtopology cpuid tsc_known_freq pni pclmulqdq ssse3 cx16 pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx hypervisor lahf_lm cpuid_fault pti ssbd ibrs ibpb stibp tsc_adjust xsaveopt arat md_clear
Virtualization features:
  Hypervisor vendor:         KVM
  Virtualization type:       full
Caches (sum of all):
  L1d:                       32 KiB (1 instance)
  L1i:                       32 KiB (1 instance)
  L2:                        4 MiB (1 instance)
  L3:                        16 MiB (1 instance)
NUMA:
  NUMA node(s):              1
  NUMA node0 CPU(s):         0
Vulnerabilities:
  Gather data sampling:      Not affected
  Indirect target selection: Mitigation; Aligned branch/return thunks
  Itlb multihit:             KVM: Mitigation: VMX unsupported
  L1tf:                      Mitigation; PTE Inversion
  Mds:                       Mitigation; Clear CPU buffers; SMT Host state unknown
  Meltdown:                  Mitigation; PTI
  Mmio stale data:           Unknown: No mitigations
  Reg file data sampling:    Not affected
  Retbleed:                  Not affected
  Reg file data sampling:    Not affected
  Spec rstack overflow:      Not affected
  Spec store bypass:         Mitigation; Speculative Store Bypass disabled via prctl
  Spectre v1:                Mitigation; usercopy/swapgs barriers and __user pointer sanitization
  Spectre v2:                Mitigation; Retpolines; IBPB conditional; IBRS_FW; STIBP disabled; RSB filling; PBRSB-eIBRS Not affected; BHI Retpoline
  Srbds:                     Not affected
  Tsa:                       Not affected
  Tsx async abort:           Not affected
  Vmscape:                   Not affected
```

### 📋 CPU Summary

| Information | Value |
|---|---|
| **Architecture** | x86_64 |
| **CPU Cores** | 1 |
| **CPU Threads** | 1 |
| **CPU Model** | Intel Xeon E312xx (Sandy Bridge) |
| **CPU Frequency** | 2.0 GHz |
| **Hypervisor** | KVM |
| **Virtualization** | Full virtualization |

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

| Resource | Total | Used | Free | Available |
|---|---:|---:|---:|---:|
| **RAM** | 1.9 GiB | 433 MiB | 768 MiB | 1.4 GiB |
| **Swap** | 1.0 GiB | 0 B | 1.0 GiB | 1.0 GiB |

---

## 💿 Available Disk Space

### Command

```bash
df -h
```

### Output

```text
Filesystem      Size  Used Avail Use% Mounted on
tmpfs           191M 1012K  190M   1% /run
/dev/vda1        19G  5.4G   13G  30% /
tmpfs           952M   84K   952M   1% /dev/shm
tmpfs           5.0M     0   5.0M   0% /run/lock
/dev/vda16      881M  117M   703M  15% /boot
/dev/vda15      105M  6.2M    99M   6% /boot/efi
tmpfs           191M  8.0K   191M   1% /run/user/1001
```

### 📋 Storage Summary

| Filesystem | Size | Used | Available | Mount Point |
|---|---:|---:|---:|---|
| `/dev/vda1` | 19G | 5.4G | 13G | `/` |
| `/dev/vda16` | 881M | 117M | 703M | `/boot` |
| `/dev/vda15` | 105M | 6.2M | 99M | `/boot/efi` |
| `tmpfs` | 191M | 1012K | 190M | `/run` |
| `tmpfs` | 952M | 84K | 952M | `/dev/shm` |
| `tmpfs` | 5.0M | 0 | 5.0M | `/run/lock` |
| `tmpfs` | 191M | 8.0K | 191M | `/run/user/1001` |

---

## 📊 System Overview

| Component | Finding |
|---|---|
| 🐧 **Operating System** | Ubuntu 24.04 LTS |
| ⚙️ **Kernel** | `6.8.0-136-generic` |
| 💻 **CPU** | Intel Xeon E312xx (Sandy Bridge) |
| 🧠 **CPU Cores** | 1 |
| 💾 **RAM** | 1.9 GiB |
| 🔄 **Swap** | 1.0 GiB |
| 💿 **Root Disk** | 19 GiB |
| 📂 **Available Root Storage** | 13 GiB |
| 🖥️ **Hypervisor** | KVM |
| 🏗️ **Architecture** | x86_64 |

---

## 🧪 Summary

The KillerCoda environment is a **virtualized Ubuntu 24.04 LTS server** running on the KVM hypervisor. It provides **1 virtual CPU core**, **1.9 GiB of RAM**, and a **19 GiB root filesystem**, with approximately **13 GiB of available storage**.

Using commands such as `lsb_release`, `uname`, `lscpu`, `free`, and `df`, I was able to inspect the main hardware and software resources of the cloud environment. This helped me understand how Linux commands can be used to collect important infrastructure information and perform a basic system audit.
