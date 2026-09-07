# Major Project : Vulnerability Assessment and Penetration Testing (VAPT) on Altoro Mutual

## Overview
- A security assessment and penetration test conducted against the Altoro Mutual web banking application (testfire.net). The project identifies critical application-level logic flaws, injection vectors, network exposure, and SSL/TLS configuration weaknesses using automated and manual security testing methodologies.

## Key Findings & Vulnerability Breakdown
***1. SQL Injection & Auth Bypass***
- Vector / Target : Login Functionality (/login.jsp)
- Impact : Critical — Bypassed authentication mechanisms to gain unauthorized access to privileged banking features.

***2. Stored Cross-Site Scripting (XSS)***
- Vector / Target : Feedback Form (/feedback.jsp)
- Impact : High — Persistent client-side script execution via intercepted and modified requests.

***3. Reflected XSS & HTML Injection***
- Vector / Target : Search Bar (/index.jsp, /search.jsp)
- Impact : High / Medium — Reflected malicious payloads and unencoded HTML rendering.

***4. CSRF Weakness***
- Vector / Target : Transfer Funds (/bank/main.jsp)
- Impact : Medium — Absence of unique anti-CSRF tokens in sensitive transaction requests.

***5. Network & Cipher Hardening***
- Vector / Target : Port 80, 443, 8080 (Apache Tomcat)
- Impact : Medium — Weak DH1024 parameters, CBC ciphers, and legacy TLS 1.0/1.1 enabled.

## Tech Stack & Environment
- OS Environment : Kali Linux
- Interception & Analysis : Burp Suite Community Edition (Proxy, Repeater, Inspector)
- Network & SSL Enumeration : Nmap (Service/Version detection, NSE Scripts)
- Automated Injection : SQLmap
