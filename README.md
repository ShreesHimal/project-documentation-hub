# Cybersecurity Internship Portfolio

Hands-on security assessment and digital forensics work completed during a
cybersecurity internship. Each project folder contains a full written report (PDF +
source `.docx`) plus its own README summarizing scope, tools, and key findings.

## Projects

| Project | Description | Report |
|---|---|---|
| 🔐 [**End-to-End Security Assessment**](./end-to-end-security-assessment/) | Full offensive security lifecycle — recon, scanning, exploitation, password auditing, and secure coding review/remediation — against a self-hosted vulnerable lab (Metasploitable2, DVWA, OWASP Juice Shop) | [PDF](./end-to-end-security-assessment/End-to-End_Security_Assessment_and_Reporting_Project.pdf) |
| 🧩 [**DFIR Investigation**](./dfir-investigation/) | Simulated two-host breach investigation (Ubuntu + Windows) with a full incident timeline, MITRE ATT&CK mapping, and IOC register | [PDF](./dfir-investigation/) |

## Repository Structure

```
.
├── README.md                              ← you are here
├── end-to-end-security-assessment/
│   ├── README.md
│   ├── End-to-End_Security_Assessment_and_Reporting_Project.pdf
│   └── docx/
│       └── End-to-End_Security_Assessment_and_Reporting_Project.docx
└── dfir-investigation/
    ├── README.md
    ├── DFIR_Investigation_Report.pdf      ← to be added
    └── docx/
        └── DFIR_Investigation_Report.docx ← to be added
```

## Lab Disclosure

All offensive testing in this portfolio was performed against intentionally vulnerable,
self-hosted, or purpose-built training targets in an isolated lab network
(Metasploitable2, DVWA, OWASP Juice Shop, and vulnweb.com — a public sandbox
maintained specifically for security testing practice). No unauthorized or
production systems were accessed at any point.

## About

Compiled as part of a cybersecurity internship program to demonstrate practical,
end-to-end competency across the penetration testing lifecycle and incident response
investigation and reporting.
