# Static Code Analysis – GREP Findings

This document demonstrates the use of GREP during static code analysis
to identify insecure coding patterns related to OWASP Top 10 vulnerabilities.

GREP was used as a supporting tool for manual code review.
---

## SQL Injection – GREP Evidence

**Command Used:**
grep -R "SELECT .* FROM" .

**Purpose:**
Identify SQL queries built using string concatenation.

**Result:**
User input was found directly embedded in SQL queries.

**OWASP Category:**
A03: Injection
