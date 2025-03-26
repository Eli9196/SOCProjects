## Projects

### **1. Incident Detection & Response Simulation**
- **Objective:** Detect security incidents using a SIEM.
- **Tools:** Wazuh, Splunk, Elastic Stack, Sysmon.
- **Setup:**
  ```bash
  bash setup.sh
  ```
- **Code Example (wazuh_rules.conf):**
  ```xml
  <group name="custom_rules">
    <rule id="100001" level="5">
      <decoded_as>json</decoded_as>
      <field name="event.action">login_failed</field>
      <description>Failed login detected</description>
    </rule>
  </group>
  ```
- **Expected Outcome:** Ability to investigate and respond to real-time security threats.

### **2. Threat Hunting in a Simulated Environment**
- **Objective:** Analyze network traffic to detect anomalies.
- **Tools:** Wireshark, Zeek, Suricata, Elastic Stack.
- **Setup:**
  ```bash
  python analyze_pcap.py pcap_analysis.pcap
  ```
- **Code Example (analyze_pcap.py):**
  ```python
  import pyshark
  capture = pyshark.FileCapture('pcap_analysis.pcap')
  for packet in capture:
      if 'HTTP' in packet:
          print(f"Suspicious HTTP request: {packet.http.host}")
  ```
- **Expected Outcome:** Hands-on experience in detecting advanced threats.

### **3. Malware Analysis & Reverse Engineering**
- **Objective:** Study malware behavior in a controlled environment.
- **Tools:** FLARE VM, Remnux, Ghidra, Cuckoo Sandbox.
- **Setup:**
  ```bash
  python analyze_malware.py malware_sample.exe
  ```
- **Code Example (analyze_malware.py):**
  ```python
  import hashlib
  def get_hash(file):
      with open(file, 'rb') as f:
          return hashlib.sha256(f.read()).hexdigest()
  print("Malware Hash:", get_hash('malware_sample.exe'))
  ```
- **Expected Outcome:** Learn malware techniques and extract Indicators of Compromise (IoCs).

### **4. Log Analysis & Correlation with SIEM**
- **Objective:** Improve log monitoring and correlation.
- **Tools:** Splunk, Wazuh, Windows Event Viewer, Sysmon.
- **Setup:**
  ```bash
  python log_parser.py logs.json
  ```
- **Code Example (log_parser.py):**
  ```python
  import json
  with open('logs.json') as f:
      logs = json.load(f)
  for log in logs:
      if 'failed login' in log['message']:
          print("Alert: Failed login detected")
  ```
- **Expected Outcome:** Enhanced log analysis and security monitoring skills.

### **5. SOC Playbook Development**
- **Objective:** Create structured incident response procedures.
- **Tools:** Markdown, Python (for automation).
- **Setup:**
  ```bash
  python automate_alerts.py
  ```
- **Code Example (automate_alerts.py):**
  ```python
  import time
  alerts = ["Phishing Attempt Detected", "Malware Execution", "Unauthorized Access"]
  for alert in alerts:
      print(f"[ALERT] {alert}")
      time.sleep(2)
  ```
- **Expected Outcome:** Documented response workflows for SOC teams.

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/Eli9196/SOC-Analyst-Projects.git
   ```
2. Navigate to a project folder and follow the setup instructions in the README.md.
3. Contribute by adding new detection rules, scripts, or research!

## License
