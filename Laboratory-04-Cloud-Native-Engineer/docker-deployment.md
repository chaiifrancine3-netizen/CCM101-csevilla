> 🟢 **Docker Container Lifecycle**
>
> This checkpoint demonstrates the basic lifecycle of a Docker container: listing, stopping, verifying, and removing a container.

---

## 🟢 1. List Running Containers

### Command

```bash
docker ps
```

### Terminal Execution

```text
root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS              PORTS                                     NAMES
7a5d64aaeb25   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   nginx-server
```

### Explanation

This command lists all Docker containers that are currently running and displays their container ID, image, status, ports, and name.

---

## 🟢 2. Stop the Running Container

### Command

```bash
docker stop 7a5d64aaeb25
```

### Terminal Execution

```text
root@ubuntu:~$ docker stop 7a5d64aaeb25
7a5d64aaeb25
```

### Explanation

This command stops the running `nginx-server` container using its container ID.

---

## 🟢 3. Verify the Container is Stopped

### Command

```bash
docker ps
```

### Terminal Execution

```text
root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
```

### Explanation

This command verifies that the container has stopped because it no longer appears in the list of running containers.

---

## 🟢 4. Remove the Container Completely

### Command

```bash
docker rm 7a5d64aaeb25
```

### Terminal Execution

```text
root@ubuntu:~$ docker rm 7a5d64aaeb25
7a5d64aaeb25
```

### Explanation

This command completely removes the stopped `nginx-server` container from the Docker system.

---

## 🟢 5. Verify the Container Was Removed

### Command

```bash
docker ps -a
```

### Terminal Execution

```text
root@ubuntu:~$ docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
root@ubuntu:~$
```

### Explanation

This command lists all containers, including stopped ones, and confirms that the removed container no longer exists.

---

## 🟩 Complete Terminal Execution

The following shows the complete sequence of commands executed during the container lifecycle:

```text
root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS              PORTS                                     NAMES
7a5d64aaeb25   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   nginx-server

root@ubuntu:~$ docker stop 7a5d64aaeb25
7a5d64aaeb25

root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

root@ubuntu:~$ docker rm 7a5d64aaeb25
7a5d64aaeb25

root@ubuntu:~$ docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES

root@ubuntu:~$
```

---

## 🟢 Summary

| Step | Command                    | Description                                              |
| ---- | -------------------------- | -------------------------------------------------------- |
| 1    | `docker ps`                | Lists all currently running containers.                  |
| 2    | `docker stop 7a5d64aaeb25` | Stops the running `nginx-server` container.              |
| 3    | `docker ps`                | Verifies that the container is no longer running.        |
| 4    | `docker rm 7a5d64aaeb25`   | Completely removes the stopped container.                |
| 5    | `docker ps -a`             | Verifies that the container has been completely removed. |

---

> 🟢 **Result:** The `nginx-server` container was successfully listed, stopped, verified as stopped, removed, and verified as completely removed.

