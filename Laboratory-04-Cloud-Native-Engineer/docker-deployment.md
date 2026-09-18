# Docker Deployment and Container Management

## Introduction

This documentation presents the Docker commands executed during Laboratory Activity 4. The activity focused on checking the Docker environment, downloading an Nginx image, running a containerized web server, and managing the container lifecycle.

## Docker Commands Executed

### 1. Check Docker Version

```bash
docker --version
```

This command displays the installed Docker version and confirms that Docker is available in the environment.

### 2. Display Docker System Information

```bash
docker info
```

This command provides detailed information about the Docker environment, including containers, images, storage, and system configuration.

### 3. Download the Nginx Image

```bash
docker pull nginx
```

This command downloads the latest Nginx image from Docker Hub to the local Docker environment.

### 4. Run the Nginx Container

```bash
docker run -d --name nginx-server -p 8080:80 nginx
```

This command creates and runs a container named nginx-server in detached mode. Port 8080 of the host is connected to port 80 inside the container.

### 5. Check Running Containers

```bash
docker ps
```

This command displays the containers that are currently running.

### 6. Test the Web Server

```bash
curl http://localhost:8080
```

This command sends an HTTP request to the Nginx web server. The HTML response confirms that the server is working correctly.

### 7. Stop the Container

```bash
docker stop nginx-server
```

This command stops the running Nginx container without deleting it.

### 8. Display All Containers

```bash
docker ps -a
```

This command displays all containers, including running and stopped containers.

### 9. Start the Container Again

```bash
docker start nginx-server
```

This command starts the previously stopped Nginx container.

## Container Lifecycle Summary

The Docker container lifecycle demonstrated in this activity included creating, running, stopping, checking, and starting a container again. These operations are important for managing applications in a containerized environment.

## Evidence

Screenshots of the Docker commands and their outputs are available in the screenshots folder of this repository.
