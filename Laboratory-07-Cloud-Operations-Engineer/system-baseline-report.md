# System Baseline Report

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Laboratory:** 07 – Cloud Operations Engineer

## 1. Purpose

This report records the initial condition of the Linux host before running a containerized web server. The baseline will help describe the resources available to the environment and provide a reference for later monitoring.

## 2. System Inspection

The following commands will be used to collect information about the host:

| Command | Purpose |
|---|---|
| `cat /etc/os-release` | Identifies the operating system |
| `uname -r` | Displays the Linux kernel version |
| `lscpu` | Displays CPU information |
| `free -h` | Checks memory and swap usage |
| `df -h /` | Checks root filesystem capacity |

## 3. Baseline Results

Complete this table using the actual output from the Linux environment.

| Resource | Actual Result |
|---|---|
| Operating system | Pending inspection |
| Kernel version | Pending inspection |
| CPU configuration | Pending inspection |
| Total and available memory | Pending inspection |
| Root filesystem capacity and available space | Pending inspection |

## 4. Initial Analysis

CPU information describes the processing resources available to the host. Memory measurements help show how much RAM is available for applications, while disk measurements indicate whether enough storage is available for container images, logs, and other files.

These initial measurements will help provide context when examining Docker performance later in the activity.

## 5. Conclusion

A system baseline provides a starting point for understanding the condition of a host before deployment. The verified measurements and supporting screenshots will be added after the inspection commands have been executed.
