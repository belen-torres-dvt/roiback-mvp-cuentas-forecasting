# Roiback MVP Análisis Cuentas y Forecasting — Epics y Tasks (lista simple)

> Versión skimmable. Para la versión tabular: `epics-and-tasks-table.md`. Para el plan completo:
> `full-plan.md`. Para importar en Jira: `jira-epics-tasks.csv`.

## Cómo leer este documento

- `## HBE0002-E01 — <nombre>`: epic.
- Bajo cada epic, una sola lista `### Tareas` con bullets `- HBE0002-E01-01 — <resumen>` (una línea por tarea).
- Las tareas spike se marcan con un `🛠 SPIKE` al final del bullet.
- Tareas con alta prioridad se marcan con `🔴`, prioridad media con `🟡`, baja con `⚪`.

## HBE0002-E01 — Fundaciones de gobernanza y datos
**Área:** Governance / Data Eng · **Milestone:** M1–M2 · **UCs:** all

### Tareas
- 🔴 HBE0002-E01-01 — Definir e implementar glosario de negocio en Dataplex
- 🔴 HBE0002-E01-02 — Implementar catálogo de datos y aspectos en Dataplex
- 🔴 HBE0002-E01-03 — Configurar Data Quality (assertions Dataform + Dataplex DQ jobs)
- 🟡 HBE0002-E01-04 — Matriz de linaje de datos (Dataform → Dataplex)

## HBE0002-E02 — Infraestructura y IaC (Terraform + Atlantis)
**Área:** DevOps / Infra · **Milestone:** M1 · **UCs:** all

### Tareas
- 🔴 HBE0002-E02-01 — Provisionar jerarquía de proyectos GCP
- 🔴 HBE0002-E02-02 — Backend remoto de Terraform en GCS (state + lock)
- 🔴 HBE0002-E02-03 — Atlantis + GitLab CI/CD para Terraform
- 🔴 HBE0002-E02-04 — Módulos Terraform reutilizables
- 🟡 HBE0002-E02-05 — Etiquetado de facturación y límites de query

## HBE0002-E03 — Capa de transformación (Dataform + Cloud Workflows)
**Área:** Data Eng · **Milestone:** M2 · **UCs:** UC-01/02/03/04

### Tareas
- 🔴 HBE0002-E03-01 — Inicializar proyecto Dataform y estructura medallón
- 🔴 HBE0002-E03-02 — Transformaciones Silver
- 🔴 HBE0002-E03-03 — Transformaciones Gold + KPIs (esquema estrella)
- 🔴 HBE0002-E03-04 — Capa Platinum (ML-ready + UC outputs)
- 🔴 HBE0002-E03-05 — Orquestación con Cloud Workflows
- 🟡 HBE0002-E03-06 — Triggers con Cloud Scheduler
- 🔴 HBE0002-E03-07 — Testing Dataform (unit + DQ assertions)

## HBE0002-E04 — Machine Learning y modelos (BigQuery ML)
**Área:** ML/AI / Data Science · **Milestone:** M2–M3 · **UCs:** UC-01/03/04

### Tareas
- 🔴 HBE0002-E04-01 — Modelo de detección de anomalías (ARIMA_PLUS)
- 🔴 HBE0002-E04-02 — Forecasting (ARIMA_PLUS / TimesFM)
- 🟡 HBE0002-E04-03 — Clustering KMeans de hoteles
- 🟡 HBE0002-E04-04 — Pipeline de reentrenamiento (daily/weekly)
- 🔴 HBE0002-E04-05 — Publicación de modelos a Platinum

## HBE0002-E05 — Sistema de alertas (Slack + Cloud Workflows)
**Área:** Data Eng / Observability · **Milestone:** M3 · **UCs:** UC-01

### Tareas
- 🔴 HBE0002-E05-01 — Integración con Slack (webhook + Bot API)
- 🔴 HBE0002-E05-02 — Notificación de anomalías (Cloud Function)
- 🔴 HBE0002-E05-03 — Notificación de forecasting vs. budget
- 🟡 HBE0002-E05-04 — Alertas de pipeline (Workflows + Logging)
- 🟡 HBE0002-E05-05 — Dashboard histórico de alertas

## HBE0002-E06 — Observabilidad, monitorización y FinOps
**Área:** DevOps / FinOps · **Milestone:** M3–M4 · **UCs:** all

### Tareas
- 🟡 HBE0002-E06-01 — Cloud Logging centralizado
- 🟡 HBE0002-E06-02 — Dashboards Cloud Monitoring
- 🟡 HBE0002-E06-03 — Alertas operativas (error rate, latencia)
- 🔴 HBE0002-E06-04 — Análisis de costes y benchmarking on-demand vs Editions
- 🟡 HBE0002-E06-05 — Presupuestos y alertas de FinOps
- 🟡 HBE0002-E06-06 — Runbook de observabilidad e incidentes

