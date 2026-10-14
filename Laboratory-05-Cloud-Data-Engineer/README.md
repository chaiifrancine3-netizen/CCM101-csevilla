
# 🎀 Laboratory 05 – Cloud Data Engineer

> 🌸 **CCM101 – Cloud Computing**

![Mission](https://img.shields.io/badge/Mission-Object%20Storage-ff69b4?style=flat-square)
![Docker](https://img.shields.io/badge/Tool-Docker-ff85a2?style=flat-square)
![MinIO](https://img.shields.io/badge/Service-MinIO-ffb6c1?style=flat-square)

*Learning cloud storage, one container at a time. 💗*

---

## 🌷 Mission Overview

This laboratory focused on deploying **MinIO**, an S3-compatible object storage server, using Docker. The activity covered launching the server, configuring administrator credentials, exposing network ports, verifying the container, and managing files through the MinIO Web Console.

The mission provided hands-on experience with cloud object storage and the tools commonly used to deploy and manage storage services.

## 🎯 Objectives

- 🌸 Deploy MinIO using Docker.
- 🌸 Configure the API and Web Console ports.
- 🌸 Set administrator credentials using environment variables.
- 🌸 Verify the running container and inspect server logs.
- 🌸 Access the MinIO Web Console.
- 🌸 Create a bucket named `client-photos`.
- 🌸 Upload `UEP LOGO.png` to the bucket.
- 🌸 Document the deployment procedures using Markdown.

## 🧰 Tools Used

| Tool | Purpose |
|---|---|
| 💻 KillerCoda Ubuntu Playground | Provided the Linux environment. |
| 🐳 Docker | Downloaded the image and deployed the container. |
| 🌸 MinIO | Provided the S3-compatible object storage service. |
| 🌐 MinIO Web Console | Managed buckets and uploaded objects. |
| ⌨️ Linux Terminal | Executed deployment and verification commands. |
| 💗 GitHub Markdown | Documented the laboratory activity. |

## 💖 Skills Learned

- Deploying containerized applications using Docker.
- Configuring applications through environment variables.
- Mapping ports between a host and a container.
- Verifying containers using `docker ps`.
- Inspecting startup logs with `docker logs`.
- Checking container status with `docker inspect`.
- Navigating the MinIO Web Console.
- Creating buckets and uploading objects.
- Understanding S3-compatible object storage.
- Writing technical documentation using Markdown.

## 🌸 Deployment Summary

| Item | Result |
|---|---|
| Storage Service | MinIO |
| Container Name | `minio-server` |
| Docker Image | `pgsty/minio` |
| API Port | `9000` |
| Web Console Port | `9001` |
| Container Status | 🟢 Running |
| Bucket Name | `client-photos` |
| Uploaded File | `UEP LOGO.png` |

## 🎀 Project Structure

```text
Laboratory-05-Cloud-Data-Engineer/
├── README.md
├── minio-deployment.md
└── screenshots/
    ├── minio-deployed.png
    └── minio-bucket.png
```

🌸 **Mission Accomplished!** 💗

*Built with Docker, MinIO, and a little pink magic.*

