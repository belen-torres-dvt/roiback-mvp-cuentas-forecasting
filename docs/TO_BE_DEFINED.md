# Roiback — MVP Análisis Cuentas y Forecasting · Cuestiones pendientes (`TO_BE_DEFINED`)

> Registro consolidado de todos los puntos marcados como `<TO_BE_DEFINED>` en los dos entregables finales:
> - [`[Roiback] - MVP Análisis Cuentas y Forecasting - Discovery.md`](./[Roiback]%20-%20MVP%20An%C3%A1lisis%20Cuentas%20y%20Forecasting%20-%20Discovery.md)
> - [`[Roiback] - MVP Análisis Cuentas y Forecasting - Diseño.md`](./[Roiback]%20-%20MVP%20An%C3%A1lisis%20Cuentas%20y%20Forecasting%20-%20Dise%C3%B1o.md)
>
> Cada fila es una pregunta abierta a resolver. Rellenar la columna **Respuesta** y cambiar **Estado**
> (🔴 Pendiente · 🟡 En curso · 🟢 Resuelto). Las preguntas formales de diseño por dominio están además
> en `../DISEÑO/preguntas diseño/*.csv`.

**Resumen:** 20 cuestiones en Discovery · 18 en Diseño · **38 en total**.

---

## 1. Discovery

### 1.1. Metodología

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| D-01 | 1.3.1 | Localizar y enlazar las **minutas de las sesiones de Discovery** (28, 29 y 30/04/2026). | No disponibles en el repositorio. | Devoteam (PM) | 🔴 | |

### 1.2. Arquitectura y datos (AS-IS)

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| D-02 | 3.2.1 | **Entidades y volumetría** del PostgreSQL on-premise y de las APIs on-premise. | Acceso futuro vía VPN HA; sin detalle. | Roiback (Otelo Pons) | 🔴 | |
| D-03 | 3.2.2 | **Volumetría exacta** de GA4 (orden de teras) y de bookings. | Belén analizará con el acceso a Analytics; ~8–9k movimientos de reserva/día. | Devoteam (Belén) + Roiback | 🔴 | |
| D-04 | 3.2.4 | Detalle del **procesamiento/transformación** heredado ("Click", 1 carga/día). | Sin capa gobernada; Dataform/dbt no desplegados. | Roiback (Otelo Pons) | 🔴 | |
| D-05 | 3.2.5 | Detalle de **orquestación/automatización** actual. | Procesos lanzados 1x/día; sin orquestador para la solución objetivo. | Roiback (Otelo Pons) | 🔴 | |
| D-06 | 3.3.2 | **Trazabilidad/ciclo de vida end-to-end** del dato actual. | Sin linaje formal. | Roiback + Devoteam | 🔴 | |

### 1.3. Gobierno, seguridad y operaciones (AS-IS)

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| D-07 | 4.1.1 | **Matriz de roles y permisos IAM** actual sobre el dato. | Acceso vía vistas en proyecto dedicado; sin matriz documentada. | Roiback (Otelo) + Devoteam (Juan Ezquerro) | 🔴 | |
| D-08 | 4.1.2 | **Gestión de credenciales** actual. | Sin herramienta de secretos; en Diseño se propone Secret Manager. | Roiback + Devoteam | 🔴 | |
| D-09 | 4.1.3 | Aplicación del **principio de mínimo privilegio**. | A formalizar (RBAC) en Diseño. | Devoteam (Juan Ezquerro) | 🔴 | |
| D-10 | 4.2 | **Organización de recursos cloud** (jerarquía carpetas/proyectos). | Propuesta TO-BE en Diseño (`roiback-dwh-ai-prod`/`-dev`, `roiback-dwh-governance`; origen en `roiback-analytics`, `roiback-web-demand`). | Devoteam | 🟡 | Ver 5.1 del Diseño |
| D-11 | 4.3.2 | **Capacidades de linaje** automatizado del dato. | Inexistentes hoy. | Devoteam | 🔴 | |
| D-12 | 4.3.3 | **Calidad y perfilado** del dato actual. | Sin procesos formales. | Roiback + Devoteam | 🔴 | |
| D-13 | 4.3.4 | **Seguridad fine-grained** (RLS/CLS). | No aplica en esta fase (sin PII). | Devoteam | 🟢 | No aplica (sin PII en alcance) |
| D-14 | 4.4.2 | **Ciclo de vida y despliegue / CI/CD** actual. | Inexistente; en Diseño se propone GitLab CI/CD. | Devoteam (Juan Ezquerro) | 🔴 | |
| D-15 | 4.4.4 | **Estándares y convenciones de nomenclatura**. | Devoteam propondrá en Diseño. | Devoteam | 🔴 | |
| D-16 | 4.5.1 | **Observabilidad técnica** actual. | No desplegada. | Devoteam | 🔴 | |

### 1.4. Costes y eficiencia (AS-IS)

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| D-17 | 5.1 | **Análisis de coste por usuario/service account** (`INFORMATION_SCHEMA.JOBS_BY_PROJECT`). | ~1.000 €/mes on-demand; sin visibilidad directa del coste de producción (acceso vía vistas). | Roiback (Otelo) + Devoteam | 🔴 | |
| D-18 | 5.2.1 | **Análisis de queries costosas** y optimización. | Riesgo por queries "todo contra todo" del nuevo proyecto. | Devoteam (Daniel/Chema) | 🔴 | |
| D-19 | 5.2.2 | **Cifras por región** (bytes procesados / slots medios) para decidir on-demand vs Editions. | Cliente on-demand, sin reservas; regiones `EU` y `europe-west1`. | Devoteam (Daniel) | 🔴 | |
| D-20 | 5.2.3 | **Análisis de almacenamiento** (lógico vs físico). | Factible a partir de las tablas existentes. | Devoteam (Belén) | 🔴 | |

