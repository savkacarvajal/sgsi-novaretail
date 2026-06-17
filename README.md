<div align="center">

# 🔐 SGSI — NovaRetail SpA

**Sistema de Gestión de Seguridad de la Información**
Desarrollado por el equipo **Thynk Unlimited** · Ramo *Gestión de la Ciberseguridad*

![ISO/IEC 27001:2022](https://img.shields.io/badge/ISO%2FIEC-27001%3A2022-1F3864)
![PCI DSS](https://img.shields.io/badge/PCI%20DSS-v4.0-2E5496)
![Ley 21.663](https://img.shields.io/badge/Ley-21.663%20Ciberseguridad-006100)
![Ley 19.628](https://img.shields.io/badge/Ley-19.628%20Datos%20Personales-9C6500)
![Estado](https://img.shields.io/badge/estado-académico-lightgrey)

</div>

---

> [!NOTE]
> **NovaRetail SpA** es una empresa **ficticia**. Este repositorio es un trabajo **académico** con fines educativos y no representa a ninguna organización real.

## 📑 Tabla de contenidos

- [Sobre el proyecto](#-sobre-el-proyecto)
- [Estructura del repositorio](#-estructura-del-repositorio)
- [Índice de políticas](#-índice-de-políticas-15)
- [Índice de procedimientos](#-índice-de-procedimientos-14)
- [Documentos de gestión](#-documentos-de-gestión)
- [Diagramas de flujo](#-diagramas-de-flujo)
- [Marco normativo](#-marco-normativo-de-referencia)
- [Equipo](#-equipo--thynk-unlimited)

## 🎯 Sobre el proyecto

NovaRetail SpA es una empresa de retail que procesa pagos con tarjeta y datos personales de sus clientes. Este SGSI define las **políticas**, **procedimientos** y **evidencias** que protegen la confidencialidad, integridad y disponibilidad de su información.

El sistema está alineado con cuatro marcos:

- **ISO/IEC 27001:2022** — controles del Anexo A.
- **PCI DSS v4.0** — protección de datos de tarjetas de pago.
- **Ley 21.663** — Marco de Ciberseguridad de Chile (reporte de incidentes a la ANCI).
- **Ley 19.628** — Protección de Datos Personales de Chile.

## 📁 Estructura del repositorio

| Carpeta | Descripción |
|---|---|
| `01-politicas/` | 15 políticas de seguridad (POL-SGSI-01 a 15) |
| `02-procedimientos/` | 14 procedimientos operativos (PROC-SGSI-01 a 14) |
| `03-evidencias/` | Diagramas de flujo (PNG / BPMN) y evidencias de respaldo |
| `04-analisis/` | Análisis, scoring y auditoría de los documentos |
| `docs/` | Mapeo normativo y documentos de gestión (maestro documental, matrices, contrato) |

## 📋 Índice de políticas (15)

| Código | Política | Controles ISO 27001:2022 |
|---|---|---|
| POL-SGSI-01 | Control de acceso | 5.15–5.18, 8.2, 8.3, 8.5 |
| POL-SGSI-02 | Gestión de contraseñas y autenticación | 5.17, 8.5 |
| POL-SGSI-03 | Respaldo y recuperación | 8.13 |
| POL-SGSI-04 | Protección contra malware | 8.7 |
| POL-SGSI-05 | Gestión de parches y actualización | 8.8, 8.19 |
| POL-SGSI-06 | Uso seguro de dispositivos y estaciones | 6.7, 7.9, 8.1 |
| POL-SGSI-07 | Seguridad de red | 8.20–8.23 |
| POL-SGSI-08 | Registro y monitoreo | 8.15–8.17 |
| POL-SGSI-09 | Gestión de vulnerabilidades | 8.8 |
| POL-SGSI-10 | Manejo de información y clasificación | 5.12–5.14, 8.10–8.12 |
| POL-SGSI-11 | Gestión de incidentes y reporte ANCI | 5.24–5.28 |
| POL-SGSI-12 | Cifrado de datos | 8.24 |
| POL-SGSI-13 | Gestión de proveedores y terceros (OIV) | 5.19–5.23 |
| POL-SGSI-14 | Contratación y desvinculación | 6.1, 6.2, 6.4–6.6 |
| POL-SGSI-15 | Línea base de software | 8.9, 8.19 |

## ⚙️ Índice de procedimientos (14)

| Código | Procedimiento | Controles ISO 27001:2022 |
|---|---|---|
| PROC-SGSI-01 | Actualización y gestión de parches | 8.8, 8.19 |
| PROC-SGSI-02 | Backup de base de datos | 8.13 |
| PROC-SGSI-03 | Rollback | 8.13, 8.32 |
| PROC-SGSI-04 | Línea base de software (Ansible) | 8.9, 8.19, 8.32 |
| PROC-SGSI-05 | Incidentes con plazos ANCI | 5.24–5.26 |
| PROC-SGSI-06 | Alta, modificación y baja de accesos | 5.16, 5.18, 8.2 |
| PROC-SGSI-07 | Revisión periódica de accesos | 5.18 |
| PROC-SGSI-08 | Uso del gestor de contraseñas | 5.17, 8.5 |
| PROC-SGSI-09 | Segmentación y revisión de firewall | 8.20, 8.22 |
| PROC-SGSI-10 | Revisión y escalada de alertas | 8.15, 8.16 |
| PROC-SGSI-11 | Escaneo de vulnerabilidades | 8.8 |
| PROC-SGSI-12 | Retención y eliminación segura | 8.10, 8.13 |
| PROC-SGSI-13 | Contratación y desvinculación | 6.1, 6.2, 6.5 |
| PROC-SGSI-14 | Evaluación de proveedores | 5.19–5.22 |

## 📊 Documentos de gestión

Ubicados en [`docs/`](docs/):

| Documento | Descripción |
|---|---|
| [Maestro Documental SGSI](docs/Maestro%20Documental%20SGSI.xlsx) | Índice maestro de las 29 políticas y procedimientos (versión, responsable, estado, controles). |
| [Matriz Legal](docs/Matriz%20Legal.xlsx) | Cruce de Ley 21.663, Ley 19.628 y PCI DSS v4.0 contra los documentos del SGSI. |
| [Matriz de Competencias](docs/Matriz%20de%20Competencias.xlsx) | Competencias de seguridad exigidas por cargo (formación, MFA, PDP, certificaciones). |
| [Contrato de Trabajo y Anexo de Seguridad](docs/Contrato%20de%20Trabajo%20y%20Anexo%20de%20Seguridad.docx) | Contrato con anexo de confidencialidad y perfil de cargo, alineado a PROC-SGSI-13. |
| [Mapeo ISO 27001](docs/mapeo-iso27001.md) | Mapeo de cada documento a los controles del Anexo A. |

## 🗺️ Diagramas de flujo

Disponibles en [`03-evidencias/diagramas/`](03-evidencias/diagramas/):

- **Gestión de incidentes y notificación ANCI** (PROC-SGSI-05) — plazos 3 h / 72 h / 15 días.
- **Contratación y desvinculación** (PROC-SGSI-13).
- **Evaluación de proveedores** (PROC-SGSI-14).
- Respaldo y rollback, actualización y parchado, desvinculación segura.

## ⚖️ Marco normativo de referencia

| Marco | Alcance |
|---|---|
| ISO/IEC 27001:2022 | Sistema de gestión y controles del Anexo A |
| PCI DSS v4.0 | Seguridad de datos de tarjetas de pago |
| Ley 21.663 | Marco de Ciberseguridad (Chile) — ANCI |
| Ley 19.628 | Protección de la Vida Privada (Chile) |

## 👥 Equipo — Thynk Unlimited

- Sergio Cubelli
- Savka Carvajal
- Joaquín Zambra
- Alejandro Tapia
- Filippo Moreno

---

<div align="center">
<sub>Repositorio académico · NovaRetail SpA es una empresa ficticia con fines educativos.</sub>
</div>
