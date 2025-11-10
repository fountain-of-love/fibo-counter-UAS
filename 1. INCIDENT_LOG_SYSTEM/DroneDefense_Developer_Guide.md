# 🇧🇪 Drone Defense – Developer Guide (v1.1)

## 🔹 Plain-Language Introduction
This guide provides a **clear and secure workflow** for developers contributing to the **Counter-UAS Incident Log System (CILS)**.  
It defines how to build, test, and deploy components within Belgium’s national DroneDefense framework — ensuring consistency, compliance, and traceability.

---

## 1️⃣ Quick Start Overview
A visual overview of the full development lifecycle:
```
Local Dev  →  Code Review  →  CI/CD Validation  →  Governance Approval  →  Deployment
```

### 🧩 Step-by-Step Setup
1. **Clone Repository:**  `git clone https://github.com/drone-defense-belgium/cils`
2. **Install Dependencies:**  `pip install -r requirements.txt`
3. **Run Tests:**  `pytest --cov`
4. **Commit Changes:**  Signed commits required: `git commit -S -m "..."`
5. **Push for Review:**  CI/CD auto-runs tests & security scan.
6. **Deploy:**  Upon approval, CI/CD merges to `main` → triggers container build + deployment.

---

## 2️⃣ Branching & Versioning Standards
| Branch | Purpose | Access | Notes |
|---------|----------|---------|-------|
| `main` | Production release | Restricted | CI/CD auto-deploys |
| `develop` | Integration & testing | Full dev team | Feature merge area |
| `feature/*` | Active dev branches | Assigned developers | Scoped per feature or fix |
| `hotfix/*` | Emergency patches | Maintainers only | Post-incident fixes |

**Semantic Versioning:** `vMAJOR.MINOR.PATCH`  
Every release must include an updated changelog and SHA verification in the Governance Repository.

---

## 3️⃣ CI/CD & Validation Integration
All builds are validated automatically through GitHub Actions, performing:
- Linting, unit tests, and coverage analysis  
- Dependency vulnerability scan  
- Docker build integrity check  

**Quality Assurance Traceability:**  
Testing and validation procedures are documented and tracked through the  
[DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md)  
for full DQM and compliance traceability.

---

## 4️⃣ Security & Compliance Requirements
| Area | Requirement | Verification |
|------|--------------|---------------|
| **Access Control** | MFA + OIDC (Okta/AzureAD) | System audit logs |
| **Code Signing** | GPG-signed commits | GitHub verification |
| **Data Governance** | Use encrypted secrets only | Compliance log |
| **Incident Response** | Immediate flag → CI lockdown | Governance Council approval |
| **Legal Assurance** | GDPR + ISO 27001 alignment | [DroneDefense_Compliance_Legal_Assurance_Register.md](DroneDefense_Compliance_Legal_Assurance_Register.md) |

---

## 5️⃣ Governance & Oversight Linkage
All code changes, release cycles, and deployments are logged into the **C-UAS Governance Repository**.  
This process is reviewed quarterly under the  
[DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md)  
for audit traceability and ethical assurance.

---

## 6️⃣ Developer Responsibilities
- Follow code of conduct and commit-signing policy.  
- Maintain data confidentiality and report potential breaches immediately.  
- Document every significant change (README, changelog).  
- Participate in quarterly DQM review and technical retrospectives.

---

## 🔗 Related Documents
- [DroneDefense_IncidentLog_TechnicalArchitecture.md](DroneDefense_IncidentLog_TechnicalArchitecture.md)  
- [DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md)  
- [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md)  
- [DroneDefense_Compliance_Legal_Assurance_Register.md](DroneDefense_Compliance_Legal_Assurance_Register.md)

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.1 — November 2025
