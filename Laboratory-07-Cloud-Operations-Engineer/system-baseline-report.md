# System Baseline Report

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Laboratory:** 07 – Cloud Operations Engineer

## 1. Purpose

This report documents the initial condition of the Linux host before deploying a containerized web server. Checking the system baseline helps identify the available resources and provides a reference for monitoring system performance during the laboratory activity.

## 2. System Inspection

The following Linux commands were used to inspect the host system:

| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identifies the operating system |
| `uname -r` | Displays the Linux kernel version |
| `lscpu` | Displays CPU and processor information |
| `free -h` | Checks memory and swap usage |
| `df -h /` | Checks root filesystem capacity |
| `top` | Monitors running processes and CPU activity |

## 3. Baseline Results

The following results were collected from the KillerCoda Ubuntu environment.

| Resource | Actual Result |
|---|---|
| Operating system | Ubuntu 24.04.4 LTS |
| Kernel version | 6.8.0-136-generic |
| CPU configuration | Intel Xeon E312xx, x86_64 architecture, 1 CPU and 1 core |
| Total RAM | 1.9 GiB |
| Used RAM | 402 MiB |
| Free RAM | 1.2 GiB |
| Available RAM | 1.5 GiB |
| Total swap | 1.0 GiB |
| Root filesystem capacity | 19 GB |
| Used disk space | 5.5 GB |
| Available disk space | 13 GB |
| Disk usage | 30% |

## 4. Initial Analysis

The host has 1.9 GiB of RAM, with approximately 1.5 GiB available when the memory check was performed. The root filesystem has a total capacity of 19 GB, with 13 GB available and 30% of the space currently used.

Checking disk space before a traffic surge is important because container images, application logs, and other files require storage. If the disk becomes full, applications and system services may experience errors or fail to operate properly.

The CPU and memory information also provide a baseline for understanding the resources available to the host. These measurements can be compared with later observations when the Nginx container is running.

## 5. Conclusion

The baseline inspection provided an overview of the operating system, kernel, CPU, memory, and disk capacity of the KillerCoda environment. These results establish a starting point for the next checkpoints, where the Nginx container, application logs, and real-time resource metrics will be examined.

The screenshots of the memory and disk checks are saved as evidence for this checkpoint.
