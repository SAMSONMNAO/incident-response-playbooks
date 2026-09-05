# Network Analysis & Packet Capture Incident Report

## Overview
This report consolidates network packet capture analyses and log investigations conducted across portfolio activities using `tcpdump` and Wireshark.

## 1. DNS Resolution & ICMP Error Analysis
* **Incident Log**: UDP query sent to DNS server on Port 53 (`your.machine.52444 > dns.google.domain: A? yummyrecipesforme.com`).
* **Symptom**: Server responded with ICMP error `udp port 53 unreachable`.
* **Root Cause**: The target DNS port was offline or blocked by security rules during a service disruption.

## 2. Web Traffic Inspection & Domain Redirection
* **Incident Log**: Standard TCP three-way handshake (`[SYN]`, `[SYN-ACK]`, `[ACK]`) established web connection.
* **Symptom**: Subsequent DNS queries redirected user traffic to `greatrecipesforme.com` (`192.0.2.172:56378`).
* **Root Cause**: Malicious HTTP redirection/DNS spoofing designed to redirect users away from legitimate web resources.

## 3. TCP SYN Flood Attack Analysis
* **Incident Log**: High volume of TCP `[SYN]` packets received on Ports 80/443 without matching `[ACK]` responses.
* **Symptom**: Web server connection timeouts and resource exhaustion.
* **Root Cause**: Denial of Service (DoS) attack targeting web server socket availability.

## Technical Mitigation Steps
1. Deploy redundant DNS servers to maintain domain resolution availability.
2. Implement firewall egress filtering to block spoofed outbound DNS requests.
3. Enable TCP SYN cookies and rate-limiting firewall rules to filter flood traffic.
