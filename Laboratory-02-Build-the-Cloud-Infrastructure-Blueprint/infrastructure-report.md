# ☁️ Cloud Infrastructure Components

---

### 🧠 1. Compute Resources

* **Purpose:** Provides the primary processing power (CPU) and active workspace (RAM) required to execute system processes, handle calculations, and run workloads.
* **KillerCoda Environment:**
  * **vCPU:** 1 virtual core (`Intel Xeon E312xx @ 2.0GHz`) running on a KVM hypervisor.
  * **Memory:** `1.9 GiB` total RAM with `1.0 GiB` Swap space.
* **Why does it matter?**
  > Compute power is the engine of the cloud. Without virtualized compute capacity, applications cannot execute instructions, scale on demand, or handle concurrent user traffic.

---

### 💾 2. Storage Resources

* **Purpose:** Retains persistent data, system binaries, configuration files, and temporary memory mounts across sessions.
* **KillerCoda Environment:**
  * **Root Disk:** `19 GiB` virtual partition (`/dev/vda1`) formatted in `ext4` with `13 GiB` available.
  * **In-Memory/Boot:** `tmpfs` mounts (`/run`, `/dev/shm`) for volatile cache alongside dedicated `/boot` partitions (`/dev/vda16`, `/dev/vda15`).
* **Why does it matter?**
  > Cloud workloads require reliable block and file storage to save state, retain logs, and ensure critical application data survives server reboots.

---

### 🌐 3. Networking Resources

* **Purpose:** Enables data transmission and routing between cloud instances, internal containers, host hypervisors, and the wider Internet.
* **KillerCoda Environment:**
  * **Primary Interface:** `enp1s0` assigned with private IP `172.30.1.2/24`.
  * **Bridge & Loopback:** `docker0` (`172.17.0.1/16`) for internal container communication and `lo` (`127.0.0.1/8`) for local loopback.
* **Why does it matter?**
  > Networking creates accessibility. Without software-defined connectivity, isolated compute nodes cannot receive user requests, talk to databases, or integrate with external services.

---

### 🐧 4. Operating System

* **Purpose:** Serves as the fundamental software layer that coordinates hardware resources, manages memory/CPU scheduling, and executes user-space utilities.
* **KillerCoda Environment:**
  * **Distribution:** Ubuntu 24.04 LTS (`noble`).
  * **Kernel:** Linux kernel `6.8.0-138-generic`.
* **Why does it matter?**
  > The OS provides the standardized runtime environment and security boundaries necessary to orchestrate, deploy, and manage cloud workloads consistently.
