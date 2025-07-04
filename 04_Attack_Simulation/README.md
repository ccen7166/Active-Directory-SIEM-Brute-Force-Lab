# 04 – Attack Simulation

This section documents the attack techniques used to simulate adversary behavior in the lab environment. The purpose of these simulations was to generate realistic security logs and validate detection capabilities in Splunk.

---

## Tools Used

- **Hydra** – Credential brute force attack tool via RDP
- **Atomic Red Team** – Adversary simulation framework mapped to MITRE ATT&CK®

---

## Simulated Techniques

| Technique ID | Technique Name                   | Tool               |
|--------------|----------------------------------|--------------------|
| T1110        | Brute Force                      | Hydra              |
| T1136.001    | Create Account: Local Account    | Atomic Red Team    |
| T1059.001    | Command and Scripting Interpreter: PowerShell               | Atomic Red Team    |

---

## 1) Hydra Brute Force Attack

**Objective:** Simulate repeated RDP login attempts against the target Windows machine using a known password wordlist to demonstrate brute force attack detection. This test used the rockyou.txt wordlist (copied and renamed as passwords.txt) to attempt logins with the user account tsmith.

**Command Used:**
`hydra -V -f -l tsmith -P password.txt rdp://192.168.10.100 -v`

**Expected Outcome:**

- Multiple failed login events (Windows Event ID 4625) recorded in Security logs
- Sysmon process creation logs
- Splunk detection of repeated login attempts and alerting based on frequency thresholds

**Screenshots:**
![image](https://github.com/user-attachments/assets/f7a5c87a-ea13-41a2-903a-e87ecf04279a)
![image](https://github.com/user-attachments/assets/7c4814e7-3052-425b-83de-a14da8d3806d)

---

## 2) Atomic Red Team Simulation

**Objective:**
Execute small, controlled simulations of common adversary techniques mapped to MITRE ATT&CK® to generate logs and validate Splunk detections.


**2a) T1136.001 – Create Account: Local Account**

Simulates the creation of a new local user account, a technique adversaries use to maintain persistence.

**Command Used:**

`Invoke-AtomicTest T1136.001`

**Expected Outcome:**

Windows Security Event ID 4720 (A user account was created)

Sysmon process creation logs

Splunk detection of unauthorized account creation

**Screenshot:**
![image](https://github.com/user-attachments/assets/962dfd2b-cdd2-444a-ae35-a9d4781a1a24)


**2b) T1059.001 – Command and Scripting Interpreter: PowerShell**

Simulates execution of a PowerShell command to represent script-based attack techniques.

**Command Used:**

`Invoke-AtomicTest T1059.001`

**Expected Outcome:**

Sysmon Event ID 1 (Process Create) with PowerShell in the command line

Windows Event Log entries for PowerShell execution

Splunk detection of suspicious PowerShell usage

**Screenshots:**
![image](https://github.com/user-attachments/assets/34e67fe7-3e1d-4b63-ab1a-b542e68f5a4d)








