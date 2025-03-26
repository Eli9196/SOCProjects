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
