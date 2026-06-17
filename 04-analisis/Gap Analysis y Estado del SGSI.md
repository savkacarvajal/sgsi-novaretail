# 🛡️ Gap Analysis y Estado del SGSI — NovaRetail SpA

> Análisis de brechas bajo **ISO/IEC 27001:2022** + **NIST CSF 2.0**.
> Última actualización: **17-06-2026** · Equipo Thynk Unlimited.

## 1. Estado de madurez

| Capa | Estado | % |
|---|---|---|
| Operativa (políticas, procedimientos, controles) | Sólida | ~85% |
| Análisis de riesgos (inventario, matriz, SoA) | Incorporada al repo | ~75% |
| Gobierno (alcance, política madre, roles, RACI) | Incorporada al repo | ~70% |
| Operación del SGSI (auditoría, revisión dirección, mejora, BCP) | Pendiente | ~20% |
| Laboratorio técnico (Zabbix/Wazuh/Ansible) | Planificado, sin montar | 0% |
| **Madurez global** | **En progreso** | **~65%** |

## 2. Lo que YA está cubierto ✅

- 15 políticas (POL-SGSI-01 a 15) y 14 procedimientos (PROC-SGSI-01 a 14).
- Documentos de gestión: Maestro Documental, Matriz Legal, Matriz de Competencias, Contrato + Anexo.
- **Gobernanza** (`00-gobernanza/`): Alcance (4.3), Política General (5.1), Acta CISO/Comité (5.3), Matriz RACI.
- **Análisis** (`04-analisis/`): Inventario de Activos (15), Matriz de Riesgos (R-01 a R-17), SoA tecnológico (8.1–8.34).
- Diagramas BPMN de procesos clave; mapeo ISO actualizado.

## 3. Lo que FALTA ⚠️ (hoja de ruta)

### 🔴 Críticas
| # | Brecha | Cláusula | Acción |
|---|---|---|---|
| G-1 | **SoA incompleto**: solo cubre controles Tecnológicos (cap. 8). Faltan **Organizacionales (5.1–5.37)**, **Personas (6.1–6.8)** y **Físicos (7.1–7.14)** | 6.1.3.d | Completar las 3 categorías restantes del Anexo A en el SoA |
| G-2 | **Laboratorio técnico** sin montar (Zabbix/Wazuh/Ansible) — requisito 3ra entrega | — | Ejecutar plan `05-laboratorio/` |

### 🟡 Medias
| # | Brecha | Cláusula |
|---|---|---|
| G-3 | **Plan de Tratamiento de Riesgos** formal (hoy implícito en las "acciones por fase" del SoA) | 6.1.3 |
| G-4 | **Procedimiento de Auditoría Interna** + programa anual | 9.2 |
| G-5 | **Procedimiento de Revisión por la Dirección** | 9.3 |
| G-6 | **Procedimiento de No Conformidades y Acciones Correctivas** | 10.1, 10.2 |
| G-7 | **Plan de Continuidad del Negocio (BCP/DRP)** | 5.29, 5.30 |
| G-8 | **Repositorio de evidencias** (registros firmados, certificados de cursos, logs) | 7.5, 9.1 |

### 🟢 Mejoras
| # | Mejora |
|---|---|
| G-9 | Documentar formalmente la **escala y criterios de aceptación del riesgo** (cl. 6.1.2). |
| G-10 | Normalizar **nombres de archivo** de los .docx (tildes mal codificadas). |
| G-11 | Unificar **fechas** de emisión entre documentos. |
| G-12 | Definir **objetivos de seguridad** con metas trimestrales medibles (base en GOB-SGSI-02). |

## 4. Prioridad sugerida

1. **G-2** Laboratorio (vence la 3ra entrega — 18/06).
2. **G-1** Completar SoA (Organizacionales + Personas + Físicos).
3. **G-4 / G-5 / G-6** Procedimientos de operación del SGSI (auditoría, revisión, mejora).
4. **G-7** BCP/DRP.
5. **G-8 a G-12** Evidencias y mejoras de calidad.

## 5. Trazabilidad con el backlog (Kanban)

| Tarea Kanban | Estado |
|---|---|
| T-01 Inventario de activos | ✅ en repo |
| T-02 Gap Analysis | ✅ este documento |
| T-03 Alcance formal | ✅ GOB-SGSI-01 |
| T-04 CISO y Comité | ✅ GOB-SGSI-03 |
| T-05 Política General | ✅ GOB-SGSI-02 |
| T-06 Matriz RACI | ✅ GOB-SGSI-04 |
| T-07 Matriz de riesgos | ✅ en repo |
| T-08 Plan de tratamiento | 🟡 parcial (SoA) |
| T-09/T-10 SoA + aprobación | 🟡 parcial (falta cap. 5/6/7) |
| T-15 a T-20 Quick wins y cultura | ⏳ pendientes |
