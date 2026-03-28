# WEP Cracking Walkthrough (Kali Linux + Wifite)

This walkthrough documents the exact steps used to crack a WEP‑protected wireless network in a **safe, emulated lab environment** using Kali Linux, Wifite, and wifi‑emulator.  
The purpose of this exercise is to understand how attackers exploit outdated encryption — and why WEP must never be used on real networks.

---

## Lab Setup

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

### Step 1 - Launch Wifite
Wifite is an automated wireless attack tool included in Kali Linux.

Start it by running:

```bash
wifite
```
Wifite will automatically detect available wireless interfaces.

### Step 2 - Select the Monitoring Interface
Choose `wlan2` as the monitoring interface.
This interface listens to wireless traffic and captures packets needed for the attack.

Wifite will then begin scanning for nearby networks.

### Step 3 - Identify the Target Network
Once scanning begins:

- Look for the **correct ESSID** (the Wi‑Fi name created by wifi‑emulator)
- Confirm that the network uses **WEP encryption**

Select the target when prompted.

### Step 4 - Start the Deauthentication Attack
Wifite automatically performs a **deauth attack** to force the client to disconnect.

Why this matters:

- When the client reconnects, it sends authentication packets
- These packets contain the data needed to crack WEP
- WEP relies on weak initialization vectors (IVs), which are easy to collect

This step is completely automated by Wifite.

### Step 5 - Capture the Authentication Packets
As devices reconnect, Wifite captures:

- IV packets
- Authentication frames
- Reconnection traffic

Once enough packets are collected, Wifite begins the cracking process.

### Step 6 - Crack the WEP Key
WEP cracking is extremely fast because:

- WEP uses weak encryption
- IVs repeat frequently
- Tools like Wifite can exploit these weaknesses automatically

In this lab, the WEP password was cracked in under **5 minutes.**

This demonstrates why WEP is considered **completely insecure.**

---

## Summary of the Attack Flow
1. Start Wifite
2. Select wlan2 as monitor interface
3. Scan for networks
4. Select the WEP network
5. Launch deauth attack
6. Capture IV packets
7. Crack the WEP key

All steps were performed in a **controlled, emulated environment.**

---

## Key Takeaways
- WEP can be cracked quickly with minimal effort
- Deauthentication attacks are simple and effective
- Packet capture is automated by modern tools
- WEP should never be used on any real network
- WPA2/WPA3 are required for secure wireless communication

---

## ⚠️ Ethical Notice
This walkthrough is for **educational purposes only.**

All testing was performed on **emulated Wi‑Fi networks** created specifically for this lab.

Never attempt wireless attacks on real networks without explicit permission.
