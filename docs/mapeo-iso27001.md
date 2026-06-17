# Mapeo SGSI ↔ ISO/IEC 27001:2022 (Anexo A)

Mapeo orientativo de cada documento del SGSI a los controles del Anexo A de la ISO/IEC 27001:2022.
La norma 2022 reorganiza los controles en 4 temas: **5. Organizacionales**, **6. Personas**, **7. Físicos**, **8. Tecnológicos**.

## Políticas

| Documento | Controles ISO 27001:2022 (Anexo A) |
|---|---|
| POL-SGSI-01 Control de acceso | 5.15, 5.16, 5.17, 5.18, 8.2, 8.3, 8.5 |
| POL-SGSI-02 Contraseñas y autenticación | 5.17, 8.5 |
| POL-SGSI-03 Respaldo y recuperación | 8.13, 8.14 |
| POL-SGSI-04 Protección contra malware | 8.7 |
| POL-SGSI-05 Gestión de parches | 8.8, 8.19 |
| POL-SGSI-06 Uso seguro de dispositivos | 6.7, 7.9, 8.1 |
| POL-SGSI-07 Seguridad de red | 8.20, 8.21, 8.22, 8.23 |
| POL-SGSI-08 Registro y monitoreo | 8.15, 8.16, 8.17 |
| POL-SGSI-09 Gestión de vulnerabilidades | 8.8, 8.29 |
| POL-SGSI-10 Manejo y clasificación de información | 5.12, 5.13, 5.14, 8.10, 8.11, 8.12, 8.33 |
| POL-SGSI-11 Incidentes y reporte ANCI | 5.24, 5.25, 5.26, 5.27, 5.28 |
| POL-SGSI-12 Cifrado de datos | 8.24 |
| POL-SGSI-13 Proveedores y terceros (OIV) | 5.19, 5.20, 5.21, 5.22, 5.23 |
| POL-SGSI-14 Contratación y desvinculación | 6.1, 6.2, 6.4, 6.5, 6.6 |
| POL-SGSI-15 Línea base de software | 8.9, 8.19 |

## Procedimientos

| Documento | Controles ISO 27001:2022 (Anexo A) |
|---|---|
| PROC-SGSI-01 Actualización y parches | 8.8, 8.19 |
| PROC-SGSI-02 Backup de base de datos | 8.13, 8.14 |
| PROC-SGSI-03 Rollback | 8.13, 8.32 |
| PROC-SGSI-04 Línea base de software (Ansible) | 8.9, 8.19, 8.32 |
| PROC-SGSI-05 Incidentes con plazos ANCI | 5.24, 5.25, 5.26 |
| PROC-SGSI-06 Alta/modificación/baja de accesos | 5.16, 5.18, 8.2 |
| PROC-SGSI-07 Revisión periódica de accesos | 5.18 |
| PROC-SGSI-08 Uso del gestor de contraseñas | 5.17, 8.5 |
| PROC-SGSI-09 Segmentación y firewall | 8.20, 8.22 |
| PROC-SGSI-10 Revisión y escalada de alertas | 8.15, 8.16 |
| PROC-SGSI-11 Escaneo de vulnerabilidades | 8.8, 8.29 |
| PROC-SGSI-12 Retención y eliminación segura | 8.10, 8.13, 8.33 |
| PROC-SGSI-13 Contratación y desvinculación | 6.1, 6.2, 6.5 |
| PROC-SGSI-14 Evaluación de proveedores | 5.19, 5.20, 5.21, 5.22 |

## Gobernanza y operación del SGSI (cláusulas 4–10)

| Documento | Cláusula ISO 27001:2022 |
|---|---|
| GOB-SGSI-01 Alcance del SGSI | 4.1, 4.2, 4.3 |
| GOB-SGSI-02 Política General de Seguridad | 5.1, 5.2 · A.5.1 |
| GOB-SGSI-03 Acta CISO y Comité SGSI | 5.1, 5.3 · A.5.2 |
| GOB-SGSI-04 Matriz RACI | 5.3 · A.5.2, A.5.3 |
| GOB-SGSI-05 Procedimiento de Auditoría Interna | 9.2 · A.5.35, A.5.36 |
| GOB-SGSI-06 Procedimiento de Revisión por la Dirección | 9.3 |
| GOB-SGSI-07 No Conformidades y Acciones Correctivas | 10.1, 10.2 |
| GOB-SGSI-08 Plan de Continuidad del Negocio (BCP/DRP) | 5.29, 5.30 · A.5.29, A.5.30, A.8.13, A.8.14 |
| GOB-SGSI-09 Objetivos de Seguridad de la Información | 6.2 |

## Análisis de riesgos (cláusula 6.1 · `04-analisis/`)

| Documento | Cláusula ISO 27001:2022 |
|---|---|
| Metodología de Evaluación y Tratamiento de Riesgos | 6.1.2 |
| Plan de Tratamiento de Riesgos | 6.1.3, 6.1.3.e, 6.1.3.f |
| Inventario de Activos | A.5.9 |
| Matriz de Evaluación de Riesgos (R-01 a R-17) | 6.1.2 |
| Declaración de Aplicabilidad (SoA — controles tecnológicos 8.1–8.34) | 6.1.3.d |

---
*Notas:*
- *El mapeo es orientativo y debe validarse contra la Declaración de Aplicabilidad (SoA) del SGSI.*
- *Controles **A.8.14** (redundancia), **A.8.29** (pruebas de seguridad en desarrollo) y **A.8.33** (información de prueba) ya estaban evaluados en el SoA y quedan ahora trazados a sus políticas y procedimientos.*
