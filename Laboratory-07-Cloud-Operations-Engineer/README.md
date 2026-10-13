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

The following commands will be used during the laboratory:

| Command | Purpose |
|---|---|
| `lscpu` | Displays CPU and processor information |
| `free -h` | Displays memory and swap usage |
| `df -h /` | Checks available root filesystem space |
| `top` | Monitors running processes and CPU activity |
| `docker ps` | Lists running containers |
| `docker logs client-website` | Displays container application logs |
| `docker stats` | Displays live container resource usage |
| `curl` | Sends HTTP requests to the web server |

## 4. Evidence and Results

Screenshots and actual command outputs will be collected during each checkpoint. Resource measurements and HTTP response results will be documented after the tests have been performed.

## 5. Skills Learned

This activity develops practical skills in Linux system administration, Docker container deployment, HTTP testing, log analysis, resource monitoring, Markdown documentation, and GitHub portfolio management.

## 6. Conclusion

System monitoring is an important part of maintaining reliable cloud infrastructure. By checking the host before deployment and examining logs and container metrics during testing, an engineer can gather evidence to investigate errors and evaluate resource consumption.

The final assessment will be based on the actual command outputs, screenshots, and observations collected during the laboratory.
