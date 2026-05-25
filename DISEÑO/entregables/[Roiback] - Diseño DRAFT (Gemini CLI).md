
# Roiback - MVP Análisis Cuentas y Forecasting

## Diseño

**Hoja de control**

**Control de documentación**

| | |
| :---- | :---- |
| **Document Code** | Roiback- MVP Análisis Cuentas y Forecasting - Entregable diseño |
| **Preparado por:** | Devoteam |
| **Fecha** | 03/06/2026 |

**Control de versiones**

| Versión | Autor | Fecha | Comentarios |
| :---- | :---- | :---- | :---- |
| v1.0.0 | Data Accelerator | 16 Jan 2026 | Plantilla entregable Diseño |

**Control de revisión y aprobación**

| | Nombre | Fecha | Firma |
| :---- | :---- | :---- | :---- |
| **Revisado por** | | | |
| **Aprobado por** | | | |

# 

# 

## 

## Índice

**[Instrucciones de uso de esta plantilla	6](#instrucciones-de-uso-de-esta-plantilla)**

[**1\. Introducción y contexto	7**](#1.-introducción-y-contexto)

[1.1. Contexto y antecedentes	7](#1.1.-contexto-y-antecedentes)

[1.2. Propósito del documento	7](#1.2.-propósito-del-documento)

[**2\. Alcance del proyecto	8**](#2.-alcance-del-proyecto)

[2.1. Objetivos estratégicos	8](#2.1.-objetivos-estratégicos)

[2.2. Puntos de dolor que resuelve	8](#2.2.-puntos-de-dolor-que-resuelve)

[2.3. Casos de uso prioritarios	9](#2.3.-casos-de-uso-prioritarios)

[2.3. Requisitos funcionales	10](#2.4.-requisitos-funcionales)

[2.4. Requisitos técnicos (no funcionales)	10](#2.5.-requisitos-técnicos-\(no-funcionales\))

[2.5. Exclusiones, supuestos y limitaciones	12](#2.6.-exclusiones,-supuestos-y-limitaciones)

[2.5.1. Exclusiones	12](#2.6.1.-exclusiones)

[2.5.2. Supuestos	12](#2.6.2.-supuestos)

[2.5.3. Limitaciones técnicas	13](#2.6.3.-limitaciones-técnicas)

[**3\. Diseño de arquitectura a alto nivel	13**](#3.-diseño-de-arquitectura-a-alto-nivel)

[3.1. Principios de arquitectura	13](#3.1.-principios-de-arquitectura)

[3.1.1. Escalabilidad	13](#3.1.1.-escalabilidad)

[3.1.2. Diseño de seguridad	14](#3.1.2.-diseño-de-seguridad)

[3.1.3. Automatización	14](#3.1.3.-automatización)

[3.1.4. Observabilidad	14](#3.1.4.-observabilidad)

[3.2. Diagrama de arquitectura	14](#3.2.-diagrama-de-arquitectura)

[3.3. Descripción de componentes	16](#3.3.-descripción-de-componentes)

[3.3.1. Capa de ingesta y orígenes	16](#3.3.1.-capa-de-ingesta-y-orígenes)

[3.3.2. Capa de procesamiento y lógica de negocio	17](#3.3.2.-capa-de-procesamiento-y-lógica-de-negocio)

[3.3.3. Capa de persistencia y almacenamiento	18](#3.3.3.-capa-de-persistencia-y-almacenamiento)

[3.3.4. Capa de consumo	19](#3.3.4.-capa-de-consumo)

[3.4. Decisiones de diseño	20](#3.4.-decisiones-de-diseño)

[**4\. Diseño técnico detallado y flujos de datos	20**](#4.-diseño-técnico-detallado-y-flujos-de-datos)

[4.1. Stack tecnológico	21](#4.1.-stack-tecnológico)

[4.2. Diseño de data pipelines	21](#4.2.-diseño-de-data-pipelines)

[4.2.1. Estrategia de carga de datos	22](#4.2.1.-estrategia-de-carga-de-datos)

[4.2.2. Estrategia de transformación de datos	22](#4.2.2.-estrategia-de-transformación-de-datos)

[4.2.3. Estrategia de calidad del dato	23](#4.2.3.-estrategia-de-calidad-del-dato)

[4.2.4. Estrategia de orquestación de datos	23](#4.2.4.-estrategia-de-orquestación-de-datos)

[4.3. Arquitectura de Datos	25](#4.3.-arquitectura-de-datos)

[4.3.1 Capa Bronze	25](#4.3.1-capa-bronze)

[4.3.2 Capa Silver	27](#4.3.2-capa-silver)

[4.3.3 Capa Gold	28](#4.3.3-capa-gold)

[4.3.4 Capa Platinum	29](#4.3.4-capa-platinum)

[4.4. Modelo de datos físico y optimización	30](#4.4.-modelo-de-datos-físico-y-optimización)

[4.4.1. Diagrama de Entidad-Relación (ERD)	30](#4.4.1.-diagrama-de-entidad-relación-\(erd\))

[4.4.2. Estrategia de Historización (SCD)	31](#4.4.2.-estrategia-de-historización-\(scd\))

[4.4.3 Estrategia de particionamiento y clustering	32](#4.4.3-estrategia-de-particionamiento-y-clustering)

[**5\. Seguridad, gobierno y cumplimiento	34**](#5.-seguridad,-gobierno-y-cumplimiento)

[5.1. Organización de recursos y jerarquía	34](#5.1.-organización-de-recursos-y-jerarquía)

[5.2. Gestión de identidades y accesos a datos	35](#5.2.-gestión-de-identidades-y-accesos-a-datos)

[5.2.1 Estrategia de autenticación	36](#5.2.1-estrategia-de-autenticación)

[5.2.2. Matriz de roles y permisos	36](#5.2.2.-matriz-de-roles-y-permisos)

[5.2.3. Gestión de secretos y credenciales	37](#5.2.3.-gestión-de-secretos-y-credenciales)

[5.2.4. Seguridad granular del dato	38](#5.2.4.-seguridad-granular-del-dato)

[5.2.4. Protocolo de acceso de emergencia (glass breaker)	40](#5.2.4.-protocolo-de-acceso-de-emergencia-\(glass-breaker\))

[5.3. Estrategias de cifrado	41](#5.3.-estrategias-de-cifrado)

[5.3.1. Cifrado en tránsito	41](#5.3.1.-cifrado-en-tránsito)

[5.3.2. Cifrado en reposo	41](#5.3.2.-cifrado-en-reposo)

[5.3.3. Gestión de claves de cifrado (KMS)	41](#5.3.3.-gestión-de-claves-de-cifrado-\(kms\))

[5.4. Seguridad de red y perímetro	42](#5.4.-seguridad-de-red-y-perímetro)

[5.4.1. Arquitectura de red	42](#5.4.1.-arquitectura-de-red)

[5.4.2. Conectividad híbrida	43](#5.4.2.-conectividad-híbrida)

[5.4.3. Seguridad de red y controles	43](#5.4.3.-seguridad-de-red-y-controles)

[5.5. Gobierno del dato	44](#5.5.-gobierno-del-dato)

[5.5.1. Descubrimiento y clasificación	44](#5.5.1.-descubrimiento-y-clasificación)

[5.5.2. Gestión de metadatos y catálogo de datos	45](#5.5.2.-gestión-de-metadatos-y-catálogo-de-datos)

[5.5.3. Glosario de negocio	47](#5.5.3.-glosario-de-negocio)

[5.5.4.Linaje de datos y trazabilidad	47](#5.5.4.linaje-de-datos-y-trazabilidad)

[5.5.5. Perfilado estadístico y calidad del dato	48](#5.5.5.-perfilado-estadístico-y-calidad-del-dato)

[5.5.6. Políticas de ciclo de vida	50](#5.5.6.-políticas-de-ciclo-de-vida)

[5.6. Cumplimiento y normativas	51](#5.6.-cumplimiento-y-normativas)

[5.6.1. Residencia y soberanía del dato	51](#5.6.1.-residencia-y-soberanía-del-dato)

[5.6.2. Matriz de cumplimiento normativo	52](#5.6.2.-matriz-de-cumplimiento-normativo)

[5.6.3. Auditoría y evidencias	53](#5.6.3.-auditoría-y-evidencias)

[**6\. Estrategia operativa (DevOps)	53**](#6.-estrategia-operativa-\(devops\))

[6.1. Estándares y prácticas de ingeniería	54](#6.1.-estándares-y-prácticas-de-ingeniería)

[6.1.1. Convenciones de nomenclatura	54](#6.1.1.-convenciones-de-nomenclatura)

[6.1.1.1 Recursos cloud (infrastructura)	54](#6.1.1.1-recursos-cloud-\(infrastructura\))

[6.1.1.2 Objetos de Datos	54](#6.1.1.2-objetos-de-datos)

[6.2. Infraestructura como código (IaC)	55](#6.2.-infraestructura-como-código-\(iac\))

[6.2.1. Estrategia y herramientas	55](#6.2.1.-estrategia-y-herramientas)

[6.2.2. Gestión del Estado	55](#6.2.2.-gestión-del-estado)

[6.2.3. Modularización y reutilización	56](#6.2.3.-modularización-y-reutilización)

[6.3. Estrategia de CI/CD y gestión de versiones	56](#6.3.-estrategia-de-ci/cd-y-gestión-de-versiones)

[6.3.1. Control de versiones	56](#6.3.1.-control-de-versiones)

[6.3.2. Estrategia de branching (flujo de trabajo)	56](#6.3.2.-estrategia-de-branching-\(flujo-de-trabajo\))

[6.3.3. Pipeline de CI/CD	57](#6.3.3.-pipeline-de-ci/cd)

[6.4. Observabilidad	58](#6.4.-observabilidad)

[6.4.1. Definición de métricas	58](#6.4.1.-definición-de-métricas)

[6.4.1.1 Métricas operativas	58](#6.4.1.1-métricas-operativas)

[6.4.1.2 Métricas de calidad del dato	59](#6.4.1.2-métricas-de-calidad-del-dato)

[6.4.1.2 Métricas de infrastructura	59](#6.4.1.2-métricas-de-infrastructura)

[6.4.2. Estrategia de monitorización y dashboards	60](#6.4.2.-estrategia-de-monitorización-y-dashboards)

[6.4.3. Estrategia de logging y auditoría	60](#6.4.3.-estrategia-de-logging-y-auditoría)

[6.4.4. Matriz de alertas y respuestas	61](#6.4.4.-matriz-de-alertas-y-respuestas)

[**7\. Estrategia de validación y pruebas	62**](#7.-estrategia-de-validación-y-pruebas)

[7.1. Pruebas unitarias	62](#7.1.-pruebas-unitarias)

[7.2. Pruebas de integración	62](#7.2.-pruebas-de-integración)

[7.3. Pruebas de calidad del dato	63](#7.3.-pruebas-de-calidad-del-dato)

[7.4. Pruebas de carga y rendimiento	63](#7.4.-pruebas-de-carga-y-rendimiento)

[7.5. Pruebas de seguridad y acceso	63](#7.5.-pruebas-de-seguridad-y-acceso)

[7.6. Pruebas de aceptación de usuario (UAT)	63](#7.6.-pruebas-de-aceptación-de-usuario-\(uat\))

[**8\. Estrategia FinOps	63**](#8.-estrategia-finops)

[8.1. Estimación de costes	64](#8.1.-estimación-de-costes)

[8.1.1. Estrategia de precios y ediciones (BigQuery Editions)	64](#8.1.1.-estrategia-de-precios-y-ediciones-\(bigquery-editions\))

[8.2. Política de presupuestos y gobernanza financiera	65](#8.2.-política-de-presupuestos-y-gobernanza-financiera)

[8.3. Gestión de límites de consumo y cuotas	67](#8.3.-gestión-de-límites-de-consumo-y-cuotas)

[8.3.1. Límites de coste por usuario y proyecto	67](#8.3.1.-límites-de-coste-por-usuario-y-proyecto)

[8.3.2. Cuotas técnicas del proveedor (capacity planning)	68](#8.3.2.-cuotas-técnicas-del-proveedor-\(capacity-planning\))

[**9\. Conclusiones y próximos pasos	69**](#9.-conclusiones-y-próximos-pasos)

[**About Devoteam	70**](#about-devoteam)

# **1\. Introducción y contexto** {#1.-introducción-y-contexto}

## 1.1. Contexto y antecedentes {#1.1.-contexto-y-antecedentes}

El presente proyecto **MVP Análisis Cuentas y Forecasting** para **Roiback** se ha estructurado en tres fases estratégicas consecutivas. Tras la finalización de la **Fase de Discovery**, donde se levantaron los hallazgos de la situación actual, el proyecto entra ahora en la **Fase de Diseño**, donde se define la arquitectura técnica y funcional futura.

Este documento toma como punto de partida el entregable previamente aprobado:

* **Discovery**: Que detalla el inventario de datos, procesos actuales y deuda técnica existente.

La coherencia entre este análisis previos y el diseño técnico presentado a continuación será la base para garantizar el éxito de la implementación.

## 1.2. Propósito del documento {#1.2.-propósito-del-documento}

El objetivo de este documento es **definir la arquitectura técnica** y el **diseño detallado de la solución de datos** para el proyecto **MVP Análisis Cuentas y Forecasting**. A partir de los hallazgos validados en la fase de Discovery, este entregable traduce los requisitos de negocio en especificaciones técnicas (TO-BE), estableciendo los patrones, herramientas y modelos necesarios para la construcción de la plataforma.

En este sentido, este documento actúa como **guía prescriptiva** para el equipo de desarrollo y cumple con los siguientes objetivos fundamentales:

* **Validación Contractual**: Servir como base para la aprobación técnica por parte de **Roiback**, asegurando la alineación antes del inicio de la construcción.

* **Definición de Arquitectura Objetivo (*TO-BE*)**: Establecer el diseño detallado de la nueva plataforma, incluyendo componentes, tecnologías, flujos de datos y estándares de ingeniería.

* **Guía de Implementación**: Actuar como plan técnico para que el equipo de ingeniería ejecute el desarrollo sin ambigüedades ni bloqueos.

* **Base Documental**: Servir como documento de referencia durante todo el ciclo de vida del proyecto para garantizar la mantenibilidad futura.

En esencia, este documento abarca el diseño técnico del proyecto **MVP Análisis Cuentas y Forecasting**, cubriendo desde el nivel conceptual hasta el detalle de implementación a alto nivel alineado con las prioridades estratégicas de **Roiback**.

# **2\. Alcance del proyecto** {#2.-alcance-del-proyecto}

Esta sección establece los límites y expectativas del proyecto **MVP Análisis Cuentas y Forecasting**. Su propósito es traducir las necesidades de negocio levantadas durante la fase de Discovery en definiciones técnicas claras, asegurando que todos los involucrados compartan una visión unificada sobre qué se va a entregar, por qué es necesario y bajo qué condiciones operará.

## 2.1. Objetivos estratégicos {#2.1.-objetivos-estratégicos}

Esta sección conecta el proyecto técnico con los objetivos estratégico de **Roiback**, definiendo el porqué de alto nivel y el impacto esperado en el negocio.

* **Detección de anomalías**: Implementar un sistema de detección de anomalías para las principales métricas de negocio (TTV, Roomnights, etc.).
* **Forecasting de ventas**: Generar pronósticos de ventas para comparar con los objetivos y tomar acciones proactivas.
* **Clustering de hoteles**: Agrupar hoteles con características similares para realizar análisis comparativos.
* **Análisis conversacional**: Habilitar un asistente de IA para que los usuarios de negocio puedan consultar datos en lenguaje natural.

## 2.2. Puntos de dolor que resuelve {#2.2.-puntos-de-dolor-que-resuelve}

Esta sección enumera los problemas y fricciones actuales detectadas durante la fase de Discovery que el presente diseño resuelve:

*   **Falta de visibilidad proactiva**: Actualmente, el análisis es reactivo. Se necesita un sistema que alerte sobre desviaciones y oportunidades de forma automática.
*   **Dificultad para comparar hoteles**: No existe una forma sistemática de comparar el rendimiento de hoteles similares, lo que dificulta la identificación de buenas prácticas y áreas de mejora.
*   **Exceso de alertas irrelevantes**: El sistema actual genera un alto volumen de alertas, lo que provoca fatiga y la pérdida de foco en las incidencias críticas.
*   **Dependencia de equipos técnicos**: Los usuarios de negocio no pueden realizar consultas complejas por sí mismos, lo que genera cuellos de botella.

## 2.3. Casos de uso prioritarios {#2.3.-casos-de-uso-prioritarios}

Esta sección define los casos de uso que se han seleccionado durante la fase de Discovery a fin de enfocar el diseño hacia quién usará la solución y las tareas concretas, priorizando aquellos que aportarán valor inmediato a negocio.

*   **Detección de anomalías en KPIs**: El sistema monitorizará continuamente las métricas clave (TTV, Roomnights, Reservas) y enviará alertas a través de Slack cuando detecte desviaciones significativas con respecto al comportamiento histórico normal.
*   **Forecasting vs. Budget**: Se generarán pronósticos de ventas a 3-4 meses, que se compararán con los presupuestos cargados. Si se proyecta que un hotel no alcanzará su objetivo, se generará una alerta proactiva.
*   **Clustering dinámico de hoteles**: Se creará un modelo que agrupe hoteles en clústeres basados en su ubicación, tipología, ADR y mercados de origen. Estos clústeres se recalcularán semanalmente y se utilizarán para análisis comparativos en los dashboards.
*   **Asistente conversacional (IA)**: Se desarrollará un chatbot que permita a los DCS (Digital Channel Specialist) realizar preguntas en lenguaje natural sobre el rendimiento de los hoteles y recibir respuestas concisas, resúmenes y datos clave, con la posibilidad de verificar siempre la fuente de la información.

## 2.4. Requisitos funcionales {#2.4.-requisitos-funcionales}

En esta sección se detallan los **requisitos funcionales** que resolverá este diseño. Estos requisitos representan el *“qué”* del proyecto, definiendo el comportamiento y las capacidades que la plataforma debe ofrecer a los usuarios finales y a la organización.

*   **Fuentes de Datos**
    *   Capa raw de Roiback en BigQuery.

*   **Infraestructura**
    *   Despliegue de recursos en **GCP**.
    *   Uso de Infraestructura como Código (IaC) mediante **Terraform**.
    *   Configuración de 2 Entornos: **DEV y PRO**.

*   **Procesos y Desarrollo**
    *   Pipelines de transformación de datos con **Dataform**.
    *   Orquestación de pipelines con **Cloud Workflows**.
    *   Modelos de Machine Learning con **BigQuery ML**.

*   **Visualización/Consumo**
    *   Dashboards en **Data Studio**.
    *   Alertas en **Slack**.
    *   Asistente conversacional.

## 2.5. Requisitos técnicos (no funcionales) {#2.5.-requisitos-técnicos-(no-funcionales)}

En esta sección se detallan los **requisitos técnicos (no funcionales)** que resolverá este diseño.

*   **Escalabilidad, rendimiento y disponibilidad**:
    *   **Desacoplamiento**: La arquitectura desacoplará el almacenamiento del cómputo para permitir el escalado independiente de recursos según la carga de trabajo.
    *   **Latencia de Datos**: El sistema debe garantizar una disponibilidad del dato (Data Freshness) diaria. Los datos deben estar actualizados a las 8:30 AM con los datos del día anterior. La tabla de bookings se actualizará cada hora. GA4 dos veces al día y Salesforce cada día.
    *   **Disponibilidad**: Se necesita investigar más.
    *   **Volumetría**: Se necesita investigar más.

*   **Seguridad y Compliance**:
    *   **Gestión de Identidades (IAM)**: Implementación estricta del principio de mínimo privilegio (Least Privilege) y control de acceso basado en roles (RBAC) a nivel de servicio y de dataset.
    *   **Cifrado**: Todos los datos deben estar cifrados tanto en tránsito (TLS) como en reposo con claves gestionadas por Google (GMEK).
    *   **Seguridad de Red**: Se configurará un Firewall a nivel de VPC. Será necesaria una VPN en HA para acceder a un Postgres on-premise y a unas APIs.

*   **Ingeniería y DevOps (Mantenibilidad)**:
    *   **Infraestructura como Código (IaC)**: Todo el aprovisionamiento de recursos en GCP debe realizarse mediante **Terraform**.
    *   **CI/CD**: Los pipelines de datos deben desplegarse mediante procesos de integración y despliegue continuo automatizados con **Gitlab**.
    *   **Versionado**: Todo el código (SQL, Python, Terraform) debe estar versionado en repositorios Git (**Gitlab**) siguiendo una estrategia de Monorepo y ramas `main` + `features`.

*   **Operabilidad y Costes**:
    *   **Observabilidad**: Centralización de logs y métricas en **Google Cloud Monitoring** para permitir la trazabilidad de errores y la configuración de alertas automáticas ante fallos de pipelines.
    *   **Etiquetado (Tagging)**: Todos los recursos deben incluir etiquetas de facturación (centro de coste, entorno, proyecto) para permitir un análisis FinOps granular. Se recomienda implementar un límite de bytes procesados por query.

## 2.6. Exclusiones, supuestos y limitaciones {#2.6.-exclusiones,-supuestos-y-limitaciones}

### 2.6.1. Exclusiones {#2.6.1.-exclusiones}
*   El desarrollo no incluye datos PII por ahora.
*   No se requiere una política de archivado en Cold Storage por el momento.
*   No se requiere la historización de cambios (SCD Tipo 2).

### 2.6.2. Supuestos {#2.6.2.-supuestos}

*   Se asume que los datos en la capa raw de Roiback son de calidad suficiente para los casos de uso definidos.
*   Se asume que el cliente proporcionará acceso a las fuentes de datos necesarias.
*   Se asume que los formatos de los datos de origen no cambiarán sin previo aviso.

### 2.6.3. Limitaciones técnicas {#2.6.3.-limitaciones-técnicas}

*   La conexión a las fuentes de datos on-premise (PostgreSQL y APIs) depende de la configuración y disponibilidad de una VPN en alta disponibilidad (HA).
*   El uso de BigQuery ML puede tener limitaciones en cuanto a la complejidad de los modelos de ML que se pueden implementar en comparación con otros frameworks como TensorFlow o PyTorch.

# **3\. Diseño de arquitectura a alto nivel** {#3.-diseño-de-arquitectura-a-alto-nivel}

## 3.1. Principios de arquitectura {#3.1.-principios-de-arquitectura}

La solución se diseña siguiendo los siguientes principios fundamentales que garantizan su sostenibilidad, seguridad y escalabilidad a largo plazo.

### 3.1.1. Escalabilidad {#3.1.1.-escalabilidad}

*   **Separación Cómputo/Almacenamiento:** Uso de BigQuery, que escala ambas dimensiones de forma independiente.
*   **Servicios Serverless**: Se prioriza el uso de servicios serverless como Cloud Functions y Cloud Run para el procesamiento de datos, que escalan automáticamente según la demanda.

### 3.1.2. Diseño de seguridad {#3.1.2.-diseño-de-seguridad}

*   **Mínimo Privilegio (PoLP):** Permisos granulares limitados estrictamente a los recursos necesarios a través de IAM.
*   **Encriptación:** Datos cifrados en reposo (GMEK) y en tránsito (TLS 1.2+).
*   **Gestión de Secretos**: Uso de Secret Manager para almacenar credenciales.

### 3.1.3. Automatización {#3.1.3.-automatización}

*   **IaC:** Infraestructura como Código con Terraform para replicar entornos.
*   **CI/CD:** Despliegue automático de pipelines con Gitlab CI/CD.
*   **Orquestación**: Uso de Cloud Workflows para automatizar y programar los flujos de datos.

### 3.1.4. Observabilidad {#3.1.4.-observabilidad}

*   **Logging Centralizado:** Envío de logs estructurados a Google Cloud Logging.
*   **Monitorización**: Uso de Google Cloud Monitoring para visualizar métricas y crear dashboards.
*   **Alertas:** Notificaciones a Slack ante fallos o anomalías.

## 3.2. Diagrama de arquitectura {#3.2.-diagrama-de-arquitectura}

![Roiback - ARCH TO-BE](DISEÑO/diagramas/Roiback%20-%20ARCH%20TO-BE.png)

La arquitectura propuesta sigue un patrón ELT (Extract, Load, Transform) sobre Google Cloud Platform. El flujo de datos se puede describir de la siguiente manera:

*   **Ingesta y Orígenes**: Los datos se originan en la capa raw de Roiback, que reside en BigQuery. Para algunas fuentes de datos (Postgres on-premise y APIs) se necesitará una VPN en HA.
*   **Procesamiento y Transformación**: Se utiliza Dataform para realizar las transformaciones de datos directamente en BigQuery, siguiendo una arquitectura de medalla (Bronze, Silver, Gold). Los modelos de Machine Learning (forecasting, detección de anomalías, clustering) se entrenan y ejecutan utilizando BigQuery ML.
*   **Persistencia y Almacenamiento**: Todas las capas de datos (Bronze, Silver, Gold) se almacenan en BigQuery.
*   **Consumo**: Los datos de la capa Gold se consumen a través de dashboards en Data Studio y un asistente conversacional. Las alertas generadas por los modelos de ML se envían a un canal de Slack.

## 3.3. Descripción de componentes {#3.3.-descripción-de-componentes}

### 3.3.1. Capa de ingesta y orígenes {#3.3.1.-capa-de-ingesta-y-orígenes}

Esta capa actúa como el punto de entrada a la plataforma de datos.

**Componentes principales**

*   **BigQuery**: La capa raw de Roiback ya se encuentra en BigQuery, por lo que no se requiere un proceso de ingesta tradicional desde fuentes externas para el alcance inicial de este proyecto.
*   **VPN HA**: Para la conexión con las fuentes de datos on-premise (Postgres y APIs).

**Inventario de fuentes de datos**

| Fuente | Entidad | Volumetría estimada | Frecuencia | Método de ingesta |
| :---- | :---- | :---- | :---- | :---- |
| BigQuery (Capa Raw Roiback) | Bookings, GA4, Salesforce | Se necesita investigar más | Bookings: cada hora. GA4: dos veces al día. Salesforce: cada día. | Nativo en BigQuery |
| PostgreSQL (on-premise) | Se necesita investigar más | Se necesita investigar más | Se necesita investigar más | Vía VPN HA |
| APIs (on-premise) | Se necesita investigar más | Se necesita investigar más | Se necesita investigar más | Vía VPN HA |

### 3.3.2. Capa de procesamiento y lógica de negocio {#3.3.2.-capa-de-procesamiento-y-lógica-de-negocio}

Esta capa es el motor computacional de la arquitectura.

**Estrategia de Procesamiento Seleccionada**

*   **Procesamiento por lotes (batch)**: Se utilizará un enfoque Batch para las transformaciones de datos y el reentrenamiento de modelos de ML. Las actualizaciones de datos son diarias, con algunas fuentes actualizándose con mayor frecuencia (cada hora, dos veces al día).
*   **Arquitectura híbrida**: Para el caso de uso de dashboards, se podrán tener datos actualizados durante el día, mientras que para las alarmas se ejecutarán los procesos con menor frecuencia (una o dos veces al día).

### 3.3.3. Capa de persistencia y almacenamiento {#3.3.3.-capa-de-persistencia-y-almacenamiento}

Esta capa define cómo y dónde se guardan los datos.

**Patrón de Arquitectura de Datos**

*   La solución implementa el patrón de arquitectura Medallón (Bronze, Silver, Gold, Platinum).

**Soluciones de Almacenamiento Físico**

*   **Data Warehouse / Lakehouse (Datos Analíticos):** Se utilizará **BigQuery** como motor unificado para almacenar datos estructurados (tablas) de las capas Bronze, Silver, Gold y Platinum.

**Ciclo de Vida y Gobierno**

*   **Gestión del Ciclo de Vida (ILM):** No se aplicarán políticas de archivado a Cold Storage por el momento.
*   **Metadatos:** Se utilizará **Dataform** para la documentación y el linaje de datos, y **Data Catalog** para el gobierno de los mismos.

### 3.3.4. Capa de consumo {#3.3.4.-capa-de-consumo}

Esta capa es la interfaz entre la plataforma y los usuarios.

**Modalidades de Consumo**

*   **Business Intelligence (BI) y Reporting:**
    *   **Herramienta:** **Data Studio**.
    *   **Estrategia:** Se prioriza el uso de modelos de datos certificados (Capa Gold) para asegurar una "Single Source of Truth".
*   **Analítica Avanzada y Data Science:**
    *   **Herramienta:** **BigQuery ML** para la creación de modelos de ML.
*   **Alertas y Notificaciones:**
    *   **Mecanismo:** **Slack** para el envío de alertas de anomalías y forecasting. Se investigará la posibilidad de adjuntar gráficos.
*   **Asistente Conversacional:**
    *   Se desarrollará un asistente de IA para consultas en lenguaje natural, con respuestas concisas y la posibilidad de verificar las fuentes.

## 3.4. Decisiones de diseño {#3.4.-decisiones-de-diseño}

| Decisión | Opción elegida | Alternativa Descartada | Justificación |
| :---- | :---- | :---- | :---- |
| *Orquestación* | *Cloud Workflows* | *Cloud Composer* | Se opta por una solución serverless y de menor coste para la orquestación de los pipelines de Dataform, ya que la complejidad actual no justifica el uso de Composer. |
| *Transformación* | *Dataform* | *dbt* | Dataform se integra de forma nativa con BigQuery y ofrece funcionalidades de linaje de datos y control de versiones sin coste adicional. |
| *Machine Learning* | *BigQuery ML* | *Vertex AI, Scikit-learn* | BigQuery ML permite entrenar y desplegar modelos de ML directamente en BigQuery con SQL, lo que simplifica el desarrollo y reduce la necesidad de mover datos. Es adecuado para los casos de uso de forecasting, detección de anomalías y clustering. |
| *Gestión de código fuente* | *GitLab* | *GitHub, Bitbucket, etc.* | Es la herramienta que utiliza actualmente el cliente. |
| *Infraestructura como código* | *Terraform* | *Pulumi, CloudFormation* | Es la herramienta preferida por el cliente. |
| *Orquestador de IaC* | *Atlantis* | *Despliegue manual* | Se propone Atlantis para facilitar y automatizar los despliegues de infraestructura. |

# **4\. Diseño técnico detallado y flujos de datos** {#4.-diseño-técnico-detallado-y-flujos-de-datos}

## 4.1. Stack tecnológico {#4.1.-stack-tecnológico}

*   **Capa de ingesta**
    *   **Tecnología**: **BigQuery**, **VPN HA**
    *   **Justificación**: La capa raw de Roiback ya reside en BigQuery. La VPN se usará para conectar a fuentes on-premise.
*   **Capa de almacenamiento**
    *   **Tecnología**: **BigQuery**
    *   **Justificación**: Data warehouse serverless, escalable y con integración nativa con el resto de herramientas de GCP.
*   **Capa de transformación:**
    *   **Tecnología**: **Dataform**
    *   **Justificación**: Transformaciones SQL, control de versiones, testing y linaje de datos integrado en BigQuery.
*   **Capa de explotación:**
    *   **Tecnología**: **Data Studio**, **Slack**, **Asistente Conversacional (IA)**
    *   **Justificación**: Herramientas de BI y comunicación ya utilizadas por el cliente, y una nueva interfaz de IA para facilitar el acceso a los datos.
*   **Orquestación:**
    *   **Tecnología:** **Cloud Workflows**
    *   **Justificación**: Orquestador serverless, económico y suficiente para gestionar las dependencias de los pipelines de Dataform.
*   **MLOps**:
    *   **Tecnología**: **BigQuery ML**
    *   **Justificación**: Simplifica el ciclo de vida de los modelos de ML al estar integrado en BigQuery.

## 4.2. Diseño de data pipelines {#4.2.-diseño-de-data-pipelines}

### 4.2.1. Estrategia de carga de datos {#4.2.1.-estrategia-de-carga-de-datos}

*   **Tipo de carga:** **Incremental** para tablas de hechos (basado en `modification_timestamp` o `fecha_modificacion`) y **Full Refresh** para tablas maestras.
*   **Frecuencia de Ejecución:**
    *   Bookings: Cada hora.
    *   GA4: Dos veces al día.
    *   Salesforce: Cada día.
    *   El resto de procesos se lanzarán una vez al día, con la posibilidad de aumentar la frecuencia para los dashboards.
*   **Criterio de Reprocesamiento:** Capacidad de ejecutar cargas "Full" bajo demanda mediante parámetros en el orquestador para regenerar históricos. Los dos últimos años de datos de bookings y GA4 serán cargados inicialmente.

### 4.2.2. Estrategia de transformación de datos {#4.2.2.-estrategia-de-transformación-de-datos}

Se ha optado por un enfoque **ELT (Extract, Load, Transform)**.

*   Los datos ya están cargados en BigQuery (capa raw de Roiback).
*   Se aprovechará la potencia de cómputo de BigQuery para realizar las transformaciones con Dataform.

La herramienta principal para las transformaciones será **Dataform**, que permite definir los pipelines de SQL con control de versiones, tests y documentación.

![Roiback - Dataform](DISEÑO/diagramas/Roiback%20-%20Dataform.png)

### 4.2.3. Estrategia de calidad del dato {#4.2.3.-estrategia-de-calidad-del-dato}

*   **Framework**: **Assertions de Dataform** y **Data Quality jobs de Dataplex**.
*   **Controles implementados:**
    *   Se implementarán reglas de calidad básicas como la detección de nulos, duplicados e integridad referencial.
    *   Las reglas específicas se definirán durante la fase de implementación.
*   **Manejo de errores:** Si una regla de calidad falla, se podrá optar por detener el pipeline, enviar una alerta o mover los registros a una tabla de cuarentena. La acción a tomar se decidirá en función de la criticidad de la regla.
*   **Notificaciones:** Las alertas de calidad se enviarán a un canal de **Slack**.

### 4.2.4. Estrategia de orquestación de datos {#4.2.4.-estrategia-de-orquestación-de-datos}

Se utilizará **Cloud Workflows** para orquestar la ejecución de los pipelines de Dataform.

*   Los flujos se definirán como código (YAML) y se versionarán en Gitlab.
*   Cloud Workflows es un servicio serverless que se integra de forma nativa con Dataform.

**Organización de flujos (DAGs/Workflows)**

*   **Estrategia de agrupación**: Los flujos se organizarán por dominio de negocio y frecuencia.
*   **Nomenclatura**: `[frecuencia]_[dominio]_[accion]` (e.g., `daily_sales_gold`, `hourly_bookings_silver`). Se definirá una convención de nomenclatura detallada propuesta por Devoteam.

**Gestión de dependencias**

*   **Intra-Pipeline**: Las dependencias entre tablas dentro de un mismo pipeline se gestionarán automáticamente con la función `ref()` de Dataform.
*   **Inter-Pipeline**: Se utilizarán triggers de Cloud Workflows para encadenar la ejecución de diferentes pipelines.

**Resiliencia y gestión de errores**

*   **Errores Transitorios:** Se aplicarán 3 reintentos con una estrategia de espera exponencial (exponential backoff).
*   **Errores Fatales:** Los fallos de código o de calidad de datos detendrán el pipeline y notificarán inmediatamente.
*   **Canales de Alerta:**
    *   **Warning**: Canal de Slack `#data-ops-logs`.
    *   **Critical**: Alertas en Slack al equipo técnico de Roiback.

## 4.3. Arquitectura de Datos {#4.3.-arquitectura-de-datos}

### 4.3.1 Capa Bronze {#4.3.1-capa-bronze}

La capa bronze corresponde a la capa raw de Roiback, que ya se encuentra en BigQuery. El rol de Devoteam en esta capa es de consumidor de los datos.

*   **Formato de almacenamiento:** Datos estructurados en BigQuery.
*   **Acceso**: El equipo de Devoteam tendrá acceso de solo lectura a esta capa.
*   **Tablas relevantes**: `bookings`, `ga4`, `salesforce`, `accounts`, `properties`.
*   **Campos de modificación**: `modification_timestamp` y `fecha_modificacion` en las tablas de hechos. Las tablas dimensionales no tienen estos campos.

### 4.3.2 Capa Silver {#4.3.2-capa-silver}

En la capa silver, los datos se limpian, estandarizan y se les aplica una lógica de negocio universal.

**Especificaciones de transformación**

*   **Limpieza y normalización**
    *   **Gestión de valores nulos:** Se tratarán según la recomendación del modelo de ML (ej: imputación, `N/A`, `-1`). Para la columna de `country` en BI se mapearán los nulos.
    *   **Formatos:** Se unificarán los tipos de datos (ej: fechas a `TIMESTAMP`).
    *   **Conversión de moneda**: Se aplicará la conversión de moneda utilizando los campos `currency_rate_eur`, `currency_rate_usd` y `currency_rate_chain`.
*   **Estrategia de deduplicación:** Se eliminarán duplicados basados en las claves primarias de cada tabla.
*   **Gestión de Historia (SCD):** No se aplicará SCD Tipo 2 en esta fase del proyecto.

**Reglas de negocio en Capa Silver**
*   **Filtrado universal**: Se excluirán las reservas de prueba y aquellas con estado nulo o pendiente.
*   **Estandarización**: Se mapeará la columna `country` para los análisis de BI.

### 4.3.3 Capa Gold {#4.3.3-capa-gold}

La capa gold contiene los modelos de datos agregados y optimizados para el consumo.

**Modelo de datos**

*   **Enfoque de modelado:** **Esquema de Estrella** para los dashboards de BI, y tablas agregadas para los modelos de ML.
*   **KPIs prioritarios**: TTV (Total Transaction Value), ADR (Average Daily Rate), LoS (Length of Stay), ABV (Average Booking Value), Lead Time, RN (Room Nights), Tasa de Conversión. El cálculo del TTV se realizará sobre el campo `amount.produced.with_taxes` o `amount.produced.without_taxes` multiplicado por el ratio de conversión correspondiente.
*   **Consumo**: **Data Studio** se conectará a esta capa.
*   Se está trabajando en la definición de las tablas y campos necesarios para esta capa.

### 4.3.4 Capa Platinum {#4.3.4-capa-platinum}

La capa platinum se utilizará para exponer los resultados de los modelos de ML y para el asistente conversacional.

| Informe /Dashboard | Origen datos | Formato salida | Actualización |
| :--- | :--- | :--- | :--- |
| Alertas de Anomalías | `gold.kpi_anomalies` | Mensaje en Slack | Según se detecten |
| Alertas de Forecasting | `gold.kpi_forecast` | Mensaje en Slack | Diaria |
| Clusters de Hoteles | `gold.hotel_clusters` | Tabla en BigQuery | Semanal |
| Asistente Conversacional | Capa Gold y Platinum | API | En tiempo real |

## 4.4. Modelo de datos físico y optimización {#4.4.-modelo-de-datos-físico-y-optimización}

### 4.4.1. Diagrama de Entidad-Relación (ERD) {#4.4.1.-diagrama-de-entidad-relación-(erd)}

Se necesita investigar más. El diagrama se creará durante la fase de implementación.

### 4.4.2. Estrategia de Historización (SCD) {#4.4.2.-estrategia-de-historización-(scd)}

No se implementará historización de datos (SCD) en esta fase del proyecto.

### 4.4.3 Estrategia de particionamiento y clustering {#4.4.3-estrategia-de-particionamiento-y-clustering}

| Entidad / Tabla | Campo de Partición | Granularidad | Campo de Clustering | Justificación |
| :--- | :--- | :--- | :--- | :--- |
| `fact_bookings` | `fecha de modificación` | Día | `chain`, `hotel_id` | Las consultas se filtran habitualmente por fecha. El clustering acelera el análisis por cadena y hotel. |
| `fact_ga4` | `fecha de modificación` | Día | `chain` | Las consultas se filtran por fecha y el clustering por cadena mejora el rendimiento de los análisis a nivel de cadena. |

# **5\. Seguridad, gobierno y cumplimiento** {#5.-seguridad,-gobierno-y-cumplimiento}

## 5.1. Organización de recursos y jerarquía {#5.1.-organización-de-recursos-y-jerarquía}

Se propone la siguiente jerarquía de carpetas y proyectos en GCP, que será definida en detalle por Devoteam:

```shell
Organization: roiback.com
├── Folder: Production
│   └── Project: rb-forecasting-prod
└── Folder: Non-Production
    └── Project: rb-forecasting-dev
```

**Estrategia de etiquetado (tags)**

Se definirán etiquetas para `environment`, `cost_center` y `owner`, cuya definición concreta se realizará más adelante.

## 5.2. Gestión de identidades y accesos a datos {#5.2.-gestión-de-identidades-y-accesos-a-datos}

### 5.2.1 Estrategia de autenticación {#5.2.1-estrategia-de-autenticación}

**Usuarios**

*   El acceso se gestionará a través de **cuentas de IAM** de Google. El equipo técnico de Roiback (3 personas) tendrá acceso.

**Service Accounts**

*   Se creará una service account por entorno y componente (por ejemplo, para Dataform), siguiendo el principio de mínimo privilegio.

### 5.2.2. Matriz de roles y permisos {#5.2.2.-matriz-de-roles-y-permisos}

Se creará una matriz detallada de roles y permisos durante la fase de implementación. Se crearán grupos de usuarios para facilitar la gestión de permisos.

### 5.2.3. Gestión de secretos y credenciales {#5.2.3.-gestión-de-secretos-y-credenciales}

*   **Almacenamiento:** Se utilizará **Google Secret Manager**.
*   **Política de rotación**: Se seguirán las políticas de seguridad de Roiback.

### 5.2.4. Seguridad granular del dato {#5.2.4.-seguridad-granular-del-dato}

No se requiere seguridad a nivel de fila (RLS) ni de columna (CLS) en esta fase del proyecto, ya que no se manejarán datos PII.

### 5.2.4. Protocolo de acceso de emergencia (*glass breaker*) {#5.2.4.-protocolo-de-acceso-de-emergencia-(glass-breaker)}

Se definirá un protocolo de acceso de emergencia más adelante si es necesario.

## 5.3. Estrategias de cifrado {#5.3.-estrategias-de-cifrado}

### 5.3.1. Cifrado en tránsito {#5.3.1.-cifrado-en-tránsito}

*   Todo el tráfico entre los servicios de GCP estará cifrado por defecto.

### 5.3.2. Cifrado en reposo {#5.3.2.-cifrado-en-reposo}

*   Los datos en BigQuery y Cloud Storage estarán cifrados en reposo utilizando **claves de cifrado gestionadas por Google (GMEK)**, ya que el cliente lo considera suficiente.

### 5.3.3. Gestión de claves de cifrado (KMS) {#5.3.3.-gestión-de-claves-de-cifrado-(kms)}

Se utilizarán GMEK, por lo que las políticas de rotación de claves son las definidas por Google.

## 5.4. Seguridad de red y perímetro {#5.4.-seguridad-de-red-y-perímetro}

### 5.4.1. Arquitectura de red {#5.4.1.-arquitectura-de-red}

*   **Región principal**: Se está evaluando si utilizar `europe-west1` para aprovechar los últimos modelos de ML, o `EU` (multiregión) donde residen actualmente los datos. La decisión se tomará tras un análisis de pros y contras.

### 5.4.2. Conectividad híbrida {#5.4.2.-conectividad-híbrida}

*   **Tipo de conexión**: Se requerirá una **VPN en alta disponibilidad (HA)** para acceder a un PostgreSQL on-premise y a APIs.

### 5.4.3. Seguridad de red y controles {#5.4.3.-seguridad-de-red-y-controles}

*   **Firewalls y filtrado**: Se configurará un Firewall a nivel de VPC. No se utilizará WAF para este proyecto.

## 5.5. Gobierno del dato {#5.5.-gobierno-del-dato}

### 5.5.1. Descubrimiento y clasificación {#5.5.1.-descubrimiento-y-clasificación}

No se manejarán datos sensibles (PII) en esta fase, por lo que no se requiere configuración de Sensitive Data Protection.

### 5.5.2. Gestión de metadatos y catálogo de datos {#5.5.2.-gestión-de-metadatos-y-catálogo-de-datos}

*   **Herramienta**: Se utilizará **Data Catalog** de Google Cloud para la gestión de metadatos.
*   **Alcance**: Se indexarán los activos de BigQuery.
*   **Enriquecimiento de metadatos**: Se definirán plantillas de etiquetas para añadir contexto de negocio (dominio, criticidad, owner).
*   **Automatización de Metadatos**: Se aprovechará la integración de Dataform con Data Catalog para documentar las tablas y columnas.
![Roiback - Knowledge Catalog](DISEÑO/diagramas/Roiback%20-%20Knowledge%20Catalog%20.png)

### 5.5.3. Glosario de negocio {#5.5.3.-glosario-de-negocio}

Se definirá un glosario de negocio en Data Catalog durante la implementación, con la colaboración de los Data Stewards/Owners de Roiback. Devoteam proveerá una plantilla para facilitar este proceso.

### 5.5.4.Linaje de datos y trazabilidad {#5.5.4.linaje-de-datos-y-trazabilidad}

*   **Herramienta:** **Dataform** generará automáticamente el linaje de datos a nivel de tabla.
*   **Visualización**: El linaje se podrá visualizar en la interfaz de Dataform y en Data Catalog. No se activará la API de linaje de datos de BigQuery por el momento para controlar costes.

### 5.5.5. Perfilado estadístico y calidad del dato {#5.5.5.-perfilado-estadístico-y-calidad-del-dato}

Se implementarán reglas de calidad básicas con las `assertions` de Dataform. Las reglas específicas y umbrales de alerta se definirán durante la fase de implementación, en función de los casos de uso. Las alertas se enviarán a Slack o se visualizarán en un dashboard.

### 5.5.6. Políticas de ciclo de vida {#5.5.6.-políticas-de-ciclo-de-vida}

No se implementarán políticas de ciclo de vida en esta fase, ya que el cliente ha indicado que no es necesario por el momento.

## 5.6. Cumplimiento y normativas {#5.6.-cumplimiento-y-normativas}

### 5.6.1. Residencia y soberanía del dato {#5.6.1.-residencia-y-soberanía-del-dato}

Todos los datos se procesarán y almacenarán en la región `EU (multirregion)` o `europe-west1` de Google Cloud, en cumplimiento con la normativa GDPR.

### 5.6.2. Matriz de cumplimiento normativo {#5.6.2.-matriz-de-cumplimiento-normativo}

Se operará bajo el cumplimiento de la normativa GDPR, aunque no se manejen datos PII en esta fase. Se necesita investigar más sobre otras normativas aplicables.

# **6\. Estrategia operativa (DevOps)** {#6.-estrategia-operativa-(devops)}

## 6.1. Estándares y prácticas de ingeniería {#6.1.-estándares-y-prácticas-de-ingeniería}

### 6.1.1. Convenciones de nomenclatura {#6.1.1.-convenciones-de-nomenclatura}

Devoteam propondrá una convención de nomenclatura para los recursos de GCP y los objetos de datos (tablas, vistas, columnas), que será validada con Roiback.

## 6.2. Infraestructura como código (IaC) {#6.2.-infraestructura-como-código-(iac)}

### 6.2.1. Estrategia y herramientas {#6.2.1.-estrategia-y-herramientas}

*   **Herramienta Estándar**: **Terraform**.
*   **Orquestador de IaC**: Se propone el uso de **Atlantis** para automatizar la ejecución de Terraform a través de Pull Requests en GitLab.

### 6.2.2. Gestión del Estado {#6.2.2.-gestión-del-estado}

*   **Backend Remoto**: El estado de Terraform se almacenará en un **bucket remoto** de Google Cloud Storage con versionado y bloqueo de estado habilitados.

## 6.3. Estrategia de CI/CD y gestión de versiones {#6.3.-estrategia-de-ci/cd-y-gestión-de-versiones}

### 6.3.1. Control de versiones {#6.3.1.-control-de-versiones}

*   **Plataforma**: **GitLab**.
*   **Estrategia de repositorios**: **Monorepo**.

### 6.3.2. Estrategia de branching (flujo de trabajo) {#6.3.2.-estrategia-de-branching-(flujo-de-trabajo)}

*   **Modelo**: **Main + Features**. Se crea una rama por cada nueva funcionalidad o corrección, que se fusiona a `main` una vez validada a través de una Pull Request.

### 6.3.3. Pipeline de CI/CD {#6.3.3.-pipeline-de-ci/cd}

*   **Herramienta**: **GitLab CI/CD**.
*   **Entornos**: Se configurarán dos entornos: **DEV** y **PROD**. Se pueden añadir más bajo demanda.

## 6.4. Observabilidad {#6.4.-observabilidad}

### 6.4.1. Definición de métricas {#6.4.1.-definición-de-métricas}

Se monitorizarán métricas operativas (latencia, tasa de error), de calidad de datos (volumen, nulos, duplicados) y de infraestructura (uso de CPU, coste).

### 6.4.2. Estrategia de monitorización y dashboards {#6.4.2.-estrategia-de-monitorización-y-dashboards}

*   **Stack de monitorización**: **Google Cloud Monitoring**.
*   **Dashboards clave**: Se crearán dashboards para `Pipelines health`, `Data quality`, `Infraestructura` y `FinOps / Costes`.

### 6.4.3. Estrategia de logging y auditoría {#6.4.3.-estrategia-de-logging-y-auditoría}

*   **Centralización**: Todos los logs se enviarán a **Google Cloud Logging**.
*   **Retención**: No se requiere una política de retención de logs específica por el momento.

### 6.4.4. Matriz de alertas y respuestas {#6.4.4.-matriz-de-alertas-y-respuestas}

*   **Canales:** **Slack**.
*   **Severidad**:
    *   **CRITICAL**: Fallos en pipelines, integridad de datos comprometida. Notificación al equipo técnico de Roiback.
    *   **WARNING**: Anomalías en KPIs, degradación de la calidad de datos. Notificación al canal de Slack.
*   Se implementará un sistema de priorización de alertas para no saturar al equipo de DCS.

# **7\. Estrategia de validación y pruebas** {#7.-estrategia-de-validación-y-pruebas}

Se definirán planes de pruebas detallados para cada una de las siguientes categorías durante la fase de implementación.

## 7.1. Pruebas unitarias {#7.1.-pruebas-unitarias}
Validación de la lógica de transformación en Dataform.

## 7.2. Pruebas de integración {#7.2.-pruebas-de-integración}
Verificación de la correcta ejecución de los pipelines orquestados con Cloud Workflows.

## 7.3. Pruebas de calidad del dato {#7.3.-pruebas-de-calidad-del-dato}
Uso de `assertions` en Dataform para validar la calidad de los datos.

## 7.4. Pruebas de carga y rendimiento {#7.4.-pruebas-de-carga-y-rendimiento}
Pruebas para asegurar que la solución escala correctamente.

## 7.5. Pruebas de seguridad y acceso {#7.5.-pruebas-de-seguridad-y-acceso}
Validación de los roles y permisos de IAM.

## 7.6. Pruebas de aceptación de usuario (UAT) {#7.6.-pruebas-de-aceptación-de-usuario-(uat)}
Un grupo piloto de 4-5 personas del equipo DCS probará la herramienta y proporcionará feedback, centrándose inicialmente en un conjunto definido de hoteles clave.

# **8\. Estrategia FinOps** {#8.-estrategia-finops}

## 8.1. Estimación de costes {#8.1.-estimación-de-costes}

Se necesita investigar más para realizar una estimación detallada. Se realizará un análisis durante la fase de implementación, probando con cuentas de diferente tamaño para proyectar los costes.

### 8.1.1. Estrategia de precios y ediciones (BigQuery Editions) {#8.1.1.-estrategia-de-precios-y-ediciones-(bigquery-editions)}

Se evaluará el uso de BigQuery Editions (reservas de slots) frente al modelo bajo demanda para optimizar costes, especialmente considerando el uso intensivo de queries para los modelos de ML. Se analizará la viabilidad de adquirir una reserva para reducir los costes.

## 8.2. Política de presupuestos y gobernanza financiera {#8.2.-política-de-presupuestos-y-gobernanza-financiera}

Se definirán presupuestos y alertas en Google Cloud para monitorizar los costes una vez se tenga una estimación más clara. La acción a tomar en caso de superar el presupuesto será notificar al equipo responsable (TBD Roiback).

## 8.3. Gestión de límites de consumo y cuotas {#8.3.-gestión-de-límites-de-consumo-y-cuotas}

### 8.3.1. Límites de coste por usuario y proyecto {#8.3.1.-límites-de-coste-por-usuario-y-proyecto}

Se recomienda aplicar límites de bytes procesados por query para evitar consultas costosas por parte de los usuarios. Las cuentas de servicio de Dataform estarán exentas de estos límites. Los límites concretos se definirán más adelante (TBD).

### 8.3.2. Cuotas técnicas del proveedor (capacity planning) {#8.3.2.-cuotas-técnicas-del-proveedor-(capacity-planning)}

No se prevé la necesidad de aumentar cuotas de API, ya que no se utilizarán de forma intensiva. Se usarán las regiones `EU` y `europe-west1`, verificando la disponibilidad de cuota en cada una.

# **9\. Conclusiones y próximos pasos** {#9.-conclusiones-y-próximos-pasos}

El presente diseño cubre los requisitos establecidos y ofrece una base sólida para la implementación de la plataforma del dato de **Roiback**.

**Próximos pasos inmediatos**

1.  Aprobación formal de este documento por parte de **Roiback**.
2.  Desarrollo del **Roadmap** de implementación con el estudio de la brecha entre la situación AS IS y TO BE, el detalle, estimación y temporalización de las actividades a desarrollar así como el dimensionamiento del equipo y costes de construcción y mantenimiento.

| About Devoteam Devoteam is a tech consulting firm specialised in cloud, cybersecurity, data, and sustainability. Tech Native for over 25 years, Devoteam guides businesses through sustainable digital transformation to unlock their full potential. With over 10,000 employees in more than 25 countries across Europe, the Middle East, and Africa, Devoteam is committed to putting technology at the service of people. To realise this vision, we partner with the top cloud platforms in the world, Microsoft Azure, Google Cloud, and AWS. |
| :--- |
