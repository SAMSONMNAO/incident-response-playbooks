# Enterprise Network Security & Incident Response Portfolio
## Project Overview
This repository contains formal security assessments, packet capture investigations, system hardening controls, and incident response playbooks mapped to the NIST Cybersecurity Framework (CSF). 

All technical findings, log analyses, and security frameworks have been consolidated into structured, browser-readable technical reports.

## Portfolio Structure
* **`README.md`**: Main repository overview and NIST CSF operational framework.
* **`network-analysis-report.md`**: Technical packet capture analysis covering `tcpdump` logs, Wireshark TCP/HTTP streams, UDP DNS errors, and DoS attack identification.
* **`security-hardening-framework.md`**: Defensive controls, multi-factor authentication (MFA) policies, network risk assessments, and incident containment playbooks.

## Core Technical Competencies
* **Packet Inspection & Log Analysis**: Deep inspection of TCP three-way handshakes (`[SYN]`, `[SYN-ACK]`, `[ACK]`), HTTP GET methods, DNS resolution queries, and ICMP unreachable errors using Wireshark and `tcpdump`.
* **Incident Response & Threat Containment**: Investigation and mitigation of SYN flood DoS attacks, ICMP flood DDoS attacks, web server credential brute forcing, and phishing account compromises.
* **System Hardening & Controls**: Deployment of rate-limiting firewall rules, port blocking, Multi-Factor Authentication (MFA), Intrusion Detection/Prevention Systems (IDS/IPS), and backup recovery workflows.

## NIST CSF Incident Response Execution
1. **Identify**: Audit log entries, trace source IP addresses, isolate compromised credentials, and evaluate affected network assets.
2. **Protect**: Deploy rate-limiting firewall policies, close unused ports, enforce MFA, and maintain offsite system backups.
3. **Detect**: Monitor incoming traffic through IDS/IPS appliances, verify source IP headers, and configure log alerts.
4. **Respond**: Isolate affected subnetworks, terminate unauthorized active sessions, and notify executive leadership and legal authorities.
5. **Recover**: Rebuild compromised database tables from clean backups, re-verify data integrity, and systematically restore core network services.
