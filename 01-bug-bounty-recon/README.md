# Beginner Bug Bounty Recon Project  

![Made with Bash](https://img.shields.io/badge/Made%20with-Bash-blue)  
![Beginner Friendly](https://img.shields.io/badge/Level-Beginner-green)  
![Ethical Hacking](https://img.shields.io/badge/Focus-Ethical%20Hacking-red)  
![License: MIT](https://img.shields.io/badge/License-MIT-yellow)

**Objective:**  
A beginner-friendly, ethical hacking practice project simulating the early stages of a bug bounty engagement — from reconnaissance to mock vulnerability reporting — using only legal and authorized targets.

---

## 📂 Project Structure
```bash
01-bug-bounty-recon/
├── scripts/                # Recon automation scripts
│   └── recon-scan.sh
├── reports/                # Mock bug reports
│   ├── bug-report-template.md
│   ├── sample-xss-report.md
│   └── sample-nmap-report.md
├── screenshots/            # Evidence screenshots
│   ├── poc.png
│   └── nmap-ssh-scan.png
└── README.md               # Project documentation
```

⸻

📌 Overview

This project walks through:
	1.	Setting up essential tools
	2.	Picking a legal target
	3.	Performing reconnaissance
	4.	Testing for safe, beginner-level vulnerabilities
	5.	Writing a professional bug report

Disclaimer: This project is for educational purposes only. Only test systems you have explicit permission to assess.

⸻

🎯 Why This Project?
	•	Build foundational bug bounty skills
	•	Practice recon and vulnerability discovery safely
	•	Learn to write professional bug reports for your portfolio

⸻

🛠️ Tools Used

Tool	Purpose
nmap	Network scanning
amass	Subdomain enumeration
httpx	Probing live hosts
waybackurls	Discover historical URLs
Burp Suite CE / OWASP ZAP	Manual web testing
nikto	Basic web server misconfiguration scan
Obsidian / Notion	Note-taking & documentation


⸻

🖥️ Setup Instructions

Install Recon Tools

sudo apt update
sudo apt install -y nmap nikto golang-go
go install github.com/owasp-amass/amass/v3/...@latest
go install github.com/projectdiscovery/httpx/cmd/httpx@latest
go install github.com/tomnomnom/waybackurls@latest
export PATH=$PATH:$(go env GOPATH)/bin


⸻

🔄 Workflow Overview

flowchart TD
    A[Pick Legal Target] --> B[Reconnaissance]
    B --> C[Scanning & Enumeration]
    C --> D[Vulnerability Discovery]
    D --> E[Document Findings]
    E --> F[Write Professional Bug Report]


⸻

🚀 Example Usage

Run recon on a target domain:

./scripts/recon-scan.sh -d target.com -o results/

Results will be saved in the results/ directory, including subdomains, live hosts, and Nmap scans.

⸻

📑 Sample Reports
	•	XSS Vulnerability Report
	•	Open SSH Weak Configuration Report

---

⚡ With these fixes, your README will:  
- Render diagrams properly (Mermaid support).  
- Show a nice tree layout for structure.  
- Display sample reports as clickable links instead of code text.  
