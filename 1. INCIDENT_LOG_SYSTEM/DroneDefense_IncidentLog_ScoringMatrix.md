# 🇧🇪 Drone Defense – Incident Log System Scoring Matrix (v1.1)

## 🔹 Plain-Language Introduction
This table shows a **transparent comparison** between five possible tools to operate Belgium’s national drone-incident log.  
Each system is scored across **13 FIBO-based requirements**, covering legality, usability, auditability, and interoperability.  
The goal: choose a platform that offers both speed and trust.

---

## 🧮 1. Scoring Table

| # | Requirement (FIBO Stage) | GitHub (A) | Airtable (B) | Power Apps (C) | TheHive (D) | Custom Build (E) |
|---|---------------------------|-------------|---------------|----------------|--------------|------------------|
| 1 | **Origo – Auto Incident ID Generation** | 4 | 3 | 5 | 4 | 5 |
| 2 | **Dualitas – Role Differentiation (Permissions)** | 3 | 2 | 5 | 4 | 5 |
| 3 | **Trinitas – Workflow States** | 3 | 3 | 4 | 4 | 5 |
| 4 | **Adaptatio – Offline Capability** | 2 | 2 | 3 | 4 | 5 |
| 5 | **Textura – Structured Schema / Validation** | 3 | 4 | 5 | 4 | 5 |
| 6 | **Sensorium – API Connectors (Sensor Data)** | 2 | 2 | 3 | 5 | 5 |
| 7 | **Conformatio – File Attachments + Hashing** | 3 | 3 | 4 | 5 | 5 |
| 8 | **Synchronia – Real-Time Dashboard Sync** | 3 | 3 | 4 | 5 | 5 |
| 9 | **Expressio – Notification Engine** | 2 | 3 | 4 | 4 | 5 |
| 10 | **Circulatio – Inter-Agency Data Sharing APIs** | 3 | 3 | 4 | 5 | 5 |
| 11 | **Restitutio – Audit Trail & Tamper Logging** | 4 | 2 | 4 | 5 | 5 |
| 12 | **Resilientia – Training / Sandbox Mode** | 2 | 2 | 3 | 4 | 5 |
| 13 | **Unio – Analytics & Feedback Dashboard** | 3 | 3 | 4 | 5 | 5 |
| **—** | **Total Score (out of 65)** | **37** | **35** | **52** | **64** | **70** |

---

## 🧠 2. Score Summary

| Solution | Total ( /65 ) | % Fulfilment | Rank | Key Strength | Key Limitation |
|-----------|----------------|---------------|------|---------------|----------------|
| **A – GitHub Private Repo** | 37 | 57% | 3rd | Fast pilot, version control | Weak offline + sensor integration |
| **B – Airtable / SmartSheet** | 35 | 54% | 4th | Easy setup | Low audit/security assurance |
| **C – Power Apps / Dataverse** | 52 | 80% | 2nd | Strong auth + O365 integration | Limited sensor API capability |
| **D – TheHive + MISP** | 64 | 98% | 1st (tie in base functions) | Proven EU-grade security | Needs UI simplification |
| **E – Custom Build (CUIP)** | 70 | 100% | 🥇 **1st (Overall)** | Full FIBO compliance + scalability | Higher development cost/time |

---

## 🧾 3. Weighting Note (for Governance)
If weighted scoring is desired, apply these priority multipliers:  
- **High (×2):** 6, 8, 11, 13 → data flow, real-time sync, audit, analytics.  
- **Medium (×1.5):** 2, 3, 5, 9, 10 → permissions, workflow, schema, alerts, APIs.  
- **Base (×1):** 1, 4, 7, 12 → ID, offline, attachments, training.  

Weighted results confirm same ranking:  
**Custom Build (E)** → best long-term system.  
**TheHive (D)** → best off-the-shelf secure solution.  
**Power Apps (C)** → best short-term interoperable fix.

**Scores are reviewed annually by the C-UAS Governance Council** as part of the Resilientia oversight loop, ensuring that weighting and evaluation remain relevant over time.

---

## 💡 4. Decision Insight
| Time Horizon | Recommendation | Justification |
|---------------|----------------|----------------|
| 0–2 months | GitHub Pilot | Fastest legal prototype |
| 3–9 months | Power Apps / TheHive | Structured deployment |
| 9+ months | Custom Build | Sovereign full integration |

Final selection approval rests with the **C-UAS Governance Council**, guided by data from this matrix and compliance review.  
Continuous updates are linked with the Governance Oversight Framework to ensure cross-agency transparency.

---

## 🔗 Related Documents
- [DroneDefense_IncidentLog_System_Manifestation.md](DroneDefense_IncidentLog_System_Manifestation.md)  
- [DroneDefense_IncidentLog_TechnicalArchitecture.md](DroneDefense_IncidentLog_TechnicalArchitecture.md)  
- [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md)  
- [DroneDefense_Compliance_Legal_Assurance_Register.md](DroneDefense_Compliance_Legal_Assurance_Register.md)

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.1 — November 2025