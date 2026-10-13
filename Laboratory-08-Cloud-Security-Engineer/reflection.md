# Laboratory 08 – Reflection Report

**Student:** Anthony Cabading  
**Laboratory:** Cloud Security Engineer

## Reflection

Completing this laboratory activity helped me understand the importance of securing cloud environments through proper firewall configuration and network access management. I learned that deploying a web application is only one part of managing a server because protecting the application and controlling network traffic are equally important responsibilities.

During the activity, I deployed an Nginx web server using Docker and verified that it was functioning through port 8080. After confirming that the application was accessible, I configured the Uncomplicated Firewall (UFW) by applying a default deny incoming policy and allowing the necessary ports for SSH and the web application. I also learned why checking existing firewall rules before enabling them is essential to avoid accidentally blocking important connections.

One of the most valuable lessons I gained was the importance of testing a system after making security changes. The Nginx application continued to respond successfully after UFW was activated. However, I also learned that Docker networking can affect how firewall rules are applied, making additional verification important when securing real cloud environments.

Overall, this laboratory improved my understanding of basic cloud security practices, particularly the Principle of Least Privilege, attack surface reduction, and firewall management. These skills will be useful in my future career as an IT professional, where maintaining secure and reliable systems is an important responsibility.

## Key Takeaways

1. A default deny policy helps limit unnecessary incoming network connections.
2. Required network ports should be explicitly allowed before activating a firewall.
3. Firewall configuration should be verified through status checks and connectivity testing.
4. Docker networking requires additional security considerations.
5. Proper documentation supports troubleshooting and future system maintenance.
