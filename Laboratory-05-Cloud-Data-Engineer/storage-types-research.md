# 🌸 Research: Types of Cloud Storage 🌸

![cloud](https://img.shields.io/badge/cloud-storage-ff85b3?style=for-the-badge&labelColor=ffe4ec)
![status](https://img.shields.io/badge/status-researched-ffb6c1?style=for-the-badge&labelColor=ffe4ec)

---

## 📊 Comparison Table

| Storage Type | Description (How it stores data) | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| 🧱 **Block Storage** | Splits data into fixed-size blocks, each with a unique address. No metadata or file hierarchy—the OS decides how to assemble blocks. | Databases, virtual machine disks, and high-performance transactional workloads requiring low latency. | AWS Elastic Block Store (EBS), Google Persistent Disk, Azure Disk Storage |
| 📁 **File Storage** | Stores data in a hierarchical folder/file structure with metadata (name, path, permissions). Accessed via network protocols (NFS, SMB). | Shared file systems for teams, home directories, and legacy applications that need POSIX compliance. | AWS Elastic File System (EFS), Azure Files, Google Filestore |
| 🪣 **Object Storage** | Stores data as discrete "objects" in a flat address space. Each object contains the data, metadata, and a unique ID (key). Accessed via HTTP/REST APIs. | Unstructured data at scale: images, videos, backups, logs, and static website assets. | AWS S3, Google Cloud Storage, Azure Blob Storage |

---

## 💖 Recommendation to the Client

### 🎀 Object Storage for your photo-sharing app

For your photo-sharing application, **Object Storage** is the best choice because it is designed to handle millions of unstructured files (images) without the performance bottlenecks of a file hierarchy or the management overhead of block volumes.

Each photo is stored as an independent object with its own metadata (such as upload date, content type), making it easy to retrieve, replicate, and serve via a URL. Object storage also scales horizontally almost infinitely and offers built-in durability, versioning, and lifecycle policies perfect for user-uploaded content that will grow rapidly.

**Why Object Storage wins 🌷**

- ✅ Massive scalability for millions of images
- ✅ Metadata per object for smart retrieval & management
- ✅ Built-in versioning and lifecycle rules
- ✅ Direct HTTP/URL access ideal for web and mobile
- ✅ High durability (often 99.999999999%)
