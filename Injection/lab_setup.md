# Injection — Lab Setup

## Objective
Practice and document **SQL Injection (SQLi)** scenarios in a controlled lab environment.  
Reproduce the issue, show PoC input, capture evidence, and propose secure fixes.

## Environment (recommended)
- Local: Docker + simple web app (e.g., OWASP Juice Shop or a minimal Flask app with a vulnerable query)
- Tools: Browser, Burp Suite / OWASP ZAP, sqlite/mysql client

## Lab Topology
- App: `vulnerable-app:5000` (HTTP)
- DB: sqlite (local) or MySQL container
- Network: localhost

## Steps to reproduce (high level)
1. Start the vulnerable app (Docker or local).  
2. Identify input fields that interact with the DB (search, login, comment forms).  
3. Intercept request with Burp/ZAP and try authentication/parameter manipulation.  
4. Confirm data exfiltration or behavior change caused by injection.

## Files in this folder
- `lab_setup.md` — this file  
- `exploit_example.md` — PoC and request/response evidence  
- `mitigation.md` — fixes and secure coding patterns
