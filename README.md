Proyecto Final — Live Incident Response

4Geeks Academy · Ciberseguridad · Junio 2026

Alumno: Raul J. Velasquez


Descripcion

Analisis de respuesta a incidentes en tiempo real (Live Incident Response) sobre un servidor Linux comprometido. El objetivo fue identificar, contener y erradicar una intrusión activa sin interrumpir el servicio.

Estructura del repositorio

ArchivoDescripcionInforme_Tecnico_Incident_Response_4Geeks_FINAL.docxInforme tecnico completo (~70 paginas) con evidencias, analisis y recomendacionesFase1_Hallazgos_RaulVelasquez.pptxPresentacion Fase 1 — Reconocimiento y HallazgosGuion_Presentacion_Fase1_RaulVelasquez.docxGuion de presentacion con comandos explicadosPASO*.pngCapturas de pantalla de evidencias del servidor comprometidoFASE 2/Documentacion de la Fase 2 — Remediacion y Restauracion

Fases del proyecto

Fase 1 — Reconocimiento e Identificacion


Analisis del estado del sistema (uptime, RAM, kernel, red)
Deteccion de usuarios no autorizados (reports, hacker)
Analisis de logs de autenticacion (auth.log)
Identificacion de puertos sospechosos (FTP puerto 21)
Evidencia de ingenieria social (phishing por email)
Descubrimiento de cronjob malicioso (backup2.sh) exfiltrando credenciales cada 15 minutos


Fase 2 — Contencion, Erradicacion y Recuperacion


Eliminacion de usuarios backdoor
Remocion del script malicioso y tarea programada
Reconfiguracion del firewall (UFW)
Cambio de credenciales comprometidas
Verificacion de integridad del sistema


Hallazgos principales


2 usuarios no autorizados creados mediante ingenieria social y acceso directo
Exfiltracion de credenciales via HTTP POST cada 15 minutos durante ~1 año
Servicio FTP activo sin autorizacion (puerto 21)
Persistencia via cronjob malicioso (/etc/cron.d/sys-maintenance)


Metodologia


Enfoque: Live Incident Response (LIR)
Framework: PICERL (Preparacion, Identificacion, Contencion, Erradicacion, Recuperacion, Lecciones)
Mapeo: MITRE ATT&CK (T1566, T1059.004, T1136.001, T1053.003, T1048.003)



Proyecto academico — 4Geeks Academy · 2026
