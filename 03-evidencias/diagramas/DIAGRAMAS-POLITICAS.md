# Diagramas de políticas (mapa de política)

Mapa mínimo de cada política: alcance → reglas clave → punto de control → ¿cumple? → conforme / gestión de incumplimiento. PNG en `politicas/` (fuente SVG en `fuentes-svg/politicas/`).

### POL-SGSI-01 — Política de control de acceso
*ISO/IEC 27001:2022: 5.15–5.18, 8.2, 8.3, 8.5*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: accesos lógicos a sistemas, datos e infraestructura"]
    N2["Mínimo privilegio y necesidad de conocer; sin cuentas compartidas; MFA"]
    N3["Ciclo de vida del acceso y revisión periódica (PROC-06 / 07)"]
    N4{"¿Cumple en la auditoría de accesos?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Gerencia TI, jefaturas, RRHH  
**Evidencia / registros:** Tickets de acceso, logs, actas de revisión  
**Plazos / hitos:** Revisión semestral  
**PNG:** `politicas/POL-SGSI-01 - Política de control de acceso.png`

### POL-SGSI-02 — Política de gestión de contraseñas y autenticación
*ISO/IEC 27001:2022: 5.17, 8.5*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: autenticación a los sistemas y servicios de NovaRetail"]
    N2["Mínimo 12 caracteres, MFA obligatorio y bloqueo tras 5 intentos"]
    N3["Custodia en gestor corporativo; prohibido planillas; rotación (PROC-08)"]
    N4{"¿Cumple en la revisión de autenticación?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Gerencia TI, usuarios  
**Evidencia / registros:** Cobertura de MFA, logs del gestor  
**Plazos / hitos:** Rotación según política  
**PNG:** `politicas/POL-SGSI-02 - Política de gestión de contraseñas y autenticación.png`

### POL-SGSI-03 — Política de respaldo y recuperación
*ISO/IEC 27001:2022: 8.13, 8.14*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: la información crítica (clientes, ERP, inventario, configuraciones)"]
    N2["Estrategia 3-2-1 con copia offsite inmutable y cifrada"]
    N3["Pruebas de restauración y objetivos RTO/RPO (PROC-02 / 03)"]
    N4{"¿Prueba de restauración conforme?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Infraestructura TI, dueños de activos  
**Evidencia / registros:** Informe de respaldo y de restauración  
**Plazos / hitos:** Prueba trimestral  
**PNG:** `politicas/POL-SGSI-03 - Política de respaldo y recuperación.png`

### POL-SGSI-04 — Política de protección contra malware
*ISO/IEC 27001:2022: 8.7*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: endpoints, servidores y correo corporativo"]
    N2["EDR en el 100% de los equipos, actualización y escaneo periódico"]
    N3["Control de dispositivos USB y respuesta ante infección (PROC-16)"]
    N4{"¿Cobertura y configuración conformes?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** Gerencia TI, Analista de Ciberseguridad, CISO  
**Evidencia / registros:** Cobertura EDR, reportes de detección  
**Plazos / hitos:** Escaneo semanal  
**PNG:** `politicas/POL-SGSI-04 - Política de protección contra malware.png`

### POL-SGSI-05 — Política de gestión de parches y actualización
*ISO/IEC 27001:2022: 8.8, 8.19*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: SO, aplicaciones, firmware y agentes de seguridad"]
    N2["Ventana mensual, parches críticos ≤ 72 h y prueba en QA"]
    N3["Respaldo de configuración previo y despliegue controlado (PROC-01)"]
    N4{"¿Parches al día y dentro del SLA?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** Gerencia TI, CISO  
**Evidencia / registros:** Reporte de parches, tickets ITSM  
**Plazos / hitos:** Críticos ≤ 72 h  
**PNG:** `politicas/POL-SGSI-05 - Política de gestión de parches y actualización.png`

### POL-SGSI-06 — Política de uso seguro de dispositivos
*ISO/IEC 27001:2022: 6.7, 7.9, 8.1*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: estaciones, laptops y dispositivos móviles corporativos"]
    N2["Cifrado de disco, bloqueo automático y escritorio limpio"]
    N3["Solo software autorizado; reporte de pérdida o robo < 1 h (PROC-17)"]
    N4{"¿Uso conforme a la política?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** Gerencia TI, usuarios, jefatura  
**Evidencia / registros:** Acta de entrega, inventario de equipos  
**Plazos / hitos:** Reporte de pérdida < 1 h  
**PNG:** `politicas/POL-SGSI-06 - Política de uso seguro de dispositivos.png`

### POL-SGSI-07 — Política de seguridad de red
*ISO/IEC 27001:2022: 8.20–8.23*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: la red corporativa, el perímetro y los enlaces a la nube"]
    N2["Segmentación por VLAN y firewall con política 'denegar todo'"]
    N3["Red de invitados separada y monitoreo de tráfico (PROC-09)"]
    N4{"¿Reglas y segmentación conformes?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Infraestructura TI  
**Evidencia / registros:** Diagrama de red, informe de firewall  
**Plazos / hitos:** Revisión trimestral  
**PNG:** `politicas/POL-SGSI-07 - Política de seguridad de red.png`

### POL-SGSI-08 — Política de registro y monitoreo
*ISO/IEC 27001:2022: 8.15–8.17*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: los logs de sistemas, aplicaciones y seguridad"]
    N2["Registro de accesos exitosos/fallidos y centralización protegida"]
    N3["Retención de 90 días en caliente y sincronización NTP (PROC-10)"]
    N4{"¿Cobertura de logs conforme?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** Gerencia TI, Analista SOC, CISO  
**Evidencia / registros:** Logs centralizados, registro de alertas  
**Plazos / hitos:** Revisión diaria  
**PNG:** `politicas/POL-SGSI-08 - Política de registro y monitoreo.png`

### POL-SGSI-09 — Política de gestión de vulnerabilidades
*ISO/IEC 27001:2022: 8.8, 8.29*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: los activos tecnológicos en producción"]
    N2["Escaneo mensual y priorización por puntuación CVSS"]
    N3["Remediación por SLA (15/30/60 d) y pentest anual (PROC-11)"]
    N4{"¿Remediación dentro del SLA?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Gerencia TI, Desarrollo  
**Evidencia / registros:** Reportes de escaneo, tickets  
**Plazos / hitos:** Críticas ≤ 15 días  
**PNG:** `politicas/POL-SGSI-09 - Política de gestión de vulnerabilidades.png`

### POL-SGSI-10 — Política de manejo de información y clasificación
*ISO/IEC 27001:2022: 5.12–5.14, 8.10–8.12, 8.33*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: toda la información en cualquier formato y ciclo de vida"]
    N2["Cuatro niveles: Pública, Interna, Confidencial y Secreta"]
    N3["Cifrado en envíos, datos de prueba enmascarados y borrado seguro (PROC-12)"]
    N4{"¿Manejo conforme a la clasificación?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** Dueños de información, CISO, DPO  
**Evidencia / registros:** Etiquetado, registro de eliminación  
**Plazos / hitos:** Revisión anual  
**PNG:** `politicas/POL-SGSI-10 - Política de manejo de información y clasificación.png`

### POL-SGSI-11 — Política de gestión de incidentes y reporte ANCI
*ISO/IEC 27001:2022: 5.24–5.28*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: detección y gestión de incidentes de ciberseguridad"]
    N2["Clasificación N1 / N2 / N3 y activación del ERI"]
    N3["Notificación a la ANCI: 3 h / 72 h / 15 días (PROC-05)"]
    N4{"¿Plazos y reportes cumplidos?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Escalada y registro de no conformidad"]
    N4 -->|No| S0
    classDef crit fill:#FBE2D5,stroke:#C00000,color:#C00000,font-weight:bold;
    class N3 crit;
```

**Roles (RACI):** CISO, ERI, Gerencia, Legal  
**Evidencia / registros:** Ticket, reportes ANCI, informe post-incidente  
**Plazos / hitos:** 3 h / 72 h / 15 días  
**PNG:** `politicas/POL-SGSI-11 - Política de gestión de incidentes y reporte ANCI.png`

### POL-SGSI-12 — Política de cifrado de datos
*ISO/IEC 27001:2022: 8.24*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: la información Confidencial/Secreta en tránsito y reposo"]
    N2["TLS 1.2 o superior en tránsito; cifrado de BD, discos y backups"]
    N3["Gestión del ciclo de vida de las llaves criptográficas (PROC-18)"]
    N4{"¿Cifrado y llaves conformes?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Gerencia TI, DBA  
**Evidencia / registros:** Configuración TLS, inventario de llaves  
**Plazos / hitos:** Rotación periódica  
**PNG:** `politicas/POL-SGSI-12 - Política de cifrado de datos.png`

### POL-SGSI-13 — Política de gestión de proveedores y terceros (OIV)
*ISO/IEC 27001:2022: 5.19–5.23*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: proveedores y terceros con acceso o servicios críticos"]
    N2["Clasificación por criticidad y due diligence (énfasis OIV)"]
    N3["Cláusulas de seguridad, SLA y auditoría periódica (PROC-14)"]
    N4{"¿El proveedor cumple los requisitos?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Adquisiciones, Legal  
**Evidencia / registros:** Due diligence, contrato, informe de auditoría  
**Plazos / hitos:** Auditoría anual  
**PNG:** `politicas/POL-SGSI-13 - Política de gestión de proveedores y terceros (OIV).png`

### POL-SGSI-14 — Política de contratación y desvinculación
*ISO/IEC 27001:2022: 6.1, 6.2, 6.4–6.6*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: el ciclo de vida laboral (ingreso, cambios y término)"]
    N2["Pre-empleo: verificación y cláusulas de confidencialidad / NDA"]
    N3["Onboarding y offboarding seguros; confidencialidad post-empleo (PROC-13)"]
    N4{"¿Controles de personal aplicados?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** RRHH, CISO, jefatura, Legal  
**Evidencia / registros:** Checklist on/offboarding, contrato firmado  
**Plazos / hitos:** Baja el mismo día  
**PNG:** `politicas/POL-SGSI-14 - Política de contratación y desvinculación.png`

### POL-SGSI-15 — Política de línea base de software
*ISO/IEC 27001:2022: 8.9, 8.19*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alcance: los sistemas y el software gestionados por TI"]
    N2["SO aprobados e Inventario de Software Autorizado (ISA)"]
    N3["Hardening (CIS) con Ansible, EDR y gestión de licencias (PROC-04)"]
    N4{"¿Cumple la línea base?"}
    N5(["Conforme · evidencia registrada"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Gestión de incumplimiento (medidas disciplinarias / POL-11)"]
    N4 -->|No| S0
```

**Roles (RACI):** CISO, Gerencia TI  
**Evidencia / registros:** ISA, reportes de cumplimiento, registro de licencias  
**Plazos / hitos:** Auditoría semestral  
**PNG:** `politicas/POL-SGSI-15 - Política de línea base de software.png`
