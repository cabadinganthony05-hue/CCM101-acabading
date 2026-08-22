# Cloud Infrastructure Components

## Introduction

Cloud infrastructure is made up of different resources that work together to provide computing services. In the KillerCoda Linux environment, these components can be observed through the available compute, storage, networking, and operating system resources.

## 1. Compute Resources

### Purpose

Compute resources provide the processing power needed to run applications, services, and operating system processes.

### Importance in Cloud Computing

Compute resources are important because cloud applications need processing power to perform tasks. Cloud platforms allow organizations to allocate computing resources based on their workload requirements.

### Relation to the KillerCoda Environment

The KillerCoda server provides an **Intel Xeon E312xx** virtual CPU with **1 CPU core**. The environment uses **KVM virtualization**, which allows the physical computing resources to be provided as a virtual cloud server.

## 2. Storage Resources

### Purpose

Storage resources are used to store the operating system, applications, configuration files, and other data.

### Importance in Cloud Computing

Reliable storage is essential because cloud applications need a place to save and retrieve data. Cloud providers offer scalable storage services that can accommodate different amounts of data.

### Relation to the KillerCoda Environment

The Linux server has a main storage device, `/dev/vda1`, with a total capacity of **19G** and approximately **13G available**. Additional mounted file systems are available for `/boot` and `/boot/efi`.

## 3. Networking Resources

### Purpose

Networking resources allow computers, applications, and users to communicate with each other.

### Importance in Cloud Computing

Networking is important because cloud services depend on communication between users, servers, applications, and other cloud resources. Proper networking enables connectivity and access to cloud services.

### Relation to the KillerCoda Environment

The KillerCoda server has the IP addresses **172.30.1.2** and **172.17.0.1**. These addresses show that the virtual Linux environment has network interfaces that allow communication within its cloud environment.

## 4. Operating System

### Purpose

The operating system manages the computer's hardware and provides the environment where applications and services can run.

### Importance in Cloud Computing

An operating system provides the foundation for running cloud workloads. It manages resources such as CPU, memory, storage, networking, and system processes.

### Relation to the KillerCoda Environment

The server runs **Ubuntu 24.04.4 LTS (Noble Numbat)** with kernel version **6.8.0-138-generic**. The Linux operating system manages the virtual resources provided by the KillerCoda environment.

## Conclusion

Compute, storage, networking, and the operating system are essential parts of cloud infrastructure. The KillerCoda environment demonstrates how these components work together in a virtualized Linux server. Understanding these resources helps cloud engineers plan and manage cloud infrastructure effectively.
