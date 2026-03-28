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

### Step 1 - Start Wifite
Launch Wifite:

```bash
wifite
```
Wifite automatically detects wireless interfaces and begins scanning.

### Step 2 - Select the Monitoring Interface
Choose:

```Code
wlan2
```
This interface is used to:

- Capture packets
- Monitor traffic
- Perform deauthentication attacks

### Step 3 - Identify the WPA Network
During scanning:

- Look for the **WPA/WPA2 network** created by wifi‑emulator
- Confirm the correct ESSID
- Select it when prompted

Wifite will prepare to capture the WPA handshake.

### Step 4 - Perform a Deauthentication Attack
Wifite automatically sends **deauth packets** to the client.

Why this works:

- WPA uses a **4‑way handshake** when a device reconnects
- Forcing a disconnect triggers a new handshake
- Capturing this handshake is required for cracking attempts

This step is automated by Wifite.

### Step 5 - Capture the WPA Handshake
As soon as the client reconnects, Wifite listens for:

- EAPOL frames
- The 4‑way handshake
- Authentication traffic

Once captured, Wifite saves the handshake file for cracking.

You will see a message similar to:

```Code
[+] WPA Handshake Captured!
```

### Step 6 - Attempt to Crack the WPA Password
Unlike WEP, WPA **cannot** be cracked instantly.

WPA cracking depends entirely on:

- Password strength
- Dictionary quality
- Time and computing power

Wifite automatically attempts a dictionary attack using its default wordlists.

If the password is weak, it may be cracked quickly.
If the password is strong, cracking may fail - which is expected.

This demonstrates why WPA security relies heavily on **password complexity.**

---

### Summary of the WPA Attack Flow
1. Start Wifite
2. Select wlan2 as monitor interface
3. Scan for WPA networks
4. Select the target ESSID
5. Launch deauthentication attack
6. Capture the 4‑way handshake
7. Attempt dictionary cracking

### Key Takeaways
- WPA is far more secure than WEP
- WPA cracking requires capturing the handshake
- Strong passwords make WPA cracking extremely difficult
- Weak passwords remain the biggest vulnerability
- WPA2/WPA3 with long, complex passphrases is recommended

### ⚠️ Ethical Notice
This walkthrough is for **educational purposes only.**

All testing was performed on **emulated Wi‑Fi networks** created specifically for this lab.

Never attempt wireless attacks on real networks without explicit permission.
