# 🇧🇪 Drone Defense – Incident Log System Technical Architecture (v1.1)

## 🔹 Plain-Language Introduction
This document defines the **technical foundation** for Belgium’s national **Counter-UAS Incident Log System (CILS)**.  
It shows how the system is designed to be secure, scalable, interoperable, and compliant with European and Belgian law.  
Each layer reflects the **Blueprint × FIBO synthesis**, ensuring the system evolves organically from detection to governance.

---

## 1️⃣ System Overview
CILS is the **digital nervous system** connecting detection points (radar, RF, optical sensors) with the national oversight dashboard.  
It provides real-time logging, synchronization, and analytics across authorized agencies.

| Layer | Function | Technology Stack | Security / Notes |
|--------|-----------|------------------|------------------|
| **Frontend (Expressio)** | Operator dashboard | React + Tailwind | Multi-language, role-based views |
| **Backend API (Adaptatio)** | Business logic + orchestration | FastAPI (Python) | RBAC + API token validation |
| **Database (Textura)** | Structured schema & logs | PostgreSQL + pgcrypto | AES-256 encryption, immutable audit table |
| **File Storage (Conformatio)** | Evidence & attachments | MinIO (S3-compatible) | SHA-256 hashing, checksum validation |
| **Notification Engine (Expressio)** | Alerts & reports | Webhooks + MQTT | Push to command networks |
| **Analytics Layer (Unio)** | Trends, dashboards | Grafana + Pandas | KPI generation, DQM indicators |

---

## 2️⃣ Architecture Diagram (Conceptual)
```
┌─────────────────────────────────────────────────────────────┐
│                      National C-UAS Dashboard                │
│       (Governance Oversight, KPI, DQM Analytics)             │
└─────────────────────────────────────────────────────────────┘
                   ▲                    ▲
                   │                    │
        ┌──────────┘                    └──────────┐
        │                                           │
┌──────────────┐                        ┌─────────────────────┐
│  API Gateway │◄────── Data Feeds ─────┤  Detection Systems  │
│ (FastAPI)    │                        │ (Radar, RF, Optical)│
└──────────────┘                        └─────────────────────┘
        │
        ▼
┌────────────────────────────┐
│   PostgreSQL + MinIO Stack │
│ (Secure Data & Evidence)   │
└────────────────────────────┘
```
---

## 3️⃣ Implementation & Security Measures
- **Hosting:** EU sovereign cloud (Brussels region) with on-prem failover.  
- **Encryption:** AES-256 (at rest), TLS 1.3 (in transit).  
- **Authentication:** OIDC with MFA (Okta / Azure AD).  
- **Audit Logging:** Append-only blockchain table with timestamped hashes.  
- **Backups:** Geo-redundant, 24h RPO / 15min RTO.

**QA and Validation:**  
All components are tested through the [DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md), with traceability stored in the Quality Assurance Log.  
This ensures architecture, data flow, and DQM compliance remain verified across releases.

---

## 4️⃣ Integration & Interoperability
| Partner | Integration Type | Purpose |
|----------|------------------|----------|
| **DGTA** | REST API | Incident data submission |
| **MoD Cyber Unit** | Secure socket / SIEM link | Threat intelligence & monitoring |
| **Federal Police** | API + Web Dashboard | Real-time situational awareness |
| **Skeyes (ATC)** | Data-sharing API | Airspace correlation |

**Governance Alignment:**  
All integrations are reviewed and approved by the [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md) team before activation to ensure data sovereignty and policy coherence.

---

## 5️⃣ DQM & Governance Traceability
| Dimension | Oversight Integration | Mechanism |
|------------|-----------------------|------------|
| **Data** | Accuracy & provenance | Schema validation + UUID tracking |
| **Quality** | Reliability & uptime | SLA dashboard linked to governance QA reports |
| **Meaning** | Transparency & explainability | KPI reporting + public dashboard summaries |

Architecture-level DQM results are compiled monthly and transmitted to the National C-UAS Council via the Governance Oversight Framework.

---

## 6️⃣ Cost & Resource Traceability
Architecture costs and scalability parameters correspond directly to the system comparison in the [DroneDefense_IncidentLog_ScoringMatrix.md](DroneDefense_IncidentLog_ScoringMatrix.md).  
This provides a transparent link between design decisions, performance, and financial feasibility.

---

## 7️⃣ Evolution & Maintenance
- **Version Control:** GitHub Enterprise repository with CI/CD (GitHub Actions).  
- **Deployment:** Docker + Kubernetes for modular scaling.  
- **Resilience:** Offline caching + checksum sync (aligned with Manifestation document).  
- **Audits:** Conducted quarterly under the Governance Oversight Framework.  
- **Change Management:** Each release logged with SHA-256 commit chain.

---

## 🔗 Related Documents
- [DroneDefense_IncidentLog_System_Manifestation.md](DroneDefense_IncidentLog_System_Manifestation.md)  
- [DroneDefense_Developer_Guide.md](DroneDefense_Developer_Guide.md)  
- [DroneDefense_Test_Validation_Protocol.md](DroneDefense_Test_Validation_Protocol.md)  
- [DroneDefense_Governance_Oversight_Framework.md](DroneDefense_Governance_Oversight_Framework.md)  
- [DroneDefense_IncidentLog_ScoringMatrix.md](DroneDefense_IncidentLog_ScoringMatrix.md)

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.1 — November 2025