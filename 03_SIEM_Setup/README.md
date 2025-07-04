# 03 - SIEM Setup

## Overview

Installed Splunk Enterprise and configured it to collect logs from the target machine using the Splunk Universal Forwarder and Sysmon.

---

## Steps

1. Installed Splunk Enterprise on Windows Server/ADDC01 and Windows machine/Target-PC
2. Installed **Sysmon** on Target-PC and ADDC01
   ![image](https://github.com/user-attachments/assets/f0c1926a-f14c-4945-ae46-0e771303fa42)
   
3. Installed **Splunk Universal Forwarder** on Target-PC and ADDC01
4. Configured inputs to collect:
   - Windows Event Logs
   - Sysmon logs
5. Verified log ingestion into Splunk
   

---

## Splunk Inputs Configuration

Configured the inputs.conf file so Universal Forwarder can forward all the logs to the endpoint.   
![image](https://github.com/user-attachments/assets/b8488918-1daf-487c-b8ac-1be8567a664e)


---

## Screenshots

![image](https://github.com/user-attachments/assets/f74f8a3e-2174-41d5-be31-5919ff36801f)


---

## Notes

- Sysmon config used: `sysmonconfig.xml`
- Windows server= ADDC01
- Windows machine= Target-PC
