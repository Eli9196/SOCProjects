## **Project 4: Log Analysis & Correlation with SIEM**
### **Scripts & Setup**
1. **Install Splunk**
   ```bash
   wget -O splunk.deb https://download.splunk.com/products/splunk/releases/latest/linux/splunk-latest-linux-2.6-amd64.deb
   sudo dpkg -i splunk.deb
Install Elastic Stack

bash
Copy
Edit
sudo apt install -y elasticsearch logstash kibana
Collect Windows Logs using Sysmon

powershell
Copy
Edit
wevtutil qe Security /c:50 /rd:true /f:text
Detect Privilege Escalation in Splunk

splunk
Copy
Edit
index=security EventCode=4672 | table _time, User, Process
README.md
markdown
Copy
Edit
# Log Analysis & Correlation with SIEM

## Overview
This project collects logs from Windows Event Viewer, Sysmon, and Suricata IDS to detect security events using Splunk and Elastic Stack.

## Setup
1. Install Splunk and Elastic Stack.
2. Collect and analyze logs.

## Detection Techniques
- **Failed Logins**: Monitor authentication failures.
- **Privilege Escalation**: Detect admin-level actions.

## Conclusion
Log analysis is critical for detecting security threats in real-time.
