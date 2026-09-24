
# Cloud Storage Types Research

**Name:** Anthony Cabading  
**Course:** BS Information Technology  
**Laboratory:** 05 – The Cloud Data Engineer

## Introduction

Cloud storage is a technology that enables data to be stored and accessed using remote infrastructure over a network. Cloud providers offer different storage services depending on how data is organized and how applications need to access it.

The three major categories are Block Storage, File Storage, and Object Storage.

## 1. Block Storage

**Description:**

Block Storage stores information in separate, fixed-sized data blocks. The blocks are addressed individually and can be combined by an operating system to form a usable storage volume.

**Primary Use Case:**

It is commonly used for virtual machine operating systems, transactional databases, and workloads that require low-latency storage access.

**Cloud Provider Examples:**

- AWS – Amazon Elastic Block Store (EBS)
- Azure – Azure Managed Disks
- Google Cloud – Persistent Disk

## 2. File Storage

**Description:**

File Storage saves information as files arranged within directories and folders. It uses a hierarchical structure and supports file-sharing protocols such as NFS and SMB.

**Primary Use Case:**

It is useful for shared office documents, team folders, shared application files, and workloads that need multiple systems to access the same files.

**Cloud Provider Examples:**

- AWS – Amazon Elastic File System (EFS)
- Azure – Azure Files
- Google Cloud – Google Cloud NetApp Volumes

## 3. Object Storage

**Description:**

Object Storage manages data as independent objects. An object contains the stored content, descriptive metadata, and a unique key. Objects are organized into buckets and are commonly accessed through HTTP-based APIs.

**Primary Use Case:**

It is suitable for storing images, videos, backups, log files, and other unstructured information. It is useful for applications that need to store and retrieve large amounts of data.

**Cloud Provider Examples:**

- AWS – Amazon Simple Storage Service (Amazon S3)
- Azure – Azure Blob Storage
- Google Cloud – Google Cloud Storage

## Why Object Storage Is Suitable for the Client's Application

For a photo-sharing application that handles millions of user-uploaded images, Object Storage provides a practical way to organize and retrieve image files. Each uploaded photo can be stored as an object with a unique key and associated metadata.

The application can use object storage APIs to upload, retrieve, and manage images without managing the underlying storage blocks. Object storage services are also designed to support large collections of unstructured data.

MinIO is useful for this laboratory because it provides an S3-compatible interface that allows us to practice bucket creation and object uploads using a self-hosted storage server.

## Conclusion

Block Storage provides disk-like storage for systems and databases. File Storage organizes information into files and directories for shared access. Object Storage manages data as objects and is useful for applications that store large collections of media files and other unstructured data.
