# Wireless Security Report — WEP & WPA Cracking (Kali Linux)

This report documents a wireless security lab conducted using **Kali Linux**, **Wifite**, and a **WiFi‑Emulator** to demonstrate how attackers exploit weak Wi‑Fi configurations and how to defend against them.

> “In this assignment, I will show how we used Kali Linux to test wireless security by cracking WEP and WPA passwords.”  
> *(from original assignment document)*

All testing was performed on **emulated Wi‑Fi networks only**, never on real devices.

---

## Introduction

This lab explored wireless encryption weaknesses by creating a virtual Wi‑Fi environment and performing controlled attacks against WEP and WPA networks.  
Using tools such as **wifi‑emulator** and **Wifite**, I simulated both an access point and a client, then captured authentication traffic to understand how attackers exploit weak configurations.

The objective was to build practical knowledge of wireless security, encryption standards, and defensive best practices.

---

## WPA and Its Vulnerabilities

WPA (Wi‑Fi Protected Access) is more secure than WEP, but it still has weaknesses.  
If an attacker captures the **4‑way handshake**, they can attempt to crack the password using dictionary or brute‑force attacks.

Key weaknesses include:

- Weak or common passwords  
- Poor router configuration  
- WPS enabled  
- Outdated WPA (instead of WPA2/WPA3)

> “Weak passwords make WPA easier to crack.” *(from assignment document)*

---

## Preparing the Lab Environment

The wireless lab was built using:

- **Kali Linux** (virtual machine)
- **wifi‑emulator** (to create virtual AP and client)
- **Wifite** (automated wireless attack tool)
- Virtual interfaces: `wlan0`, `wlan1`, `wlan2`

### Steps performed:

1. Installed **wifi‑emulator**  
2. Created configuration files for:
   - Virtual Access Point  
   - Virtual Client  
3. Generated three virtual Wi‑Fi interfaces  
4. Verified interfaces using:

   ```bash
   ip a
   ```
5. Started the access point on `wlan0`
6. Started the client on `wlan1`
7. Prepared `wlan2` as the attacker interface

This setup allowed a safe, isolated environment for wireless testing.

---

## Method Used to Crack WEP

The WEP cracking process was performed using **Wifite:**

1. Launched Wifite in Kali Linux
2. Selected `wlan2` as the monitoring interface
3. Scanned for available networks
4. Identified the target ESSID
5. Performed a **deauthentication attack** to force reconnection
6. Captured the authentication handshake
7. Wifite automatically attempted to crack the WEP key
8. The password was successfully cracked within minutes

This demonstrated how outdated WEP encryption can be broken quickly with minimal effort.

---

## Results

### WiFi Emulator
A virtual AP and client were successfully created using wifi‑emulator, allowing safe wireless testing.

### Wifite Cracking
Wifite captured the handshake and cracked the WEP key rapidly, confirming the weakness of WEP encryption.

Screenshots will be added soon.

---

## Recommendations
To improve wireless security:

- Use **WPA2** or **WPA3** instead of WEP/WPA
- Set **strong, complex passwords**
- Disable **WPS**
- Update router firmware regularly
- Monitor connected devices
- Use firewalls and intrusion detection systems
- Understand attacker techniques to improve defence
- Only practice wireless testing in safe lab environments

---

## WLAN Security Checklist

A detailed checklist is available in:

➡️ [WLAN Security Checklist](../checklists/wlan_security_checklist.md)

It includes:

- Encryption requirements
- Password complexity
- Firmware updates
- Device monitoring
- WPS configuration

---

## Bibliography

- Kali Linux Documentation (2023)
- Wifite GitHub Repository (2023)
- TryHackMe Wireless Security Labs (2023)
- Wi‑Fi Alliance: WPA/WPA2/WPA3 Security (2023)
- TAFE Cybersecurity Lab Notes (2025)

---

## ⚠️ Ethical Use

This report is for **educational purposes only.**

All testing was performed on **emulated networks.**

Never attempt wireless attacks on real networks without explicit permission.
