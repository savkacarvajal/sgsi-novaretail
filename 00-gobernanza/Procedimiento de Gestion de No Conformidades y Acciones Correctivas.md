# Procedimiento de Gestión de No Conformidades y Acciones Correctivas — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 10.1 «Mejora continua» y 10.2 «No conformidad y acción correctiva»
> NIST CSF 2.0 — Función **IMPROVE (ID.IM)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-07 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Comité SGSI |

## 2. Propósito

Establecer cómo NovaRetail SpA identifica, registra y trata las **no conformidades** del SGSI mediante **acciones correctivas**, y cómo impulsa la **mejora continua**, conforme a las cláusulas 10.1 y 10.2 de ISO/IEC 27001:2022.

## 3. Definiciones

- **No conformidad (NC)**: incumplimiento de un requisito (de la norma, de una política/procedimiento propio o de un requisito legal/contractual).
- **Corrección**: acción inmediata para eliminar la NC detectada.
- **Acción correctiva**: acción para eliminar la **causa raíz** y evitar que la NC vuelva a ocurrir.
- **Oportunidad de mejora**: cambio que aumenta la eficacia del SGSI sin originarse en una NC.

## 4. Fuentes de no conformidades

Auditorías internas (GOB-SGSI-05), incidentes de seguridad (PROC-SGSI-05), resultados de monitoreo y KPIs (GOB-SGSI-09), revisiones por la dirección (GOB-SGSI-06), reclamos de partes interesadas y hallazgos de cumplimiento legal/PCI.

## 5. Proceso (cl. 10.2)

1. **Detección y registro** de la NC en el **Registro de No Conformidades** (ver sección 7), con descripción, origen, fecha y responsable.
2. **Reacción inmediata**: aplicar la corrección y controlar/contener las consecuencias.
3. **Evaluación de la necesidad de acción correctiva**: ¿requiere eliminar la causa para que no se repita?
4. **Análisis de causa raíz** (p. ej. «5 porqués» o Ishikawa); revisar si NC similares existen o podrían ocurrir en otros procesos.
5. **Plan de acción correctiva**: acciones, responsable y plazo.
6. **Implementación** de las acciones.
7. **Verificación de la eficacia**: confirmar que la causa fue eliminada y la NC no reincide.
8. **Actualización del SGSI** si corresponde: ajustar riesgos (ANR-SGSI-02), políticas, procedimientos o el SoA.
9. **Cierre** de la NC, dejando registro de la evidencia.

```
NC detectada → corrección inmediata → ¿acción correctiva?
   └─ sí → causa raíz → plan → implementación → verificación de eficacia → cierre
   └─ no → corrección + registro → cierre
```

## 6. Clasificación y plazos sugeridos

| Severidad | Criterio | Plazo objetivo de cierre |
|---|---|---|
| Mayor | Falla sistémica o incumplimiento legal/PCI | ≤ 30 días |
| Menor | Desviación puntual | ≤ 60 días |
| Observación / mejora | Sin incumplimiento | Según planificación |

## 7. Registro de No Conformidades

Se mantiene un registro (planilla o sistema) con, al menos: ID, fecha, origen, descripción, severidad, corrección, causa raíz, acción correctiva, responsable, plazo, verificación de eficacia y estado (Abierta / En curso / Cerrada). Se archiva en `03-evidencias/`.

## 8. Mejora continua (cl. 10.1)

La organización mejora de forma continua la conveniencia, adecuación y eficacia del SGSI usando: la política y los objetivos de seguridad, los resultados de auditoría, el análisis de datos (KPIs), las acciones correctivas y las salidas de la revisión por la dirección.

## 9. Roles (según Matriz RACI — GOB-SGSI-04)

- **CISO**: gestiona el registro y coordina las acciones correctivas (Responsable).
- **Comité SGSI**: supervisa la mejora continua (Accountable).
- **Dueños de procesos**: ejecutan correcciones y acciones correctivas en su ámbito.

## 10. Documentos relacionados

- Auditoría Interna (GOB-SGSI-05) · Revisión por la Dirección (GOB-SGSI-06)
- Gestión de incidentes y reporte ANCI (POL-SGSI-11 · PROC-SGSI-05)

## 11. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial (cierra la brecha G-6 del Gap Analysis). |