---

## 2. Diseño

### 2.1. Alcance y requisitos

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-01 | 2.5 | **Disponibilidad (SLA) y volumetría** exactas del sistema. | Frescura conocida (08:30, D-1); SLA/volumen sin cuantificar. | Devoteam + Roiback | 🔴 | |

### 2.2. Arquitectura e ingesta

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-02 | 3.3.1 | **Volumetría estimada** de la capa raw (Bookings, GA4, Salesforce). | Frecuencias conocidas; volumen sin cuantificar. | Devoteam (Belén) + Roiback | 🔴 | |
| S-03 | 3.3.1 | **Entidad, volumetría y frecuencia** del PostgreSQL y de las APIs on-premise (ingesta vía VPN HA). | Sin detalle (mismo origen que D-02). | Roiback (Otelo Pons) | 🔴 | |

### 2.3. Diseño técnico y modelo de datos

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-04 | 4.2.1 | **Ventana exacta de carga histórica inicial** (2 vs 3 años de bookings y GA4). | En sesión se barajó ~3 años; Diseño propone 2–3. Depende del modelo. | Devoteam (Chema) + Roiback | 🔴 | |
| S-05 | 4.3.3 | **Definición de tablas y campos de la capa Gold** (KPIs/esquema estrella). | En curso. | Devoteam | 🟡 | |
| S-06 | 4.4.1 | **Diagrama Entidad-Relación (ERD)**. | Se elaborará en implementación. | Devoteam | 🔴 | |

### 2.4. Seguridad, gobierno y cumplimiento

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-07 | 5.1 | **Definición concreta de etiquetas** (`environment`, `cost_center`, `owner`). | Etiquetas identificadas; valores sin definir. | Devoteam + Roiback | 🔴 | |
| S-08 | 5.2.2 | **Matriz de roles y permisos** (TO-BE) y grupos de usuarios. | Se detallará en implementación. | Devoteam (Juan Ezquerro) | 🔴 | |
| S-09 | 5.2.5 | **Protocolo de acceso de emergencia** (*glass breaker*). | A definir si es necesario. | Devoteam + Roiback | 🔴 | |
| S-10 | 5.4.1 | **Región principal**: `europe-west1` (últimos modelos ML) vs `EU` multirregión (donde residen los datos). | Decisión pendiente tras análisis de pros/contras. | Devoteam (Daniel/Belén) + Roiback | 🔴 | |
| S-11 | 5.5.5 | **Reglas y umbrales de calidad del dato**. | Básicas definidas; concretas por caso de uso en implementación. | Devoteam + Roiback | 🔴 | |
| S-12 | 5.6.2 | **Otras normativas aplicables** además de GDPR. | Solo GDPR confirmado. | Roiback (Legal) + Devoteam | 🔴 | |
| S-13 | 5.6.3 | **Auditoría y evidencias** (estrategia, Cloud Audit Logs). | A definir en implementación. | Devoteam | 🔴 | |

### 2.5. DevOps

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-14 | 6.1.1 | **Convenciones de nomenclatura** (recursos GCP y objetos de datos). | Devoteam propondrá y validará con Roiback. | Devoteam | 🔴 | |
| S-15 | 6.2.3 | **Modularización y reutilización** de IaC (Terraform). | A definir en implementación. | Devoteam (Juan Ezquerro) | 🔴 | |

### 2.6. FinOps

| ID | Sección | Pregunta / dato pendiente | Estado actual | Responsable sugerido | Estado | Respuesta |
| :-- | :-- | :-- | :-- | :-- | :--: | :-- |
| S-16 | 8.1 | **Estimación de costes detallada** (pruebas con cuentas pequeña/mediana/grande). | Referencia actual ~1.000 €/mes. | Devoteam (Daniel/Chema) | 🔴 | |
| S-17 | 8.2 | **Equipo responsable** ante exceso de presupuesto y **acción** a tomar. | Acción = notificar; responsable a definir. | Roiback | 🔴 | |
| S-18 | 8.3.1 | **Límites concretos** de bytes procesados por query (SA de Dataform exentas). | Política acordada; valores sin fijar. | Devoteam (Daniel) + Roiback | 🔴 | |

---

## 3. Temas transversales (agrupación)

Varias cuestiones comparten origen y conviene resolverlas en bloque:

- **Volumetría / fuentes on-premise**: D-02, D-03, S-01, S-02, S-03 → una única sesión de volumetría con Roiback.
- **IAM y seguridad TO-BE**: D-07, D-08, D-09, D-14, S-08, S-09 → taller de seguridad/DevOps.
- **Costes / FinOps**: D-17, D-18, D-19, D-20, S-16, S-17, S-18 → análisis de coste + decisión Editions vs on-demand.
- **Región** (S-10) condiciona almacenamiento, ML y cumplimiento → decisión temprana recomendada.
- **Calidad y gobierno del dato**: D-11, D-12, S-11, S-13 → se materializan por caso de uso con Dataform + Dataplex.