## HBE0002-E07 — Seguridad, IAM y cumplimiento
**Área:** Security / Governance · **Milestone:** M1 · **UCs:** all

### Tareas
- 🔴 HBE0002-E07-01 — Matriz de roles IAM TO-BE
- 🔴 HBE0002-E07-02 — Service accounts por componente/entorno
- 🔴 HBE0002-E07-03 — Google Secret Manager + rotación
- 🔴 HBE0002-E07-04 — VPN HA hacia PostgreSQL y APIs on-prem
- 🟡 HBE0002-E07-05 — Firewall (VPC) y políticas de red
- 🟡 HBE0002-E07-06 — Cloud Audit Logs + evidencias de cumplimiento
- 🟡 HBE0002-E07-07 — Políticas de cumplimiento + glass-breaker

## HBE0002-E08 — Dashboard integral de reunión (UC-02)
**Área:** BI / Data Eng · **Milestone:** M3 · **UCs:** UC-02

### Tareas
- 🔴 HBE0002-E08-01 — ERD + esquema Gold para UC-02
- 🔴 HBE0002-E08-02 — Agregados y vistas BI
- 🔴 HBE0002-E08-03 — Dashboard Looker Studio (UC-02)
- 🟡 HBE0002-E08-04 — Integración del resumen de IA en el dashboard

## HBE0002-E09 — Asistente conversacional (UC-05)
**Área:** ML/AI / Data Eng · **Milestone:** M3 · **UCs:** UC-05

### Tareas
- 🟡 HBE0002-E09-01 — Arquitectura del agente conversacional 🛠 SPIKE
- 🟡 HBE0002-E09-02 — Backend del chatbot (Cloud Run)
- 🟡 HBE0002-E09-03 — Integración con Slack (Bot App)
- 🟡 HBE0002-E09-04 — Validación de respuestas y ground truth

## HBE0002-E10 — Validación, testing y UAT
**Área:** QA / Testing · **Milestone:** M4 · **UCs:** all

### Tareas
- 🟡 HBE0002-E10-01 — Test suites unitarios Dataform
- 🔴 HBE0002-E10-02 — Pruebas de integración end-to-end
- 🔴 HBE0002-E10-03 — Pruebas de calidad del dato
- 🟡 HBE0002-E10-04 — Pruebas de carga y rendimiento
- 🔴 HBE0002-E10-05 — Pruebas de seguridad e IAM
- 🔴 HBE0002-E10-06 — UAT con grupo piloto DCS (4–5 personas)

## HBE0002-E11 — Documentación y handover
**Área:** PM / Documentation · **Milestone:** M4 · **UCs:** all

### Tareas
- 🟡 HBE0002-E11-01 — Documento de arquitectura final
- 🟡 HBE0002-E11-02 — Runbooks operativos
- 🟡 HBE0002-E11-03 — Glosario de negocio final (Dataplex)
- 🔴 HBE0002-E11-04 — Onboarding equipo técnico Roiback (3 sesiones)
- ⚪ HBE0002-E11-05 — Notebooks de ejemplo (Jupyter)

## HBE0002-E12 — Spikes y decisiones pendientes
**Área:** PM / Architecture · **Milestone:** M1 · **UCs:** all (unblocks)

### Tareas
- 🔴 HBE0002-E12-01 — SPIKE Volumetría (bookings, GA4, on-prem) 🛠 SPIKE
- 🔴 HBE0002-E12-02 — SPIKE Decisión de región (EU vs europe-west1) 🛠 SPIKE
- 🔴 HBE0002-E12-03 — SPIKE Taller de seguridad e IAM 🛠 SPIKE
- 🔴 HBE0002-E12-04 — SPIKE Análisis de costes detallado 🛠 SPIKE
- 🔴 HBE0002-E12-05 — SPIKE Definición de KPIs y esquema Gold 🛠 SPIKE
- 🟡 HBE0002-E12-06 — SPIKE Estrategia on-premise (PostgreSQL + APIs) 🛠 SPIKE

## Resumen

- Epics: 12
- Tareas: 64
- Spikes: 8 (E09-01 + E12-01..06; revisa la WBS canónica)
- Distribución por milestone:
  - M1 — Foundations (W1–3): 20 tareas (E02 completo, E07 completo, E12 completo, E01-01/02 parcial)
  - M2 — Pipelines + first UC (W4–8): 10 tareas (E03 completo, E04-01, E01-03/04)
  - M3 — Alerts / BI / IA (W9–12): 17 tareas (E05, E08, E09, E04-02/03/04/05)
  - M4 — Testing & handover (W13–16): 17 tareas (E10, E11, E06)
- Casos de uso entregados:
  - UC-01 → E05, E04
  - UC-02 → E08, E04
  - UC-03 → E04, E05
  - UC-04 → E04
  - UC-05 → E09, E08
