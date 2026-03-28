# Wireless Security Lab — WEP & WPA Cracking (Kali Linux)

This repository documents a controlled wireless security lab where I used **Kali Linux**, **Wifite**, and a **WiFi‑Emulator** to demonstrate how attackers exploit weak Wi‑Fi configurations — and how to defend against them.

> “In this assignment, I will show how we used Kali Linux to test wireless security by cracking WEP and WPA passwords.”  

All testing was performed on **emulated Wi‑Fi networks only**, never on real devices.

---

## Project Overview

This lab demonstrates:

- Cracking **WEP** using Wifite  
- Capturing and attacking **WPA handshakes**  
- Using **wifi‑emulator** to create virtual APs and clients  
- Understanding wireless encryption weaknesses  
- Applying defensive best practices for WLAN security  

This project forms part of my cybersecurity learning pathway and supports my SOC and network security development.

---

## Lab Environment

- **Kali Linux** (Virtual Machine)  
- **wifi‑emulator** (creates virtual AP + client)  
- **Wifite** (automated wireless attack tool)  
- Virtual interfaces: `wlan0`, `wlan1`, `wlan2`  
- All attacks performed in a **safe, isolated lab environment**

---

## Key Learning Outcomes

- Why WEP is insecure and easily cracked  
- How WPA handshakes are captured and attacked  
- How deauthentication attacks work  
- How password strength affects WPA cracking  
- How to harden wireless networks against common threats  
- How attackers think — and how defenders can respond  

---

## 📂 Repository Structure

This project is organised into clear folders so each part of the wireless security lab is easy to navigate.

| Folder / File | Description |
|---------------|-------------|
| [`report/`](report) | Contains the full wireless security report. |
| └── [`wireless_security_report.md`](report/wireless_security_report.md) | Detailed write‑up including introduction, methodology, results, and recommendations. |
| [`lab-notes/`](lab-notes) | Step‑by‑step walkthroughs of WEP and WPA attacks performed in the lab. |
| └── [`wep_cracking_walkthrough.md`](lab-notes/wep_cracking_walkthrough.md) | Full WEP cracking procedure using Wifite. |
| └── [`wpa_cracking_walkthrough.md`](lab-notes/wpa_cracking_walkthrough.md) | WPA handshake capture and cracking walkthrough. |
| [`checklists/`](checklists) | Practical WLAN security checklist for defensive hardening. |
| └── [`wlan_security_checklist.md`](checklists/wlan_security_checklist.md) | Security requirements, improvements, and comments. |
| [`images/`](images) | Screenshots from the emulator and cracking process. |
| └── `Emulator.png` | WiFi‑Emulator AP/Client setup screenshot. |
| └── `Wifite Cracking.png` | WPA handshake capture + cracking output. |
| [`README.md`](README.md) | Overview of the project, tools used, learning outcomes, and navigation. |



---

## 📝 Included Documentation

### **Wireless Security Report**
Full write‑up including introduction, vulnerabilities, methodology, results, and recommendations.  
➡️ `report/wireless_security_report.md`

### **WEP Cracking Walkthrough**
Step‑by‑step guide showing how WEP was cracked using Wifite.  
➡️ `lab-notes/wep_cracking_walkthrough.md`

### **WPA Handshake Walkthrough**
Short explanation of WPA handshake capture and password cracking.  
➡️ `lab-notes/wpa_cracking_walkthrough.md`

### **WLAN Security Checklist**
A practical checklist for securing wireless networks.  
➡️ `checklists/wlan_security_checklist.md`

---

## Defensive Recommendations

This project reinforces key wireless security practices:

- Use **WPA2/WPA3** instead of WEP/WPA  
- Disable **WPS**  
- Use **strong, complex passwords**  
- Update router firmware regularly  
- Monitor connected devices  
- Understand attacker techniques to improve defence  

---

## ⚠️ Ethical Use

This project was completed **only** in a controlled lab environment using emulated Wi‑Fi networks.  
These techniques must **never** be used on real networks without explicit permission.

---

## Contact

If you’d like to discuss wireless security or SOC learning:

- **GitHub:** https://github.com/AlAbbas-cloud  
- **LinkedIn:** https://www.linkedin.com/in/ali-abbas-895bb8268  

---


