# 📊 Análisis de Riesgos y Auditoría

Núcleo del sistema de gestión basado en riesgos (ISO/IEC 27001:2022 cap. 6 · NIST CSF 2.0 — ID.RA / GV.RM).

## Contenido

| Archivo | Descripción | Cláusula |
|---|---|---|
| [Análisis de Riesgos — Inventario, Matriz de Riesgos y SoA.xlsx](Analisis%20de%20Riesgos%20-%20Inventario%2C%20Matriz%20de%20Riesgos%20y%20SoA.xlsx) | Libro con 3 hojas: **Registro de Activos** (15), **Evaluación de Riesgo** (R-01 a R-17), **SoA** (controles tecnológicos 8.1–8.34). | 5.9, 6.1.2, 6.1.3.d |
| [Metodología de Evaluación y Tratamiento de Riesgos.docx](Metodologia%20de%20Evaluacion%20y%20Tratamiento%20de%20Riesgos.docx) | ANR-SGSI-01 — método, escalas de impacto/probabilidad y **criterios de aceptación del riesgo**. | 6.1.2 |
| [Plan de Tratamiento de Riesgos.docx](Plan%20de%20Tratamiento%20de%20Riesgos.docx) | ANR-SGSI-02 — tratamiento de R-01 a R-17 (controles, responsable, plazo y riesgo residual). | 6.1.3 |
| [Gap Analysis y Estado del SGSI.docx](Gap%20Analysis%20y%20Estado%20del%20SGSI.docx) | Análisis de brechas, estado de madurez y hoja de ruta de lo que falta. | 4–10 |

## Metodología de riesgo

**Nivel de riesgo = Impacto (1–5) × Probabilidad (1–5)** → escala 1–25.

| Nivel | Rango | Color | Criterio |
|---|---|---|---|
| Crítico | ≥ 15 | 🔴 | Tratamiento inmediato |
| Alto | 10–14 | 🟠 | Tratamiento planificado |
| Moderado/Bajo | < 10 | 🟢 | Monitoreo / aceptación |

El detalle de las escalas, el mapa de calor 5×5 y los **criterios de aceptación del riesgo** (quién acepta cada nivel residual) está en la **Metodología de Evaluación y Tratamiento de Riesgos (ANR-SGSI-01)**. El tratamiento concreto de cada riesgo está en el **Plan de Tratamiento de Riesgos (ANR-SGSI-02)**.

> Cada control del SoA enlaza a sus riesgos (R-0X) y cada activo a sus amenazas, manteniendo la trazabilidad **activo → riesgo → control → política**.
