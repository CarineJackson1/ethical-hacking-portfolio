# 🐛 Bug Report – Reflected XSS on Login Page

## 📌 Report Information
- **Report ID:** BBP-001
- **Date Reported:** 2025-08-16
- **Reporter:** Carine Jackson
- **Target:** https://demo.testfire.net (authorized test target)

---

## 🎯 Vulnerability Summary
A **reflected cross-site scripting (XSS)** vulnerability was identified on the login page of `demo.testfire.net`.  
When user-supplied input is returned in the response without proper sanitization, an attacker can inject malicious JavaScript.

---

## 🔍 Details & Steps to Reproduce
1. Navigate to the login page:  
   `https://demo.testfire.net/login.jsp?username=`
2. Enter the following payload into the `username` parameter:  
   ```html
   <script>alert('XSS')</script>
```

	3.	Submit the request.

Expected behavior: Input should be properly sanitized or rejected.
Actual behavior: The payload is reflected back in the page, triggering a JavaScript alert.

⸻

📸 Evidence / Proof of Concept
	•	Screenshot: ../screenshots/xss-alert.png
	•	Burp Suite request/response log:

GET /login.jsp?username=<script>alert('XSS')</script> HTTP/1.1
Host: demo.testfire.net

⸻

🎯 Impact

An attacker could:
	•	Execute arbitrary JavaScript in the victim’s browser
	•	Steal cookies/session tokens
	•	Perform phishing attacks or redirect users
	•	Exploit authenticated users to perform unwanted actions

⸻

🛠️ Recommended Remediation
	•	Implement output encoding for user-supplied data
	•	Apply input validation and block unsafe characters (< > " ')
	•	Set a Content Security Policy (CSP) to mitigate XSS payload execution

⸻

✅ References
	•	OWASP XSS Prevention Cheat Sheet
	•	CWE-79: Improper Neutralization of Input During Web Page Generation

⸻
