
# MinIO Deployment and Technical Configuration

**Name:** Anthony Cabading  
**Course:** BS Information Technology  
**Laboratory:** 05 – The Cloud Data Engineer

## 1. Introduction

This document describes the process of deploying MinIO as a containerized object storage service. The deployment was performed using Docker in the KillerCoda Ubuntu Playground.

MinIO provides an S3-compatible storage interface that can be used to store and manage unstructured data such as images, videos, and backups.

## 2. Environment and Tools

| Component | Details |
|---|---|
| Operating System | Ubuntu 24.04 |
| Container Platform | Docker |
| Storage Server | MinIO |
| Environment | KillerCoda Ubuntu Playground |
| Web Interface | MinIO Web Console |

## 3. Downloading the MinIO Image

The original image command specified in the activity was unavailable. Therefore, I downloaded the image from the Quay.io registry.

```bash
docker pull quay.io/minio/minio
```

The download completed successfully, making the image available for container deployment.

## 4. Container Deployment

I used the following Docker command to start the MinIO service:

```bash
docker run -d \
  --name minio-server \
  -p 9000:9000 \
  -p 9001:9001 \
  -e "MINIO_ROOT_USER=admin" \
  -e "MINIO_ROOT_PASSWORD=MinioAdmin123!" \
  quay.io/minio/minio server /data --console-address ":9001"
```

### Configuration Details

- `-d`: Starts the container in the background.
- `--name minio-server`: Identifies the container using a custom name.
- `-p 9000:9000`: Exposes the MinIO S3 API port.
- `-p 9001:9001`: Exposes the MinIO Web Console port.
- `MINIO_ROOT_USER`: Defines the administrator username.
- `MINIO_ROOT_PASSWORD`: Defines the administrator password.
- `server /data`: Starts the storage server using `/data` as its storage directory.
- `--console-address ":9001"`: Configures the console to listen on port 9001.

The environment variables configure the administrator login credentials for this laboratory deployment.

## 5. Container Verification

To verify the deployment, I executed:

```bash
docker ps
```

The output displayed the `minio-server` container with an Up status. The port mappings showed that ports 9000 and 9001 were exposed.

This indicated that the MinIO container was running.

## 6. Accessing the Web Console

I opened the MinIO Web Console through KillerCoda's port forwarding interface using port 9001.

After logging in with the configured credentials, I accessed the Object Browser, where I could create and manage storage buckets.

Port 9000 was assigned to the MinIO API, while port 9001 was used for the browser-based console.

## 7. Bucket Creation and Object Upload

I created the required object storage bucket:

`client-photos`

I then uploaded a sample image from my computer using the Upload function in the MinIO Web Console.

The uploaded file was displayed inside the bucket, demonstrating that MinIO could accept and store objects.

## 8. Evidence and Screenshots

The following evidence was captured during the deployment:

| File | Purpose |
|---|---|
| `screenshots/minio-deployed.png` | Evidence of the running container and exposed ports. |
| `screenshots/minio-bucket-upload.png` | Evidence of the bucket and successfully uploaded sample object. |

## 9. Conclusion

The activity demonstrated how a containerized storage service can be deployed and accessed through a web interface. I gained practical experience with Docker image retrieval, container configuration, port mapping, and object storage management.

The MinIO deployment provided an opportunity to apply cloud computing concepts in a working environment.
