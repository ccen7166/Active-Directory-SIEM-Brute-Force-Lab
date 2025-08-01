# Active-Directory-SIEM-Brute-Force-Lab

Homelab project: Building Active Directory, simulating brute force attacks, detecting them with Splunk SIEM, and testing Atomic Red Team.

## Objective

This project demonstrates building a realistic multi-VM homelab to simulate enterprise security scenarios. The lab includes Active Directory deployment, brute force attacks using Hydra,  detection with Splunk SIEM.

### Skills Learned

This project strengthened my understanding of:
- Windows enterprise infrastructure
- Credential attack techniques
- Log collection pipelines
- Detection engineering in Splunk
- Incident response fundamentals

### Tools Used

- Windows Server 2022 – Active Directory Domain Controller
- Windows 10 – Target machine
- Kali Linux – Attacker machine
- Ubuntu Server 24.04.02 – Splunk SIEM server
- Sysmon – Enhanced Windows telemetry
- Splunk Universal Forwarder – Log collection agent
- Hydra – Brute force tool
- Atomic Red Team – MITRE ATT&CK simulation

## Project Structure

| Folder | Description |
|--------|-------------|
| <a href="https://github.com/ccen7166/Active-Directory-SIEM-Brute-Force-Lab/blob/main/01_Homelab_Setup/README.md">`01_Homelab_Setup`</a>| Virtual machine configurations, network diagram, and static IP setup |
| <a href="https://github.com/ccen7166/Active-Directory-SIEM-Brute-Force-Lab/blob/main/02_AD_Configuration/README.md">`02_AD_Configuration`</a>| Active Directory Domain Services installation and domain configuration |
| <a href="https://github.com/ccen7166/Active-Directory-SIEM-Brute-Force-Lab/blob/main/03_SIEM_Setup/README.md">`03_SIEM_Setup`</a>| Sysmon deployment and Splunk Universal Forwarder installation |
| <a href="https://github.com/ccen7166/Active-Directory-SIEM-Brute-Force-Lab/blob/main/04_Attack_Simulation/README.md">`04_Attack_Simulation`</a>| Simulated attacks: Hydra brute force and Atomic Red Team |
| <a href="https://github.com/ccen7166/Active-Directory-SIEM-Brute-Force-Lab/blob/main/README.md">`05_Detection`</a>| Search queries and analysis of attack traces |

## Steps

Detailed steps are broken down in the folders above. 

Below is the diagram diagram for this homelab project.  
![Screenshot 2025-07-01 193414](https://github.com/user-attachments/assets/0ea2d2e4-6d16-487d-b2d6-e57650701481)

## Reflection

ALWAYS TAKE SNAPSHOTS AFTER A MAJOR CHANGE IN THE VM! That was one painful lesson I had to learn when I put in the wrong syntax and messed up all the progress I made at that point. This project was challenging at times with the issues I ran into but being able to troubleshoot issues was greatly rewarding. I can't wait to do more projects and build more cybersecurity skills! 
