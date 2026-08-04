# End-to-End Security Assessment and Reporting Project

A full-lifecycle, hands-on security assessment completed as a cybersecurity internship
project. The engagement moves through reconnaissance, vulnerability scanning,
exploitation, password auditing, secure code review, and a final consolidated report —
the same workflow a junior penetration tester would follow for a real client engagement.

📄 **[Read the full report (PDF)](./End-to-End_Security_Assessment_and_Reporting_Project.pdf)**

## Lab Environment

| Role | System | Address |
|---|---|---|
| Attacker | Kali Linux | `192.168.122.128` |
| Primary target | Metasploitable2 (Ubuntu) | `192.168.122.135` |
| Web app target | DVWA (Docker) | `localhost:8000` |
| Web app target | OWASP Juice Shop (Docker) | `localhost:3000` |
| Recon-only target | testaspnet.vulnweb.com | public |

All activity was performed inside an isolated host-only virtual network. No production
or third-party systems were accessed outside the designated test targets.

## Report Structure

| # | Section | Summary |
|---|---|---|
| 1 | Research & Documentation | CIA Triad, threat categories, ethical hacking methodology, legal/ethical boundaries |
| 2 | Reconnaissance & Information Gathering | WHOIS, nslookup/dig, Shodan, Wappalyzer, Nmap, WhatWeb against the recon target |
| 3 | Vulnerability Scanning | Nessus Advanced Scan of Metasploitable2, CVSS-prioritized findings, Nmap NSE cross-verification |
| 4 | Exploitation & Penetration Testing | vsftpd 2.3.4 backdoor & WebDAV upload → RCE; SUID Nmap privilege escalation to root; credential harvesting |
| 5 | Password Cracking & Security Measures | John the Ripper / Hashcat against shadow, ZIP, and PDF hashes; password policy & MFA recommendations |
| 6 | Secure Coding & Mitigation | SQL Injection, Stored/DOM XSS, CSRF, and IDOR found, exploited, and patched in DVWA and OWASP Juice Shop; secure coding guide |
| 7 | Final Project Report & Demonstration | Consolidated findings, tools/techniques, and remediation across all six phases |

## Tools Used

`Nmap` · `WHOIS / nslookup / dig` · `Shodan` · `Wappalyzer` · `WhatWeb` · `Nessus` ·
`Metasploit Framework` · `msfvenom` · `netcat` · `John the Ripper` · `Hashcat` ·
`DVWA` · `OWASP Juice Shop` · `Kali Linux`

## Key Findings

- 5 critical-severity network/service vulnerabilities (CVSS 9.8–10.0), including the
  vsftpd 2.3.4 backdoor and a bind-shell UnrealIRCd backdoor
- Full unauthenticated remote code execution and root-level privilege escalation
  achieved on the primary target
- Weak/default credentials recovered from Linux shadow hashes, a protected ZIP, and a
  protected PDF via offline cracking
- Four web application vulnerability classes (SQLi, XSS, CSRF, IDOR) identified,
  exploited, and patched at the source-code level across two applications

## Files in This Folder

```
end-to-end-security-assessment/
├── End-to-End_Security_Assessment_and_Reporting_Project.pdf   ← read this
└── docx/
    └── End-to-End_Security_Assessment_and_Reporting_Project.docx
```

> **Note:** All testing was performed against intentionally vulnerable, self-hosted
> lab applications (Metasploitable2, DVWA, OWASP Juice Shop) and a public
> vulnerability-testing sandbox (vulnweb.com) intended for this purpose. No
> unauthorized systems were targeted.
