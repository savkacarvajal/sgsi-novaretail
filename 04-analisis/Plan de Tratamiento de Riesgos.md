# Plan de Tratamiento de Riesgos — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 6.1.3 «Tratamiento de riesgos de seguridad de la información» (incluye 6.1.3.e Plan de tratamiento y 6.1.3.f riesgos residuales)
> NIST CSF 2.0 — Función **GOVERN (GV.RM)** y **PROTECT (PR)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | ANR-SGSI-02 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Comité SGSI |

## 2. Propósito

Formalizar el tratamiento de cada riesgo identificado en la **Matriz de Evaluación de Riesgos (R-01 a R-17)**, indicando la opción de tratamiento, los **controles del Anexo A** seleccionados (trazados al SoA), la política/procedimiento responsable, el responsable de la acción, el plazo objetivo y el **riesgo residual esperado**. Da cumplimiento a la cláusula 6.1.3.e/f y operacionaliza la **Metodología de Evaluación y Tratamiento de Riesgos (ANR-SGSI-01)**.

## 3. Fases de implementación

| Fase | Ventana | Foco |
|---|---|---|
| **Fase 1 — Quick wins** | 2026-Q3 (jul–sep 2026) | MFA, EDR, backups 3-2-1, parches críticos, centralización de logs |
| **Fase 2 — Estructural** | 2026-Q4 a 2027-Q1 | Segmentación de red, PAM/gestor, SDLC seguro, monitoreo, hardening |
| **Fase 3 — Madurez** | 2027-Q2 | Auditoría, mejora continua, DLP avanzado, pruebas de continuidad |

## 4. Plan de tratamiento por riesgo

> Nivel inicial según la Matriz. Controles según el SoA (trazabilidad **riesgo → control → política**). «Residual esperado» es el nivel objetivo tras aplicar el tratamiento.

