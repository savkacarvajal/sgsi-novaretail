# 🧪 Laboratorio SGSI — NovaRetail SpA

Laboratorio técnico de la **3ra entrega**: montaje real de **Zabbix**, **Wazuh** y **Ansible**
con Docker, conectado a los procedimientos del SGSI ya documentados.

> Estado: **EN CONSTRUCCIÓN** · vence 18-06-2026

---

## 🎯 Objetivo

Materializar de forma práctica los controles que el SGSI define en papel:

| Herramienta | Qué demuestra | Política / Procedimiento que cumple |
|---|---|---|
| **Ansible** | Línea base de software automatizada (hardening, parches, usuarios) | POL-SGSI-15 · PROC-SGSI-04 |
| **Zabbix** | Monitoreo de infraestructura y disparo de alertas | POL-SGSI-08 · PROC-SGSI-10 |
| **Wazuh** | SIEM/XDR: detección de amenazas e incidentes | POL-SGSI-04 · POL-SGSI-09 · PROC-SGSI-05 · PROC-SGSI-11 |

---

## ⚠️ Restricción de recursos

Host de pruebas: **8 GB RAM / 8 CPU**. Montar los 3 stacks a la vez es arriesgado
(Wazuh usa OpenSearch, ~4 GB). Estrategia:

- **Ansible** queda corriendo siempre (liviano).
- **Zabbix** y **Wazuh** se levantan **de a uno**: levantar → capturar evidencia → bajar → siguiente.
- Reducir el heap de Wazuh indexer a ~1 GB para que entre.

En la **torre** (más RAM) probablemente se puedan levantar los tres juntos sin problema.

---

## 📁 Estructura objetivo

```
05-laboratorio/
├── README.md                 # esta guía
├── zabbix/
│   ├── docker-compose.yml
│   └── README.md             # instalación + qué monitorea + evidencia
├── wazuh/
│   ├── docker-compose.yml
│   └── README.md
├── ansible/
│   ├── inventory.ini
│   ├── playbooks/
│   │   ├── linea-base.yml     # ← PROC-SGSI-04 / POL-SGSI-15
│   │   └── hardening.yml
│   └── README.md
└── evidencias/               # capturas de pantalla de cada herramienta
```

---

## ✅ Plan de ejecución (checklist)

### Fase 0 — Entorno (~30 min)
- [ ] Instalar Docker (Colima recomendado en Mac de 8 GB; Docker Desktop en la torre).
- [ ] `colima start --cpu 4 --memory 6` (o más en la torre).
- [ ] Verificar `docker compose version`.

### Fase 1 — Estructura (~10 min)
- [ ] Crear carpetas `zabbix/`, `wazuh/`, `ansible/`, `evidencias/`.

### Fase 2 — Ansible → PROC-SGSI-04 / POL-SGSI-15 (~45 min)
- [ ] Control node + 1-2 nodos target (contenedores Ubuntu).
- [ ] `playbooks/linea-base.yml`: paquetes permitidos, deshabilitar servicios, parches, usuarios/MFA, firewall.
- [ ] `playbooks/hardening.yml`: endurecimiento básico (SSH, contraseñas, permisos).
- [ ] Evidencia: salida de `ansible-playbook` aplicando la línea base.

### Fase 3 — Zabbix → POL-SGSI-08 / PROC-SGSI-10 (~45 min)
- [ ] `docker-compose.yml`: zabbix-server + postgres + web + agent.
- [ ] Configurar 1 host monitoreado + 1 trigger/alerta (CPU o disco).
- [ ] Evidencia: dashboard con host y alerta disparada.

### Fase 4 — Wazuh → POL-SGSI-04/09 + PROC-SGSI-05/11 (~45 min)
- [ ] `docker-compose.yml` oficial de Wazuh con heap reducido.
- [ ] Agente reportando + 1 regla de detección (login fallido / archivo modificado).
- [ ] Evidencia: dashboard con alerta de seguridad.

### Fase 5 — Cierre (~30 min)
- [ ] README de cada herramienta con pasos + capturas.
- [ ] Tabla herramienta → política/procedimiento en cada README.
- [x] Actualizar **README principal**: agregar `05-laboratorio/` a la estructura.
- [x] `docs/mapeo-iso27001.md` ya incluye **PROC-SGSI-13/14** y los controles **8.14/8.29/8.33**.
- [ ] Commit + push.

---

## ⏱️ Estimación

- **Total:** ~4 horas efectivas.
- **Riesgo principal:** RAM para Wazuh → mitigado levantando de a uno.
- **Fallback Wazuh:** si la RAM no alcanza, dejar el `docker-compose.yml` listo + capturas, sin mantenerlo corriendo.

---

## 🔗 Trazabilidad con el SGSI existente

El laboratorio **no es genérico**: cada herramienta ejecuta un procedimiento ya escrito por el equipo.

- `ansible/playbooks/linea-base.yml` ↔ **PROC-SGSI-04 — Línea base de software (Ansible)**
- Alertas de **Zabbix** ↔ **PROC-SGSI-10 — Revisión y escalada de alertas**
- Detecciones de **Wazuh** ↔ **PROC-SGSI-05 — Incidentes con plazos ANCI**

---

<sub>Equipo Thynk Unlimited · NovaRetail SpA (empresa ficticia, fines académicos)</sub>
