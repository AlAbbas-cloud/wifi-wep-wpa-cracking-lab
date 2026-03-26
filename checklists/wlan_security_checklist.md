# WLAN Security Checklist

This checklist summarises the key wireless security controls used to protect Wi‑Fi networks from common attacks.  
It is based on the findings from my wireless security lab, where I tested WEP and WPA vulnerabilities using Kali Linux, Wifite, and a WiFi‑Emulator.

---

## Encryption & Authentication

| Security Requirement | Expected Improvement | Comments |
|----------------------|----------------------|----------|
| **Use WPA2 or WPA3 encryption** | Stronger protection against attacks | WEP and WPA are outdated and easily cracked |
| **Disable WPS (Wi‑Fi Protected Setup)** | Removes a known weak point | WPS PIN attacks can bypass strong passwords |
| **Use strong, complex passwords** | Harder for attackers to guess or brute‑force | Use a mix of letters, numbers, and symbols |

---

## Network Configuration

| Security Requirement | Expected Improvement | Comments |
|----------------------|----------------------|----------|
| **Update router firmware regularly** | Fixes known bugs and vulnerabilities | Helps protect against new threats |
| **Disable unused services** | Reduces attack surface | Turn off guest networks or remote admin if not needed |
| **Change default router credentials** | Prevents easy compromise | Default logins are widely known |

---

## Monitoring & Detection

| Security Requirement | Expected Improvement | Comments |
|----------------------|----------------------|----------|
| **Monitor connected devices** | Detects unknown or suspicious activity | Check for devices that shouldn’t be connected |
| **Enable router logs** | Helps identify unusual behaviour | Useful for detecting repeated login attempts |
| **Use firewalls or IDS/IPS** | Adds an extra layer of defence | Helps block or alert on malicious traffic |

---

## Physical & Environmental Security

| Security Requirement | Expected Improvement | Comments |
|----------------------|----------------------|----------|
| **Reduce Wi‑Fi signal range if possible** | Limits external access | Prevents attackers from connecting outside the premises |
| **Place router in a secure location** | Prevents tampering | Avoid placing routers near windows or public areas |

---

## 🧭 Summary

This checklist can be used when configuring home or small‑office Wi‑Fi networks, or during wireless security assessments.  
It reinforces the importance of strong encryption, secure configuration, and continuous monitoring to defend against common wireless attacks.

