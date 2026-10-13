# Laboratory 07: Cloud Operations Engineer

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Mission:** Cloud Operations and Observability

## 1. Mission Overview

CloudNova Technologies is preparing its web infrastructure for a major marketing campaign. Before the expected increase in website visitors, the cloud operations team must check the host system, deploy a web server, generate test traffic, and examine the application's logs and resource usage.

This laboratory simulates those responsibilities using Linux and Docker. The goal is to establish a system baseline and collect evidence that can help identify performance issues and application errors.

## 2. Mission Objectives

- Check the host's CPU, memory, and disk capacity.
- Deploy an Nginx web server inside a Docker container.
- Generate HTTP requests to simulate website visitors.
- Examine access logs and identify successful and unsuccessful requests.
- Monitor CPU, memory, and network activity using Docker.
- Record the findings in Markdown and organize the evidence in GitHub.

## 3. Monitoring Commands Executed

The following commands were used during the laboratory to inspect the host system, test the web server, and monitor the container.

| Command | Purpose |
|---|---|
| `lscpu` | Displays CPU and processor information |
| `free -h` | Displays memory and swap usage |
| `df -h /` | Checks available root filesystem space |
| `top` | Monitors running processes and CPU activity |
| `docker ps` | Lists running containers |
| `docker run -d --name client-website -p 8080:80 nginx` | Deploys the Nginx container in the background |
| `curl http://localhost:8080` | Sends an HTTP GET request to the web server |
| `curl -I http://localhost:8080` | Checks the web server's HTTP response headers |
| `curl http://localhost:8080/hidden-admin-page` | Tests a missing page and checks the HTTP 404 response |
| `docker logs client-website` | Displays container logs |
| `docker stats` | Monitors live container resource usage |

## 4. Evidence and Results

The host system was checked using Linux monitoring commands to identify available memory and disk space. An Nginx web server was deployed in a Docker container named `client-website` and accessed through port 8080.

HTTP requests were sent using `curl` to test the web server. Successful requests returned HTTP 200 responses, while a request to `/hidden-admin-page` returned HTTP 404 because the requested page was not found.

The container logs were inspected using `docker logs client-website`, and resource usage was monitored using `docker stats`. The results and observations are documented in `system-baseline-report.md` and `container-observability.md`. Screenshots of the checkpoints are stored in the `screenshots/` folder.

## 5. Skills Learned

This activity developed practical skills in:

- Linux system administration and resource monitoring.
- Docker container deployment and management.
- HTTP request testing using `curl`.
- Application log inspection and error identification.
- Container performance monitoring using `docker stats`.
- Markdown documentation and GitHub portfolio management.

## 6. Conclusion

This laboratory demonstrated the importance of monitoring host resources, testing web services, examining application logs, and tracking container performance. These practices help cloud operations engineers identify errors, investigate resource issues, and maintain reliable infrastructure. The commands and observations from this activity provide practical experience in Linux system administration and Docker observability.
