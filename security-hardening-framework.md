# Defensive Security Hardening & Incident Response Playbook

## Overview
This framework summarizes defensive security controls, risk assessments, and incident response playbooks compiled across portfolio activity files.

## 1. Defensive Security Controls Matrix

| Control Category | Security Action | Threat Prevented |
| :--- | :--- | :--- |
| **Authentication** | Multi-Factor Authentication (MFA) | Unverified logins, credential theft, phishing attacks. |
| **Network Perimeter** | Firewall Port Filtering & Rate-Limiting | Unauthorized port access, TCP SYN floods, ICMP DoS attacks. |
| **Monitoring** | Intrusion Detection System (IDS) rules | Malicious packet signatures, malware traffic, unauthorized access. |
| **Data Protection** | Encrypted Offsite Backups | Malware encryption, unauthorized database modification, data loss. |

## 2. Incident Response Playbook: Malware Infection & Account Compromise
* **Containment**: Immediately isolate infected host systems from the local network, disable compromised user accounts in Active Directory, and terminate active database sessions.
* **Remediation**: Remove malicious executable files, force credentials reset across affected user groups, and restore modified files or database tables from clean backup sources.

## 3. Incident Response Playbook: Network Denial of Service (DDoS)
* **Containment**: Isolate affected subnetworks, drop unauthorized traffic at the perimeter, and prioritize core business traffic.
* **Remediation**: Apply rate-limiting rules on external firewalls, filter spoofed source IP traffic, and systematically restore network services.
