# Matriz RACI del SGSI — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 5.3 (Roles, responsabilidades y autoridades) · Control Anexo A 5.2, 5.3
> NIST CSF 2.0 — Función **GOVERN (GV.RR)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-04 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Aprobado por | Gerencia General |

## 2. Convención

- **R** = Responsable (ejecuta) · **A** = Aprobador / *Accountable* (rinde cuentas, uno solo) · **C** = Consultado · **I** = Informado

## 3. Roles

| Sigla | Rol |
|---|---|
| GG | Gerencia General |
| CISO | Encargado de Ciberseguridad |
| CS | Comité SGSI |
| TI | Gerencia / Infraestructura TI |
| DEV | Jefe de Desarrollo |
| RH | Recursos Humanos |
| DPO | Delegado de Protección de Datos |
| ADQ | Adquisiciones / Compras |
| AI | Auditoría Interna |
| DA | Dueños de activos / Jefaturas |

## 4. Matriz RACI por proceso del SGSI

| # | Proceso / Actividad | Doc. SGSI | GG | CISO | CS | TI | DEV | RH | DPO | ADQ | AI | DA |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Definir y aprobar el Alcance del SGSI | GOB-01 | A | R | C | C | I | I | C | I | I | C |
| 2 | Aprobar la Política General de Seguridad | GOB-02 | A | R | C | I | I | I | I | I | I | I |
| 3 | Nombrar CISO y constituir el Comité | GOB-03 | A | C | R | I | I | C | I | I | I | I |
| 4 | Mantener la Matriz RACI | GOB-04 | A | R | C | I | I | I | I | I | I | I |
| 5 | Evaluación de riesgos (Matriz R-01..17) | 04-analisis | A | R | C | C | C | I | C | C | I | C |
| 6 | Plan de tratamiento y SoA | 04-analisis | A | R | C | C | C | I | C | C | I | C |
| 7 | Gestión de accesos (alta/baja/revisión) | POL-01, PROC-06/07 | I | A | I | R | I | C | I | I | C | C |
| 8 | Autenticación y gestor de contraseñas | POL-02, PROC-08 | I | A | I | R | I | I | I | I | I | C |
| 9 | Respaldo y recuperación | POL-03, PROC-02/03 | I | A | I | R | I | I | I | I | C | I |
| 10 | Protección contra malware | POL-04 | I | A | I | R | I | I | I | I | I | I |
| 11 | Gestión de parches y vulnerabilidades | POL-05/09, PROC-01/11 | I | A | I | R | C | I | I | I | C | I |
| 12 | Seguridad de red y firewall | POL-07, PROC-09 | I | A | I | R | I | I | I | I | C | I |
| 13 | Registro, monitoreo y alertas | POL-08, PROC-10 | I | A | I | R | I | I | I | I | C | I |
| 14 | Clasificación y manejo de información | POL-10, PROC-12 | I | A | C | R | C | I | C | I | I | R |
| 15 | Cifrado de datos | POL-12 | I | A | I | R | C | I | C | I | I | I |
| 16 | Gestión de incidentes y reporte ANCI | POL-11, PROC-05 | I | A | C | R | C | C | C | I | C | I |
| 17 | Gestión de proveedores y terceros | POL-13, PROC-14 | I | A | C | C | I | I | C | R | C | C |
| 18 | Contratación y desvinculación | POL-14, PROC-13 | I | C | I | R | I | A | I | I | I | C |
| 19 | Capacitación y concientización | Matriz Competencias | I | A | C | I | I | R | C | I | I | C |
| 20 | Desarrollo seguro (SDLC) | (gap SoA) | I | A | I | C | R | I | I | I | C | I |
| 21 | Línea base de software | POL-15, PROC-04 | I | A | I | R | C | I | I | I | C | I |
| 22 | Auditoría interna | GOB-05 | I | C | A | C | C | I | C | C | R | C |
| 23 | Revisión por la Dirección | GOB-06 | A | R | R | C | I | C | C | I | C | I |
| 24 | No conformidades y mejora continua | GOB-07 | A | R | C | C | C | C | C | C | C | C |
| 25 | Continuidad del negocio (BCP/DRP) | GOB-08 | A | R | C | R | I | I | I | C | C | C |

## 5. Notas
- Cada proceso tiene **un único A** (rinde cuentas).
- El proceso 20 (Desarrollo seguro / SDLC) es la única brecha documental pendiente; auditoría (GOB-05), revisión por la dirección (GOB-06), no conformidades (GOB-07) y continuidad (GOB-08) ya cuentan con su documento.
- Esta matriz debe revisarse en cada cambio organizacional relevante.

## 6. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial |
