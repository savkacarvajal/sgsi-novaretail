# Objetivos de Seguridad de la Información y KPIs — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 6.2 «Objetivos de seguridad de la información y planificación para lograrlos» · apoyo en 9.1 (Seguimiento y medición)
> NIST CSF 2.0 — Función **GOVERN (GV.RM, GV.OV)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-09 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Gerencia General |

## 2. Propósito

Definir los **objetivos de seguridad de la información** de NovaRetail SpA y la forma de planificarlos, medirlos y revisarlos, conforme a la cláusula 6.2 de ISO/IEC 27001:2022. Estos objetivos desarrollan y hacen medibles los enunciados en la **Política General de Seguridad (GOB-SGSI-02, sección 6)**.

## 3. Principios (cl. 6.2)

Los objetivos son **coherentes** con la política, **medibles** (cuando es posible), consideran los requisitos aplicables y los resultados de la evaluación de riesgos, se **monitorean**, se **comunican** y se **actualizan** según corresponda.

## 4. Cuadro de objetivos y KPIs

| ID | Objetivo | Indicador (KPI) | Línea base (2026-Q2) | Meta | Frecuencia | Responsable |
|---|---|---|---|---|---|---|
| O-1 | Reducir el riesgo residual de los riesgos críticos (Nivel ≥ 15) | N.º de riesgos críticos abiertos | 8 (R-01, R-02, R-03, R-04, R-07, R-11, R-12, R-13) | ↓ ≥ 50 % anual | Trimestral | CISO |
| O-2 | Cobertura de MFA en cuentas con acceso a sistemas | % de cuentas con MFA | ~0 % | 100 % | Trimestral | Gerencia TI |
| O-3 | Cumplir los plazos de notificación a la ANCI | % de incidentes N3 reportados ≤ 3 h | s/d | 100 % | Por incidente | CISO |
| O-4 | Backups probados (esquema 3-2-1) | % de pruebas de restauración exitosas | s/d | 100 % trimestral | Trimestral | Infraestructura TI |
| O-5 | Personal capacitado en seguridad | % de personal con curso aprobado | s/d | ≥ 95 % anual | Anual | RRHH |
| O-6 | Vulnerabilidades críticas remediadas en SLA | % remediadas en plazo (≤ 15 días) | s/d | ≥ 90 % | Mensual | CISO / TI |
| O-7 | Cierre oportuno de no conformidades | % de NC cerradas dentro de plazo | s/d | ≥ 90 % | Trimestral | CISO |
| O-8 | Cobertura de revisión de accesos | % de accesos revisados según calendario | s/d | 100 % trimestral | Trimestral | Gerencia TI |

> «s/d» = sin dato de línea base aún; se establecerá en la primera medición. La reducción de O-1 se mide contra el **Plan de Tratamiento de Riesgos (ANR-SGSI-02)**.

## 5. Planificación para lograrlos (cl. 6.2 — qué/recursos/quién/cuándo/evaluación)

| Objetivo | Acciones clave | Recursos | Plazo | Cómo se evalúa |
|---|---|---|---|---|
| O-1, O-6 | Ejecutar Fases 1–2 del Plan de Tratamiento; ciclo de escaneo y remediación | Herramienta de escaneo, horas de TI | 2026-Q3 a 2027-Q1 | KPIs trimestrales |
| O-2 | Habilitar MFA en portal, correo y cuentas privilegiadas | IdP / MFA | 2026-Q3 | Reporte de cobertura |
| O-4 | Implantar 3-2-1 inmutable y probar restauraciones | Almacenamiento offsite | 2026-Q3 | Informes de prueba (BCP/DRP) |
| O-3, O-7 | Operar PROC-SGSI-05 y GOB-SGSI-07 | Equipo SGSI | Continuo | Registros de incidentes y NC |
| O-5 | Plan anual de capacitación y concientización | RRHH / contenidos | 2026-Q4 | % de aprobación |

## 6. Seguimiento, medición y comunicación (cl. 9.1)

- El **CISO** consolida los KPIs según su frecuencia y los presenta en la **Revisión por la Dirección (GOB-SGSI-06)**.
- Los resultados se comunican al Comité SGSI y a las áreas responsables.
- Las desviaciones relevantes pueden originar **no conformidades** (GOB-SGSI-07).

## 7. Roles (según Matriz RACI — GOB-SGSI-04)

- **Gerencia General**: aprueba los objetivos y asigna recursos (Accountable).
- **CISO**: define, mide y reporta los KPIs (Responsable).
- **Áreas (TI, RRHH, Operaciones)**: ejecutan las acciones y reportan sus indicadores.

## 8. Documentos relacionados

- Política General de Seguridad (GOB-SGSI-02) · Revisión por la Dirección (GOB-SGSI-06)
- Plan de Tratamiento de Riesgos (ANR-SGSI-02) · No Conformidades (GOB-SGSI-07)

## 9. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial: objetivos medibles con metas y frecuencia (cierra la brecha G-12 del Gap Analysis). |
