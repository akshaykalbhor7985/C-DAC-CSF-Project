# Major Project : Vulnerability Assessment and Penetration Testing (VAPT) on Altoro Mutual

## Overview
A security assessment and penetration test conducted against the Altoro Mutual web banking application (testfire.net). The project identifies critical application-level logic flaws, injection vectors, network exposure, and SSL/TLS configuration weaknesses using automated and manual security testing methodologies.

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

# Minor Project : Digital Forensic Investigation and Evidence Recovery (Minor Project)

## Overview
A forensically sound, end-to-end digital investigation executed on a suspect 16 GB FAT32 USB flash drive using C-DAC's CyberCheck 6.0 Forensic Suite (incorporating TrueBackWin 2.1). The project covers every stage of the forensic lifecycle, maintaining strict chain of custody and legal compliance under ISO/IEC 27037 and the Indian IT Act.

## Key Features & Methodology
***1. Evidence Acquisition & Hashing (TrueBackWin 2.1)***
- Acquired raw bit-stream physical disk images (.P01) while simultaneously performing multi-threaded MD5 and block-level cryptographic hashing.

***2. Evidence Carving & Deleted File Recovery***
- Reconstructed deleted partitions and carved overwritten documents (PPTX, DOCX, HTML, PDF) from unallocated drive space.

***3. Steganography & Anomaly Detection***
- Executed automated scans to identify hidden steganographic payloads and flagged file extension spoofing via header-extension signature analysis.

***4. Artifact & Multimedia Analysis***
- Conducted keyword/GREP searches across unallocated clusters and parsed recovered visual artifacts (JPEG) and video lectures (MP4) using integrated preview tools.

## Tech Stack & Standards
- Tools : C-DAC CyberCheck 6.0 (TrueBackWin 2.1 & CyberCheck Probe)
- Standards & Frameworks : ISO/IEC 27037, Write-Blocking, Cryptographic Checksums (MD5)
