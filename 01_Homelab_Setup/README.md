# 01 - Homelab Setup

## Overview

Configured a homelab environment with 4 virtual machines:
- **Windows Server 2022** – Active Directory Domain Controller
- **Ubuntu Server 24.04.2** – Splunk SIEM server
- **Windows 10** – Target machine
- **Kali Linux** – Attacker machine

---

## Steps

1. Installed VirtualBox
2. Created VMs in VirtualBox - all 4 VMS are pictured below.
   ![Screenshot 2025-07-01 211111](https://github.com/user-attachments/assets/a2c885c9-7155-4069-9513-2b08cef9743e)

4. Assigned static IP addresses for consistent networking
5. Configured Host-Only Network (IP 192.168.10.0) to isolate lab traffic
6. Verified connectivity with `ping' and `RDP`

---

## Network Diagram

![Screenshot 2025-07-01 193414](https://github.com/user-attachments/assets/e10012dc-3fe4-4c9f-af6e-633f0b849bed)

---

## Notes

- Used NAT network for initial updates and package installations
- Switched to Host-Only Network for attack simulation
