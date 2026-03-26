# 🔓 WEP Cracking Walkthrough (Kali Linux + Wifite)

This walkthrough documents the exact steps used to crack a WEP‑protected wireless network in a **safe, emulated lab environment** using Kali Linux, Wifite, and wifi‑emulator.  
The purpose of this exercise is to understand how attackers exploit outdated encryption — and why WEP must never be used on real networks.

---

## 🧪 Lab Setup

The wireless environment was created using **wifi‑emulator**, which generated:

- A virtual Access Point (AP)  
- A virtual Client  
- Three virtual Wi‑Fi interfaces:  
  - `wlan0` → Access Point  
  - `wlan1` → Client  
  - `wlan2` → Attacker / Monitor mode  

To confirm the interfaces, the following command was used:

```bash
ip a
```

---

