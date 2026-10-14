
# 🌸 Mission Reflection: Cloud Object Storage

> 💗 **CCM101 – Cloud Computing | Laboratory 05**

Completing this laboratory helped me understand how object storage works and why it is useful for managing large amounts of data. I learned that object storage is better suited for storing millions of photos than traditional block storage because it organizes files as individual objects with unique identifiers and metadata. This makes it easier to store, retrieve, and manage large collections of images without depending on a traditional file system structure.

Using Docker also made deploying MinIO much easier. Instead of manually installing and configuring every component, I was able to download the MinIO image and start the server using a single command. Docker also allowed me to configure the required ports and administrator credentials through environment variables. This made the deployment process faster, more organized, and easier to repeat.

In cloud storage, a **bucket** is a container used to organize and store objects. In this activity, I created a bucket named `client-photos` and uploaded `UEP LOGO.png` through the MinIO Web Console. This helped me understand how files are organized and managed in an object storage system.

Large enterprise companies protect their object storage data through redundancy, replication, and regular backups. They may store copies of data across multiple physical drives, servers, or geographical locations. If one server crashes, another copy can help restore access to the stored files. Monitoring systems and recovery procedures also help reduce the risk of permanent data loss.

Finally, this activity improved my confidence in using the Linux command line. I practiced running Docker commands, checking container status with `docker ps`, viewing server logs with `docker logs`, and verifying the container using `docker inspect`. I am becoming more comfortable troubleshooting errors and understanding command outputs. I still have more to learn, but this laboratory gave me valuable hands-on experience with containerization and cloud storage.

---

🌷 *Every laboratory is another step toward becoming a better Cloud Engineer!* 💗

