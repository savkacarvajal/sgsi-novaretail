# Plan de Continuidad del Negocio (BCP/DRP) — NovaRetail SpA

> ISO/IEC 27001:2022 — Controles Anexo A 5.29 «Seguridad de la información durante la disrupción» y 5.30 «Preparación de las TIC para la continuidad del negocio» · apoyo en 8.13/8.14
> NIST CSF 2.0 — Función **RECOVER (RC.RP, RC.CO)** y **PROTECT (PR.IR)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-08 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Gerencia General |

## 2. Propósito

Asegurar que NovaRetail SpA pueda **mantener o restaurar oportunamente** sus procesos críticos y la seguridad de la información ante una disrupción (ciberataque, falla de infraestructura o indisponibilidad de un proveedor crítico), definiendo el **Plan de Continuidad del Negocio (BCP)** y el **Plan de Recuperación ante Desastres (DRP)** de las TIC.

## 3. Alcance

Procesos críticos del alcance del SGSI (GOB-SGSI-01): **venta e-commerce, procesamiento de pagos, gestión de inventario/ERP y soporte a clientes**, y los activos que los soportan (ACT-1 a ACT-15).

## 4. Análisis de impacto al negocio (BIA) y objetivos de recuperación

> **RTO** (Recovery Time Objective): tiempo máximo tolerable de indisponibilidad.
> **RPO** (Recovery Point Objective): pérdida máxima tolerable de datos.

| Proceso / Activo | Criticidad | RTO objetivo | RPO objetivo | Estrategia de recuperación |
|---|---|---|---|---|
| Pasarela de pagos (ACT-3) | Crítica | 1 h | ~0 | Tercero (Transbank/Webpay) + conmutación a medio de pago alterno |
| Portal e-commerce (ACT-1) | Crítica | 4 h | 1 h | Redespliegue desde imagen + WAF/anti-DDoS |
| Base de datos de clientes (ACT-2) | Crítica | 4 h | 1 h | Restauración desde backup inmutable + replicación |
| ERP / pedidos (ACT-10) | Crítica | 8 h | 4 h | Replicación de BD; operación manual transitoria |
| Correo corporativo (ACT-13) | Alta | 8 h | 4 h | Servicio en la nube (M365 / Workspace) |
| BD de inventario (ACT-9) | Alta | 24 h | 12 h | Restauración desde backup |

## 5. Estrategia de continuidad (cl. A.5.29)

- **Roles de crisis**: la Gerencia General activa el plan; el CISO coordina la respuesta técnica y de seguridad; las jefaturas mantienen los procesos en modo contingencia.
- **Modo degradado**: procedimientos manuales transitorios para ventas y despacho mientras se recuperan los sistemas.
- **Comunicación**: protocolo de comunicación interna y a partes interesadas (clientes, ANCI cuando aplique según PROC-SGSI-05, marcas de tarjetas).
- **Seguridad durante la disrupción**: los controles esenciales (accesos, cifrado, registro) se mantienen incluso en operación de contingencia.

## 6. Recuperación ante desastres de TIC (DRP, cl. A.5.30)

1. **Detección y declaración** del desastre por el CISO/Gerencia TI.
2. **Contención** (si hay incidente de seguridad asociado, se enlaza con PROC-SGSI-05).
3. **Restauración** desde respaldos **3-2-1 inmutables y offsite** (POL-SGSI-03 · PROC-SGSI-02), con verificación de integridad antes de reconectar.
4. **Conmutación / replicación** de los servicios con redundancia (control A.8.14).
5. **Validación funcional y de seguridad** previa a la vuelta a producción.
6. **Vuelta a la normalidad** y registro de lecciones aprendidas.

## 7. Escenarios considerados

| Escenario | Riesgo asociado | Respuesta principal |
|---|---|---|
| Ransomware que cifra datos/respaldos | R-02, R-11 | Aislar, restaurar desde copia inmutable offsite, no pagar rescate |
| Caída prolongada del ERP/portal | R-10 | Conmutar a réplica; operación manual transitoria |
| Indisponibilidad de proveedor crítico (pago/logística) | R-03, R-08 | Activar proveedor o canal alterno; cláusulas de SLA |
| Pérdida de sede o datacenter | R-10, R-11 | Operar desde servicios en la nube y respaldos offsite |

## 8. Pruebas y mantenimiento (cl. A.5.30)

- **Prueba de restauración de respaldos**: trimestral (alineada al objetivo O-4 — GOB-SGSI-09).
- **Ejercicio de continuidad (tabletop o simulacro)**: al menos **anual**.
- El plan se actualiza tras cada prueba, incidente mayor o cambio relevante de infraestructura.

## 9. Roles (según Matriz RACI — GOB-SGSI-04)

- **Gerencia General**: activa el plan y rinde cuentas (Accountable).
- **CISO**: coordina la respuesta y mantiene el plan (Responsable).
- **Infraestructura TI**: ejecuta la recuperación técnica.
- **Jefaturas de proceso**: sostienen la operación en modo contingencia.

## 10. Registros y evidencias (cl. 7.5)

Resultados de pruebas de restauración, actas de ejercicios, registros de activación e informes de lecciones aprendidas se archivan en `03-evidencias/`.

## 11. Documentos relacionados

- Política de respaldo y recuperación (POL-SGSI-03) · Procedimientos de backup y rollback (PROC-SGSI-02 / 03)
- Gestión de incidentes y reporte ANCI (POL-SGSI-11 · PROC-SGSI-05)
- Plan de Tratamiento de Riesgos (ANR-SGSI-02) — R-10, R-11

## 12. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial (cierra la brecha G-7 del Gap Analysis). |
