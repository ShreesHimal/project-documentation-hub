# Digital Forensics & Incident Response (DFIR) Investigation

**Case Reference:** DFIR-2026-0630-UBW

A simulated two-host breach investigation covering an Ubuntu web server and a Windows
workstation. The report reconstructs the incident end-to-end: initial access, a master
timeline of attacker activity, MITRE ATT&CK technique mapping, an indicators-of-compromise
(IOC) table, and an evidence hash register suitable for chain-of-custody documentation.

📄 **Report:** `DFIR_Investigation_Report.pdf` *(add your file to this folder — see note below)*

## Scope

| Host | Role |
|---|---|
| Ubuntu web server | Initial point of compromise |
| Windows workstation | Lateral movement / secondary target |

## Report Contents

- Executive summary and incident scope
- Master timeline of attacker activity across both hosts
- MITRE ATT&CK technique mapping
- Indicators of Compromise (IOC) table
- Evidence hash register (chain-of-custody style documentation)
- Embedded figures and screenshots supporting each finding
- Timed video walkthrough script for the recorded demonstration

## Tools & Techniques

Standard DFIR triage and log/artifact analysis techniques were used to reconstruct the
timeline across both the Linux and Windows hosts, correlating file system, log, and
network artifacts into a single incident narrative.

## Files in This Folder

```
dfir-investigation/
├── DFIR_Investigation_Report.pdf     ← add this file
└── docx/
    └── DFIR_Investigation_Report.docx
```

---

> ⚠️ **Action needed:** This report wasn't part of the current session, so the file
> itself isn't included yet. Drop your `DFIR_Investigation_Report.docx` (and/or a PDF
> export of it) into this folder — and, ideally, `docx/` for the source file — following
> the same layout as the `end-to-end-security-assessment/` folder. If you'd like, upload
> it here and I'll convert it to PDF and refine this README with the exact details from
> the report.
