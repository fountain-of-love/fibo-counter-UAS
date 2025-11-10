# 🇧🇪 Drone Defense – Incident Log System Manifestation (Draft v1.0)

## 🔹 Plain-Language Introduction
This document describes **how Belgium’s national drone-incident log should work in practice** — as a secure, living system.  
It defines 13 core requirements (based on the FIBO stages) and compares five implementation options, including a custom-built solution.  
Goal: choose a platform that is **fast to deploy, legally compliant, auditable, and interoperable**.

---

## 1️⃣ Concept Overview
The **C-UAS Incident Log System (CILS)** is the **digital backbone** collecting and analyzing all drone incidents from airports, bases, ports, and events.  
It replaces scattered spreadsheets with a **secure, version-controlled, collaborative database**, feeding the National C-UAS Dashboard.

---

## 2️⃣ Thirteen System Requirements (Aligned to FIBO Stages)

| # | FIBO Stage | Requirement | Purpose |
|---|-------------|-------------|----------|
| 1 | Origo | Auto-generate unique incident ID | Ignition of record |
| 2 | Dualitas | Role differentiation (civil/military) | Keep authority boundaries clear |
| 3 | Trinitas | Workflow state: open → investigating → closed → reviewed | Lifecycle control |
| 4 | Adaptatio | Offline logging & later sync | Field resilience |
| 5 | Textura | Structured schema with validation | Data consistency |
| 6 | Sensorium | API connectors to sensors | Real-time automation |
| 7 | Conformatio | File attachments + SHA-256 hashing | Forensic integrity |
| 8 | Synchronia | Real-time sync to dashboard | Shared awareness |
| 9 | Expressio | Notification engine | Automatic alert routing |
| 10 | Circulatio | Inter-agency data sharing API | Analytics exchange |
| 11 | Restitutio | Immutable audit trail | Legal defensibility |
| 12 | Resilientia | Training/sandbox mode | Continuous learning |
| 13 | Unio | Analytics feedback dashboard | National insight engine |

---

## 3️⃣ Technical & Security Baseline
- **Hosting:** Private GitHub Enterprise or EU sovereign cloud.  
- **Stack:** Python (FastAPI + PostgreSQL + React UI).  
- **Encryption:** AES-256 (rest), TLS 1.3 (transit).  
- **Auth:** OIDC (Okta / Azure AD) + MFA.  
- **Audit:** Append-only block log.  
- **Compliance:** GDPR + ISO 27001.

---

## 4️⃣ Evaluation Matrix (Summary)

| Option | Description | Strengths | Weaknesses | FIBO Coverage | Setup Time | 2-Yr Cost |
|---------|--------------|------------|-------------|----------------|-------------|-----------|
| A – GitHub Private Repo | Incident = Issue; version control | Fast pilot, immutable | No sensor API, US hosting | 65% | 1 wk | €0 |
| B – Airtable / SmartSheet | Cloud table + forms | Easy setup | Weak audit, limited auth | 55% | 2 wks | €5k/yr |
| C – Power Apps / Dataverse | Form app in O365 | Strong auth, Teams integration | Limited API flexibility | 80% | 4–6 wks | €20k |
| D – TheHive + MISP | Cyber incident platform | Proven security, API-rich | Needs UI tuning | 85% | 6–8 wks | €50k |
| E – Custom C-UAS Platform | Python/PostgreSQL custom | Full fit, sovereign, scalable | Higher initial cost | 100% | 3–4 mo | €120–180k |

---

## 5️⃣ Evaluation Summary
- **Speed:** GitHub → ideal pilot.  
- **Security:** TheHive / Custom build → EU compliance.  
- **Integration:** Custom build → full sensor/data alignment.  
- **Accessibility:** Power Apps → short-term O365 solution.  
- **Scalability:** Custom build → long-term.

**Recommended Path:**  
Start with **GitHub pilot (60 days)** → collect feedback → transition to **Custom C-UAS Platform** for rollout.

---

## 6️⃣ Pilot Manifestation (GitHub Prototype)
| Component | Implementation | Notes |
|------------|----------------|------|
| Repo Structure | `/incidents/YYYY/BE-SITE-ID-####/` | One folder = one incident |
| Metadata File | `incident.yml` | Fields match template |
| Automation | GitHub Actions → validate + hash | Push to dashboard API |
| Access | Teams: Operators, Police, DGTA, Cell | Granular permissions |
| Audit | Commits = immutable record | Meets Restitutio |
| Dashboard Bridge | Webhook → API POST | Near-real-time sync |

---

## 7️⃣ Transition Plan (to Custom Platform)
| Phase | Goal | Duration | Deliverables |
|--------|------|-----------|---------------|
| 1 | Pilot feedback | 2 mo | GitHub export dataset |
| 2 | MVP development | 3 mo | CUIP v1.0 beta |
| 3 | Integration & test | 1 mo | Live 3–5 pilot sites |
| 4 | National rollout | 4 mo | CUIP production v1.0 |

---

## 8️⃣ Expected Benefits
- Fast deployment and iteration.  
- Full GDPR and audit compliance.  
- Integrated into national dashboard.  
- Supports long-term sovereign data control.

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.0 — November 2025  
**SHA-256:** 3bc66f0b214ddccdfab4bb3ac2586f47a2b007d8c2c3efc6208b5a43d65d7436