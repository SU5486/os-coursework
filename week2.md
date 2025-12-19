# Week 2 – Security Planning and Threat Model

## 1. Security Objectives

The main security objective for this system is to protect the Ubuntu Server from unauthorised access while allowing legitimate remote administration. As the server is accessible over a network, strong access control and secure communication are essential.

Another objective is to minimise potential attack surfaces by disabling unnecessary services and following the principle of least privilege. This ensures that users only have access to the permissions required to perform their tasks.

---

## 2. Threat Identification

Several potential security threats were identified during the planning stage. These include unauthorised SSH access, brute-force login attempts, and privilege escalation attacks. As the server is managed remotely, SSH represents the primary attack vector.

There is also a risk of misconfiguration, which could expose services unintentionally or allow insecure authentication methods. Human error is therefore considered a significant threat.

---

## 3. User and Access Management

To reduce security risks, the system is designed to use a non-root administrative user for day-to-day management. Direct root login is avoided to prevent accidental system damage and to reduce the impact of a compromised account.

Administrative privileges are granted using the sudo mechanism, which allows actions to be logged and controlled. This approach follows standard Linux security best practices.

---

## 4. Authentication Strategy

SSH is selected as the primary method of remote access due to its strong encryption and widespread industry use. Password-based authentication is initially enabled to allow access during setup, with the intention of enforcing stronger authentication methods in later weeks.

The use of SSH keys is planned to further improve security by eliminating password-based logins. This reduces the risk of brute-force attacks and credential theft.

---

## 5. Network Security Considerations

The server operates behind a NAT network provided by VirtualBox, which limits direct exposure to external networks. Port forwarding is configured explicitly for SSH access, ensuring that only required ports are accessible.

A firewall strategy is planned using UFW to control incoming and outgoing traffic. Only essential services will be permitted, reducing the system’s overall attack surface.

---

## 6. Security Tools and Controls

Ubuntu Server includes built-in security tools that are planned for use throughout the coursework. These include OpenSSH for secure access, UFW for firewall management, and system logging for monitoring administrative actions.

Regular updates are also considered part of the security plan to ensure vulnerabilities are patched in a timely manner.

---

## 7. Security Planning Summary

This week focused on identifying potential risks and planning appropriate security controls before system implementation. By defining users, access methods, and network restrictions early, the system is prepared for secure deployment.

The security decisions made in this week guide the configuration tasks completed in later weeks, ensuring a structured and consistent approach to system security.
