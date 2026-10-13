# Container Observability Report

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing  
**Laboratory:** 07 – Cloud Operations Engineer

## 1. Purpose

This report documents the deployment and monitoring of an Nginx web server running in a Docker container. It covers HTTP testing, application log inspection, and container resource monitoring.

## 2. Nginx Container Deployment

Docker will be used to run Nginx as a containerized web server. The container status and port mapping will be checked to verify that the service is running and accessible.

The deployment commands and their actual results will be recorded after testing.

## 3. HTTP Traffic Simulation

HTTP requests will be sent to the web server to simulate visitors accessing the website. Both a valid request and a request for a nonexistent page will be tested.

| Test | Expected Observation |
|---|---|
| Request to the website root | Successful HTTP response |
| Request to a nonexistent page | HTTP 404 response, if the server is configured normally |

The actual status codes and results will be recorded after the requests are executed.

## 4. Application Logs

The Docker logs command will be used to inspect requests recorded by the Nginx container. The logs will help identify requested paths, response status codes, and possible errors.

## 5. Container Resource Metrics

The `docker stats` command will be used to monitor the container's CPU usage, memory consumption, network input/output, and other available resource metrics.

The actual measurements will be documented after monitoring the running container.

## 6. Evidence

The following screenshots will be collected and saved in the `screenshots/` directory:

- Nginx container deployment.
- HTTP traffic simulation.
- Application log inspection.
- Live container resource metrics.

## 7. Conclusion

Container observability helps an engineer understand how an application behaves while running. HTTP responses show whether requests succeed, application logs provide details about incoming requests, and resource metrics help evaluate the container's use of system resources.

Actual test results and screenshots will be added after completing the corresponding laboratory checkpoints.
