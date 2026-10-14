
# 🌸 MinIO Object Storage Deployment

> 💗 **CCM101 – Cloud Computing | Laboratory 05: Cloud Data Engineer**

![Status](https://img.shields.io/badge/Status-Running-ff69b4?style=flat-square)
![Storage](https://img.shields.io/badge/Storage-MinIO-ff85a2?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Docker-ffb6c1?style=flat-square)

---

## 🎀 1. Mission Overview

This laboratory activity focused on deploying **MinIO**, an S3-compatible object storage server, using Docker in the KillerCoda Ubuntu Playground. The activity introduced the fundamentals of cloud object storage, including container deployment, environment variable configuration, port mapping, bucket creation, and file uploading through the MinIO Web Console.

## 🌷 2. Docker Deployment Command

The following command was used to deploy the MinIO server:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=<REDACTED>" \
  pgsty/minio server /data --console-address ":9001"
```

### 💕 Command Breakdown

| Command | Description |
|---|---|
| `docker run` | Creates and starts a container. |
| `-d` | Runs the container in the background. |
| `-p 9000:9000` | Maps the MinIO API port. |
| `-p 9001:9001` | Maps the MinIO Web Console port. |
| `--name minio-server` | Assigns a name to the container. |
| `-e "MINIO_ROOT_USER=cloudadmin"` | Sets the administrator username. |
| `-e "MINIO_ROOT_PASSWORD=..."` | Sets the administrator password. |
| `pgsty/minio` | Specifies the Docker image. |
| `server /data` | Starts the server and uses `/data` as its storage directory. |
| `--console-address ":9001"` | Configures the Web Console to listen on port 9001. |

### 🌸 Environment Variables

The `-e` flag passes environment variables into a Docker container during startup.

- 💗 `MINIO_ROOT_USER` defines the root administrator username.
- 💗 `MINIO_ROOT_PASSWORD` defines the root administrator password.

These variables configure the credentials used to administer the MinIO server. Sensitive credentials should never be committed to a public repository.

## 🌷 3. Port Configuration

| Service | Port | Purpose |
|---|---:|---|
| MinIO API | `9000` | Handles S3-compatible object storage requests. |
| MinIO Web Console | `9001` | Provides a browser-based management interface. |

The Web Console uses port **9001**. In KillerCoda, it can be accessed through the appropriate port preview or forwarding feature.

## 💗 4. Deployment Verification

The following commands were used to verify the deployment:

```bash
docker ps
docker logs minio-server
docker inspect -f '{{.State.Status}}' minio-server
```

### Verification Results

- ✅ Container name: `minio-server`
- ✅ Container status: `running`
- ✅ API port: `9000`
- ✅ Web Console port: `9001`
- ✅ Server logs displayed the API and WebUI endpoints.
- ✅ Docker downloaded the `pgsty/minio` image successfully.

The `docker ps` command confirmed that the container was running. The `docker logs` command displayed the server startup information, and the inspection command returned `running`.

## 🌸 5. Bucket Creation and Object Upload

- **Bucket Name:** `client-photos`
- **Uploaded Object:** `UEP LOGO.png`
- **Access Level:** Private

The `client-photos` bucket was created through the MinIO Web Console. The image file `UEP LOGO.png` was uploaded successfully.

A bucket is a logical container used to organize and store objects in an object storage system.

## 🎀 6. Screenshots and Evidence

Store the actual screenshots in the `screenshots/` directory.

| Screenshot | Evidence |
|---|---|
| `minio-deployed.png` | Terminal showing successful deployment and the running container. |
| `minio-bucket.png` | MinIO Web Console showing the bucket and uploaded image. |

## 💕 7. Conclusion

This laboratory helped me understand how to deploy a cloud object storage service using Docker. I learned how to configure environment variables, map ports, inspect container logs, and verify that a server is running properly.

I also gained practical experience using the MinIO Web Console to create a bucket and upload an object. These skills strengthened my understanding of cloud storage concepts, container management, and technical documentation.

