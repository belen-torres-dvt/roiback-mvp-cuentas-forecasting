# Roiback MVP Análisis Cuentas y Forecasting — Epics y Tasks (tabular)

> Fuente canónica: `/tmp/roiback-wbs.md`. Para descripciones detalladas y contexto narrativo ver
> `full-plan.md`. Para la lista simple ver `epics-and-tasks-simple.md`. Para importar en Jira ver
> `jira-epics-tasks.csv`.

## Epics

| External ID | Nombre | Área | Milestone | Casos de uso | Nº tasks | Story points (suma) |
|---|---|---|---|---|---|---|
| HBE0002-E01 | Fundaciones de gobernanza y datos | Governance / Data Eng | M1–M2 | all | 4 | 18 |
| HBE0002-E02 | Infraestructura y IaC (Terraform + Atlantis) | DevOps / Infra | M1 | all | 5 | 20 |
| HBE0002-E03 | Capa de transformación (Dataform + Cloud Workflows) | Data Eng | M2 | UC-01/02/03/04 | 7 | 38 |
| HBE0002-E04 | Machine Learning y modelos (BigQuery ML) | ML/AI / Data Science | M2–M3 | UC-01/03/04 | 5 | 29 |
| HBE0002-E05 | Sistema de alertas (Slack + Cloud Workflows) | Data Eng / Observability | M3 | UC-01 | 5 | 19 |
| HBE0002-E06 | Observabilidad, monitorización y FinOps | DevOps / FinOps | M3–M4 | all | 6 | 21 |
| HBE0002-E07 | Seguridad, IAM y cumplimiento | Security / Governance | M1 | all | 7 | 27 |
| HBE0002-E08 | Dashboard integral de reunión (UC-02) | BI / Data Eng | M3 | UC-02 | 4 | 20 |
| HBE0002-E09 | Asistente conversacional (UC-05) | ML/AI / Data Eng | M3 | UC-05 | 4 | 19 |
| HBE0002-E10 | Validación, testing y UAT | QA / Testing | M4 | all | 6 | 31 |
| HBE0002-E11 | Documentación y handover | PM / Documentation | M4 | all | 5 | 21 |
| HBE0002-E12 | Spikes y decisiones pendientes | PM / Architecture | M1 | all (unblocks) | 6 | 17 |

## Tasks

