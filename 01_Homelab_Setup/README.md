# 01 - Homelab Setup

## Overview

Configured a homelab environment with 4 virtual machines:
- **Windows Server 2022** – Active Directory Domain Controller (ADDC01)
- **Ubuntu Server 24.04.2** – Splunk SIEM server
- **Windows 10** – Target machine
- **Kali Linux** – Attacker machine

---

## Steps

1. Installed VirtualBox
2. Created VMs in VirtualBox - all 4 VMS are pictured below.
   ![Screenshot 2025-07-01 211111](https://github.com/user-attachments/assets/a2c885c9-7155-4069-9513-2b08cef9743e)

3. Assigned static IP addresses for consistent networking with these settings:
      ![Screenshot 2025-07-01 212326](https://github.com/user-attachments/assets/59101237-549c-4d73-ba8d-ec3938d36e90)
   
4. Configured Host-Only Network (IP 192.168.10.0) to isolate lab traffic
5. Verified connectivity with `ping` and `RDP`

---

## Network Diagram

![Screenshot 2025-07-01 193414](https://github.com/user-attachments/assets/e10012dc-3fe4-4c9f-af6e-633f0b849bed)

---

## Key Takeaways

- Reinforced my understanding of static vs. dynamic IP addresses and the protocols associated with them.
- Learned that Netplan is a useful tool for configuring network settings using YAML files to simplify the configuration process.
- Initially struggled to set a static IP because edits in the Netplan file (/etc/netplan/50-cloud-init.yaml) were temporary due to cloud-init defaults.
- Resolved the issue by disabling cloud-init networking, which allowed persistent static IP configuration.


