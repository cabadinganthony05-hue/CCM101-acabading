# Infrastructure Report

## Cloud Server Investigation

This report documents the Linux environment provided through the KillerCoda Playground.

## Operating System

- **Operating System:** Ubuntu 24.04.4 LTS (Noble Numbat)

## Kernel Version

- **Kernel Version:** 6.8.0-138-generic

## CPU Information

- **CPU Model:** Intel Xeon E312xx (Sandy Bridge, IBRS update)
- **CPU Cores:** 1
- **Architecture:** x86_64
- **Hypervisor:** KVM

## Memory

- **Total RAM:** 1.9 GiB
- **Available RAM:** 1.4 GiB

## Disk Capacity

The main filesystem is `/dev/vda1`, with a total capacity of 19G.

| Filesystem | Size | Used | Available | Mounted On |
|---|---:|---:|---:|---|
| /dev/vda1 | 19G | 5.4G | 13G | / |
| /dev/vda16 | 881M | 117M | 703M | /boot |
| /dev/vda15 | 105M | 6.2M | 99M | /boot/efi |
| tmpfs | 191M | 1000K | 190M | /run |
| tmpfs | 952M | 84K | 952M | /dev/shm |
| tmpfs | 5.0M | 0 | 5.0M | /run/lock |

## Hostname

- **Hostname:** ubuntu

## IP Address

- **IP Address:** 172.30.1.2
- **Additional Interface:** 172.17.0.1

## Linux Commands Used

```bash
cat /etc/os-release
uname -r
lscpu
free -h
df -h
hostname
hostname -I
