# Diagramas de procedimientos (BPMN / flowchart)

Un diagrama por procedimiento del SGSI de NovaRetail SpA. Se renderizan en GitHub (Mermaid) y tienen su PNG en `procedimientos/` (fuente SVG en `fuentes-svg/procedimientos/`).

### PROC-SGSI-01 — Gestión de actualizaciones y parches
*ISO/IEC 27001:2022: 8.8, 8.19*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Identificar y clasificar parches (SO, apps, firmware)"]
    N2{"¿Parche crítico (SLA ≤ 72 h)?"}
    N3["Probar en QA y respaldar la configuración previa"]
    N4["Desplegar (Ansible para equipos masivos)"]
    N5["Verificar el resultado y registrar en ITSM"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Incluir en la ventana mensual"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** Gerencia TI  
**Evidencia / registros:** Ticket ITSM, reporte de parches  
**Plazos / hitos:** Críticos ≤ 72 h  
**PNG:** `procedimientos/PROC-SGSI-01 - Gestión de actualizaciones y parches.png`

### PROC-SGSI-02 — Backup de base de datos
*ISO/IEC 27001:2022: 8.13, 8.14*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Programar respaldos 3-2-1 (incremental diario / completo semanal)"]
    N2["Cifrar la copia de respaldo"]
    N3["Almacenar en 2 medios + 1 copia offsite inmutable"]
    N4{"¿Prueba de restauración trimestral exitosa?"}
    N5["Registrar evidencia y aplicar la retención"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Abrir incidente y corregir"]
    N4 -->|No| S0
    N5 --> N6
```

**Roles (RACI):** Gerencia TI / DBA  
**Evidencia / registros:** Informe de respaldo y de restauración  
**Plazos / hitos:** Prueba trimestral  
**PNG:** `procedimientos/PROC-SGSI-02 - Backup de base de datos.png`

### PROC-SGSI-03 — Rollback
*ISO/IEC 27001:2022: 8.13, 8.32*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Detectar falla tras un cambio o actualización"]
    N2{"¿Se decide ejecutar rollback?"}
    N3["Restaurar el último estado estable conocido (backup / imagen)"]
    N4["Validar integridad de datos y del servicio"]
    N5["Si la falla fue de seguridad, notificar al CISO (POL-11)"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Continuar análisis / aplicar hotfix"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** Gerencia TI / DBA  
**Evidencia / registros:** Registro de rollback, ticket de cambio  
**PNG:** `procedimientos/PROC-SGSI-03 - Rollback.png`

### PROC-SGSI-04 — Línea base de software (Ansible)
*ISO/IEC 27001:2022: 8.9, 8.19, 8.32*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Definir la línea base (CIS Benchmarks) y el playbook"]
    N2["Aplicar la línea base con Ansible a los nodos"]
    N3{"¿Los nodos cumplen la línea base?"}
    N4["Registrar el cumplimiento (auditoría mensual)"]
    N5(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 -->|Sí| N4
    S0["Remediar y volver a aplicar"]
    N3 -->|No| S0
    N4 --> N5
```

**Roles (RACI):** Gerencia TI  
**Evidencia / registros:** Salida de Ansible, reporte de cumplimiento  
**Plazos / hitos:** Auditoría mensual  
**PNG:** `procedimientos/PROC-SGSI-04 - Línea base de software (Ansible).png`

### PROC-SGSI-05 — Gestión de incidentes y notificación ANCI
*ISO/IEC 27001:2022: 5.24, 5.25, 5.26*

```mermaid
flowchart TD
    N0(["Detección del evento"])
    N1["Registro y triage (SIEM / ticket)"]
    N2{"¿Incidente N3 o afecta un servicio esencial?"}
    N3["Alerta temprana a ANCI ≤ 3 horas"]
    N4["Contención y preservación de evidencia"]
    N5["Actualización a ANCI ≤ 72 h (24 h si OIV)"]
    N6["Erradicación y recuperación (PROC-02 / 03)"]
    N7["Informe final a ANCI ≤ 15 días corridos"]
    N8["Cierre y lecciones aprendidas"]
    N9(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Gestión interna y registro (cierre)"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
    N6 --> N7
    N7 --> N8
    N8 --> N9
    classDef crit fill:#FBE2D5,stroke:#C00000,color:#C00000,font-weight:bold;
    class N3,N5,N7 crit;
```

**Roles (RACI):** CISO, ERI, Gerencia TI, Legal  
**Evidencia / registros:** Ticket, cadena de custodia, reportes ANCI  
**Plazos / hitos:** 3 h / 72 h / 15 días  
**PNG:** `procedimientos/PROC-SGSI-05 - Gestión de incidentes y notificación ANCI.png`

### PROC-SGSI-06 — Alta, modificación y baja de accesos
*ISO/IEC 27001:2022: 5.16, 5.18, 8.2*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Solicitud de acceso mediante ticket ITSM"]
    N2{"¿Aprueba la jefatura (y el CISO si es privilegiado)?"}
    N3["Alta con mínimo privilegio y MFA"]
    N4["Modificar accesos ante cambio de rol (≤ 48 h)"]
    N5["Baja de todos los accesos el día de la desvinculación"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Rechazar y registrar"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** Gerencia TI, RRHH, jefatura  
**Evidencia / registros:** Ticket aprobado, logs de acceso  
**Plazos / hitos:** Baja el mismo día  
**PNG:** `procedimientos/PROC-SGSI-06 - Alta, modificación y baja de accesos.png`

### PROC-SGSI-07 — Revisión periódica de accesos
*ISO/IEC 27001:2022: 5.18*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Ciclo semestral: el CISO envía el formulario FVA-02"]
    N2["Las jefaturas validan los accesos de su equipo (10 días)"]
    N3{"¿El acceso sigue siendo necesario?"}
    N4["Consolidar el informe y presentarlo al Comité SGSI"]
    N5(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 -->|Sí| N4
    S0["Revocar el acceso"]
    N3 -->|No| S0
    N4 --> N5
```

**Roles (RACI):** CISO, jefaturas  
**Evidencia / registros:** Formulario FVA-02, informe  
**Plazos / hitos:** Semestral  
**PNG:** `procedimientos/PROC-SGSI-07 - Revisión periódica de accesos.png`

### PROC-SGSI-08 — Uso del gestor de contraseñas
*ISO/IEC 27001:2022: 5.17, 8.5*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Alta del usuario en el gestor (Bitwarden) con MFA"]
    N2["Guardar toda credencial en el gestor (nunca en planillas)"]
    N3["Compartir credenciales por bóvedas de equipo"]
    N4["Rotar según política o ante sospecha"]
    N5["Baja: revocar acceso y rotar credenciales críticas"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** CISO, Gerencia TI, usuarios  
**Evidencia / registros:** Logs de bóvedas, registro de rotación  
**PNG:** `procedimientos/PROC-SGSI-08 - Uso del gestor de contraseñas.png`

### PROC-SGSI-09 — Segmentación y revisión de firewall
*ISO/IEC 27001:2022: 8.20, 8.22*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Solicitud de regla mediante formulario FSR-03"]
    N2{"¿El CISO aprueba (regla mínima necesaria)?"}
    N3["Implementar con comentario (ticket, fecha, responsable)"]
    N4["Revisión trimestral: eliminar reglas obsoletas o 'any-any'"]
    N5["Documentar el informe trimestral de firewall"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Rechazar o proponer alternativa"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** CISO, Infraestructura TI  
**Evidencia / registros:** Formulario FSR-03, informe trimestral  
**Plazos / hitos:** Revisión trimestral  
**PNG:** `procedimientos/PROC-SGSI-09 - Segmentación y revisión de firewall.png`

### PROC-SGSI-10 — Revisión y escalada de alertas
*ISO/IEC 27001:2022: 8.15, 8.16*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Revisión diaria de logs y alertas (SIEM / EDR / firewall)"]
    N2["Clasificar la alerta por prioridad"]
    N3{"¿Es un incidente de seguridad?"}
    N4["Escalar al Equipo de Respuesta a Incidentes (PROC-05)"]
    N5(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 -->|Sí| N4
    S0["Registrar y cerrar"]
    N3 -->|No| S0
    N4 --> N5
```

**Roles (RACI):** Analista SOC, CISO  
**Evidencia / registros:** Registro de alertas, ticket de escalada  
**Plazos / hitos:** Revisión diaria  
**PNG:** `procedimientos/PROC-SGSI-10 - Revisión y escalada de alertas.png`

### PROC-SGSI-11 — Escaneo de vulnerabilidades
*ISO/IEC 27001:2022: 8.8, 8.29*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Escaneo mensual (servidores, aplicaciones web, red)"]
    N2["Priorizar por puntuación CVSS y criticidad"]
    N3["Crear un ticket por hallazgo (responsable y plazo)"]
    N4{"¿Remediado dentro del SLA (15/30/60 días)?"}
    N5["Re-escanear, cerrar y emitir el informe mensual"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Escalar o control compensatorio (aprueba CISO)"]
    N4 -->|No| S0
    N5 --> N6
```

**Roles (RACI):** CISO, Gerencia TI, Desarrollo  
**Evidencia / registros:** Reporte de escaneo, tickets de remediación  
**Plazos / hitos:** Mensual; SLA 15/30/60 d  
**PNG:** `procedimientos/PROC-SGSI-11 - Escaneo de vulnerabilidades.png`

### PROC-SGSI-12 — Retención y eliminación segura
*ISO/IEC 27001:2022: 8.10, 8.13, 8.33*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Clasificar la información y definir su período de retención"]
    N2{"¿Cumplió su ciclo de vida?"}
    N3["Eliminación segura (borrado certificado o destrucción física)"]
    N4["Registrar la evidencia de eliminación"]
    N5(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Conservar según la retención"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
```

**Roles (RACI):** Gerencia TI, DPO  
**Evidencia / registros:** Registro de eliminación, certificado de borrado  
**Plazos / hitos:** Revisión anual  
**PNG:** `procedimientos/PROC-SGSI-12 - Retención y eliminación segura.png`

### PROC-SGSI-13 — Contratación y desvinculación
*ISO/IEC 27001:2022: 6.1, 6.2, 6.5*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Pre-empleo: verificación de antecedentes + cláusulas / NDA"]
    N2["Onboarding: firma de políticas, MFA, gestor y equipo cifrado"]
    N3["Durante el empleo: capacitación anual y cambios de rol"]
    N4["Offboarding: revocar accesos el mismo día + devolución + borrado"]
    N5(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
```

**Roles (RACI):** RRHH, Gerencia TI, jefatura  
**Evidencia / registros:** Checklist on/offboarding firmado  
**Plazos / hitos:** Baja el mismo día  
**PNG:** `procedimientos/PROC-SGSI-13 - Contratación y desvinculación.png`

### PROC-SGSI-14 — Evaluación de proveedores
*ISO/IEC 27001:2022: 5.19, 5.20, 5.21, 5.22*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Clasificar al proveedor por criticidad (Crítico / Alto / Estándar)"]
    N2{"¿Es proveedor crítico u OIV?"}
    N3["Due diligence + cláusulas OIV + auditoría anual"]
    N4["Monitorear los accesos y el SLA de seguridad"]
    N5["Baja: revocar accesos y exigir eliminación de datos"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 -->|Sí| N3
    S0["Acuerdo de confidencialidad y cláusulas estándar"]
    N2 -->|No| S0
    N3 --> N4
    N4 --> N5
    N5 --> N6
```

**Roles (RACI):** CISO, Adquisiciones  
**Evidencia / registros:** Due diligence, cláusulas, informe de auditoría  
**Plazos / hitos:** Auditoría anual  
**PNG:** `procedimientos/PROC-SGSI-14 - Evaluación de proveedores.png`

### PROC-SGSI-15 — Desarrollo seguro (SDLC)
*ISO/IEC 27001:2022: 8.25–8.29, 8.31*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Requisitos de seguridad desde el diseño (OWASP ASVS)"]
    N2["Diseño y arquitectura segura (modelado de amenazas)"]
    N3["Codificación segura (sin secretos en el código)"]
    N4["Pruebas SAST / DAST / SCA en el pipeline de CI"]
    N5{"¿Pasa las pruebas y el pentest?"}
    N6["Aprobación del CISO y paso a producción"]
    N7(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 -->|Sí| N6
    S0["Corregir los hallazgos antes de avanzar"]
    N5 -->|No| S0
    N6 --> N7
```

**Roles (RACI):** Jefe de Desarrollo, CISO  
**Evidencia / registros:** Reportes SAST/DAST, informe de pentest  
**Plazos / hitos:** Pentest en release mayor  
**PNG:** `procedimientos/PROC-SGSI-15 - Desarrollo seguro (SDLC).png`

### PROC-SGSI-16 — Respuesta ante malware
*ISO/IEC 27001:2022: 8.7*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Prevención: EDR en el 100% + control de USB y correo"]
    N2["Detección por EDR y revisión de alertas (PROC-10)"]
    N3["Contención: aislar el host y bloquear cuentas"]
    N4["Erradicación: limpiar o reimagen (PROC-04)"]
    N5["Recuperación desde un respaldo limpio (PROC-02)"]
    N6{"¿Es ransomware o afecta datos / servicios?"}
    N7["Activar PROC-05 (incidente y reporte ANCI)"]
    N8(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 --> N5
    N5 --> N6
    N6 -->|Sí| N7
    S0["Cierre y registro del evento"]
    N6 -->|No| S0
    N7 --> N8
    classDef crit fill:#FBE2D5,stroke:#C00000,color:#C00000,font-weight:bold;
    class N7 crit;
```

**Roles (RACI):** Analista de Ciberseguridad, CISO  
**Evidencia / registros:** Alertas EDR, informe post-evento  
**PNG:** `procedimientos/PROC-SGSI-16 - Respuesta ante malware.png`

### PROC-SGSI-17 — Uso seguro de dispositivos
*ISO/IEC 27001:2022: 8.1, 7.9, 6.7*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Entrega: cifrado de disco + EDR + MFA + línea base (PROC-04)"]
    N2["Uso seguro: bloqueo, escritorio limpio, software autorizado"]
    N3["Teletrabajo: acceso solo por VPN con MFA"]
    N4{"¿Pérdida o robo del dispositivo?"}
    N5["Reporte < 1 h + borrado remoto + revocar accesos (PROC-06)"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Devolución: borrado seguro (PROC-12)"]
    N4 -->|No| S0
    N5 --> N6
```

**Roles (RACI):** Gerencia TI, usuario, jefatura  
**Evidencia / registros:** Acta de entrega/devolución, reporte de pérdida  
**Plazos / hitos:** Reporte < 1 h  
**PNG:** `procedimientos/PROC-SGSI-17 - Uso seguro de dispositivos.png`

### PROC-SGSI-18 — Cifrado y gestión de llaves
*ISO/IEC 27001:2022: 8.24*

```mermaid
flowchart TD
    N0(["Inicio"])
    N1["Cifrado en tránsito (TLS 1.2 o superior)"]
    N2["Cifrado en reposo (BD de clientes, discos, respaldos)"]
    N3["Gestión de llaves en bóveda / HSM con mínimo privilegio"]
    N4{"¿Sospecha de compromiso de una llave?"}
    N5["Rotación / revocación inmediata + respaldo de llaves"]
    N6(["Fin"])
    N0 --> N1
    N1 --> N2
    N2 --> N3
    N3 --> N4
    N4 -->|Sí| N5
    S0["Rotación periódica programada"]
    N4 -->|No| S0
    N5 --> N6
```

**Roles (RACI):** CISO, Gerencia TI / DBA  
**Evidencia / registros:** Inventario de llaves, configuración TLS  
**Plazos / hitos:** Rotación periódica  
**PNG:** `procedimientos/PROC-SGSI-18 - Cifrado y gestión de llaves.png`
