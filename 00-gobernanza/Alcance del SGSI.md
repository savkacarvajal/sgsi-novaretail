# Declaración de Alcance del SGSI — NovaRetail SpA

> ISO/IEC 27001:2022 — Cláusula 4.3 «Determinación del alcance del sistema de gestión de la seguridad de la información»
> NIST CSF 2.0 — Función **GOVERN (GV.OC — Organizational Context)**

## 1. Control documental

| Campo | Valor |
|---|---|
| Código | GOB-SGSI-01 |
| Versión | 1.0 |
| Fecha de emisión | 17-06-2026 |
| Próxima revisión | 17-06-2027 |
| Clasificación | Interno |
| Elaborado por | Equipo SGSI — Thynk Unlimited |
| Revisado por | CISO |
| Aprobado por | Gerencia General |

## 2. Propósito

Definir los límites y la aplicabilidad del Sistema de Gestión de Seguridad de la Información (SGSI) de **NovaRetail SpA**, estableciendo qué procesos, activos, ubicaciones y tecnologías quedan cubiertos, en cumplimiento de la cláusula 4.3 de ISO/IEC 27001:2022.

## 3. Contexto de la organización (cl. 4.1)

NovaRetail SpA es una empresa chilena de **retail** con canal físico y **comercio electrónico**, que procesa **pagos con tarjeta** (alcance PCI DSS v4.0) y **datos personales** de clientes (Ley 19.628). Por su rol en la distribución de bienes esenciales, puede ser calificada como **Operador de Importancia Vital (OIV)** bajo la **Ley 21.663**, lo que la obliga a reportar incidentes a la **ANCI**.

### Cuestiones internas y externas relevantes

| Tipo | Cuestiones |
|---|---|
| Internas | Operación multi-sede (Santiago / La Serena), desarrollo propio del portal, equipo TI reducido, dependencia de proveedores críticos (pasarela de pago, logística). |
| Externas | Ley 21.663 y fiscalización ANCI, Ley 19.628 (datos personales), PCI DSS, amenazas de ransomware/phishing al retail, estacionalidad (CyberDay). |

## 4. Partes interesadas y requisitos (cl. 4.2)

| Parte interesada | Requisito principal |
|---|---|
| Clientes | Confidencialidad e integridad de sus datos personales y de pago |
| ANCI / Estado (Ley 21.663) | Notificación de incidentes (3 h / 72 h / 15 días) y gestión de riesgos |
| Marcas de tarjetas (PCI DSS) | Protección de datos de tarjetahabientes |
| Gerencia / Accionistas | Continuidad operacional y protección de la reputación |
| Empleados y contratistas | Reglas claras de uso y protección de la información |
| Proveedores críticos | Cláusulas de seguridad y niveles de servicio |

## 5. Alcance del SGSI (cl. 4.3)

El SGSI **aplica a** la protección de la confidencialidad, integridad y disponibilidad de la información asociada a los procesos de **venta presencial y e-commerce, procesamiento de pagos, gestión de inventario y logística, y soporte a clientes** de NovaRetail SpA.

### 5.1 Ubicaciones incluidas
- **Oficinas centrales — Santiago (Región Metropolitana)**: administración, finanzas, gobierno del SGSI y firma de contratos estratégicos.
- **Bodega y operación regional — La Serena (Región de Coquimbo)**: recepción, despacho, inventario y soporte operativo local.
- **Servicios en la nube**: Microsoft 365 / Google Workspace y la infraestructura IaaS del portal.

### 5.2 Procesos y activos incluidos
Portal e-commerce, ERP/gestión de pedidos, bases de datos de clientes e inventario, pasarela de pago (Transbank/Webpay), correo corporativo, red corporativa (LAN/Wi-Fi), firewall perimetral, respaldos, estaciones de trabajo y cuentas privilegiadas. *(Ver `04-analisis/` — Inventario de Activos.)*

### 5.3 Exclusiones y justificación
- **Infraestructura interna de la pasarela de pago**: gestionada por el proveedor externo (Transbank/Webpay); NovaRetail controla la **integración y las llaves API**, no la plataforma del tercero. La seguridad del proveedor se gobierna vía **POL-SGSI-13 / PROC-SGSI-14**.
- **Tiendas físicas de terceros / franquicias** (si aplica): fuera del control directo de NovaRetail.

## 6. Interfaces y dependencias
El SGSI depende de servicios de terceros (pasarela de pago, logística, nube). Estas interfaces se gestionan mediante contratos con cláusulas de seguridad, derecho de auditoría y SLA de respuesta a incidentes compatibles con la Ley 21.663.

## 7. Documentos relacionados
- Política General de Seguridad (GOB-SGSI-02)
- Inventario de Activos, Matriz de Riesgos y SoA (`04-analisis/`)
- Las 15 políticas (POL-SGSI-01 a 15) y 14 procedimientos (PROC-SGSI-01 a 14)

## 8. Control de cambios

| Versión | Fecha | Descripción |
|---|---|---|
| 1.0 | 17-06-2026 | Emisión inicial |
