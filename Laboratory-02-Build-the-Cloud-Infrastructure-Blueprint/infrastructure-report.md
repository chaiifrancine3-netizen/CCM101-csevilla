# Checkpoint 3 – Cloud Infrastructure Components

## 1. Compute Resources

* **Purpose:** Compute resources provide the processing power (CPU) and working memory (RAM) required to execute instructions, run applications, and manage workloads.
* **Importance in Cloud Computing:** In cloud computing, compute power is virtualized and provisioned on-demand. This allows workloads to scale dynamically without physical hardware constraints, enabling multi-tenancy and efficient resource allocation.
* **KillerCoda Linux Environment Findings:**
  * **vCPU:** 1 virtual core (`CPU(s): 1`), identified as an `Intel Xeon E312xx (Sandy Bridge)` running under the **KVM** hypervisor.
  * **Memory (RAM):** Total memory of `1.9 GiB` (`free -h`), with `873 MiB` free and `1.0 GiB` configured as Swap space.

---

## 2. Storage Resources

* **Purpose:** Storage resources provide persistent and non-persistent capacity to save the operating system files, application binaries, logs, and user data.
* **Importance in Cloud Computing:** Cloud storage abstracts physical disks into flexible volumes (Block Storage, Object Storage, or File Storage). It ensures data persistence, replication, fast I/O throughput, and high availability across distributed nodes.
* **KillerCoda Linux Environment Findings:**
  * **Root Filesystem (`/`):** A `19 GiB` virtual disk partition (`/dev/vda1`) formatted with the `ext4` filesystem, having `13 GiB` available.
  * **Temporary In-Memory Storage:** Multiple `tmpfs` mounts (e.g., `/run` at `191M`, `/dev/shm` at `952M`) used for fast, volatile memory storage.
  * **Boot Storage:** `/dev/vda16` (`881M`, `ext4`) mounted on `/boot` and `/dev/vda15` (`105M`, `vfat`) for EFI boot support.

---

## 3. Networking Resources

* **Purpose:** Networking resources establish communication channels between instances, host hypervisors, internal container runtimes, and external networks (Internet).
* **Importance in Cloud Computing:** Cloud networking uses Software-Defined Networking (SDN) to deliver Virtual Private Clouds (VPCs), subnets, routing, and firewalling. This guarantees secure data transmission, workload isolation, and external accessibility.
* **KillerCoda Linux Environment Findings:**
  * **Loopback Interface (`lo`):** `127.0.0.1/8` for local internal host communication.
  * **Primary Network Interface (`enp1s0`):** Virtual Ethernet interface assigned with the private IP `172.30.1.2/24`.
  * **Container Bridge Interface (`docker0`):** Virtual bridge assigned with `172.17.0.1/16` to manage internal container networking.

---

## 4. Operating System

* **Purpose:** The Operating System acts as the core software layer that manages hardware/virtualized resources, handles system calls, controls file access, and provides the user space/CLI environment.
* **Importance in Cloud Computing:** Cloud-optimized OS distributions provide lightweight, secure, and standardized images (such as cloud-init enabled images) designed for rapid boot times, headless remote management, and automated orchestration.
* **KillerCoda Linux Environment Findings:**
  * **Distribution:** Ubuntu 24.04 LTS (`noble`) verified via `lsb_release -a`.
  * **Kernel Version:** Linux kernel `6.8.0-138-generic` verified via `uname -r`.
  * **Hostname:** Configured as `ubuntu`.
