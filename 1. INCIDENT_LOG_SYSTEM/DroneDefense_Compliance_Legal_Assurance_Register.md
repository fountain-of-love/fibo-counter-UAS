# 🇧🇪 Drone Defense – Compliance & Legal Assurance Register (v1.1)

## 🔹 Plain-Language Introduction
This register connects every operational and technical element of **DroneDefense Belgium** to the **legal and regulatory frameworks** that govern national airspace, cybersecurity, and data protection.  
It ensures full compliance with **EU law**, **Belgian national regulations**, and **international aviation and defense standards**.

---

## 1️⃣ Purpose & Scope
- Establish a clear mapping between DroneDefense components and governing legal frameworks.  
- Ensure continuous compliance with **GDPR**, **NIS2**, **ISO 27001**, **EASA**, and **Belgian Penal Code** requirements.  
- Provide a single source of truth for audits, inspections, and governance reporting.

Applies to all DroneDefense subsystems including the **C-UAS Incident Log System (CILS)**, dashboards, APIs, and archives.

---

## 2️⃣ Legal Summary (Plain-Language Overview)
| Legal Area | What It Means Practically | Example Control |
|-------------|----------------------------|-----------------|
| **GDPR (EU 2016/679)** | Citizens’ data must be protected and anonymized. | Incident logs remove identifying info before analytics. |
| **NIS2 Directive (EU 2022/2555)** | Critical systems must have cybersecurity governance. | CILS uses RBAC, MFA, and encrypted audit logs. |
| **ISO 27001:2022** | Continuous information security management. | Regular risk assessment and mitigation logs. |
| **Belgian Penal Code (Art. 189–196)** | Unauthorized interference with airspace = criminal offense. | Legal escalation process embedded in SOP. |
| **EASA UAS Regulation (EU 2019/947)** | Drones operating near sensitive sites must follow strict limits. | Integration with airspace geofencing data. |

---

## 3️⃣ Compliance Mapping Table
| Standard / Regulation | Clause Reference | System Control | Review Frequency | Owner |
|------------------------|------------------|----------------|------------------|--------|
| GDPR | Art. 5–6 | Privacy-by-design, data minimization | Quarterly | DPO |
| NIS2 | Art. 21–23 | Cyber resilience, supply chain security | Semi-annual | MoD Cyber QA |
| ISO 27001 | A.5–A.18 | Access control, monitoring, audits | Annual | QA Lead |
| EASA | Annex IX | Airspace conformity | Quarterly | DGTA Ops |
| BE Penal Code | Art. 189–196 | Law enforcement escalation | As needed | Police Liaison |

All compliance actions are logged in the immutable **Governance Repository** and verified with SHA-256 hashes.

---

## 4️⃣ Public Compliance Summary (Transparency Requirement)
Each year, a **Public Compliance Summary** is released by the National C-UAS Council.  
It includes anonymized statistics, audit highlights, and system improvements — written in accessible language for citizens.  
This fulfills the *Expressio* requirement of the Blueprint × FIBO model: communication and accountability.

---

## 5️⃣ Oversight & Audit Integration
| Oversight Layer | Verification Activity | Linked Document |
|------------------|-----------------------|-----------------|
| **Operational QA** | Technical audit and code review | [DroneDefense_Developer_Guide.md](DroneDefense_Developer_Guide.md) |
| **Validation Testing** | Continuous KPI-based QA | [DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md) |
| **Governance Review** | Quarterly compliance evaluation | [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md) |
| **Legal Harmonization** | National–EU alignment | Annual Legal Council review |

---

## 6️⃣ Continuous Improvement (Resilientia → Unio)
- Quarterly reviews ensure the register evolves with new regulations.  
- Legal counsel collaborates with MoD Cyber QA to monitor NIS2 and ISO updates.  
- Long-term goal: harmonize DroneDefense’s compliance framework with **EU and NATO C-UAS standards**.  
- Each compliance version archived for **10 years** to ensure historical accountability.

---

## 🔗 Related Documents
- [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md)  
- [DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md)  
- [DroneDefense_Developer_Guide.md](DroneDefense_Developer_Guide.md)  
- [DroneDefense_IncidentLog_TechnicalArchitecture.md](DroneDefense_IncidentLog_TechnicalArchitecture.md)

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.1 — November 2025