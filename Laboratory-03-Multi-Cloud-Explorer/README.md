# 🔵 Laboratory 03 – Multi-Cloud Explorer

## 🔷 Mission Overview

This laboratory activity explores three major public cloud platforms: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP).

The goal of this activity is to compare their services, analyze different business requirements, and recommend suitable cloud solutions.

---

## 🔷 Cloud Platforms

The three platforms investigated in this laboratory are:

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud Platform (GCP)

---

## 🔷 Linux Investigation

I used KillerCoda to investigate a Linux server environment.

### 🔹 Operating System

Command used:

```bash
cat /etc/os-release
````

Result:

> **Ubuntu 24.04.4 LTS (Noble Numbat)**

The Linux server is running Ubuntu 24.04.4 LTS with version ID 24.04 and codename Noble Numbat.

---

### 🔹 CPU Information

Command used:

```bash
lscpu
```

Result:

> **CPU:** 1
> **Architecture:** x86_64
> **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
> **CPU Frequency:** 2.0 GHz
> **Core(s) per socket:** 1
> **Thread(s) per core:** 1
> **Socket(s):** 1
> **Hypervisor:** KVM

The server has one virtual CPU based on an Intel Xeon E312xx processor.

---

### 🔹 Memory

Command used:

```bash
free -h
```

Result:

> **Total Memory:** 1.9 GiB
> **Used Memory:** 410 MiB
> **Free Memory:** 870 MiB
> **Available Memory:** 1.5 GiB
> **Swap:** 1.0 GiB

---

### 🔹 Disk Space

Command used:

```bash
df -h
```

Result:

> **Main Disk:** 19G
> **Used:** 5.4G
> **Available:** 13G
> **Usage:** 30%
> **Mounted on:** `/`

The server also has an 881M `/boot` partition and a 105M `/boot/efi` partition.

---

## 🔷 Cloud Hosting Options

If this Linux server were migrated to the cloud, it could be hosted using virtual machine services from all three major cloud providers.

### 🔹 AWS

The server could be hosted using:

* Amazon EC2
* Amazon EBS
* Amazon VPC

**Amazon EC2** could host the Ubuntu Linux virtual machine.
**Amazon EBS** could provide persistent disk storage for the operating system and files.
**Amazon VPC** could provide the virtual networking environment for the server.

---

### 🔹 Microsoft Azure

The server could be hosted using:

* Azure Virtual Machines
* Azure Managed Disks
* Azure Virtual Network

**Azure Virtual Machines** could host the Ubuntu Linux server.
**Azure Managed Disks** could provide persistent storage for the server.
**Azure Virtual Network** could provide networking for the virtual machine.

---

### 🔹 Google Cloud

The server could be hosted using:

* Compute Engine
* Persistent Disk
* Virtual Private Cloud

**Compute Engine** could host the Ubuntu Linux virtual machine.
**Persistent Disk** could provide storage for the operating system and data.
**Virtual Private Cloud** could provide the networking environment for the server.

These services provide virtual computing, storage, and networking resources that can be used to host Linux workloads.



## 🔷 Screenshot Evidence

The Linux terminal investigation screenshot is stored in: Screenshots Folder.

---

### 🔵 My brief results

| 🔹 Category | 🔵 Result |
|---|---|
| **Operating System** | Ubuntu 24.04.4 LTS (Noble Numbat) |
| **Architecture** | x86_64 |
| **CPU** | 1 × Intel Xeon E312xx |
| **CPU Frequency** | 2.0 GHz |
| **Memory** | 1.9 GiB |
| **Available Memory** | 1.5 GiB |
| **Swap** | 1.0 GiB |
| **Main Disk** | 19 GB |
| **Disk Used** | 5.4 GB |
| **Disk Available** | 13 GB |
| **Disk Usage** | 30% |

