# 🐛 Bug Report Template

## 📌 Report Information
- **Report ID:** [unique-id or ticket #]
- **Date Reported:** [YYYY-MM-DD]
- **Reporter:** [Your Name / Handle]
- **Target:** [Domain / Asset Name]

---

## 🎯 Vulnerability Summary
> Provide a concise description of the issue.  
Example: *An XSS vulnerability was found on the login page that allows an attacker to inject arbitrary JavaScript.*

---

## 🔍 Details & Steps to Reproduce
1. Navigate to: [URL or endpoint]  
2. Input the following payload / request:

3. Observe: [Describe the behavior or response]  

*Expected behavior:* [What should have happened]  
*Actual behavior:* [What happened instead]  

---

## 📸 Evidence / Proof of Concept
- Screenshot: `../screenshots/[filename].png`
- Logs / Output:

---

## 🎯 Impact
Explain the security risk and what an attacker could achieve.  
Example: *This could allow attackers to steal user session tokens, redirect victims, or perform actions on behalf of logged-in users.*

---

## 🛠️ Recommended Remediation
Provide clear, actionable fixes.  
Example:
- Implement proper input validation and sanitization
- Use output encoding for user-supplied data
- Apply a Content Security Policy (CSP)

---

## ✅ References
- [OWASP Cheat Sheet](https://cheatsheetseries.owasp.org/)  
- [CWE Database](https://cwe.mitre.org/)  

---
