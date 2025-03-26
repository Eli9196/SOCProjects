

## **Project 3: Malware Analysis & Reverse Engineering**
### **Scripts & Setup**
1. **Install Remnux (Linux)**
   ```bash
   wget -qO - https://remnux.org/install.sh | sudo bash
Install FLARE VM (Windows)

powershell
Copy
Edit
Invoke-WebRequest -Uri https://github.com/fireeye/flare-vm -OutFile FLARE-VM.zip
Expand-Archive FLARE-VM.zip
Extract File Hash

bash
Copy
Edit
sha256sum malware.exe
Monitor Registry Changes

powershell
Copy
Edit
Get-EventLog -LogName Security -Newest 50 | Select-String "Registry"
README.md
markdown
Copy
Edit
# Malware Analysis & Reverse Engineering

## Overview
This project sets up a malware analysis lab with Remnux and FLARE VM to inspect malware behavior, extract IoCs, and generate reports.

## Setup
1. Install **Remnux** (Linux) or **FLARE VM** (Windows).
2. Analyze malware samples:
   ```bash
   sha256sum malware.exe
   Monitor registry and network changes.

Key Findings
Extracted malware IoCs.

Identified registry modifications.

## Conclusion
Understanding malware behavior helps in cybersecurity defense.

