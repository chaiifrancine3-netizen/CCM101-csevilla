
# Checkpoint 7 – Mission Reflection

Completing this laboratory activity helped me understand how important security is when managing cloud servers. A host-based firewall protects a server by controlling incoming and outgoing network traffic directly on the machine. Even if the physical network perimeter is breached, the firewall can still block unauthorized connections and allow only trusted services.

Managing open network ports is important because every open port can become a possible entry point for attackers. By allowing only the ports required by the application, we can reduce the server's attack surface and improve its security.

In a real enterprise environment, leaving a database port such as 3306 for MySQL open to the public internet is dangerous. Attackers could attempt unauthorized logins, exploit database vulnerabilities, or access sensitive customer information. Database access should only be allowed from trusted application servers or authorized networks.

This mission changed my perspective because I realized how easily a server can become exposed when security settings are not properly configured. Even a simple application can become a target if unnecessary ports and services are left open. Learning to configure UFW showed me how important it is to establish security rules before allowing public access.

Looking at my GitHub portfolio with eight completed missions, I can see how much I have learned throughout the activities. I started with basic cloud concepts and gradually learned about infrastructure, virtualization, containers, deployment, monitoring, and security. Each mission helped me develop practical skills in managing cloud environments.

Overall, I learned that cloud security is not just about installing a firewall. It also requires careful planning, proper access control, regular monitoring, and continuous improvement. This experience made me more aware of the responsibilities of a Cloud Security Engineer.

