# 🇧🇪 Drone Defense – Communication Tree Protocol (Revised v1.1)

## 🔹 Plain-Language Introduction
This chart shows **who calls whom** when a drone is detected.  
It ensures information moves **fast, clear, and lawfully** — without confusion or overlap.  
Everyone from the operator to national command follows the same path.

---

## 1️⃣ Purpose
Define a **standardized communication chain** for all Belgian C-UAS operations, ensuring quick escalation, accurate information, and legal accountability.

---

## 2️⃣ Communication Principles
1. **One Voice Per Level:** Only designated liaison may speak for that level.  
2. **Speed First:** Flow starts within 30 seconds of confirmation.  
3. **Redundancy:** If primary channel fails > 2 min, use fallback (secondary line or dashboard chat).  
4. **Traceability:** All alerts auto-logged to C-UAS Dashboard (<60 s sync).  
5. **Security:** No open radio; encrypted systems only (AES-256).

---

## 3️⃣ Role Categories & Call Signs

| Level | Role | Call Sign Prefix | Channel Type |
|--------|------|-----------------|---------------|
| L0 | Operator / Sensor Technician | OP-# | Internal / Dashboard |
| L1 | Site Supervisor / Comms Officer | SUP-# | Radio / Phone Secure |
| L2 | Police Liaison | POL-# | Secure Mobile / Radio |
| L3 | DGTA Watch Officer | DG-# | Secure Call / Dashboard |
| L4 | C-UAS Cell Duty Officer | CELL-# | Dashboard + Video Bridge |
| L5 | Public Comms Officer | COM-# | Press / Gov.be Channels |

Minimum staffing: **1 Comms Officer per active shift**.

---

## 4️⃣ Communication Flow (Expressio Layer)

| Step | From | To | Message Type | Target Time | Fallback |
|------|------|----|--------------|--------------|-----------|
| 1 | Operator (OP-#) | Supervisor (SUP-#) | Alert: “Drone detected” | ≤30 sec | Intercom |
| 2 | Supervisor | Police Liaison (POL-#) | Verification request | ≤1 min | Radio |
| 3 | Police Liaison | DGTA Watch (DG-#) | Airspace notification | ≤2 min | Secure SMS |
| 4 | DGTA Watch | C-UAS Cell (CELL-#) | Incident log update | ≤3 min | Dashboard sync |
| 5 | C-UAS Cell | All Agencies | Situation summary | ≤5 min | Email failover |
| 6 | C-UAS Cell | Public Comms (COM-#) | Press if approved (Level 3) | ≤30 min | Gov.be release |

---

## 5️⃣ Standard Message Templates

**Alert Message**  
> “Unidentified drone detected at [SITE] – [Time]. Altitude [xx m]. Moving [N/S/E/W]. Confidence [%]. Action requested.”

**Status Update**  
> “Level [x] confirmed. Police on site. Awaiting DGTA confirmation.”

**All-Clear**  
> “Drone neutralized / departed. Ops resumed at [Time]. Incident ID #xxxx.”

All messages auto-timestamped and archived.

---

## 6️⃣ Dashboard Integration (Unio Layer)
Every message is mirrored to the **national C-UAS dashboard**, creating a single live log.  
The dashboard feeds national analytics and annual performance reviews.

---

## 7️⃣ Post-Incident Review (Resilientia Layer)
- C-UAS Cell audits message latency and accuracy monthly.  
- Sites receive a **“Comms Performance Score.”**  
- Recurrent issues trigger retraining within 30 days.

---

## 8️⃣ How This Prevents Panic and Confusion
Clear communication prevents panic before it spreads.  
When citizens see coordinated authority response, they trust and comply faster — keeping everyone safe.

---

**Prepared by:** Yves Langeraert with Enigma  
**Version:** v1.1 — November 2025  
**SHA-256:** 4d41a81f7edc799b4d3f64f3cf0a2e1347e8e10d72dc90d40df7a4f00a76db65