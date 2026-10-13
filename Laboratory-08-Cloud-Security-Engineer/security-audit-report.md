# Security Audit Report

**Student:** Anthony Cabading  
**Laboratory:** 08 – Cloud Security Engineer

## 1. Principle of Least Privilege (PoLP)

The Principle of Least Privilege is a security practice that gives users, applications, and services only the permissions required to perform their assigned tasks. It is important because limiting unnecessary access reduces the possibility of unauthorized changes, accidental errors, and security breaches.

For example, a regular user should not automatically receive administrator privileges unless those privileges are necessary for a specific task.

## 2. Attack Surface

An attack surface refers to all possible entry points that an unauthorized person might attempt to exploit in a computer system or network. These may include open network ports, running services, applications, and user accounts.

Reducing the attack surface is important because unnecessary services and exposed ports can create additional security risks. Disabling unused services and restricting network access can help protect a server.

## 3. Default Deny Policy

A Default Deny policy blocks incoming network connections unless they are explicitly permitted by a firewall rule.

This approach is generally safer than allowing all incoming traffic and manually blocking individual threats because new or unexpected services are not automatically accessible.

For this laboratory, the firewall will be configured to deny incoming traffic by default while allowing authorized SSH access on port 22 and web application access on port 8080.

## Conclusion

Applying the Principle of Least Privilege, reducing the attack surface, and implementing a Default Deny firewall policy can improve server security. These practices help ensure that only necessary services and authorized network connections are permitted.

## References

- National Institute of Standards and Technology. (n.d.). *Least privilege*. CSRC Glossary. https://csrc.nist.gov/glossary/term/least_privilege
- OWASP Foundation. (n.d.). *Attack surface analysis cheat sheet*. https://cheatsheetseries.owasp.org/cheatsheets/Attack_Surface_Analysis_Cheat_Sheet.html
- Ubuntu. (n.d.). *Firewall*. Ubuntu Server documentation. https://documentation.ubuntu.com/server/how-to/security/firewalls/