| External ID | Epic | Resumen | Descripción | Prioridad | SP | Spike | Dependencias | Items abiertos | Asignado | Componentes | Labels |
|---|---|---|---|---|---|---|---|---|---|---|---|
| HBE0002-E01-01 | E01 | Definir e implementar glosario de negocio en Dataplex | Crear glosario en Dataplex con ≥50 términos validados por Roiback (TTV, RN, ABV, % cancelación, lead time, paridad…) como base de la capa semántica única. | Alta | 5 | No | HBE0002-E12-05 | S-14, D-12 | Belén | Governance, Data-Eng | governance, glossary |
| HBE0002-E01-02 | E01 | Implementar catálogo de datos y aspectos en Dataplex | Indexar activos de BigQuery; plantillas de etiquetas (Data Classification, Owner, Area, Process); enriquecimiento desde Dataform. | Alta | 5 | No | HBE0002-E01-01 | S-05, S-07 | Belén | Governance, Data-Eng | governance, catalog |
| HBE0002-E01-03 | E01 | Configurar Data Quality (assertions Dataform + Dataplex DQ jobs) | 15+ reglas: nulos, duplicados, integridad referencial; pipeline detenido ante DQ critical; alertas a `#data-ops-logs`. | Alta | 5 | No | HBE0002-E03-01 | S-11 | Belén | Governance, Data-Eng | governance, data-quality |
| HBE0002-E01-04 | E01 | Matriz de linaje de datos (Dataform → Dataplex) | Linaje automático visible en Dataform y Dataplex para 100 % de tablas Silver/Gold/Platinum. | Media | 3 | No | HBE0002-E03-02, HBE0002-E03-03, HBE0002-E03-04 | — | Belén | Governance | governance, lineage |
| HBE0002-E02-01 | E02 | Provisionar jerarquía de proyectos GCP | Crear `roiback-dwh-ai-prod`, `roiback-dwh-ai-dev`, `roiback-dwh-governance` bajo `roiback.com`; carpetas Production/Non-Production. | Alta | 5 | No | HBE0002-E12-02 | S-10 | Juan | DevOps, Infra | infra, gcp, bootstrap |
| HBE0002-E02-02 | E02 | Backend remoto de Terraform en GCS (state + lock) | Bucket versionado + bloqueo de estado; convenciones de naming validadas. | Alta | 2 | No | HBE0002-E02-01 | — | Juan | DevOps | infra, iac |
| HBE0002-E02-03 | E02 | Atlantis + GitLab CI/CD para Terraform | PRs auto-plan + apply; flujo monorepo `main + features`. | Alta | 5 | No | HBE0002-E02-02 | S-15 | Juan | DevOps | infra, cicd, atlantis |
| HBE0002-E02-04 | E02 | Módulos Terraform reutilizables | Módulos: `bq_dataset`, `iam_roles`, `cloud_workflows`, `secret_manager`, `monitoring`. | Alta | 5 | No | HBE0002-E02-03 | S-14 | Juan | DevOps | infra, iac, modules |
| HBE0002-E02-05 | E02 | Etiquetado de facturación y límites de query | Etiquetas `environment`, `cost_center`, `owner`; límite de bytes por query (SA Dataform exenta). | Media | 3 | No | HBE0002-E02-01 | S-07, S-18 | Juan | DevOps, FinOps | finops, tagging, quotas |
| HBE0002-E03-01 | E03 | Inicializar proyecto Dataform y estructura medallón | Carpetas `sources/`, `intermediate/`, `output/{silver,gold,platinum}` operativas con un modelo de ejemplo en cada capa. | Alta | 5 | No | HBE0002-E02-01, HBE0002-E01-01 | — | Belén | Data-Eng | dataform, medallion |
| HBE0002-E03-02 | E03 | Transformaciones Silver | Modelos `silver/{crs,core,google_analytics,sources}`: deduplicación, conversión de moneda (`currency_rate_*`), mapeo `country` con `tb_map_country_iso`, filtros de reservas de prueba. | Alta | 8 | No | HBE0002-E03-01 | S-04, S-02 | Belén | Data-Eng | dataform, silver |
| HBE0002-E03-03 | E03 | Transformaciones Gold + KPIs (esquema estrella) | Fact/dim tables; KPIs TTV (`amounts.total.producedWithTaxes`), RN, ABV, ADR, LoS, % cancelación; particionado por `modification_timestamp_utc`, clusterizado por `chain`/`hotel_id`. | Alta | 8 | No | HBE0002-E03-02, HBE0002-E12-05 | S-05, S-06 | Belén | Data-Eng | dataform, gold, kpi |
| HBE0002-E03-04 | E03 | Capa Platinum (ML-ready + UC outputs) | Tablas `gold.kpi_anomalies`, `gold.kpi_forecast`, `gold.hotel_clusters`, salidas para asistente conversacional. | Alta | 5 | No | HBE0002-E03-03, HBE0002-E04-05 | — | Belén | Data-Eng | dataform, platinum |
| HBE0002-E03-05 | E03 | Orquestación con Cloud Workflows | Workflows YAML versionados en GitLab (`hourly_bookings_silver`, `daily_sales_gold`, `daily_ml_platinum`); 3 reintentos con backoff. | Alta | 5 | No | HBE0002-E03-01 | — | Belén | Data-Eng, DevOps | cloud-workflows, orchestration |
| HBE0002-E03-06 | E03 | Triggers con Cloud Scheduler | Bookings cada hora; GA4 2×/día; Salesforce diario; resto a las 08:30 Madrid. | Media | 2 | No | HBE0002-E03-05 | — | Juan | DevOps | scheduling |
| HBE0002-E03-07 | E03 | Testing Dataform (unit + DQ assertions) | Cobertura ≥80 % de transformaciones críticas; integración referencial; nulls/duplicados. | Alta | 5 | No | HBE0002-E03-02, HBE0002-E03-03 | — | Belén | Data-Eng, QA | qa, assertions |
| HBE0002-E04-01 | E04 | Modelo de detección de anomalías (ARIMA_PLUS) | Por hotel/cadena; objetivo F1 > 0.75 en validación; activa UC-01. | Alta | 8 | No | HBE0002-E03-03 | — | Chema | ML-AI | bqml, anomaly-detection, arima |
| HBE0002-E04-02 | E04 | Forecasting (ARIMA_PLUS / TimesFM) | Horizonte 3–4 meses; RMSE < 10 %; activa UC-03. | Alta | 8 | No | HBE0002-E03-03 | — | Chema | ML-AI | bqml, forecasting, timesfm |
| HBE0002-E04-03 | E04 | Clustering KMeans de hoteles | Recalculado semanalmente; silueta > 0.5; activa UC-04. | Media | 5 | No | HBE0002-E03-03 | — | Chema | ML-AI | bqml, clustering, kmeans |
| HBE0002-E04-04 | E04 | Pipeline de reentrenamiento (daily/weekly) | Métricas logged en BigQuery; orquestado por Cloud Workflows. | Media | 5 | No | HBE0002-E04-01, HBE0002-E04-02, HBE0002-E04-03 | — | Chema | ML-AI | bqml, mlops |
| HBE0002-E04-05 | E04 | Publicación de modelos a Platinum | `gold.kpi_anomalies`, `gold.kpi_forecast`, `gold.hotel_clusters` pobladas con cadencia acordada. | Alta | 3 | No | HBE0002-E04-04, HBE0002-E03-04 | — | Chema | ML-AI, Data-Eng | bqml, serving |
| HBE0002-E05-01 | E05 | Integración con Slack (webhook + Bot API) | Canales `#data-alerts`, `#forecast-warnings`, `#data-ops-logs`; secrets en Secret Manager. | Alta | 3 | No | HBE0002-E07-03 | — | Belén | Data-Eng | slack, integration |
| HBE0002-E05-02 | E05 | Notificación de anomalías (Cloud Function) | UC-01: payload con hotel, métrica, comparativa L7D/L4W/YoY; gating por priorización. | Alta | 5 | No | HBE0002-E04-01, HBE0002-E05-01 | S-11 | Belén | Data-Eng, ML-AI | slack, anomaly |
| HBE0002-E05-03 | E05 | Notificación de forecasting vs. budget | UC-03: alerta proactiva si proyección < budget ±10 %; evaluar adjuntar gráfico. | Alta | 5 | No | HBE0002-E04-02, HBE0002-E05-01 | — | Belén | Data-Eng | slack, forecast |
| HBE0002-E05-04 | E05 | Alertas de pipeline (Workflows + Logging) | CRITICAL detiene pipeline y notifica al equipo técnico Roiback; WARNING a `#data-ops-logs`. | Media | 3 | No | HBE0002-E03-05, HBE0002-E03-06 | — | Juan | DevOps, Observability | pipeline, alerts |
| HBE0002-E05-05 | E05 | Dashboard histórico de alertas | Últimos 30 días por hotel/cadena/métrica para evaluar falsos positivos. | Media | 3 | No | HBE0002-E06-02 | — | Belén | Observability | alerts, dashboard |
| HBE0002-E06-01 | E06 | Cloud Logging centralizado | Dataform, Workflows, Cloud Functions → Cloud Logging; auditoría Cloud Audit Logs. | Media | 3 | No | — | S-13 | Juan | DevOps, Observability | logging |
| HBE0002-E06-02 | E06 | Dashboards Cloud Monitoring | Pipelines Health, Data Quality, Infrastructure, FinOps. | Media | 5 | No | HBE0002-E06-01 | — | Juan | DevOps, Observability | monitoring, dashboards |
| HBE0002-E06-03 | E06 | Alertas operativas (error rate, latencia) | Slack notifications; matriz de severidades CRITICAL/WARNING. | Media | 3 | No | HBE0002-E06-02 | — | Juan | DevOps, Observability | alerting |
| HBE0002-E06-04 | E06 | Análisis de costes y benchmarking on-demand vs Editions | Desglose `INFORMATION_SCHEMA.JOBS_BY_PROJECT`; pruebas con cuentas chica/mediana/grande. | Alta | 5 | No | HBE0002-E12-04 | S-16, S-17, S-18, D-17, D-18, D-19, D-20 | Daniel | FinOps | finops, cost-analysis |
| HBE0002-E06-05 | E06 | Presupuestos y alertas de FinOps | Budgets por entorno; alertas 50/90/100 %. | Media | 2 | No | HBE0002-E06-04 | S-16, S-17 | Daniel | FinOps | finops, budgets |
| HBE0002-E06-06 | E06 | Runbook de observabilidad e incidentes | SLA, escalado, on-call, contactos. | Media | 3 | No | HBE0002-E06-01, HBE0002-E06-02 | S-01 | Juan | DevOps, Documentation | runbook |
| HBE0002-E07-01 | E07 | Matriz de roles IAM TO-BE | Grupos `data-engineers`, `analysts-dcs`, `ml-engineers`, `devops-team`, `business-users`; permisos mínimo privilegio. | Alta | 5 | No | HBE0002-E12-03 | D-07, D-08, D-09, S-08 | Juan | Security | iam, rbac |
| HBE0002-E07-02 | E07 | Service accounts por componente/entorno | `dataform-{env}`, `workflows-{env}`, `chatbot-{env}`, `monitoring-{env}`. | Alta | 3 | No | HBE0002-E07-01 | — | Juan | Security | iam, service-accounts |
| HBE0002-E07-03 | E07 | Google Secret Manager + rotación | Credenciales on-prem, Slack webhooks, claves chatbot. | Alta | 3 | No | HBE0002-E07-02 | — | Juan | Security | secrets, rotation |
| HBE0002-E07-04 | E07 | VPN HA hacia PostgreSQL y APIs on-prem | Cloud VPN HA; pruebas de conectividad y failover. | Alta | 5 | No | HBE0002-E02-01, HBE0002-E12-06 | S-03 | Juan | Security, Infra | network, vpn |
| HBE0002-E07-05 | E07 | Firewall (VPC) y políticas de red | Ingress/egress restrictivos; documentación de aperturas. | Media | 3 | No | HBE0002-E02-01 | — | Juan | Security | network, firewall |
| HBE0002-E07-06 | E07 | Cloud Audit Logs + evidencias de cumplimiento | Audit logs habilitados; retención GDPR. | Media | 5 | No | HBE0002-E06-01 | S-13 | Juan | Security, Governance | audit, gdpr |
| HBE0002-E07-07 | E07 | Políticas de cumplimiento + glass-breaker | Acceso de emergencia, residencia del dato, matriz GDPR. | Media | 3 | No | HBE0002-E07-01 | S-09, S-12 | Daniel | Security, PM | compliance, policy |
| HBE0002-E08-01 | E08 | ERD + esquema Gold para UC-02 | Tablas `fact_daily_summary`, `dim_hotel_comparison`; campos TTV, RN, Reservas, Forecast, Anomalía. | Alta | 5 | No | HBE0002-E03-03, HBE0002-E12-05 | S-05, S-06 | Belén | BI, Data-Eng | bi, data-modeling |
| HBE0002-E08-02 | E08 | Agregados y vistas BI | Comparativas L7D vs L4W vs YoY; histórico de anomalías 30 días. | Alta | 5 | No | HBE0002-E08-01 | — | Belén | BI, Data-Eng | bi, sql-views |
| HBE0002-E08-03 | E08 | Dashboard Looker Studio (UC-02) | 5+ visualizaciones; filtros por hotel/cadena/período; aprobación con DCS. | Alta | 5 | No | HBE0002-E08-02 | — | Belén | BI | looker-studio, dashboard |
| HBE0002-E08-04 | E08 | Integración del resumen de IA en el dashboard | Llamada al chatbot con resumen contextual de tráfico/ventas/anomalías/forecast. | Media | 5 | No | HBE0002-E09-02, HBE0002-E05-02, HBE0002-E04-02 | — | Chema | BI, ML-AI | bi, ai-integration |
| HBE0002-E09-01 | E09 | Arquitectura del agente conversacional | Spike: elegir LLM (Vertex AI / Claude / Gemini) y patrón RAG sobre BigQuery; documentación de flujo. | Media | 3 | Sí | — | — | Chema | ML-AI | ai, architecture, spike |
| HBE0002-E09-02 | E09 | Backend del chatbot (Cloud Run) | Servicio REST con verificación de fuente (`source_table`, `query_timestamp`, `confidence`). | Media | 8 | No | HBE0002-E03-04, HBE0002-E09-01 | — | Chema | ML-AI, Data-Eng | cloud-run, chatbot |
| HBE0002-E09-03 | E09 | Integración con Slack (Bot App) | Comandos/menciones, rate limiting, manejo de errores. | Media | 5 | No | HBE0002-E09-02 | — | Chema | ML-AI | slack-bot |
| HBE0002-E09-04 | E09 | Validación de respuestas y ground truth | Conjunto de 10 queries validadas con DCS; medición de precisión. | Media | 3 | No | HBE0002-E09-02 | — | Chema | ML-AI, QA | ai, qa |
| HBE0002-E10-01 | E10 | Test suites unitarios Dataform | Suites unitarios Dataform sobre transformaciones críticas. | Media | 3 | No | HBE0002-E03-07 | — | Belén | QA, Data-Eng | qa, unit |
| HBE0002-E10-02 | E10 | Pruebas de integración end-to-end | Pipeline Bronze → Silver → Gold → BI con datos reales. | Alta | 5 | No | HBE0002-E03-05 | — | Belén | QA | qa, integration |
| HBE0002-E10-03 | E10 | Pruebas de calidad del dato | Validación de reglas de calidad sobre Silver/Gold/Platinum. | Alta | 5 | No | HBE0002-E01-03 | — | Belén | QA, Governance | qa, data-quality |
| HBE0002-E10-04 | E10 | Pruebas de carga y rendimiento | Tiempos de query objetivo < 2 minutos para volúmenes esperados. | Media | 5 | No | HBE0002-E03-03, HBE0002-E12-01 | S-02 | Juan | QA | qa, performance |
| HBE0002-E10-05 | E10 | Pruebas de seguridad e IAM | Validación de roles, accesos y service accounts. | Alta | 5 | No | HBE0002-E07-01 | — | Juan | QA, Security | qa, security |
| HBE0002-E10-06 | E10 | UAT con grupo piloto DCS (4–5 personas) | Sign-off Roiback sobre UC-01, UC-02, UC-03. | Alta | 8 | No | HBE0002-E05-02, HBE0002-E08-04, HBE0002-E04-01, HBE0002-E04-02, HBE0002-E04-03 | — | Daniel | QA, PM | qa, uat |
| HBE0002-E11-01 | E11 | Documento de arquitectura final | Documento técnico de arquitectura final del MVP. | Media | 5 | No | — | — | Daniel | Documentation, PM | documentation, architecture |
| HBE0002-E11-02 | E11 | Runbooks operativos | Pipeline failure, DQ alert, cost spike, Dataform deploy, chatbot debugging. | Media | 5 | No | HBE0002-E05-04, HBE0002-E06-06 | — | Juan | Documentation, DevOps | documentation, runbooks |
| HBE0002-E11-03 | E11 | Glosario de negocio final (Dataplex) | Glosario final consolidado en Dataplex con validación Roiback. | Media | 3 | No | HBE0002-E01-01 | — | Belén | Documentation, Governance | documentation, glossary |
| HBE0002-E11-04 | E11 | Onboarding equipo técnico Roiback (3 sesiones) | Sesiones de transferencia técnica al equipo Roiback. | Alta | 5 | No | HBE0002-E11-01, HBE0002-E11-02 | — | Daniel | PM | documentation, handover, training |
| HBE0002-E11-05 | E11 | Notebooks de ejemplo (Jupyter) | Notebooks de ejemplo para uso del data warehouse y modelos. | Baja | 3 | No | HBE0002-E03-03, HBE0002-E04-01, HBE0002-E09-02 | — | Chema | Documentation, ML-AI | documentation, notebooks |
| HBE0002-E12-01 | E12 | SPIKE Volumetría (bookings, GA4, on-prem) | Spike de volumetría de bookings, GA4 y on-prem para dimensionar la plataforma. | Alta | 3 | Sí | — | D-02, D-03, S-01, S-02, S-03 | Belén | PM, Data-Eng | spike, volumetry |
| HBE0002-E12-02 | E12 | SPIKE Decisión de región (EU vs europe-west1) | Spike para decidir región GCP (EU multi vs europe-west1). | Alta | 2 | Sí | — | S-10 | Daniel | PM, Architecture | spike, region |
| HBE0002-E12-03 | E12 | SPIKE Taller de seguridad e IAM | Spike/taller de seguridad e IAM para definir matriz de roles. | Alta | 3 | Sí | — | D-07, D-08, D-09, S-08, S-09 | Juan | PM, Security | spike, security |
| HBE0002-E12-04 | E12 | SPIKE Análisis de costes detallado | Spike de análisis de costes detallado por cuenta y tipo de carga. | Alta | 3 | Sí | — | S-16, S-17, S-18, D-17, D-18, D-19, D-20 | Daniel | PM, FinOps | spike, finops |
| HBE0002-E12-05 | E12 | SPIKE Definición de KPIs y esquema Gold | Spike para definir KPIs y esquema Gold con Roiback. | Alta | 3 | Sí | — | S-05, S-06 | Chema | PM, Data-Eng | spike, data-modeling |
| HBE0002-E12-06 | E12 | SPIKE Estrategia on-premise (PostgreSQL + APIs) | Spike de estrategia de integración on-premise (PostgreSQL + APIs). | Media | 3 | Sí | — | S-03 | Juan | PM, Infra | spike, integration |

## Resumen

- Total epics: 12
- Total tasks: 64
- Spikes: 8
- Story points totales: 280
- Distribución por milestone (asignando cada epic a su milestone primaria):
  - M1: 22 tasks · 82 SP (E01, E02, E07, E12)
  - M2: 12 tasks · 67 SP (E03, E04)
  - M3: 19 tasks · 79 SP (E05, E06, E08, E09)
  - M4: 11 tasks · 52 SP (E10, E11)
- Distribución por área principal (asignando cada epic a su área primaria):
  - Governance / Data Eng (E01): 4 tasks · 18 SP
  - DevOps / Infra (E02, E06): 11 tasks · 41 SP
  - Data Eng (E03, E05): 12 tasks · 57 SP
  - ML-AI / Data Science (E04, E09): 9 tasks · 48 SP
  - Security (E07): 7 tasks · 27 SP
  - BI (E08): 4 tasks · 20 SP
  - QA (E10): 6 tasks · 31 SP
  - PM / Documentation (E11, E12): 11 tasks · 38 SP
