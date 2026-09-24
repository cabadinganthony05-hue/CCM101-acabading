
# Reflection: Cloud Data Engineering

**Name:** Anthony Cabading  
**Course:** BS Information Technology  
**Laboratory:** 05 – The Cloud Data Engineer

## Reflection

Through this laboratory activity, I gained a better understanding of cloud storage and how it can be used in real-world applications. I learned that Object Storage is suitable for applications that manage millions of photos because it stores data as objects with unique keys and metadata. This approach allows applications to organize and retrieve images without directly managing individual storage blocks.

I also discovered how Docker simplifies the deployment of a MinIO storage server. By downloading a container image and configuring the required ports and environment variables, I was able to run MinIO in an isolated environment. When the initial image command failed, I used another image registry to continue the deployment. This helped me develop my troubleshooting skills.

A bucket is a container used to organize objects in an object storage system. For this activity, I created a bucket named `client-photos` and uploaded a sample image through the MinIO Web Console. This allowed me to experience how applications can store and manage files using object storage.

Large enterprises protect their data from physical server failures through replication, redundant storage devices, regular backups, and geographically distributed copies. These strategies help organizations recover important information and maintain access to their data even when hardware problems occur.

My confidence in navigating the Linux command line also improved throughout the activity. I practiced executing Docker commands, checking container status, and configuring a storage service. These tasks helped me become more familiar with Linux and understand how command-line tools are used in cloud infrastructure management.

Overall, this laboratory provided useful hands-on experience with Docker and MinIO. It improved my technical knowledge and helped me appreciate the importance of reliable and secure cloud storage.
