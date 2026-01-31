# Vulnerable Web Lab

This lab is provided as a pre-built Docker image.

## Requirements
- Docker

## Run the Lab
```bash
docker run -d -p 3000:3000 fayaldabbas/vulnerable-lab:latest

⚠️ Security Notice – XSS Limitation
Warning:
Although the application contains input points that could theoretically be
vulnerable to Cross-Site Scripting (XSS), the attack does not execute in practice.

This behavior is intentional, as the Docker image enforces security restrictions
that prevent the execution of malicious JavaScript within the containerized
environment.

The XSS scenario is included for educational and analytical purposes only,
without allowing real exploitation.
