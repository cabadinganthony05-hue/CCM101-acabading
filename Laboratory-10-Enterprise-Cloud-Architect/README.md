# Laboratory 10 – Enterprise Cloud Architect

## Project Summary

For this laboratory, our group created a small private cloud environment for CloudNova Technologies. The system was built using an Ubuntu Server virtual machine running inside Oracle VirtualBox.

We used Docker Compose to deploy a two-tier application consisting of **Ghost 6 as the web application** and **MySQL 8.0 as the database**. The project also includes persistent storage, firewall protection, and an automated database backup system.

The purpose of the project was to apply the cloud computing concepts learned from the previous laboratory missions into one working infrastructure.

## Infrastructure Used

The project was built using the following technologies:

- Windows host computer
- Oracle VirtualBox
- Ubuntu Server
- Docker
- Docker Compose
- Ghost 6
- MySQL 8.0
- UFW Firewall
- Bash scripting
- Cron
- GitHub

The Ubuntu Server uses NAT networking with port forwarding. The web application is accessed through `localhost:8080`, while SSH uses port `2222`.

## Application Setup

The application is divided into two main containers:

**Ghost Application**
- Container name: `ghost_app`
- Image: Ghost 6
- Handles the website and user interface

**MySQL Database**
- Container name: `ghost_db`
- Image: MySQL 8.0
- Stores the application's database information

Ghost and MySQL communicate through the Docker network. The MySQL service does not have a public port mapping, so it is only accessed by the Ghost container.

Persistent Docker volumes are also included for the database and Ghost content.

## Security Configuration

The Ubuntu Server was protected using UFW. Incoming connections are denied by default, while only the required services are allowed.

The allowed ports are:

- `22/tcp` – SSH
- `80/tcp` – Web traffic

The MySQL port was intentionally not exposed to the outside network. This keeps the database accessible only through the internal Docker network.

The database credentials are also stored in the `.env` file instead of being directly placed in the Compose configuration. The real credentials file is not included in the GitHub repository.

## Backup and Automation

A Bash script was created to handle database backups.

The script reads the database information from the environment file and uses `mysqldump` inside the MySQL container to create an SQL backup. It also removes backup files that are more than seven days old and records successful backup operations in a log.

The backup script is scheduled through Cron and runs every day at **2:00 AM**.

## Important Commands

Some of the main commands used during the setup were:

```bash
sudo apt update && sudo apt upgrade -y
sudo timedatectl set-timezone Asia/Manila

sudo apt install -y docker.io docker-compose-v2
sudo systemctl enable --now docker
sudo usermod -aG docker $USER

docker run hello-world
docker compose version

mkdir ~/cloudnova
cd ~/cloudnova

chmod 600 .env

docker compose config
docker compose pull
docker compose up -d
docker compose ps

sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw enable
sudo ufw status verbose

sudo ss -tulpn

chmod +x automation-script.sh
./automation-script.sh

ls -lh ~/backups
crontab -l

sudo reboot
docker ps
```

## Files in This Laboratory

| File | Purpose |
|---|---|
| `README.md` | Overview and summary of the laboratory |
| `architecture-diagram.png` | Shows the structure and connection of the cloud environment |
| `docker-compose.yml` | Configuration for the Ghost and MySQL containers |
| `automation-script.sh` | Script used for automated database backups |
| `operational-manual.md` | Instructions for deployment, security, backup, and maintenance |
| `final-reflection.md` | Personal reflection covering the learning from Mission 1 to Mission 10 |

## What We Accomplished

At the end of the laboratory, we were able to deploy the Ghost website and connect it to the MySQL database. We also configured persistent storage, secured the server with UFW, created an automated backup process, and tested the system after a reboot.

The operational manual contains the detailed deployment, security, backup, restore, maintenance, and troubleshooting procedures for the system. 

## Key Learning

This laboratory helped us understand how different cloud infrastructure components work together. We applied Linux administration, virtualization, containerization, networking, security, storage, and automation in one project.

It also showed us that deploying an application is not enough. The system also needs proper security, persistent data, backups, and documentation so it can be maintained and recovered when problems occur.
