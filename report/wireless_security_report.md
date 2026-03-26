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
5. Started the access point on **wlan0**
6. Started the client on **wlan1**
7. Prepared **wlan2** as the attacker interface

This setup allowed a safe, isolated environment for wireless testing.
