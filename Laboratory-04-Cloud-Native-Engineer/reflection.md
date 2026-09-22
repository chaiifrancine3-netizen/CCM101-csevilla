# 🟢 Mission Reflection

<div align="center">

## 🌿 Docker & Cloud Infrastructure Reflection

</div>

---

### 🟢 Virtual Machines vs. Docker Containers

This laboratory activity helped me understand how **Docker containers differ from traditional Virtual Machines (VMs)**. Installing an operating system on a VM usually takes several minutes because it requires setting up a complete guest operating system, allocating resources, and configuring software. In contrast, Docker containers start within seconds because they share the host operating system and only package the application along with its dependencies. This makes deployment **faster, lighter, and more efficient**.

### 🌱 Understanding Port Mapping

I also learned the importance of **port mapping** when running applications inside containers. The command `-p 8080:80` maps port **8080 on the host machine** to port **80 inside the container**. Without port mapping, users outside the container would not be able to access the web server. This allows the Nginx application running in the container to be reached through `http://localhost:8080`.

### 🍃 Container Data and `docker rm`

Another concept I learned is what happens when the `docker rm` command is used. Removing a container deletes the container and its internal data that is not stored in external volumes. This showed me that containers are **temporary environments**, and important data should be stored outside the container if it needs to be preserved.

### 🌿 Docker and Collaboration

Containerization also changes the way **software developers and IT operations teams** work together. Developers can create applications in consistent environments, while operations teams can deploy the same containers without worrying about differences in configuration. This improves collaboration, supports **DevOps practices**, and speeds up software delivery.

### 🌳 My GitHub Portfolio

Finally, my GitHub portfolio is continuously evolving as I complete more laboratory activities. Each mission adds new documentation, screenshots, and technical knowledge that showcase my skills in **cloud computing, Linux, Docker, and technical writing**. My portfolio is becoming a record of my learning journey and practical experience in cloud technologies.

---

<div align="center">

### 🟩 Keep Learning • Keep Building • Keep Growing 🌱

</div>
