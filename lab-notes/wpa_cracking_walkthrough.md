# WPA Handshake Capture & Cracking Walkthrough (Kali Linux + Wifite)

This walkthrough explains how WPA authentication can be tested in a **safe, emulated wireless lab** using Kali Linux, Wifite, and wifi‑emulator.  
The goal is to understand how attackers capture WPA handshakes and why **password strength** is critical for WPA security.

All testing was performed on **virtual Wi‑Fi networks only**.

---

## 🧪 Lab Setup

The environment was created using **wifi‑emulator**, which generated:

- A virtual Access Point (WPA‑protected)
- A virtual Client
- Three virtual Wi‑Fi interfaces:
  - `wlan0` → Access Point  
  - `wlan1` → Client  
  - `wlan2` → Attacker / Monitor mode  

To verify interfaces:

```bash
ip a
```

---

