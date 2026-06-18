# Diagramas swimlane (carriles por rol) — procedimientos transversales

Versión BPMN con carriles por actor (RACI) de los procedimientos con más de un responsable. PNG en `swimlanes/` (fuente SVG en `fuentes-svg/swimlanes/`); abajo la versión Mermaid (subgraph por carril) que se renderiza en GitHub.

### PROC-SGSI-05 — Gestión de incidentes y notificación ANCI
*ISO/IEC 27001:2022: 5.24–5.26 · carriles: Usuario / Monitoreo · Analista ERI · CISO · Gerencia / Legal*

```mermaid
flowchart TD
  subgraph L0["Usuario / Monitoreo"]
    N0(["Detección del evento"])
  end
  subgraph L1["Analista ERI"]
    N1["Registro y triage (SIEM / ticket)"]
    N2{"¿N3 o servicio esencial?"}
    N4["Contención y preservación de evidencia"]
    N6["Erradicación y recuperación (PROC-02/03)"]
  end
  subgraph L2["CISO"]
    N3["Alerta temprana a ANCI ≤ 3 h"]
    N5["Actualización a ANCI ≤ 72 h (24 h OIV)"]
    N7["Informe final a ANCI ≤ 15 días"]
  end
  subgraph L3["Gerencia / Legal"]
    N8(["Cierre y lecciones aprendidas"])
  end
  N0 --> N1
  N1 --> N2
  N2 -->|Sí| N3
  S0["Gestión interna y cierre"]
  N2 -->|No| S0
  N3 --> N4
  N4 --> N5
  N5 --> N6
  N6 --> N7
  N7 --> N8
  classDef crit fill:#FBE2D5,stroke:#C00000,color:#C00000,font-weight:bold;
  class N3,N5,N7 crit;
```

**PNG:** `swimlanes/PROC-SGSI-05 - Gestión de incidentes y notificación ANCI (swimlane).png`

### PROC-SGSI-06 — Alta, modificación y baja de accesos
*ISO/IEC 27001:2022: 5.16, 5.18, 8.2 · carriles: Solicitante / Jefatura · CISO · Gerencia TI · RRHH*

```mermaid
flowchart TD
  subgraph L0["Solicitante / Jefatura"]
    N0(["Solicitud de acceso (ticket ITSM)"])
  end
  subgraph L1["CISO"]
    N1{"¿Aprueba (jefatura + CISO si privilegiado)?"}
  end
  subgraph L2["Gerencia TI"]
    N2["Alta con mínimo privilegio + MFA"]
    N3["Modificación por cambio de rol (≤ 48 h)"]
    N5(["Baja de accesos el mismo día"])
  end
  subgraph L3["RRHH"]
    N4["RRHH notifica la desvinculación"]
  end
  N0 --> N1
  N1 -->|Sí| N2
  S0["Rechazar y registrar"]
  N1 -->|No| S0
  N2 --> N3
  N3 --> N4
  N4 --> N5
```

**PNG:** `swimlanes/PROC-SGSI-06 - Alta, modificación y baja de accesos (swimlane).png`

### PROC-SGSI-13 — Contratación y desvinculación
*ISO/IEC 27001:2022: 6.1, 6.2, 6.5 · carriles: RRHH · Jefatura · Gerencia TI · CISO*

```mermaid
flowchart TD
  subgraph L0["RRHH"]
    N0(["Pre-empleo: verificación + cláusulas / NDA"])
    N3["Capacitación anual y cambios de rol"]
    N4{"¿Término de la relación laboral?"}
  end
  subgraph L1["Jefatura"]
    N1["Aprueba el perfil y los accesos del cargo"]
  end
  subgraph L2["Gerencia TI"]
    N2["Onboarding: alta, MFA, gestor, equipo cifrado"]
    N6(["Offboarding: revocar accesos + devolución + borrado"])
  end
  subgraph L3["CISO"]
    N5["Revisión de logs si es despido por causa grave"]
  end
  N0 --> N1
  N1 --> N2
  N2 --> N3
  N3 --> N4
  N4 -->|Sí| N5
  S0["Continúa en operación"]
  N4 -->|No| S0
  N5 --> N6
```

**PNG:** `swimlanes/PROC-SGSI-13 - Contratación y desvinculación (swimlane).png`

### PROC-SGSI-14 — Evaluación de proveedores
*ISO/IEC 27001:2022: 5.19–5.22 · carriles: Adquisiciones · CISO · Legal · Gerencia TI*

```mermaid
flowchart TD
  subgraph L0["Adquisiciones"]
    N0(["Identificar y clasificar proveedor"])
    N6(["Baja: revocar accesos + eliminación de datos"])
  end
  subgraph L1["CISO"]
    N1{"¿Crítico u OIV?"}
    N2["Due diligence (cuestionario, certificaciones)"]
    N5["Auditoría anual del proveedor"]
  end
  subgraph L2["Legal"]
    N3["Cláusulas OIV + SLA + derecho de auditoría"]
  end
  subgraph L3["Gerencia TI"]
    N4["Accesos del proveedor con MFA + monitoreo"]
  end
  N0 --> N1
  N1 -->|Sí| N2
  S0["NDA + cláusulas estándar"]
  N1 -->|No| S0
  N2 --> N3
  N3 --> N4
  N4 --> N5
  N5 --> N6
```

**PNG:** `swimlanes/PROC-SGSI-14 - Evaluación de proveedores (swimlane).png`
