# Firewall Configuration Report

**Student:** Anthony Cabading  
**Laboratory Activity:** 08 – Cloud Security Engineer  
**Environment:** KillerCoda Ubuntu 24.04  
**Tools:** Docker, Nginx, UFW, and cURL

## 1. Objective

The purpose of this activity was to configure a firewall on an Ubuntu cloud environment, apply a default deny policy, and verify that an Nginx web application remained accessible after the security configuration.

## 2. Application Deployment

The Nginx web server was deployed using Docker.

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
```

The application was tested using:

```bash
curl -I http://localhost:8080
```

**Observed Result:** HTTP/1.1 200 OK

The response confirmed that the Nginx application was accessible locally through port 8080.

## 3. Initial Firewall Status

The firewall status was checked using:

```bash
ufw status verbose
```

**Observed Result:** Status: inactive

This indicated that UFW was not yet enabled.

## 4. Firewall Configuration

The following commands were executed to configure the firewall:

```bash
ufw allow 22/tcp
ufw default deny incoming
ufw default allow outgoing
ufw allow 8080/tcp
ufw show added
ufw enable
```

These commands allowed SSH and application traffic, established the default firewall policies, and activated UFW.

## 5. Firewall Verification

The firewall configuration was verified using:

```bash
ufw status verbose
```

**Observed Results:**

- Firewall Status: Active
- Logging: On (low)
- Default Incoming: Deny
- Default Outgoing: Allow
- Default Routed: Deny
- Port 22/TCP: Allow
- Port 8080/TCP: Allow
- IPv6 Rules: Enabled for both ports

## 6. Application Connectivity Test

After activating UFW, the Nginx application was tested again.

```bash
curl -I http://localhost:8080
```

**Observed Result:** HTTP/1.1 200 OK

The successful HTTP response confirmed that the application remained accessible from the local Ubuntu environment after the firewall was enabled.

**Technical Limitation:** Docker-published ports may bypass certain UFW filtering rules. Therefore, this local connectivity test does not independently prove that external traffic is restricted as intended.

## 7. Security Observations

The firewall configuration demonstrated how explicit access rules can be combined with restrictive default policies. SSH access was permitted to support remote administration, while port 8080 was allowed for the Nginx application.

This activity also highlighted the importance of validating security controls rather than relying exclusively on configuration status.

## 8. Conclusion

This laboratory demonstrated the basic process of configuring and verifying an Ubuntu firewall. UFW was successfully activated with a default deny incoming policy, and the Nginx application remained accessible locally.

Additional external connectivity testing would be necessary to confirm the effective filtering behavior of Docker-published ports.

## 9. Screenshot Evidence

The following evidence will be attached after completing the laboratory:

- `screenshots/vulnerable-app-running.png`
- `screenshots/firewall-activated.png`
- `screenshots/firewall-allowed.png`
