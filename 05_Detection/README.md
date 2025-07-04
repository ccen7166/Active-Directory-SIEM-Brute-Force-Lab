# 05 – Detection and Analysis

This section documents how each simulated attack was detected using Splunk. Screenshots and queries show evidence of log ingestion and analysis.

---

## 🛡️ Hydra Brute Force Detection

**Search Used:**
`index=endpoint tsmith`

**Findings:**
- Multiple failed login attempts for account `tsmith` will show up as code 4625
- Host: TARGET-PC 

**Screenshot:**
![image](https://github.com/user-attachments/assets/3a130b4e-3364-4c9a-b22f-3db552263416)

Search showing code 4625
![image](https://github.com/user-attachments/assets/5b7c258b-6fa4-401f-8b76-58b6d99b4155)

Simultaneously failed login attempts show that brute force occurred
![image](https://github.com/user-attachments/assets/a239a448-8a77-4a95-8079-746c30f4713e)


---

## 🛡️ Atomic Red Team Detection

### T1136.001 – Local Account Creation

**Search Used:**
'index=endpoint NewLocalUSer'

**Findings:**
- Unauthorized account creation detected
- New account: `NewLocalUser`

**Screenshot:**
![image](https://github.com/user-attachments/assets/a4600554-022b-44f3-9401-f1198be755d1)

---

### T1059.001 – PowerShell Execution

**Search Used:**
`index=endpoint powershell`

**Findings:**
- PowerShell execution recorded
- The powershell test and SIEM report both show the command `-exec bypass -noprofile "$Xml'` was used

**Screenshot:**
![image](https://github.com/user-attachments/assets/92a4d0ea-30b3-477c-94b2-a142351ed463)
![image](https://github.com/user-attachments/assets/91fc70a4-6d9d-49b7-b0e6-105da63b7b4e)


---

## Summary

- Confirmed log ingestion for each technique
- Validated detection coverage for brute force, account creation, and PowerShell execution
- Demonstrated ability to correlate logs to MITRE ATT&CK techniques