| Riesgo | Nivel inicial | Tratamiento | Controles SoA | Política / Proc. | Acción principal | Responsable | Fase | Residual esperado |
|---|---|---|---|---|---|---|---|---|
| R-01 Phishing a admin del portal | 🔴 20 | Mitigar | 8.5, 8.7, 8.16, 8.23 | POL-01/02/11 · PROC-05/10 | MFA obligatorio + EDR + monitoreo de accesos | CISO / TI | 1 | 🟠 Alto |
| R-02 Ransomware en BD de clientes | 🔴 20 | Mitigar | 8.7, 8.8, 8.13, 8.33 | POL-03/04/09 · PROC-02/11 | EDR + backups 3-2-1 inmutables + ciclo de parches | CISO / TI | 1 | 🟢 Moderado |
| R-03 Fraude transaccional en pasarela | 🔴 15 | Mitigar + Transferir | 8.24 | POL-12/13 · PROC-14 | Conciliación y monitoreo transaccional + contrato Transbank/Webpay | Gerencia Finanzas | 2 | 🟢 Moderado |
| R-04 Explotación de vuln. en servidor | 🟠 16 | Mitigar | 8.8, 8.9, 8.15, 8.19 | POL-05/09/15 · PROC-01/04 | Parches + hardening CIS + quitar admin local | Infraestructura TI | 1 | 🟢 Moderado |
| R-05 Movimiento lateral (red plana) | 🟠 12 | Mitigar | 8.20, 8.21, 8.22 | POL-07 · PROC-09 | Segmentación en VLANs + NGFW + IDS/IPS | Infraestructura TI | 2 | 🟢 Moderado |
| R-06 Robo físico de estaciones de bodega | 🟢 9 | Mitigar | 8.1, 8.7 | POL-06 | Cifrado de disco (BitLocker) + control de acceso físico | Gerencia Operaciones | 2 | 🟢 Bajo |
| R-07 Compromiso de credenciales privilegiadas | 🔴 20 | Mitigar | 8.2, 8.5, 8.16 | POL-01/02/14 · PROC-06/08 | PAM + MFA + capacitación anti-ingeniería social | CISO / RRHH | 1 | 🟠 Alto |
| R-08 Brecha en proveedor logístico | 🟠 12 | Mitigar + Transferir | 8.10 | POL-13 · PROC-14 | Cláusulas de seguridad + derecho de auditoría al tercero | Adquisiciones | 2 | 🟢 Moderado |
| R-09 Manipulación de BD de inventario | 🟢 9 | Mitigar | 8.3, 8.15 | POL-08/10 · PROC-07 | Mínimo privilegio + trazabilidad y logs | Gerencia Operaciones | 2 | 🟢 Bajo |
| R-10 Caída prolongada del ERP (sin HA) | 🟠 10 | Mitigar + Aceptar | 8.6, 8.13, 8.14 | POL-03 · GOB-08 (BCP/DRP) | Replicación de BD + BCP/DRP; HA evaluada por costo | Gerencia TI | 2 | 🟢 Moderado |
| R-11 Destrucción/cifrado de respaldos | 🔴 15 | Mitigar | 8.7, 8.13 | POL-03/04 · PROC-02/03 | Backup inmutable offsite + pruebas de restauración | Infraestructura TI | 1 | 🟢 Moderado |
| R-12 Robo de credenciales en planillas | 🔴 15 | Mitigar | 8.2, 8.5 | POL-02 · PROC-08 | Gestor de contraseñas corporativo / PAM | Gerencia TI | 1 | 🟢 Moderado |
| R-13 Compromiso de correo (phishing/BEC) | 🟠 16 | Mitigar | 8.5, 8.16, 8.21, 8.23 | POL-04/07/08 · PROC-10 | DMARC/SPF/DKIM + MFA + filtrado + capacitación | Gerencia TI | 1 | 🟢 Moderado |
| R-14 Reglas de firewall obsoletas | 🟢 8 | Mitigar | 8.8, 8.20 | POL-07 · PROC-09 | Revisión periódica de reglas + actualización de firmware | Infraestructura TI | 2 | 🟢 Bajo |
| R-15 Divulgación de datos por ing. social | 🟢 9 | Mitigar | 8.16 | POL-10/14 · PROC-13 | Capacitación y concientización del personal | RRHH | 2 | 🟢 Bajo |
| R-16 DDoS al portal e-commerce | 🟠 12 | Mitigar + Transferir | 8.20 | POL-07 | WAF + protección anti-DDoS (proveedor) | Infraestructura TI | 2 | 🟢 Moderado |
| R-17 Vulnerabilidad introducida en el código | 🟠 12 | Mitigar | 8.4, 8.25, 8.28, 8.29, 8.31 | POL-09/15 · PROC-04/11 | SDLC seguro + SAST/DAST + pentest previo a release | Jefe de Desarrollo | 2 | 🟢 Moderado |

## 5. Resumen del tratamiento

| Métrica | Valor |
|---|---|
| Riesgos evaluados | 17 (R-01 a R-17) |
| Críticos (≥ 15) | 6 → objetivo: reducir a Alto o inferior |
| Altos (10–14) | 5 → objetivo: reducir a Moderado |
| Moderados/Bajos (< 10) | 6 → tratamiento o aceptación con monitoreo |
| Opción predominante | Mitigar (con transferencia parcial en R-03, R-08, R-16) |
| Riesgos aceptados sin tratamiento | 0 (la fracción aceptada de R-10 queda documentada) |

## 6. Seguimiento y riesgo residual (cl. 6.1.3.f)

- El **CISO** mantiene el seguimiento del plan y reporta el avance en la **Revisión por la Dirección (GOB-SGSI-06)** y según los **Objetivos de Seguridad (GOB-SGSI-09)**.
- El **riesgo residual** se reevalúa al cierre de cada acción; su aceptación sigue los criterios de la **Metodología (ANR-SGSI-01)**: los residuales Crítico/Alto requieren aprobación de la **Gerencia General**.
- Las evidencias de implementación y aceptación se archivan en `03-evidencias/`.

## 7. Documentos relacionados

- Metodología de Evaluación y Tratamiento de Riesgos (ANR-SGSI-01)
- Inventario de Activos, Matriz de Riesgos y SoA (`04-analisis/`)
- Política General de Seguridad (GOB-SGSI-02) · Objetivos de Seguridad (GOB-SGSI-09)
- Plan de Continuidad del Negocio (GOB-SGSI-08)

## 8. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial: formaliza el tratamiento de R-01 a R-17 a partir de la Matriz de Riesgos y el SoA. |
