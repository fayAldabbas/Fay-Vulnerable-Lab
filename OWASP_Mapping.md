# OWASP Top 10 Mapping

This document maps each discovered vulnerability to the OWASP Top 10 category,
including its location in the source code and remediation approach.

---

## A03: Injection – SQL Injection Authentication Bypass

- **OWASP Category:** A03:2021 – Injection
- **Affected Endpoint:** /login
- **File:** app.js
- **Root Cause:**
  User input is directly concatenated into SQL queries without parameterization.
- **Impact:**
  Authentication bypass and full account takeover.
- **Remediation:**
  Use parameterized queries to separate code from data.

---

## A07: Identification and Authentication Failures

### Authentication Bypass via Inconsistent Input Normalization
- **Affected Endpoints:** /register, /login
- **Root Cause:**
  Inconsistent trimming of usernames.
- **Impact:**
  Account takeover.
- **Remediation:**
  Apply consistent input normalization using `.trim()`.

---

## A03: Injection – Stored Cross-Site Scripting (XSS)

- **Endpoint:** /
- **Root Cause:**
  User input stored and rendered without output encoding.
- **Impact:**
  Session hijacking.
- **Remediation:**
  Output escaping + HttpOnly cookies.

---

## A01: Broken Access Control

- **Endpoint:** /users
- **Root Cause:**
  Authorization based on client-side cookie.
- **Impact:**
  Vertical privilege escalation.
- **Remediation:**
  Server-side role validation using sessions.

---

## A08: Software and Data Integrity Failures – Insecure File Upload

- **Endpoint:** /upload
- **Root Cause:**
  No file type or MIME validation.
- **Impact:**
  Potential Remote Code Execution.
- **Remediation:**
  File type whitelisting and size limits.

---

## A02: Cryptographic Failures

- **Endpoints:** /register, /login
- **Root Cause:**
  Usage of MD5 for password hashing.
- **Impact:**
  Credential compromise.
- **Remediation:**
  Replace MD5 with bcrypt.

---

## A06: Vulnerable and Outdated Components

- **Root Cause:**
  Use of outdated jQuery and AngularJS libraries.
- **Impact:**
  Client-side exploitation.
- **Remediation:**
  Update dependencies and run `npm audit`.
