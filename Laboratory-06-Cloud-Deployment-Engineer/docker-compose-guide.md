# Docker Compose Deployment Guide

## Overview

Docker Compose is used to define and manage multiple containers as one application stack. In this laboratory, Docker Compose is used to deploy a Nextcloud application together with a MariaDB database.

## Prerequisites

Before deployment, make sure that Docker and Docker Compose are installed and working.

## Deployment Procedure

The following commands were used to verify Docker and Docker Compose, clone the repository, deploy the application, verify the containers, test the application, and manage the containers:

```bash
docker --version
docker-compose version

git clone https://github.com/cabadinganthony05-hue/CCM101-acabading.git
cd CCM101-acabading/Laboratory-06-Cloud-Deployment-Engineer

docker-compose up -d

docker-compose ps

curl -I http://localhost:8080

docker-compose logs

docker-compose down

docker-compose ps
```

The Docker environment used Docker Compose version 1.29.2. The `docker-compose up -d` command started the Nextcloud application container and the MariaDB database container.

The `docker-compose ps` command was used to verify that both containers were running. The Nextcloud application was exposed through port `8080`.

The application was tested using `curl -I http://localhost:8080`, which returned an `HTTP/1.1 200 OK` response. The application was also accessed through a web browser using:

```text
http://localhost:8080
```

The Nextcloud installation page was successfully displayed.

## Docker Compose Configuration

The deployment uses two services. The first service is the MariaDB database, which stores the application's persistent data. The second service is the Nextcloud application, which provides the web interface.

The database service uses:

```yaml
database:
  image: mariadb:10.6
```

The application service uses:

```yaml
app:
  image: nextcloud
  ports:
    - 8080:80
```

The Nextcloud application connects to the MariaDB database through the Docker Compose service name `database`.

## Deployment Result

The deployment successfully demonstrated a two-tier containerized application. Nextcloud served as the web and application tier, while MariaDB served as the database tier. Docker Compose allowed both services to be configured, deployed, monitored, and stopped as one application stack.

## Conclusion

This laboratory provided practical experience in Docker Compose, container management, multi-tier architecture, application deployment, service verification, and troubleshooting. The successful deployment of Nextcloud and MariaDB demonstrated how separate containerized services can communicate and work together to provide a functional cloud application environment.
