# Metodología de Evaluación y Tratamiento de Riesgos — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 6.1.2 «Evaluación de riesgos de seguridad de la información» y 6.1.3 «Tratamiento de riesgos»
> NIST CSF 2.0 — Función **GOVERN (GV.RM — Risk Management Strategy)** e **IDENTIFY (ID.RA — Risk Assessment)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | ANR-SGSI-01 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Comité SGSI |

## 2. Propósito

Definir el método consistente y repetible con que NovaRetail SpA **identifica, analiza, evalúa, trata y acepta** los riesgos de seguridad de la información, dando cumplimiento a las cláusulas 6.1.2 y 6.1.3 de ISO/IEC 27001:2022. Esta metodología es la base del **Inventario de Activos**, la **Matriz de Evaluación de Riesgos (R-01 a R-17)**, la **Declaración de Aplicabilidad (SoA)** y el **Plan de Tratamiento de Riesgos (ANR-SGSI-02)**.

## 3. Alcance

Aplica a todos los activos de información dentro del alcance del SGSI (GOB-SGSI-01): procesos de venta presencial y e-commerce, procesamiento de pagos, gestión de inventario y logística, y soporte a clientes, en las sedes de Santiago y la operación regional, más los servicios en la nube.

## 4. Proceso de gestión de riesgos

```
1. Identificar activos        → Inventario de Activos (ACT-1..15)
2. Identificar amenazas/vuln. → por activo
3. Estimar impacto y prob.    → escala 1–5
4. Calcular nivel de riesgo   → Impacto × Probabilidad (1–25)
5. Evaluar y priorizar        → contra criterios de aceptación
6. Tratar el riesgo           → mitigar / transferir / evitar / aceptar
7. Seleccionar controles      → SoA (Anexo A)
8. Estimar riesgo residual    → reevaluar tras controles
9. Aceptar el riesgo residual → autoridad según nivel
10. Monitorear y revisar      → mínimo anual o ante cambios
```

## 5. Identificación y valoración de activos

Cada activo se registra en el **Inventario de Activos** con: propietario, proceso asociado, ubicación, **clasificación** (Pública, Interna, Confidencial, Secreta) y **criticidad** (Baja, Media, Alta, Crítica), junto con sus amenazas, vulnerabilidades y controles actuales. La criticidad orienta la prioridad de tratamiento.

## 6. Criterios de impacto (1–5)

| Valor | Nivel | Confidencialidad / Integridad / Disponibilidad | Referencia legal / financiera / reputacional |
|---|---|---|---|
| 1 | Insignificante | Sin afectación apreciable | Sin impacto |
| 2 | Menor | Afectación interna leve y recuperable | Molestia operativa; sin obligación de reporte |
| 3 | Moderado | Interrupción acotada o exposición de datos internos | Reclamo de clientes; costo operativo medio |
| 4 | Mayor | Exposición de datos personales o de pago; caída de servicio relevante | Notificación a la ANCI / sanción Ley 19.628; pérdida financiera significativa |
| 5 | Crítico | Brecha masiva de datos de clientes/tarjetas o caída prolongada del negocio | Sanción mayor, daño reputacional grave, incumplimiento PCI DSS / Ley 21.663 |

## 7. Criterios de probabilidad (1–5)

| Valor | Nivel | Criterio |
|---|---|---|
| 1 | Rara | Improbable; no se ha observado en el sector |
| 2 | Poco probable | Podría ocurrir excepcionalmente |
| 3 | Posible | Ha ocurrido en organizaciones similares |
| 4 | Probable | Esperable en el horizonte de un año dada la exposición actual |
| 5 | Casi certera | Ocurre o se intenta de forma recurrente |

## 8. Cálculo y niveles de riesgo

**Nivel de riesgo = Impacto × Probabilidad** → escala **1 a 25**.

| Nivel | Rango | Color | Criterio de tratamiento |
|---|---|---|---|
| Crítico | ≥ 15 | 🔴 | Tratamiento inmediato |
| Alto | 10–14 | 🟠 | Tratamiento planificado |
| Moderado | 5–9 | 🟢 | Tratamiento o aceptación con justificación |
| Bajo | 1–4 | 🟢 | Monitoreo / aceptación |

### Mapa de calor (5×5)

| P \ I | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| **5** | 5 | 10 | 15 | 20 | 25 |
| **4** | 4 | 8 | 12 | 16 | 20 |
| **3** | 3 | 6 | 9 | 12 | 15 |
| **2** | 2 | 4 | 6 | 8 | 10 |
| **1** | 1 | 2 | 3 | 4 | 5 |

## 9. Opciones de tratamiento (cl. 6.1.3)

| Opción | Cuándo se aplica |
|---|---|
| **Mitigar** | Reducir el riesgo mediante controles del Anexo A (opción por defecto). |
| **Transferir** | Trasladar parte del riesgo a un tercero (seguro, proveedor, pasarela de pago). |
| **Evitar** | Eliminar la actividad o el activo que origina el riesgo. |
| **Aceptar** | Asumir el riesgo de forma consciente cuando está dentro de los criterios de aceptación. |

Los controles seleccionados para mitigar se registran en la **Declaración de Aplicabilidad (SoA)**, con su justificación de aplicabilidad o exclusión (cl. 6.1.3.d).

## 10. Criterios de aceptación del riesgo (cl. 6.1.2.a)

| Nivel residual | ¿Aceptable? | Autoridad que aprueba la aceptación |
|---|---|---|
| Crítico (≥ 15) | No | Debe reducirse; la aceptación excepcional la aprueba la **Gerencia General** por escrito |
| Alto (10–14) | Solo excepcional y temporal | **Gerencia General** (a propuesta del CISO) |
| Moderado (5–9) | Sí, con justificación | **CISO** / dueño del activo |
| Bajo (1–4) | Sí | **Dueño del activo**; monitoreo periódico |

- El objetivo de tratamiento es llevar todo riesgo **Crítico** a nivel **Alto o inferior**, y todo **Alto** a **Moderado o inferior**.
- Toda aceptación de riesgo residual queda registrada (responsable, fecha y fundamento) como evidencia (`03-evidencias/`).

## 11. Roles (según Matriz RACI — GOB-SGSI-04)

- **Gerencia General**: aprueba la metodología y los criterios; acepta los riesgos residuales Crítico/Alto (Accountable).
- **CISO**: ejecuta y mantiene la evaluación de riesgos, propone tratamientos y el SoA (Responsable).
- **Comité SGSI**: revisa y prioriza.
- **Dueños de activos / Jefaturas**: aportan información y ejecutan los tratamientos en su ámbito.

## 12. Frecuencia de revisión

La evaluación de riesgos se revisa **al menos una vez al año** y ante cambios significativos (nuevos sistemas o procesos, incidentes relevantes, cambios regulatorios o de alcance). Los resultados alimentan la **Revisión por la Dirección (GOB-SGSI-06)**.

## 13. Documentos relacionados

- Inventario de Activos, Matriz de Evaluación de Riesgos y SoA (`04-analisis/`)
- Plan de Tratamiento de Riesgos (ANR-SGSI-02)
- Política General de Seguridad (GOB-SGSI-02) · Objetivos de Seguridad (GOB-SGSI-09)

## 14. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial: formaliza la metodología implícita en el SoA y los criterios de aceptación del riesgo. |
