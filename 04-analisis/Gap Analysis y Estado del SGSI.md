# 🛡️ Gap Analysis y Estado del SGSI — NovaRetail SpA

> Análisis de brechas bajo **ISO/IEC 27001:2022** + **NIST CSF 2.0**.
> Última actualización: **17-06-2026** · Equipo Thynk Unlimited.

## 1. Estado de madurez

| Capa | Estado | % |
|---|---|---|
| Operativa (políticas, procedimientos, controles) | Sólida | ~85% |
| Análisis de riesgos (inventario, matriz, SoA, metodología, plan de tratamiento) | Completa (alcance tecnológico) | ~90% |
| Gobierno (alcance, política madre, roles, RACI) | Sólida | ~90% |
| Operación del SGSI (auditoría, revisión dirección, mejora, BCP, objetivos) | Incorporada al repo | ~90% |
| Laboratorio técnico (Zabbix/Wazuh/Ansible) | Planificado, sin montar | 0% |
| **Madurez global** | **En progreso** | **~80%** |

## 2. Lo que YA está cubierto ✅

- 15 políticas (POL-SGSI-01 a 15) y 18 procedimientos (PROC-SGSI-01 a 18).
- Documentos de gestión: Maestro Documental, Matriz Legal, Matriz de Competencias, Contrato + Anexo.
- **Gobernanza y operación** (`00-gobernanza/`): Alcance (4.3), Política General (5.1), Acta CISO/Comité (5.3), Matriz RACI (5.3), **Auditoría Interna (9.2)**, **Revisión por la Dirección (9.3)**, **No Conformidades y Acciones Correctivas (10)**, **BCP/DRP (5.29–5.30)** y **Objetivos de Seguridad medibles (6.2)**.
- **Análisis** (`04-analisis/`): Inventario de Activos (15), Matriz de Riesgos (R-01 a R-17), SoA tecnológico (8.1–8.34), **Metodología de riesgos con criterios de aceptación (6.1.2)** y **Plan de Tratamiento de Riesgos (6.1.3)**.
- Diagramas BPMN de procesos clave; **repositorio de evidencias estructurado (7.5/9.1)**; mapeo ISO actualizado (incluye 8.14/8.29/8.33).

## 3. Lo que FALTA ⚠️ (hoja de ruta)

### ✅ Resueltas en esta versión
| # | Brecha | Cláusula | Documento que la cierra |
|---|---|---|---|
| G-3 | Plan de Tratamiento de Riesgos | 6.1.3 | ANR-SGSI-02 |
| G-4 | Procedimiento de Auditoría Interna + programa anual | 9.2 | GOB-SGSI-05 |
| G-5 | Procedimiento de Revisión por la Dirección | 9.3 | GOB-SGSI-06 |
| G-6 | No Conformidades y Acciones Correctivas | 10.1, 10.2 | GOB-SGSI-07 |
| G-7 | Plan de Continuidad del Negocio (BCP/DRP) | 5.29, 5.30 | GOB-SGSI-08 |
| G-8 | Repositorio de evidencias estructurado | 7.5, 9.1 | `03-evidencias/README.md` + carpetas e índice |
| G-9 | Escala y **criterios de aceptación del riesgo** | 6.1.2 | ANR-SGSI-01 |
| G-10 | Nombres de archivo .docx normalizados (tildes mal codificadas) | — | 23 archivos renombrados |
| G-11 | Fechas de emisión unificadas | — | Maestro alineado a los .docx (pol/proc **22-04-2026**; gobernanza/análisis **17-06-2026**) |
| G-12 | Objetivos de seguridad medibles | 6.2 | GOB-SGSI-09 |
| G-13 | Procedimiento de Desarrollo Seguro (SDLC) | 8.25–8.29 | PROC-SGSI-15 |
| G-14 | Procedimientos dedicados de malware, dispositivos y cifrado | 8.7 / 8.1 / 8.24 | PROC-SGSI-16 / 17 / 18 |

### ◻️ Decisión de alcance (no es brecha)
| # | Tema | Cláusula | Decisión |
|---|---|---|---|
| G-1 | SoA cubre **solo controles Tecnológicos** (8.1–8.34) | 6.1.3.d | Alcance deliberado de esta versión: Organizacionales (5.x), Personas (6.x) y Físicos (7.x) quedan fuera. |

### ⏳ Pendiente (fuera de esta entrega documental)
| # | Brecha | Cláusula | Acción |
|---|---|---|---|
| G-2 | **Laboratorio técnico** sin montar (Zabbix/Wazuh/Ansible) | — | Ejecutar plan `05-laboratorio/` (trabajo de máquinas/VMs, fuera de este alcance) |

> **Cobertura procedimental (revisión política↔procedimiento):** las **15 políticas tienen ahora un procedimiento dedicado** y vinculado con hipervínculo en ambos sentidos. Se agregaron **PROC-SGSI-15 (SDLC)**, **16 (malware → POL-04)**, **17 (dispositivos → POL-06)** y **18 (cifrado → POL-12)**.

## 4. Prioridad restante

1. **G-2** Laboratorio técnico (Zabbix/Wazuh/Ansible) — **único pendiente**; trabajo de infraestructura/VMs.
2. *(Opcional, solo si se amplía el alcance)* Completar el SoA con las categorías Organizacionales, Personas y Físicas (G-1).

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
| T-08 Plan de tratamiento | ✅ ANR-SGSI-02 |
| T-09/T-10 SoA + aprobación | ✅ tecnológico (alcance definido) |
| T-11–T-14 Operación del SGSI (auditoría, revisión, NC, BCP) | ✅ GOB-SGSI-05 a 08 |
| Metodología + criterios de aceptación de riesgo | ✅ ANR-SGSI-01 |
| Objetivos de seguridad medibles | ✅ GOB-SGSI-09 |
| Cobertura procedimental 15/15 (SDLC, malware, dispositivos, cifrado) | ✅ PROC-SGSI-15 a 18 |
| T-15 a T-20 Quick wins y cultura (laboratorio) | ⏳ pendientes (G-2) |
