# 🛡️ Final Project — Live Incident Response

**4Geeks Academy · Cybersecurity · June 2026**
Student: Raúl Velásquez

## 📋 Overview

Live incident response analysis performed on a compromised Linux server. The goal was to identify, contain, and eradicate an active intrusion without interrupting the service.

---

## 🧭 Methodology

- **Approach:** Live Incident Response (LIR)
- **Framework:** PICERL (Preparation, Identification, Containment, Eradication, Recovery, Lessons Learned)
- **MITRE ATT&CK Mapping:** T1566, T1059.004, T1136.001, T1053.003, T1048.003

---

## 🔍 Phase 1 — Reconnaissance & Identification

- ✅ System state analysis (uptime, RAM, kernel, network)
- ✅ Detection of unauthorized users (`reports`, `hacker`)
- ✅ Authentication log analysis (`auth.log`)
- ✅ Identification of suspicious open ports (FTP port 21)
- ✅ Evidence of social engineering (email phishing)
- ✅ Discovery of a malicious cronjob (`backup2.sh`) exfiltrating credentials every 15 minutes

## 🧯 Phase 2 — Containment, Eradication & Recovery

- ✅ Removal of backdoor user accounts
- ✅ Removal of the malicious script and scheduled task
- ✅ Firewall reconfiguration (UFW)
- ✅ Rotation of compromised credentials
- ✅ System integrity verification

---

## 🎯 Key Findings

| # | Finding |
|---|---|
| 1 | 2 unauthorized users created via social engineering and direct access |
| 2 | Credential exfiltration via HTTP POST every 15 minutes for ~1 year |
| 3 | Unauthorized active FTP service (port 21) |
| 4 | Persistence via malicious cronjob (`/etc/cron.d/sys-maintenance`) |

---

## 📁 Repository Structure

| File | Description |
|---|---|
| `Informe_Tecnico_Incident_Response_4Geeks_FINAL.docx` | 📄 Full technical report (72 pages) with evidence, analysis, and recommendations |
| `Fase1_Hallazgos_RaulVelasquez.pptx` | 🖥️ Phase 1 presentation — Reconnaissance & Findings |
| `Guion_Presentacion_Fase1_RaulVelasquez.docx` | 📝 Presentation script with explained commands |
| `PASO*.png` | 📸 Screenshots of evidence from the compromised server |
| `FASE 2/` | 🧯 Phase 2 documentation — Remediation & Restoration |

---

## 👤 Author

**Raúl Velásquez**

---
Academic project — 4Geeks Academy · 2026
