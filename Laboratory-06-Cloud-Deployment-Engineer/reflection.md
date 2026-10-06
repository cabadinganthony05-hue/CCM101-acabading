# Mission Reflection

## What I Learned

This laboratory helped me understand how Docker Compose can be used to deploy and manage a multi-tier cloud application. I learned that the application and database can run in separate containers while still communicating with each other. In this activity, Nextcloud served as the application layer and MariaDB served as the database layer.

I also learned how a `docker-compose.yml` file can simplify the deployment process. Instead of manually starting each container, Docker Compose allowed me to define the services in one configuration and manage them together.

## Challenges Encountered

One of the challenges I encountered was making sure that the application and database containers were properly started and connected. I needed to check the container status and verify that the application could be accessed through port `8080`. Using commands such as `docker-compose ps` and `curl -I http://localhost:8080` helped me determine whether the deployment was working correctly.

Another challenge was understanding how the Nextcloud application communicates with the MariaDB database through the Docker Compose network. This helped me understand the importance of correctly configuring service names, ports, and environment variables.

## Skills Gained

Through this activity, I improved my skills in Docker Compose, container management, multi-tier architecture, application deployment, and troubleshooting. I also gained experience in checking running services, testing an application, viewing container logs, and documenting the deployment process.

## Reflection

This laboratory gave me a better understanding of how cloud applications can be organized using containers. I learned that separating the application and database services makes the system easier to manage and troubleshoot. The activity also showed me how important proper configuration and verification are when deploying a cloud-based application.

Overall, this laboratory was a useful hands-on experience because I was able to apply cloud computing concepts through an actual containerized deployment. The knowledge I gained can help me in future projects involving web applications, databases, Docker, and cloud infrastructure.
