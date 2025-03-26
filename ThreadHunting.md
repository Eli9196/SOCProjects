Project 2: Threat Hunting in a Simulated Environment
Scripts & Setup
Install Wireshark and Zeek

bash
Copy
Edit
#!/bin/bash
sudo apt update && sudo apt install -y wireshark zeek
Capture Network Traffic with Zeek

bash
Copy
Edit
sudo zeek -i eth0 -C
Analyze DNS Queries for Suspicious Domains

bash
Copy
Edit
awk '$9 ~ /malicious-domain.com/ {print $0}' /var/log/zeek/dns.log
Identify C2 Traffic

bash
Copy
Edit
grep "suspicious-ip" /var/log/zeek/conn.log
README.md
markdown
Copy
Edit
# Threat Hunting in a Simulated Environment

## Overview
This project uses Wireshark and Zeek for network traffic analysis to detect anomalies, including phishing, C2 traffic, and suspicious DNS queries.

## Setup
1. Install required tools:
   ```bash
   sudo apt install -y wireshark zeek
