<div align="center">

# Edgar Valenzuela

### Security Engineer in Progress

Started in the SOC watching attacks happen. Now I'm on the other side, breaking and fixing the applications that generate those alerts.

📍 Currently building full-lifecycle AppSec assessments — **threat model → exploit → detect → fix**

</div>

---

## Application Security

| Project | What it demonstrates | Key Result |
|---|---|---|
| **[TaskVault](https://github.com/edgarjvalen/websec-assessment-taskvault)** — FastAPI + PostgreSQL app, deliberately vulnerable then remediated | Threat modeling, secure code review, SQLi/XSS/IDOR/auth flaws, SAST (Semgrep), DAST (OWASP ZAP), dependency & secrets scanning (Trivy, Gitleaks), remediation with regression tests | Found and fixed 15 vulnerabilities, zero regressions |
| **[API Security Lab](https://github.com/edgarjvalen/api-security-lab)** — Intentionally vulnerable REST API, manually assessed | OWASP API Security Top 10, BOLA, BFLA, mass assignment → privilege escalation, JWT security, Burp Suite manual testing, automated-vs-manual DAST comparison | Manually caught 6 critical flaws that automated scanning missed entirely |
| **[TaskVault CI/CD Pipeline](https://github.com/edgarjvalen/taskvault-cicd-pipeline)** — Same vulnerable app, wrapped in an enforced security pipeline | GitHub Actions, shift-left security, SAST/SCA/secrets/DAST wired into CI, SARIF → GitHub Security tab, branch protection blocking insecure merges | Built a pipeline that blocks insecure code before it merges |

<details>
<summary><b>More on each project</b></summary>
<br>

**TaskVault** — Full-lifecycle assessment of a ticketing app: built a secure baseline, threat-modeled it with STRIDE, deliberately planted 8 vulnerabilities on a separate branch, ran the full tooling stack, triaged 15 findings, remediated everything with regression tests, and shipped a PDF security report.

**API Security Lab** — A tightly scoped notes API with six real, manually exploited vulnerabilities, chained mass assignment into full privilege escalation. The standout result: automated DAST (ZAP) caught **zero** of the six confirmed vulnerabilities on either the vulnerable or remediated branch, everything it found required manual, logic-driven testing built around an authorization matrix.

**TaskVault CI/CD Pipeline** — Took the same vulnerable codebase and inverted the workflow: built the GitHub Actions security pipeline *first*, let it fail red against vulnerable code, then fixed findings in commits while watching jobs flip to green. Five parallel jobs (pytest, Semgrep, Trivy, Gitleaks, authenticated ZAP DAST spun up live inside the CI runner) now gate every merge to `main` via branch protection.

</details>

---

## Background

Before AppSec, I worked the defensive side: SOC monitoring, incident response, forensics. That's the lens I bring to finding vulnerabilities, I've triaged what these bugs look like from the analyst's side of the alert.

**Security Operations & IR**
- [Azure Honeynet & SOC: Cyber Attacks in Real Time](https://github.com/edgarjvalen/azure-soc-honeynet/blob/main/README.md)
- [Incident Response Documentation on Findings](https://github.com/edgarjvalen/azure-incident-response/blob/main/README.md)
- [ForensiFox — Firefox Digital Forensics Tool](https://github.com/edgarjvalen/ForensiFox)
- [Investigate Scheduled Tasks in a CrowdStrike Falcon RTR Session](https://github.com/edgarjvalen/Investigate-Scheduled-Tasks-in-Falcon-RTR-Session/tree/main)

**Tooling & Automation (Python)**
- [VirusTotal API Analysis Tool](https://github.com/edgarjvalen/sec_analysis_tool/blob/main/README.md)
- [Scalable IP Address Management for SOC Ops](https://github.com/edgarjvalen/ipinfo/blob/main/README.md)

**Cloud & Infrastructure**
- [AWS Multi-Tier Infrastructure with Terraform](https://github.com/edgarjvalen/AWS-Multi-Tier-Infrastructure/tree/main)
- [AWS Static Website with CloudFront CDN](https://github.com/edgarjvalen/S3-StaticWebsite-CloudFront)
- [Active Directory + User Creation via PowerShell](https://github.com/edgarjvalen/install-active-directory-create-users)
- [MFA & RDP Hardening with Duo (Server 2019)](https://github.com/edgarjvalen/rdp-mfa-duo-azure/blob/main/README.md)

---

## Tools & Tech

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Burp Suite](https://img.shields.io/badge/-Burp%20Suite-FF6633?style=flat-square&logo=burpsuite&logoColor=white)
![OWASP ZAP](https://img.shields.io/badge/-OWASP%20ZAP-000000?style=flat-square&logo=owasp&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/-AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Terraform](https://img.shields.io/badge/-Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)

---

## Certifications

`AWS Certified Solutions Architect - Associate` · `Certified Web Red Team Analyst (Web-RTA)` · `CompTIA Pentest+` · `CompTIA CySA+` · `CompTIA Security+` · `CompTIA Network+` · `CompTIA A+` · `Azure AZ-900` · `ISC2 SSCP` · `TryHackMe SOC Analyst I` · `LPI Linux Essentials` · `ITIL 4 Foundation`
