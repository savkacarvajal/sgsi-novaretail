# Procedimiento de Auditoría Interna del SGSI — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 9.2 «Auditoría interna» · Controles Anexo A 5.35 (Revisión independiente) y 5.36 (Cumplimiento de políticas)
> NIST CSF 2.0 — Función **GOVERN (GV.OV — Oversight)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-05 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Comité SGSI |

## 2. Propósito

Establecer cómo NovaRetail SpA planifica y ejecuta auditorías internas para verificar que el SGSI **es conforme** con los requisitos de ISO/IEC 27001:2022, con los requisitos propios de la organización (PCI DSS v4.0, Ley 21.663, Ley 19.628), y que está **implementado y mantenido eficazmente**.

## 3. Alcance

Cubre todos los procesos, políticas (POL-SGSI-01 a 15), procedimientos (PROC-SGSI-01 a 14) y controles del SoA dentro del alcance del SGSI (GOB-SGSI-01).

## 4. Principios

- **Independencia y objetividad**: los auditores no auditan su propio trabajo ni el de su área directa.
- **Evidencia objetiva**: los hallazgos se sustentan en registros, entrevistas y observación.
- **Enfoque basado en riesgos**: se prioriza la auditoría de los procesos asociados a riesgos Crítico/Alto.

## 5. Programa anual de auditoría (cl. 9.2.2)

| Aspecto | Definición |
|---|---|
| Frecuencia | Al menos **una auditoría interna anual** del SGSI; los procesos críticos pueden auditarse con mayor frecuencia. |
| Responsable del programa | CISO (planifica); **Auditoría Interna** o tercero independiente (ejecuta). |
| Criterios | ISO/IEC 27001:2022, políticas y procedimientos del SGSI, requisitos legales y PCI DSS. |
| Aprobación | Comité SGSI. |

## 6. Etapas del proceso

1. **Planificación** — definir objetivo, alcance, criterios y calendario de la auditoría; designar al equipo auditor independiente.
2. **Preparación** — revisar documentación, auditorías previas y estado de riesgos; elaborar la lista de verificación.
3. **Ejecución** — reunión de apertura, recopilación de evidencia (entrevistas, registros, observación) y registro de hallazgos.
4. **Clasificación de hallazgos**:

   | Tipo | Descripción |
   |---|---|
   | Conformidad | Cumple el criterio auditado. |
   | No conformidad mayor | Ausencia o falla sistémica de un requisito. |
   | No conformidad menor | Desviación puntual que no compromete el sistema. |
   | Observación | Debilidad potencial que conviene atender. |
   | Oportunidad de mejora | Sugerencia que agrega valor sin ser un incumplimiento. |

5. **Informe de auditoría** — resultados, hallazgos clasificados y conclusiones; se entrega al CISO y al Comité SGSI.
6. **Tratamiento** — las no conformidades se derivan al **Procedimiento de No Conformidades y Acciones Correctivas (GOB-SGSI-07)**.
7. **Seguimiento** — verificación del cierre de las acciones en la siguiente auditoría o en un plazo definido.

## 7. Entradas a la Revisión por la Dirección

Los resultados de auditoría son una **entrada obligatoria** de la **Revisión por la Dirección (GOB-SGSI-06, cl. 9.3)**.

## 8. Roles (según Matriz RACI — GOB-SGSI-04)

- **Auditoría Interna**: ejecuta la auditoría (Responsable).
- **Comité SGSI**: aprueba el programa y recibe los resultados (Accountable).
- **CISO**: planifica, facilita y da seguimiento.
- **Dueños de procesos**: aportan evidencia y ejecutan las acciones correctivas.

## 9. Registros y evidencias (cl. 7.5 / 9.2)

Programa anual, plan de cada auditoría, listas de verificación, informe de auditoría y registros de seguimiento se archivan en `03-evidencias/` con su control de versión.

## 10. Documentos relacionados

- Revisión por la Dirección (GOB-SGSI-06) · No Conformidades y Acciones Correctivas (GOB-SGSI-07)
- Política General de Seguridad (GOB-SGSI-02) · Matriz RACI (GOB-SGSI-04)

## 11. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial (cierra la brecha G-4 del Gap Analysis). |
