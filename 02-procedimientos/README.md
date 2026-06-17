# 📘 Procedimientos Operativos

Los **18 procedimientos** del SGSI (PROC-SGSI-01 a 18) que operacionalizan las [políticas](../01-politicas/).
Cada procedimiento es un documento `.docx` en esta carpeta. Trazabilidad completa en el [Maestro Documental](../docs/Maestro%20Documental%20SGSI.xlsx) y el [mapeo ISO](../docs/mapeo-iso27001.md).

| Código | Procedimiento | Controles ISO 27001:2022 | Política | Responsable |
|---|---|---|---|---|
| PROC-SGSI-01 | Actualización y gestión de parches | 8.8, 8.19 | POL-05 | Gerencia TI |
| PROC-SGSI-02 | Backup de base de datos | 8.13, 8.14 | POL-03 | Gerencia TI / DBA |
| PROC-SGSI-03 | Rollback | 8.13, 8.32 | POL-03 | Gerencia TI / DBA |
| PROC-SGSI-04 | Línea base de software (Ansible) | 8.9, 8.19, 8.32 | POL-15 | Gerencia TI |
| PROC-SGSI-05 | Incidentes con plazos ANCI | 5.24–5.26 | POL-11 | CISO |
| PROC-SGSI-06 | Alta, modificación y baja de accesos | 5.16, 5.18, 8.2 | POL-01 | Gerencia TI / RRHH |
| PROC-SGSI-07 | Revisión periódica de accesos | 5.18 | POL-01 | CISO |
| PROC-SGSI-08 | Uso del gestor de contraseñas | 5.17, 8.5 | POL-02 | CISO |
| PROC-SGSI-09 | Segmentación y revisión de firewall | 8.20, 8.22 | POL-07 | Gerencia TI |
| PROC-SGSI-10 | Revisión y escalada de alertas | 8.15, 8.16 | POL-08 | SOC / CISO |
| PROC-SGSI-11 | Escaneo de vulnerabilidades | 8.8, 8.29 | POL-09 | CISO |
| PROC-SGSI-12 | Retención y eliminación segura | 8.10, 8.13, 8.33 | POL-10 | Gerencia TI / Delegado PDP |
| PROC-SGSI-13 | Contratación y desvinculación | 6.1, 6.2, 6.5 | POL-14 | RRHH |
| PROC-SGSI-14 | Evaluación de proveedores | 5.19–5.22 | POL-13 | CISO / Adquisiciones |
| PROC-SGSI-15 | Desarrollo seguro (SDLC) | 8.4, 8.25–8.29, 8.31 | POL-15/09 | Jefe de Desarrollo / CISO |
| PROC-SGSI-16 | Respuesta ante malware | 8.7 | POL-04 | Ciberseguridad / TI |
| PROC-SGSI-17 | Uso seguro de dispositivos | 6.7, 7.9, 8.1 | POL-06 | Gerencia TI |
| PROC-SGSI-18 | Cifrado y gestión de llaves | 8.24 | POL-12 | Gerencia TI / DBA |

> Versión 1.0 · emisión 22-04-2026 (PROC-01 a 14) y 17-06-2026 (PROC-15 a 18) · aprobados por el **CISO** · clasificación **Interno**.
> Cada procedimiento tiene su **diagrama de flujo (BPMN)** en [`../03-evidencias/diagramas/`](../03-evidencias/diagramas/) (18 diagramas, uno por procedimiento).
