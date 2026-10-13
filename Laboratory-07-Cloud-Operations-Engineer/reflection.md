# Laboratory 07 Reflection

**Student:** Anthony Cabading  
**Course:** CCM101 – Cloud Computing

## 1. Why is it important to check the host server's resources even if your containers are running perfectly?

Checking the host server is important because containers still depend on the resources of the machine where they run. Even if an application works properly, low memory, high CPU usage, or limited disk space can cause performance problems. For example, if disk space becomes full, the system may have difficulty saving logs or running other processes. Monitoring the host helps identify possible issues early and prevents them from affecting the application.

## 2. If a user complains that they cannot log into a web application, how would the Docker logs command help you solve the problem?

I would use `docker logs client-website` to check the messages produced by the container. These logs may show application errors, failed requests, or other clues about what happened when the user tried to log in. I would check the timestamps, response codes, and error messages to narrow down the possible cause. After that, I could perform additional checks based on what the logs show.

## 3. What is the difference between monitoring logs (Checkpoint 4) and monitoring metrics (Checkpoint 5)?

Logs provide details about individual events, such as HTTP requests, response codes, and application errors. Metrics show numerical measurements such as CPU usage, memory consumption, and network activity. Logs help explain what happened, while metrics help show how the system is performing. Using both allows engineers to investigate errors and determine whether resource usage may be contributing to an issue.

## 4. How do you think large enterprise companies monitor thousands of containers at the same time?

Large companies can use monitoring tools such as Prometheus and Grafana. Prometheus collects metrics from different containers and servers, while Grafana displays the information through dashboards and graphs. These tools help engineers monitor many services in one place, recognize unusual resource usage, and investigate possible performance problems. Automated alerts can also notify the team when certain measurements exceed expected limits.

## 5. How has your ability to troubleshoot Linux environments improved?

This activity helped me understand that troubleshooting requires checking evidence instead of guessing the cause of a problem. Linux commands allow me to inspect system resources, while Docker logs and metrics provide information about application behavior and performance. Testing the Nginx container also helped me understand HTTP response codes, including successful requests and a 404 error. I am now more familiar with using these tools to investigate issues in a structured way.

## Conclusion

This laboratory helped me understand the importance of combining host resource checks, application logs, and performance metrics. These practices are useful for identifying errors, investigating resource problems, and maintaining reliable cloud infrastructure.
