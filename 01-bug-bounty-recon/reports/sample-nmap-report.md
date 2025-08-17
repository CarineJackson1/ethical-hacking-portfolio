# 🐛 Bug Report – Open SSH Service with Weak Configuration

## 📌 Report Information
- **Report ID:** BBP-002  
- **Date Reported:** 2025-08-16  
- **Reporter:** Carine Jackson  
- **Target:** 192.168.56.101 (authorized lab target)  

---

## 🎯 Vulnerability Summary
An SSH service was found running on port **22** with a weak configuration.  
The service allows outdated ciphers and protocols, potentially exposing the system to brute-force or downgrade attacks.

---

## 🔍 Details & Steps to Reproduce
1. Reconnaissance performed using Nmap:  
   ```bash
   nmap -sV -p22 --script ssh2-enum-algos 192.168.56.101
    ```

   PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.2p2 Ubuntu 4ubuntu2.8 (Ubuntu Linux; protocol 2.0)
| ssh2-enum-algos: 
|   kex_algorithms: (3) diffie-hellman-group1-sha1, diffie-hellman-group14-sha1, rsa1024-sha1
|   encryption_algorithms: (2) aes128-cbc, 3des-cbc
|   mac_algorithms: (2) hmac-md5, hmac-sha1
⸻

	3.	Observed behavior:
	•	Server supports deprecated algorithms (diffie-hellman-group1-sha1, aes128-cbc).
	•	Running outdated OpenSSH version (7.2p2).

⸻

📸 Evidence / Proof of Concept
	•	Screenshot: ../screenshots/nmap-ssh-scan.png
	•	Saved scan log: ../reports/nmap_scan_ssh.txt

⸻

🎯 Impact

An attacker could:
	•	Exploit weak SSH algorithms for downgrade attacks
	•	Brute force authentication more easily
	•	Gain unauthorized access to the server

⸻

🛠️ Recommended Remediation
	•	Upgrade OpenSSH to the latest stable version
	•	Disable deprecated key exchange and cipher algorithms in /etc/ssh/sshd_config
Example:

KexAlgorithms curve25519-sha256@libssh.org,diffie-hellman-group-exchange-sha256
Ciphers aes256-ctr,aes192-ctr,aes128-ctr
MACs hmac-sha2-256,hmac-sha2-512


	•	Restart SSH service after making changes.

⸻

✅ References
	•	Nmap Scripting Engine – ssh2-enum-algos
	•	OpenSSH Security Updates
	•	CWE-327: Use of a Broken or Risky Cryptographic Algorithm

---
