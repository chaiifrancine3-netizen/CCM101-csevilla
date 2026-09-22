# 🟢 Mission 4 — The Cloud-Native Engineer

> 🌿 **CCM101 – Cloud Computing**  
> **Laboratory Activity 4**  
> **Cloud-Native Engineering with Docker**

---

## 🟩 Mission Overview

In this mission, I learned how containerization works and how it differs from traditional Virtual Machines (VMs). I used the KillerCoda Docker Playground to practice basic Docker commands and deploy an Nginx web server inside a container.

The main goal of this mission was to understand how Docker containers can provide lightweight, portable, and fast application deployment. I also practiced managing the complete lifecycle of a container, from downloading an image and running it to stopping and removing the container.

---

## 🎯 Objectives

The objectives of this laboratory activity were to:

- 🟢 Understand the difference between Virtual Machines and Containers.
- 🟢 Access and use a Docker-enabled environment through KillerCoda.
- 🟢 Execute fundamental Docker CLI commands.
- 🟢 Pull and run an Nginx container.
- 🟢 Map a host port to the container's web server port.
- 🟢 Verify that the Nginx web server is running.
- 🟢 Stop, verify, and remove a Docker container.
- 🟢 Document Docker operations using Markdown.
- 🟢 Improve my GitHub Cloud Computing portfolio.

---

## 🐳 Docker Commands Executed

### 🟢 Checkpoint 3 — Enter the Docker Playground

I verified that Docker was installed and checked the Docker environment.

#### Check Docker Version

```bash
docker --version
````

This command displays the installed Docker version.

#### Check Docker Environment

```bash
docker info
```

This command displays information about the Docker environment and confirms that Docker is running.

---

### 🟢 Checkpoint 4 — Deploy Your First Container

I downloaded the official Nginx image from Docker Hub.

#### Pull the Nginx Image

```bash
docker pull nginx
```

This command downloads the Nginx Docker image.

#### Run the Nginx Container

```bash
docker run -d -p 8080:80 nginx
```

This command creates and starts an Nginx container in detached mode.

The port mapping:

```text
8080:80
```

connects **port 8080 on the host** to **port 80 inside the Nginx container**.

#### Test the Nginx Web Server

```bash
curl http://localhost:8080
```

This command sends an HTTP request to the Nginx web server and displays its HTML response in the terminal.

---

### 🟢 Checkpoint 5 — The Container Lifecycle

I listed the running containers.

#### List Running Containers

```bash
docker ps
```

This command displays the Docker containers that are currently running.

#### Stop the Container

```bash
docker stop <container_id>
```

This command stops the specified running container.

#### Verify the Container is Stopped

```bash
docker ps
```

This command checks the list of currently running containers to verify that the Nginx container has stopped.

#### Remove the Container

```bash
docker rm <container_id>
```

This command permanently removes the stopped container.

---

## 🛠️ Skills Learned

During this laboratory activity, I learned how to:

* 🟢 Use basic Docker CLI commands.
* 🟢 Check whether Docker is installed and running.
* 🟢 Download Docker images from Docker Hub.
* 🟢 Create and run Docker containers.
* 🟢 Run containers in detached mode.
* 🟢 Configure port mapping using Docker.
* 🟢 Test a containerized web server using `curl`.
* 🟢 List running Docker containers.
* 🟢 Stop and remove containers.
* 🟢 Understand the basic lifecycle of a Docker container.
* 🟢 Document technical procedures using Markdown.
* 🟢 Organize technical work in a GitHub repository.

---

## ⚠️ Challenges Encountered

One challenge I encountered was understanding the difference between a Docker image and a running container. I learned that an image provides the files and configuration needed to create a container, while the container is the running instance of that image.

Another challenge was understanding port mapping. The `-p 8080:80` option initially required some explanation, but I learned that it connects port 8080 on the host environment to port 80 inside the Nginx container.

I also needed to understand the container lifecycle, particularly the difference between stopping a container with `docker stop` and permanently removing it with `docker rm`.

Through the hands-on activities in KillerCoda, I was able to understand these Docker operations more clearly and gain practical experience with container deployment and management.

---

## 🟢 Mission Summary

> **Docker makes application deployment faster, portable, and easier to manage.**
>
> Through this laboratory, I gained practical experience in deploying an Nginx container, configuring network ports, testing a web server, and managing the container lifecycle using Docker CLI commands.

---

## 🌱 Cloud-Native Engineer

**CCM101 – Cloud Computing**
**Laboratory Activity 4**

> 🟩 *Learn. Build. Deploy. Manage.*

```

