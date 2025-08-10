# Beginner Bug Bounty Recon Project

**Objective:**  
A beginner-friendly, ethical hacking practice project simulating the early stages of a bug bounty engagement — from reconnaissance to mock vulnerability reporting — using only legal and authorized targets.

---

## 📌 Overview
This project walks through:
1. **Setting up essential tools**
2. **Picking a legal target**
3. **Performing reconnaissance**
4. **Testing for safe, beginner-level vulnerabilities**
5. **Writing a professional bug report**

> **Disclaimer:** This project is for educational purposes only. Only test systems you have explicit permission to assess.

---

## 🎯 Why This Project?
- Build foundational bug bounty skills
- Practice recon and vulnerability discovery safely
- Learn to write professional bug reports for your portfolio

---

## 🛠️ Tools Used
| Tool | Purpose |
|------|---------|
| `nmap` | Network scanning |
| `amass` | Subdomain enumeration |
| `httpx` | Probing live hosts |
| `waybackurls` | Discover historical URLs |
| Burp Suite CE / OWASP ZAP | Manual web testing |
| `nikto` | Basic web server misconfiguration scan |
| Obsidian / Notion | Note-taking & documentation |

---

## 🖥️ Setup Instructions

**Install Recon Tools**
```bash
sudo apt update
sudo apt install -y nmap nikto golang-go
go install github.com/owasp-amass/amass/v3/...@latest
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
go install github.com/tomnomnom/waybackurls@latest
export PATH=$PATH:$(go env GOPATH)/bin
```
