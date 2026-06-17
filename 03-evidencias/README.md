# 🗂️ Repositorio de Evidencias del SGSI

Información documentada que **evidencia la operación** del SGSI (ISO/IEC 27001:2022 — cl. **7.5** Información documentada y **9.1** Seguimiento y medición · NIST CSF 2.0 — GV.OV).
Aquí se conservan los registros que demuestran que las políticas y procedimientos se ejecutan en la práctica.

## Estructura

| Carpeta | Contenido | Documento que la origina |
|---|---|---|
| `diagramas/` | Diagramas de flujo BPMN/PNG de los procesos | PROC-SGSI-05/13/14 y otros |
| `actas/` | Actas del Comité SGSI, de revisión por la dirección y de aceptación de riesgos | GOB-SGSI-03/06 · ANR-SGSI-01 |
| `auditorias/` | Programa anual, planes, listas de verificación e informes de auditoría | GOB-SGSI-05 |
| `no-conformidades/` | Registro de no conformidades y acciones correctivas | GOB-SGSI-07 |
| `capacitacion/` | Certificados y registros de cursos de concientización | POL-SGSI-14 · O-5 |
| `accesos/` | Registros de alta/baja y de revisión periódica de accesos | PROC-SGSI-06/07 |
| `respaldos/` | Informes de pruebas de restauración (3-2-1) | POL-SGSI-03 · PROC-SGSI-02 · O-4 |
| `incidentes/` | Registros de incidentes y comprobantes de reporte a la ANCI | PROC-SGSI-05 |
| `vulnerabilidades/` | Reportes de escaneo y tickets de remediación | PROC-SGSI-11 · O-6 |
| `kpis/` | Mediciones periódicas de los indicadores | GOB-SGSI-09 |

> Nota: por ser un repositorio **académico**, las carpetas definen la estructura esperada; las evidencias reales se incorporarían durante la operación del SGSI. No se versionan datos personales reales ni secretos.

## Convención de nombres

`AAAA-MM-DD_TIPO_descripcion-corta.ext` — ejemplo: `2026-09-30_acta_revision-direccion.pdf`.

## Diagramas BPMN disponibles

En [`diagramas/`](diagramas/). La narrativa de cada uno está en `Evidencias de diagramas.docx`; la fuente editable es `Diagramas.bpm`.

**Versión canónica (vigente):**
- `PROC-SGSI-05 Gestión de incidentes y notificación ANCI.png` — alerta temprana 3 h · actualización 72 h (24 h si OIV) · informe final 15 días corridos.
- `PROC-SGSI-13 Contratación y desvinculación.png`
- `PROC-SGSI-14 Evaluación de proveedores.png`

**Antecedente (versiones previas, se conservan):** `Actualización y parchado.png` · `Respaldo y rollback.png` · `Desvinculación Segura.png` · `Incidentes y sanciones.png`.

## Índice de evidencias (registro maestro)

| ID | Fecha | Tipo | Documento / control que evidencia | Responsable | Ubicación | Estado |
|---|---|---|---|---|---|---|
| EVI-0001 | 2026-06-17 | Diagrama | PROC-SGSI-05 (incidentes/ANCI) | CISO | `diagramas/` | Vigente |
| EVI-0002 | 2026-06-17 | Diagrama | PROC-SGSI-13 (contratación/desvinculación) | RRHH | `diagramas/` | Vigente |
| EVI-0003 | 2026-06-17 | Diagrama | PROC-SGSI-14 (evaluación de proveedores) | Adquisiciones | `diagramas/` | Vigente |
| _(plantilla)_ | AAAA-MM-DD | Acta / Informe / Certificado / Log | _documento o control_ | _responsable_ | _carpeta_ | Abierta / Vigente |

## Trazabilidad

Cada evidencia se vincula al **control del SoA**, **política** o **procedimiento** que la origina, manteniendo la cadena **control → procedimiento → evidencia** exigida por la cláusula 7.5.
