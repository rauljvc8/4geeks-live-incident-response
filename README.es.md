# 🛡️ Proyecto Final — Live Incident Response

**4Geeks Academy · Ciberseguridad · Junio 2026**
Alumno: Raúl Velásquez

## 📋 Descripción

Análisis de respuesta a incidentes en tiempo real (Live Incident Response) sobre un servidor Linux comprometido. El objetivo fue identificar, contener y erradicar una intrusión activa sin interrumpir el servicio.

---

## 🧭 Metodología

- **Enfoque:** Live Incident Response (LIR)
- **Framework:** PICERL (Preparación, Identificación, Contención, Erradicación, Recuperación, Lecciones)
- **Mapeo MITRE ATT&CK:** T1566, T1059.004, T1136.001, T1053.003, T1048.003

---

## 🔍 Fase 1 — Reconocimiento e Identificación

- ✅ Análisis del estado del sistema (uptime, RAM, kernel, red)
- ✅ Detección de usuarios no autorizados (`reports`, `hacker`)
- ✅ Análisis de logs de autenticación (`auth.log`)
- ✅ Identificación de puertos sospechosos (FTP puerto 21)
- ✅ Evidencia de ingeniería social (phishing por email)
- ✅ Descubrimiento de cronjob malicioso (`backup2.sh`) exfiltrando credenciales cada 15 minutos

## 🧯 Fase 2 — Contención, Erradicación y Recuperación

- ✅ Eliminación de usuarios backdoor
- ✅ Remoción del script malicioso y tarea programada
- ✅ Reconfiguración del firewall (UFW)
- ✅ Cambio de credenciales comprometidas
- ✅ Verificación de integridad del sistema

---

## 🎯 Hallazgos Principales

| # | Hallazgo |
|---|---|
| 1 | 2 usuarios no autorizados creados mediante ingeniería social y acceso directo |
| 2 | Exfiltración de credenciales vía HTTP POST cada 15 minutos durante ~1 año |
| 3 | Servicio FTP activo sin autorización (puerto 21) |
| 4 | Persistencia vía cronjob malicioso (`/etc/cron.d/sys-maintenance`) |

---

## 📁 Estructura del Repositorio

| Archivo | Descripción |
|---|---|
| `Informe_Tecnico_Incident_Response_4Geeks_FINAL.docx` | 📄 Informe técnico completo (72 páginas) con evidencias, análisis y recomendaciones |
| `Fase1_Hallazgos_RaulVelasquez.pptx` | 🖥️ Presentación Fase 1 — Reconocimiento y Hallazgos |
| `Guion_Presentacion_Fase1_RaulVelasquez.docx` | 📝 Guion de presentación con comandos explicados |
| `PASO*.png` | 📸 Capturas de pantalla de evidencias del servidor comprometido |
| `FASE 2/` | 🧯 Documentación de la Fase 2 — Remediación y Restauración |

---

## 👤 Autor

**Raúl Velásquez**

---
Proyecto académico — 4Geeks Academy · 2026
