# Final Reflection – Mission 1 to Mission 10

**Name:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Laboratory:** Laboratory Activity 10  
**Mission:** Mission 10 – The Enterprise Cloud Architect  
**Project:** CloudNova Technologies  

---

## My Experience in CCM101 Cloud Computing

When I started CCM101, I only had a basic idea about cloud computing. Most of the things I knew were about using online services, but I did not fully understand what happens behind the applications and servers. As we continued with the different missions, I learned that cloud computing also involves Linux, networking, storage, deployment, security, automation, and system management.

### Mission 1 – Welcome to the Cloud

Mission 1 was where I started learning the basic Linux commands and how to work inside a server environment. I learned how to navigate directories, create files, check system information, and use the terminal. I also started using Markdown and GitHub to document my work.

At first, some commands were confusing because I was not used to working mostly through the terminal. As I practiced, I became more comfortable using Linux commands and understanding what each command was doing.

### Mission 2 – Build the Cloud Infrastructure

In Mission 2, I started to understand that a cloud environment needs proper infrastructure before applications can be deployed. I learned more about servers, virtual machines, networking, and the resources needed to run a system.

This helped me understand that infrastructure is an important part of cloud computing because applications depend on the server and network where they are running.

### Mission 3 – Multi-Cloud Explorer

Mission 3 helped me understand that cloud computing is not limited to only one platform or environment. I learned about different cloud approaches and how cloud services can be used depending on the needs of an organization.

It also made me realize that choosing a cloud solution requires considering the resources, purpose, reliability, and requirements of a project.

### Mission 4 – Cloud-Native Engineer

Mission 4 introduced me more to cloud-native concepts and how applications can be designed to work better in modern cloud environments.

I learned that applications can be separated into different components instead of putting everything into one system. This became useful later when we worked with containers and separate application and database services.

### Mission 5 – Cloud Data Engineer

Mission 5 helped me understand the importance of data in cloud systems. I learned that storing data is not just about saving files, because the data also needs to be organized, protected, and available when it is needed.

This became more important in our final project because our Ghost application needed a database and persistent storage so that the information would not simply disappear when containers were restarted.

### Mission 6 – Cloud Deployment Engineer

Mission 6 helped me understand the process of deploying applications into a server environment. I learned that deployment requires more than just running an application. The environment, configuration, networking, and services also need to work together.

The knowledge from this mission helped me when we eventually deployed our Ghost and MySQL containers using Docker Compose in Mission 10.

### Mission 7 – Cloud Operations Engineer

Mission 7 taught me more about managing and observing a running system. We worked with Docker, Nginx, HTTP requests, logs, and container resource usage.

I learned that checking whether an application is running is not enough. It is also important to check logs, CPU, memory, network activity, and other system information. This helped me understand how cloud engineers monitor systems after deployment.

### Mission 8 – Cloud Security Engineer

Mission 8 made me more aware of the security risks that can happen when managing servers and cloud applications. I learned that services should not simply be exposed without considering which connections are actually needed.

This knowledge was applied in our final project when we configured UFW with a default-deny incoming policy and only allowed the ports needed by the system. We also kept the MySQL database from being directly exposed to the outside network.

### Mission 9 – Cloud Automation Engineer

Mission 9 helped me understand why automation is useful when managing cloud systems. Repeating the same administrative task manually can take time and can also lead to mistakes.

The idea of automation was applied in our final project through a Bash backup script and Cron. Instead of manually creating a database backup every day, the system can run the backup automatically at a scheduled time.

### Mission 10 – Enterprise Cloud Architect

Mission 10 was the biggest application of what we learned from the previous missions. Our group created a private cloud environment using Ubuntu Server, VirtualBox, Docker, Docker Compose, Ghost, and MySQL.

We created two containers for the application and database. We also used persistent volumes so that the data could remain available, configured UFW for security, and created a backup script scheduled with Cron.

One of the important things I learned from this project is that a working application is not enough. We also need to think about security, storage, backup, recovery, and maintenance.

## Challenges I Experienced

One of the challenges I experienced throughout the laboratory activities was getting used to Linux commands and working with systems through the terminal. There were also times when networking, Docker, or configuration caused problems and I had to check the commands and outputs carefully.

In Mission 10, the setup also required several components to work together. We had to make sure that Ubuntu, Docker, Ghost, MySQL, networking, UFW, storage, and the backup process were properly configured.

These problems taught me that troubleshooting is an important skill for a cloud computing student. Instead of immediately starting over, I learned to check the error, understand what caused it, and then find the correct solution.

## What I Learned Overall

Looking back from Mission 1 to Mission 10, I can say that my understanding of cloud computing improved. I started with basic Linux commands and documentation, and eventually worked with containers, networking, security, databases, monitoring, and automation.

The final laboratory showed me how these different topics can be combined into one working infrastructure. The Ghost and MySQL system also helped me see the difference between simply deploying an application and actually managing an environment that is expected to be secure, persistent, automated, and maintainable.

## What I Would Improve

If I were given more time to improve the project, I would improve the backup system by storing copies outside the virtual machine so that the backups would still be available even if the VM itself was lost. I would also add HTTPS, better monitoring, and alerts.

The current project already has a working database backup, but the backup is stored on the same VM and mainly covers the database. These are areas that can be improved in a future version of the system.

## Final Reflection

Overall, CCM101 gave me more practical experience with cloud computing and Linux administration. I learned that cloud computing is not only about hosting applications. It also involves planning, deployment, security, storage, monitoring, automation, and proper documentation.

Mission 10 was a good way to put the lessons from the previous missions together. It was challenging, but it also showed me how the different skills I learned can be used in an actual infrastructure project. I still have more to learn, especially in advanced security, automation, and cloud platforms, but this laboratory gave me a better foundation for continuing to improve my skills in cloud computing.
