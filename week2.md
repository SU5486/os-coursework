# Week 2 – Security Planning and Testing Methodology

## 1. Introduction

The focus of this part was to plan a secure baseline for the Ubuntu Server and to design a performance testing methodology. No system configuration changes were implemented during this phase. Instead, potential risks were identified and appropriate security controls were planned to guide later implementation.

This planning stage ensures that security and performance considerations are addressed in a structured way before any advanced configuration is applied.

---

## 2. Security Objectives

The primary security objective is to protect the server from unauthorised access while still allowing legitimate remote administration. As the server is accessed remotely using SSH, strong authentication and access control are essential.

Another objective is to reduce the system’s attack surface by limiting network exposure, restricting user privileges, and applying industry-standard security practices.

---

## 3. Performance Testing Plan

Performance testing will be carried out remotely from the workstation using SSH. Monitoring will be performed while different workloads are executed on the server to observe how system resources are used under varying conditions.

The following performance metrics will be monitored:
- CPU usage
- Memory usage
- Disk I/O performance
- Network throughput and latency

Monitoring tools such as `top`, `htop`, `vmstat`, `iostat`, and network utilities will be used to observe system behaviour in real time. Performance data will be collected during baseline testing, under application load, and after applying optimisation changes.

All monitoring activities will be conducted remotely via SSH, reflecting real-world server administration practices.

---

## 4. Security Configuration Checklist

The following checklist outlines the planned security controls that will be implemented in later weeks of the coursework.

| Security Area | Planned Control |
|--------------|----------------|
| SSH Hardening | Disable root login and restrict access to authorised users |
| Firewall Configuration | Use UFW to allow only essential incoming connections |
| Mandatory Access Control | Apply AppArmor to restrict application permissions |
| Automatic Updates | Enable automatic installation of security updates |
| User Privilege Management | Use non-root administrative users with sudo access |
| Network Security | Use NAT networking and controlled port forwarding |

---

## 5. Threat Model

Several potential security threats were identified along with planned mitigation strategies.

| Threat | Description | Mitigation Strategy |
|------|------------|-------------------|
| Brute-force SSH attacks | Repeated login attempts to gain unauthorised access | Enforce strong authentication and limit SSH access |
| Privilege escalation | A user gains higher permissions than intended | Apply least-privilege principles and sudo controls |
| Misconfiguration | Incorrect system settings expose vulnerabilities | Follow security checklists and verify configurations |
| Unpatched vulnerabilities | Outdated software contains known security flaws | Enable automatic security updates |

---

## 6. Testing Methodology Summary

Security and performance testing will follow a structured approach. Baseline measurements will be recorded before running workloads, followed by monitoring during active load. Results will then be compared after applying optimisation or security changes.

This approach allows the impact of each configuration decision to be measured and evaluated using quantitative data.

---

## 7. Reflection

This week highlighted the importance of planning security and performance strategies before implementing system changes. Identifying potential threats early helped clarify which security controls are necessary and why they are important. Designing the performance testing methodology in advance also ensures that later analysis is consistent and meaningful.
