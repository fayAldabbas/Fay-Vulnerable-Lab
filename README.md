# Fay Vulnerable Lab – OWASP Top 10

Fay Vulnerable Lab is a hands-on training project focused on identifying,
exploiting, and remediating common web application vulnerabilities based on
the OWASP Top 10 framework.

---

## 📌 Project Overview
Fay Vulnerable Lab is an intentionally vulnerable web application designed to
demonstrate practical Web Application Security Assessment techniques.
The project combines Manual Static Code Review and Dynamic Penetration Testing
to identify real-world security flaws, analyze their root causes, and apply
secure coding remediations aligned with OWASP best practices.

---

## 🔬 Methodology
The security assessment was conducted using a hybrid methodology based on the
OWASP Web Security Testing Guide (WSTG):

### White Box Testing
- Manual Static Code Review (grep-based discovery)
- Source code inspection (Node.js / Express.js / SQLite)

### Dynamic Penetration Testing
- Authentication and session testing
- Authorization and access control testing
- Input validation and injection testing

---

## 🧰 Technology Stack
- Backend: Node.js (Express.js)
- Frontend: EJS (Embedded JavaScript Templates)
- Database: SQLite3
- Environment: Docker (isolated vulnerable lab)

---

## 🚨 Key Findings (Mapped to OWASP Top 10 – 2021)

### 🔴 High Severity (7)
- SQL Injection – Authentication Bypass (A03: Injection)
- Authentication Bypass via Inconsistent Input Normalization (A07: Identification and Authentication Failures)
- Stored Cross-Site Scripting (XSS) (A03: Injection)
- Broken Access Control – Vertical Privilege Escalation (A01: Broken Access Control)
- Insecure File Upload (A05: Security Misconfiguration)
- Sensitive Data Exposure (A02: Cryptographic Failures)
- Cryptographic Failures – Insecure Password Hashing (MD5) (A02: Cryptographic Failures)

### 🟠 Medium Severity (1)
- Vulnerable and Outdated Components (A06: Vulnerable and Outdated Components)

---

## 📄 Full Security Assessment Report
A comprehensive security assessment report is included, covering:
- Static and dynamic analysis
- Proof-of-Concept (PoC) exploitation
- Root-cause analysis
- Secure code remediation recommendations

📄 **OWASP Top 10 Assessment Report (PDF)**

---

## 🎯 Skills Demonstrated
- OWASP Top 10 Web Application Security Assessment
- Manual Static Code Review (White Box Testing)
- Web Application Penetration Testing
- Authentication & Authorization Security Analysis
- Secure Coding and Remediation Techniques
- Vulnerability Severity and Risk Assessment

---

## 🐳 Docker Lab Environment
A Dockerized environment is provided to safely deploy and test the vulnerable
application without affecting production systems.

---

## ⚠️ Disclaimer
This project is intended strictly for educational and training purposes.
All vulnerabilities are intentionally introduced in a controlled lab
environment and must not be deployed in real-world production systems.
