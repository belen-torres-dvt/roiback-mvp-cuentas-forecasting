# 

# 

# 

# \#\#Cliente\#\# \- \#\#Proyecto\#\#

## 

## Diseño

**Hoja de control**

**Control de documentación**

|  |  |
| :---- | :---- |
| **Document Code** | \#\#Cliente\#\#- \#\#Proyecto\#\# \- Entregable diseño |
| **Preparado por:** | \#\#Nombre técnico Devoteam\#\# |
| **Fecha** | \#\#dd/mm/yyyy\# |

**Control de versiones**

| Versión | Autor | Fecha | Comentarios |
| :---- | :---- | :---- | :---- |
| v1.0.0 | Data Accelerator | 16 Jan 2026 | Plantilla entregable Diseño |
|  |  |  |  |
|  |  |  |  |

**Control de revisión y aprobación**

|  | Nombre | Fecha | Firma |
| :---- | :---- | :---- | :---- |
| **Revisado por** |  |  |  |
| **Aprobado por** |  |  |  |

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

[5.6.3. Auditoría  y evidencias	53](#5.6.3.-auditoría-y-evidencias)

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

# **Instrucciones de uso de esta plantilla** {#instrucciones-de-uso-de-esta-plantilla}

**Esta página debe eliminarse antes de la entrega del documento al cliente**.

- Usar siempre fuente **Montserrat Normal** (en estilo estándar o negrita, según convenga) con **tamaño 10.5** e **interlineado de 1.15** en bloques de texto.

- Respetar los **formatos de título** (Heading 1, Heading 2 y Heading 3 con sus respectivos tamaños de fuente) definidos en este documento.

- Tened cuidado de no modificar la fuente o espaciado por accidente al copiar y pegar desde otros orígenes.

- La **orientación** del documento será siempre **vertical** y se deberán respetar los márgenes del documento evitando en todo momento que las imágenes, diagramas o tablas excedan dichos márgenes.

- Una vez finalizado el documento **regenerar el índice** y comprobar formatos ya que suelen alterarse cambiando la fuente a otra que no es Montserrat.

- Los comentarios añadidos con *\#\#sombreado gris y en cursiva\#\#* deben **eliminarse o reemplazarse** por el texto adecuado ya que son ejemplos ilustrativos o notas con referencias a documentos externos. En todo caso, se debe revisar que no exista ningún comentario con este formato en el momento de la entrega a Cliente. *\#\#sombreado rojo y en cursiva\#\#*  se encuentra la explicación de qué rellenar en las secciones, eliminar después de rellenar  
- **Eliminar** todas las explicaciones que empiezan y acaban por los caracteres “**\#**”

- Los links a los documentos de anexos (checklist, inventario de recursos o similares) deberán clonarse desde sus respectivas plantillas del [Shared Drive del Acelerador](https://drive.google.com/drive/folders/1VYaRYObi9oXvUWdEs05b_CJVBtz3XCi2?usp=sharing) y hacer una copia editable en la carpeta del cliente, para así vincularlos a este documento.

# **1\. Introducción y contexto** {#1.-introducción-y-contexto}

## 1.1. Contexto y antecedentes {#1.1.-contexto-y-antecedentes}

El presente proyecto *\#\#Nombre del Proyecto\#\#* para *\#\#Cliente\#\#* se ha estructurado en tres fases estratégicas consecutivas. Tras la finalización de la **Fase de Discovery**, donde se levantaron los hallazgos de la situación actual, el proyecto entra ahora en la **Fase de Diseño**, donde se define la arquitectura técnica y funcional futura.

Este documento toma como punto de partida el entregable previamente aprobado:

* **Discovery** *\#\#Añadir link a documento de Discovery linkado a la palabra Discovery\#\#*: Que detalla el inventario de datos, procesos actuales y deuda técnica existente.

La coherencia entre este análisis previos y el diseño técnico presentado a continuación será la base para garantizar el éxito de la implementación.

## 1.2. Propósito del documento {#1.2.-propósito-del-documento}

El objetivo de este documento es **definir la arquitectura técnica** y el **diseño detallado de la solución de datos** para el proyecto *\#\#Nombre del Proyecto\#\#*. A partir de los hallazgos validados en la fase de Discovery, este entregable traduce los requisitos de negocio en especificaciones técnicas (TO-BE), estableciendo los patrones, herramientas y modelos necesarios para la construcción de la plataforma.

En este sentido, este documento actúa como **guía prescriptiva** para el equipo de desarrollo y cumple con los siguientes objetivos fundamentales:

* **Validación Contractual**: Servir como base para la aprobación técnica por parte de *\#\#Cliente\#\#*, asegurando la alineación antes del inicio de la construcción.

* **Definición de Arquitectura Objetivo (*TO-BE*)**: Establecer el diseño detallado de la nueva plataforma, incluyendo componentes, tecnologías, flujos de datos y estándares de ingeniería.

* **Guía de Implementación**: Actuar como plan técnico para que el equipo de ingeniería ejecute el desarrollo sin ambigüedades ni bloqueos.

* **Base Documental**: Servir como documento de referencia durante todo el ciclo de vida del proyecto para garantizar la mantenibilidad futura.

En esencia, este documento abarca el diseño técnico del proyecto *\#\#Nombre del Proyecto\#\#*, cubriendo desde el nivel conceptual hasta el detalle de implementación a alto nivel alineado con las prioridades estratégicas de *\#\#Cliente\#\#*.

# **2\. Alcance del proyecto**  {#2.-alcance-del-proyecto}

Esta sección establece los límites y expectativas del proyecto *\#\#Nombre del Proyecto\#\#*. Su propósito es traducir las necesidades de negocio levantadas durante la fase de Discovery en definiciones técnicas claras, asegurando que todos los involucrados compartan una visión unificada sobre qué se va a entregar, por qué es necesario y bajo qué condiciones operará.

## 2.1. Objetivos estratégicos {#2.1.-objetivos-estratégicos}

Esta sección conecta el proyecto técnico con los objetivos estratégico de *\#\#Cliente\#\#*, definiendo el porqué de alto nivel y el impacto esperado en el negocio.

*\#En este apartado se espera un resumen ejecutivo de los objetivos estratégicos levantados durante la fase de Discovery (ver apartado **2.1. Objetivos Estratégicos** del documento de Discovery) de forma que aparezcan priorizados y sean tenidos en cuenta en la fase de Diseño.* 

*Enumerar usando bullet points y destacar en negrita las palabras clave para mayor claridad.\#*

\# **Ejemplo:**

* **Democratización del Dato**: Habilitar a los equipos de Marketing y Ventas para acceder a datos en tiempo real sin dependencia del equipo de TI.  
* **Reducción de Costes:** Migrar la infraestructura on-premise a la nube para reducir el TCO (Total Cost of Ownership) en un 20%.  
* **Cumplimiento Normativo:** Garantizar que el tratamiento de datos de clientes cumpla estrictamente con la GDPR/RGPD.  
* **Optimización de Procesos:** Automatizar la generación de informes financieros, reduciendo el tiempo de entrega de 5 días a 4 horas.

\#

## 2.2. Puntos de dolor que resuelve {#2.2.-puntos-de-dolor-que-resuelve}

Esta sección enumera los problemas y fricciones actuales detectadas durante la fase de Discovery que el presente diseño resuelve:

*\#Se espera un resumen ejecutivo de los puntos de dolor detectados en la fase de Discovery (ver apartado **6.2 Identificación de puntos de dolor** del documento de Discovery) de forma que aparezcan priorizados y sean tenidos en cuenta en la fase de Diseño.* 

*Enumerar usando bullet points y destacar en negrita las palabras clave para mayor claridad detallando el problema a resolver, su impacto en el negocio, las métricas que lo evidencias y por qué es crítico resolverlo\#*

\#Ejemplo:

* **Ineficiencia operativa en Reporting**  
  * **Problema:** El equipo financiero consolida manualmente hojas de cálculo de 4 fuentes distintas para el cierre mensual.  
  * **Impacto en negocio:** Retraso en la entrega de informes a dirección y alto riesgo de errores humanos en fórmulas críticas.  
  * **Métricas / Evidencia:** Se invierten **\[20 horas/semana\]** por analista en limpieza de datos; tasa de error actual del **\[15%\]** en el primer borrador.  
  * **Criticidad:** Alta. La dirección no tiene visibilidad del cierre hasta el día 10 del mes siguiente, impidiendo correcciones tácticas rápidas.

\#

## 2.3. Casos de uso prioritarios {#2.3.-casos-de-uso-prioritarios}

Esta sección define los casos de uso que se han seleccionado durante la fase de Discovery a fin de enfocar el diseño hacia quién usará la solución y las tareas concretas, priorizando aquellos que aportarán valor inmediato a negocio.

*\#Enumerar usando bullet points, destacar en negrita las palabras clave para mayor claridad y hacer resumen del caso de uso.\#*

\#Ejemplo:

* **Dashboard Ejecutivo:** El CEO y directores podrán visualizar los KPIs diarios de ventas desglosados por región antes de las 9:00 AM.  
* **Modelo de Propensión de Fuga:** El equipo de retención recibirá una lista diaria de clientes con alta probabilidad de baja (churn) para activar campañas preventivas.  
* …

\#

## 2.4. Requisitos funcionales {#2.4.-requisitos-funcionales}

En esta sección se detallan los **requisitos funcionales** que resolverá este diseño. Estos requisitos representan el *“qué”* del proyecto, definiendo el comportamiento y las capacidades que la plataforma debe ofrecer a los usuarios finales y a la organización.

*\#\# Seguir el formato de bulletpoints por requisito funcional  organizados en torno a títulos en negrita y agrupando los requisitos de la misma tipología o tópico y describiendo lo que se persigue con dichos requisitos. Se pueden rescatar de aquellos detectados en la fase de Discovery (sección 2.3.1. Requisitos funcionales) o según el ejemplo adjunto.\#*

* **Fuentes de Datos**  
  * *Fuente de datos \#1: \[CRM, ERP, API Externa\]*.  
  * *Fuente de datos \#2: \[CRM, ERP, API Externa\]*.  
  * …

* **Infraestructura**  
  * Despliegue de recursos en *CLOUD PROVIDER (GCP/AWS)*   
  * Uso de Infrastructure as Code mediante *\#HERRAMIENTA\_IAC\#(Terraform/Pulumi/CloudFormation).*  
  * *Configuración de \# X NÚMERO\_ENTORNOS\# Entornos: \#LISTA\_ENTORNOS ej (Dev, QA, Prod)\#*

* **Procesos y Desarrollo**  
  * *\[Lista de pipelines/transformaciones,  orquestación…\]*

* **Visualización/Consumo**  
  * *Creación de \[X\] dashboards en \[HERRAMIENTA\] y/o exposición de \[X\] vistas de datos.*  
* ***…***

## 2.5. Requisitos técnicos (no funcionales) {#2.5.-requisitos-técnicos-(no-funcionales)}

En esta sección se detallan los **requisitos técnicos (no funcionales)** que resolverá este diseño. Estos requisitos representan el “cómo” del proyecto, definiendo el marco tecnológico, la arquitectura y los estándares de ingeniería necesarios para soportar las funcionalidades de negocio. Se centran en la infraestructura y la calidad del software, definiendo cómo se deben construir, asegurar y optimizar las soluciones en el entorno de la nube (GCP) para garantizar el rendimiento, escalabilidad y mantenimiento a futuro.

*\#\# Seguir el formato de bulletpoints por requisito técnico (no funcional)  organizados en torno a títulos en negrita y agrupando los requisitos de la misma tipología o tópico y describiendo lo que se persigue con dichos requisitos. Se pueden rescatar de aquellos detectados en la fase de Discovery (sección 2.3.2. Requisitos técnicos (no funcionales)) o según el ejemplo adjunto.\#*

*\# Ejemplo*

* ***Escalabilidad, rendimiento y disponibilidad**:*  
  * ***Desacoplamiento**: La arquitectura debe desacoplar el almacenamiento del cómputo para permitir el escalado independiente de recursos según la carga de trabajo.*  
  * ***Latencia de Datos**: El sistema debe garantizar una disponibilidad del dato (Data Freshness) acorde al SLA definido (ej. Batch diario antes de las 08:00 AM o Near-Real-Time con latencia \< 5 min).*  
  * ***Tiempos de Respuesta**: Las consultas analíticas estándar no deben exceder los \#\#X\#\# segundos de ejecución para garantizar una buena experiencia de usuario en los dashboards.*  
  * ***Disponibilidad**: El sistema debe estar disponible un \#XX.X%\# (SLA).*  
  * ***Volumetría**: El sistema debe soportar \#X GB\# de ingesta diaria/semanal/mensual, con un crecimiento estimado de \#X Gb\# al \#mes/dia/año\#.*  
  * ***Latencia**:  Los procesos batch finalizarán antes de las \#HH:MM\# cada día. / Las APIs responderán en \< \#X\#ms.*  
  * ***RTO/RPO \#SI APLICA\#**: En caso de desastre, se aceptan \#X horas\# de pérdida de datos (RPO) y \#Y horas\# para recuperar el servicio (RTO).*

* ***Seguridad y Compliance**:*  
  * ***Gestión de Identidades (IAM)**: Implementación estricta del principio de mínimo privilegio (Least Privilege) y control de acceso basado en roles (RBAC) a nivel de servicio y de dataset.*  
  * ***Cifrado**: Todos los datos deben estar cifrados tanto en tránsito (TLS) como en reposo (Claves gestionadas por Google o CMEK según proceda).*  
  * ***Seguridad de Red**: Los servicios de datos no deben tener IPs públicas expuestas; la comunicación debe realizarse dentro de una VPC privada o mediante túneles seguros.*

* ***Ingeniería y DevOps (Mantenibilidad)**:*  
  * ***Infraestructura como Código (IaC)**: Todo el aprovisionamiento de recursos en GCP debe realizarse mediante código (ej. Terraform), evitando configuraciones manuales en consola.*  
  * ***CI/CD**: Los pipelines de datos deben desplegarse mediante procesos de integración y despliegue continuo automatizados, con tests unitarios y de integración.*  
  * ***Versionado**: Todo el código (SQL, Python, Terraform) debe estar versionado en repositorios Git siguiendo una estrategia de ramas definida (ej. GitFlow o Trunk-based).*

* ***Operabilidad y Costes**:*  
  * ***Observabilidad**: Centralización de logs y métricas para permitir la trazabilidad de errores y la configuración de alertas automáticas ante fallos de pipelines.*  
  * ***Etiquetado (Tagging)**: Todos los recursos deben incluir etiquetas de facturación (ej. centro de coste, entorno, proyecto) para permitir un análisis FinOps granular.*  

*\#\#*

## 2.6. Exclusiones, supuestos y limitaciones {#2.6.-exclusiones,-supuestos-y-limitaciones}

En esta sección se detallan aquellos aspectos que delimitan el alcance del proyecto de forma explícita así como aquellas asunciones se han hecho y las restricciones técnicas existentes.

*\#\# Seguir el formato de bulletpoints en torno a títulos en negrita y agrupando las exclusiones, supuestos o limitaciones técnicas de la misma tipología o tópico y el motivo (si aplica).\#*

### 2.6.1. Exclusiones {#2.6.1.-exclusiones}

*\# Ejemplos*

* *No se migrarán datos históricos anteriores al año \#Año\#.*  
* *La integración con la API de \#Nombre API\# queda pendiente para la fase 2\.*  
* *No se incluye formación a usuarios finales (solo a train-the-trainers).*

*\#*

### 2.6.2. Supuestos {#2.6.2.-supuestos}

*\# Ejemplos*

* *Se asume que el cliente proporcionará acceso a los datos el día X*  
* *La calidad del dato en origen es responsabilidad del sistema fuente*

*\#*

Para evitar ambigüedades y desviaciones, se excluyen explícitamente del scope del presente proyecto: 

* *\#\[Exclusión 1\]\# ej Migración de datos históricos \#SI APLICA\#*  
* *\#\[Exclusión 2\]\# ej Gobernanza de datos*  
* *\#\[Exclusión 3\]\# ej Mantenimiento de la estructura post deployment (SI NO ESTÁ CONTRATADO)*

###  2.6.3. Limitaciones técnicas {#2.6.3.-limitaciones-técnicas}

*\# Ejemplos*

* *El cliente usa una VPN específica, no se permite IPs públicas, etc.\]\#*  
* *Ej: Compliance: Los datos no pueden salir de la región europe-west1.*

*\#*

# **3\. Diseño de arquitectura a alto nivel** {#3.-diseño-de-arquitectura-a-alto-nivel}

Este apartado define la **visión estructural** de la solución diseñada describiendo los principios arquitectónicos, el diagrama general de bloques y la justificación de las decisiones arquitectónicas clave proporcionando una **foto a alto nivel** del sistema.

## 3.1. Principios de arquitectura {#3.1.-principios-de-arquitectura}

La solución se diseña siguiendo los siguientes principios fundamentales que garantizan su sostenibilidad, seguridad y escalabilidad a largo plazo.

*\#\# Seguir el formato de bulletpoints en torno a títulos en negrita y agrupando elementos de la misma tipología o tópico y dando una pequeña explicación (ver ejemplos).\#*

### 3.1.1. Escalabilidad {#3.1.1.-escalabilidad}

El objetivo de esta solución es garantizar que el sistema soporte crecimiento en volumen de datos y concurrencia sin degradación del servicio.

*\# Ejemplos*

* ***Separación Cómputo/Almacenamiento:** Uso de arquitecturas (ej.BigQuery) que escalan ambas dimensiones de forma independiente.*  
* ***Escalado Horizontal:** Procesamiento distribuido en clusters efímeros que se auto-ajustan según la carga.*  
* *…*

*\#*

### 3.1.2. Diseño de seguridad {#3.1.2.-diseño-de-seguridad}

El objetivo de esta solución es proteger la integridad y confidencialidad mediante un enfoque “Zero Trust”.

*\# Ejemplos*

* ***Mínimo Privilegio (PoLP):** Permisos granulares limitados estrictamente a los recursos necesarios.*  
* ***Encriptación:** Datos cifrados en reposo y en tránsito (TLS 1.2+).*  
* *…*

*\#*

### 3.1.3. Automatización {#3.1.3.-automatización}

El objetivo de esta solución es minimizar la intervención manual para reducir errores y acelerar el *Time-to-Market*.

*\# Ejemplos*

* ***IaC:** Infraestructura como Código (Terraform) para replicar entornos.*  
* ***CI/CD:** Despliegue automático de pipelines tras validación de tests.*  
* *…*

*\#*

### 3.1.4. Observabilidad {#3.1.4.-observabilidad}

El objetivo de esta solución es tener visibilidad total sobre la salud de los procesos y la calidad del dato.

*\# Ejemplos*

* ***Logging Centralizado:** Envío de logs estructurados a la herramienta de monitorización corporativa.*  
* ***Alertas:** Notificaciones multicanal (Email/Slack) ante fallos de SLA.*  
* *…*

*\#*

## 3.2. Diagrama de arquitectura {#3.2.-diagrama-de-arquitectura}

*\# Insertar aquí el diagrama de arquitectura siguiendo el formato de las [plantillas de Lucidcharts del Squad](https://lucid.app/lucidchart/1e7860c8-a29b-4262-9413-44dccb320701/edit?viewport_loc=-3395%2C-599%2C9490%2C4810%2C0_0&invitationId=inv_49e1e952-1c05-4449-93b8-9c0d5b884c19) \#*

*![][image1]*

*\# Hacer a continuación un resumen ejecutivo de la arquitectura y el flujo de datos de izquierda a derecha: desde la ingesta de fuentes de datos heterogéneas, pasando por el almacenamiento hasta su refinamiento, procesado y exposición en herramientas de BI. Destacar los componentes principales y sus relaciones. El detalle más profundo se hará en la* [sección 3.3.](#3.3.-descripción-de-componentes)*\#*

*\#Ejemplo:*

*La arquitectura propuesta implementa un patrón ELT (Extract, Load, Transform) sobre infraestructura Cloud, diseñado para centralizar la información dispersa de la organización en una única fuente de verdad. El diagrama anterior ilustra el flujo de datos de izquierda a derecha, dividido en cuatro etapas lógicas…*

* ***Ingesta y landing:**  Los datos se capturan desde fuentes heterogéneas: el CRM (Salesforce) y el ERP (SAP) mediante conectores gestionados, y archivos planos (CSV/Excel) desde servidores FTP.  Se utiliza un enfoque de "mínima transformación" en la entrada para asegurar que los datos llegan al lago lo antes posible. Todos los datos aterrizan inicialmente en la Capa Bronze (Raw) del Data Lakehouse.*

* ***Procesamiento y Transformación:** El motor de transformación (dbt) recoge los datos crudos y aplica reglas de limpieza, tipado y estandarización para moverlos a la Capa Silver. Posteriormente, se ejecutan las agregaciones y cruces de negocio para generar el modelo dimensional (Estrella) en la Capa Gold. Todo este proceso está orquestado centralmente para gestionar las dependencias (ej. no procesar ventas hasta tener actualizados los clientes).*

* ***Persistencia y almacenamiento:** Todos los datos aterrizan inicialmente en la Capa Bronze (Raw) del Data Lakehouse. Aquí se almacenan en su formato original para garantizar la inmutabilidad y permitir la auditoría o reprocesamiento futuro. Los archivos no estructurados (PDFs, imágenes) se desvían a Cloud Storage, mientras que los datos tabulares entran directamente a tablas de staging.*

* ***Consumo:** En el extremo derecho, las herramientas de BI (Looker/Tableau) se conectan exclusivamente a la Capa Gold para garantizar rendimiento y consistencia. Se expone una API segura para que aplicaciones de terceros puedan consumir datos procesados (Reverse ETL).\#*

## 3.3. Descripción de componentes {#3.3.-descripción-de-componentes}

Tras visualizar la arquitectura en el diagrama anterior, esta sección detalla los componentes lógicos y físicos que conforman la solución. Aquí se define la estrategia de ingesta, el paradigma de procesamiento y el patrón de almacenamiento que soportará los requisitos del negocio.

### 3.3.1. Capa de ingesta y orígenes {#3.3.1.-capa-de-ingesta-y-orígenes}

Esta capa actúa como el punto de entrada a la plataforma de datos. Es responsable de la conectividad con los sistemas externos, la autenticación y el transporte seguro de la información hacia la landing zone.

La estrategia de ingesta prioriza mecanismos que minimicen el impacto en los sistemas operacionales (origen) y garanticen la integridad de los datos transferidos.

**Componentes principales**

*\#Ejemplo*

* ***Ejemplo 1 (SaaS/Connectors):** Servidores de Ingesta Gestionada (ej. Fivetran/Airbyte) para la replicación automática de fuentes SaaS y Bases de Datos estándar.*  
* ***Ejemplo 2 (Custom):** Cloud Functions / Lambdas para la ingesta de APIs propietarias o sin conectores estándar.*  
* ***Ejemplo 3 (Eventos):** Bus de Mensajería (ej. Kafka/PubSub) para la captura de eventos en tiempo real.\#*

**Inventario de fuentes de datos**  
Basándonos en los hallazgos realizados durante la fase discovery se identifican las siguientes fuentes de datos con las siguientes características:

| Fuente | Entidad | Volumetría estimada | Frecuencia | Método de ingesta |
| :---- | :---- | :---- | :---- | :---- |
| *SQL Server (on-prem)* | *Tabla XXX* |  *\~50GB carga inicial* | *200MB* | *Diaria 2:00 AM \- 4:00 AM* |
| *API externa* | *Endpoint XX* | *\~150GB carga inicial* | *Desconocido* | *TBD* |

*\#Si esta tabla es demasiado extensa por la cantidad de fuentes, se puede usar el siguiente documento [\[Template\] Inventario de recursos descubiertos](https://docs.google.com/spreadsheets/u/0/d/14CH4-j3OeSWCYkWHzswKdCXA6nZ-c3Wfsw7Ec891IWI/edit) y mención a la pestaña correspondiente para que el documento quede más limpio. DE NO SER NECESARIO BORRAR EL LINK y la pestaña del archivo\#*

### 3.3.2. Capa de procesamiento y lógica de negocio {#3.3.2.-capa-de-procesamiento-y-lógica-de-negocio}

Esta capa actúa como el motor computacional de la arquitectura. En ella residen los algoritmos y reglas que transforman los datos crudos en activos de información aplicando limpieza, estandarización, enriquecimiento y agregación.

**Estrategia de Procesamiento Seleccionada**

*\#Ejemplos*

* ***Procesamiento por lotes (batch)***  
  *Se utilizará un enfoque Batch para cargas masivas y periódicas. Los datos se procesan en ventanas de tiempo definidas (ej. diariamente, cada hora), lo que permite optimizar costes y manejar grandes volúmenes de historia. Es el estándar para Business Intelligence y Reporting regulatorio.*  
* ***Procesamiento en Tiempo Real (streaming)***  
  *Se utilizará un enfoque Streaming para procesar los datos evento a evento a medida que se generan. Esta estrategia es necesaria para casos de uso que requieren latencia inferior a segundos/minutos, como detección de fraude, personalización en vivo o monitorización operativa.*  
* ***Arquitectura híbrida***  
  *Se implementará una arquitectura híbrida con una "Speed Layer" (Streaming) para datos en tiempo real y una "Batch Layer" para la consolidación histórica y corrección de datos.*

*\#*

### 3.3.3. Capa de persistencia y almacenamiento {#3.3.3.-capa-de-persistencia-y-almacenamiento}

Esta capa es donde se define cómo y dónde se guardan los datos a lo largo de su ciclo de vida. La arquitectura de almacenamiento debe equilibrar el coste, el rendimiento de lectura y la capacidad de recuperación ante desastres.

**Patrón de Arquitectura de Datos**

La solución implementa el patrón de arquitectura Medallón (Bronze, Silver, Gold). Este enfoque organiza los datos en zonas de calidad creciente, garantizando que el dato fluya desde su estado crudo (Bronze) hasta un estado refinado y validado (Silver), finalizando en modelos optimizados para el consumo (Gold). Esto asegura trazabilidad completa y permite regenerar el sistema desde la fuente en caso de error.

*\#Alternativa (si aplica): Data Vault / Data Mesh.\#*

**Soluciones de Almacenamiento Físico**

Se adopta una estrategia de almacenamiento *\#\[Híbrida / Cloud Native\]\#*:

*\# Ejemplos*

* ***Data Lake (Datos No Estructurados / Raw):***  
  * *Ejemplo: Se utilizará **Object Storage (S3 / GCS / Azure Blob)** para almacenar archivos en formato original (CSV, JSON, PDF), logs y copias de seguridad. Es la base de la capa Bronze.*  
* ***Data Warehouse / Lakehouse (Datos Analíticos):***  
  * *Ejemplo: Se utilizará **\[BigQuery / Snowflake / Databricks\]** como motor unificado para almacenar datos estructurados (tablas) de las capas Silver y Gold, permitiendo consultas SQL de alto rendimiento.*

*\#*

**Ciclo de Vida y Gobierno**  
Para garantizar la eficiencia de costes y el cumplimiento normativo , se aplican las siguientes políticas:

*\#Ejemplos*

* ***Gestión del Ciclo de Vida (ILM):** Los datos en la capa Raw con antigüedad superior a **\[X años\]** se moverán automáticamente a clases de almacenamiento "Cold/Archive" (más baratas, acceso más lento).*  
* ***Metadatos:** Se utilizará un Catálogo de Datos centralizado para registrar definiciones, propietarios del dato (Data Owners) y linaje.*

*\#*

### 3.3.4. Capa de consumo {#3.3.4.-capa-de-consumo}

Esta capa representa la interfaz entre la plataforma técnica de datos y los usuarios de negocio o aplicaciones externas. Su objetivo es democratizar el acceso a la información, garantizando que los datos procesados en las capas anteriores estén disponibles de forma segura, gobernada y en el formato adecuado para cada tipo de consumidor (humano o máquina).

*\#Adaptar según lo que se vaya a hacer en esta capa.\#*

**Modalidades de Consumo**

*\#Ejemplos*

* ***1\. Business Intelligence (BI) y Reporting:***  
  *Orientado a la visualización de datos, seguimiento de KPIs y toma de decisiones estratégicas.*  
  * ***Herramienta:** **\[Ej. Power BI / Tableau / Looker / Qlik\]**.*  
  * ***Estrategia:** Se prioriza el uso de modelos de datos certificados (Capa Gold) para asegurar que todos los departamentos reporten las mismas cifras ("Single Source of Truth"). Se habilita también un entorno Self-Service controlado para usuarios avanzados.*  
* ***2\. Analítica Avanzada y Data Science:***  
  *Entornos dedicados a la exploración profunda, minería de datos y desarrollo de modelos de Machine Learning.*  
  * ***Herramienta:** **\[Ej. Jupyter Notebooks / Vertex AI / Databricks Notebooks\]**.*  
  * ***Acceso:** Conexión directa a las capas Silver (para datos granulares) y Gold, con capacidad de cómputo aislada para no afectar el rendimiento de los reportes corporativos.*  
* ***3\. Integración de Datos (Reverse ETL / APIs):***  
  *Mecanismos para "activar" el dato, enviando información procesada de vuelta a los sistemas operativos o aplicaciones de terceros.*  
  * ***Mecanismo:** **\[Ej. Reverse ETL (Hightouch/Census) / API REST propia / Exportación a FTP\]**.*  
  * ***Caso de Uso:** Enviar segmentos de clientes calculados en el Data Warehouse hacia el CRM (Salesforce) o la herramienta de Email Marketing para campañas personalizadas. \#*

**Seguridad en el Consumo**

El acceso en esta capa se rige por estrictas políticas de seguridad que se definirán con mayor detalle en la [sección 5.2.4](#5.2.4.-seguridad-granular-del-dato) pero que incluyen:

* **RBAC (Role-Based Access Control):** Los usuarios solo ven los datos pertinentes a su rol (ej. Un Manager de Ventas solo ve su región).  
* **Row-Level Security (RLS):** Filtrado automático de filas según los permisos del usuario logueado.

##  3.4. Decisiones de diseño {#3.4.-decisiones-de-diseño}

En este apartado se documentan las decisiones arquitectónicas y tecnológicas adoptadas para la solución así como su justificación. El objetivo de esta sección no es realizar un listado exhaustivo de todas las herramientas elegidas, sino registrar aquellas elecciones críticas donde existían varias alternativas viables. En este sentido, se explica el porqué de la selección final basada en criterios objetivos (coste, rendimiento, time-to-market, skills del equipo o restricciones de seguridad), dejando constancia de las alternativas descartadas para evitar re-evaluaciones futuras redundantes.

| Decisión | Opción elegida | Alternativa Descartada | Justificación |
| :---- | :---- | :---- | :---- |
| *Orquestación* | *Cloud Workflows* | *Cloud Composer* | *El volumen de datos hace que no merezca la pena la instalación . . .*  |
| *\#Decisión\#* | *\#Elección\#* | *\#Alternativa\#* | *\#Justificación\#* |

# 

# **4\. Diseño técnico detallado y flujos de datos** {#4.-diseño-técnico-detallado-y-flujos-de-datos}

Esta sección desciende al nivel de implementación (bajo nivel) detallando la configuración del stack, la lógica de los pipelines, las especificaciones por capa de la arquitectura de datos y las estrategias de optimización física.

El stack tecnológico detallado a continuación puede estar sujeto a ajustes menores durante la implementación basados en hallazgos técnicos o cambios en requisitos. Cualquier cambio significativo será comunicado y documentado.

## 4.1. Stack tecnológico {#4.1.-stack-tecnológico}

*\#\# Seguir el formato de bulletpoints en torno a títulos en negrita (por capa, tecnología usada y justificación de la elección). Se pueden añadir más apartados según sea necesario \- Ver ejemplos.\#*

A continuación se detallan los componentes que conformarán la solución:

* **Capa de ingesta**  
  * ***Tecnología**: \#\[Ej: Cloud Run, Dataflow, Fivetran\]\#*  
  * ***Justificación**: \#Conectores gestionados para fuentes SaaS\#* 

* **Capa de almacenamiento**  
  * ***Tecnología**: \#\[Ej: Cloud Storage, BigQuery\]\#*  
  * ***Justificación**: \#Data warehouse serverless\#*

* **Capa de transformación:**  
  * ***Tecnología**: \#\[Ej: Dataform, dbt\]*  
  * ***Justificación**: \#Transformaciones SQL y tests de calidad\#* 

* **Capa de explotación:**  
  * ***Tecnología**: \#\[Ej: Looker\]*  
  * ***Justificación**: \#\[Ej: Capa semántica y dashboards\#*

* **Orquestación:**  
  * ***Tecnología:**  \#\[Ej: Cloud Composer (Airflow), Workflows\]\#*  
  * ***Justificación**: \#Gestión de dependencias y retries\#* 

## 4.2. Diseño de data pipelines {#4.2.-diseño-de-data-pipelines}

En esta sección se detalla la metodología técnica para la ingesta, movimiento y transformación de los datos así como el flujo de la información entre las distintas zonas de la arquitectura, garantizando los requisitos de latencia, integridad y disponibilidad.

*\#En los siguientes apartados, seguir el formato de bulletpoints describiendo la lógica utilizada para capturar, transformar, orquestar y testear los datos. En cada caso se debe justificar la elección en función del volumen de datos, la ventana de tiempo disponible,... y otros factores involucrados.\#*

### 4.2.1. Estrategia de carga de datos {#4.2.1.-estrategia-de-carga-de-datos}

En esta sección se define la estrategia de movimiento y carga de datos desde los sistemas origen.

* **Tipo de carga:** *\# Carga Incremental (Delta) basada en marcas de agua (watermarks) de fecha de modificación\#.*

* **Frecuencia de Ejecución:** *\#Batch Diario (Nocturno) / Micro-batch cada 15 min / Streaming en tiempo real\]\#*

* **Criterio de Reprocesamiento:** *\#Capacidad de ejecutar cargas "Full" bajo demanda mediante parámetros en el orquestador para regenerar históricos.\#*

* **Excepciones:**  
  * **Entidad/Tabla:** *\#NOMBRE TABLA EXCEPCIÓN\#*  
  * **Estrategia Diferenciada***: \#Para tablas maestras pequeñas (ej. Maestro de Divisas), se realizará siempre una carga completa (Snapshot) con truncado previo (Truncate & Load).\#*

### 4.2.2. Estrategia de transformación de datos {#4.2.2.-estrategia-de-transformación-de-datos}

En esta sección se define la estrategia de transformación de datos detallando el enfoque arquitectónico y las herramientas que procesarán el dato para aplicarle la lógica de negocio y estructura.

En este diseño se ha optado por un enfoque *\#ELT vs ETL\#* dadas las siguientes circunstancias:

*\#Detallar la justificación del enfoque describiéndolos de forma organizada en bullet points. Ver ejemplos:\#*

* *\[Ej ELT: Se prioriza la carga rápida al Data Lake y se utiliza la potencia del motor de base de datos destino para las transformaciones complejas.\]*  
* *\[Ej ETL: Se realizan transformaciones y anonimizado al vuelo antes de persistir el dato por requisitos estrictos de seguridad.\]*

Asimismo, para realizar dichas transformaciones se ha elegido como **herramienta principal** *\#HERRAMIENTA TRANSFORMACIÓN \[Ejemplo: dbt / Dataform / Stored Procedures / Spark Jobs\]\#* ya que *\#describir justificación\#* .

La lógica de transformación por capas se explicará con más detalle en la [sección 4.3](#4.3.-arquitectura-de-datos) del presente documento. 

### 4.2.3. Estrategia de calidad del dato {#4.2.3.-estrategia-de-calidad-del-dato}

En esta sección se detalla el enfoque adoptado para la validación escalonada de datos que impide la propagación de datos erróneos hacia las capas de consumo.

* **Framework**: *\#FRAMEWORK DQ Ej dbt tests / Librería propia en Python / Servicios nativos del Cloud provider/ Assertions…\#*

* **Controles implementados:**  
* ***Validación de esquemas**: verificación de tipos de datos y columnas obligatorias.*  
  * ***Acción ante el fallo:** Parado del Pipeline*  
* ***Checks de duplicados:** identificación de registros duplicados por clave de negocio*  
  * ***Acción ante el fallo:** Alerta (Warning)*  
* ***Validación de rangos:** valores numéricos dentro de umbrales esperados*  
  * ***Acción ante el fallo:** Se ponen los datos en cuarentena*  
* ***Checks de integridad referencial:** validación de foreign keys*  
  * ***Acción ante el fallo:** Parado del Pipeline\#*

* **Manejo de errores:** *\# Los registros fallidos se derivan a una tabla de Dead Letter Queue (DLQ) para análisis post-mortem sin detener el flujo general (salvo en errores críticos).\#*

* ***Notificaciones:** \#Se enviará una alerta al canal **\[Ej. \#data-quality-alerts\]** incluyendo el nombre del modelo fallido y el número de registros afectados.\#*

### 4.2.4. Estrategia de orquestación de datos {#4.2.4.-estrategia-de-orquestación-de-datos}

La orquestación es el componente central que coordina, planifica y monitoriza la ejecución de los flujos de datos (pipelines). Esta sección define cómo se gobierna el ciclo de vida de los procesos, asegurando que las tareas se ejecuten en el orden correcto, en el momento adecuado y con los recursos necesarios. El objetivo es pasar de una ejecución de scripts aislados a un sistema resiliente, observable y automatizado que garantice la entrega del dato.

Para la gestión centralizada, programación y monitorización de estos flujos de trabajo, se utilizará *\#Herramientas de orquestación Ej. Google Cloud Composer\#*. Esta elección permite:

*\#Describir las características del orquestador, definir lenguajes de programación usados para su desarrollo y detallar cómo será su mantenimiento. Organizar en bulletpoints y resaltar con negritas los elementos clave o títulos.\#*

*\#Ejemplo:*

* *Definición como Código (DaC): Todos los flujos se definen mediante código Python, lo que permite control de versiones (Git), revisión de código y despliegue automatizado (CI/CD)*  
* *Los procesos se estructuran como DAGs, lo que permite visualizar claramente las tareas y sus relaciones.*  
* *Al ser un servicio gestionado, Cloud Composer maneja automáticamente la infraestructura subyacente, reiniciando tareas fallidas (retries) y enviando alertas en caso de error.*

*\#*

**Organización de flujos (DAGs/Workflows)**  
Para garantizar la mantenibilidad, los procesos de datos se deben estructurar en unidades lógicas de trabajo. Esta segmentación facilita la detección de errores, permite re-ejecuciones parciales y clarifica la propiedad de cada proceso.

* **Estrategia de agrupación**: Los flujos se organizará por *\#Ejemplo: Dominio de Negocio (Ventas/Logística) / Frecuencia de carga / Capa de datos\#*.  
* **Nomenclatura**: Se seguirá el estándar de nombres: *\#Ejemplo: \[frecuencia\]\_\[dominio\]\_\[acción\]. EJ: daily\_sales\_ingestion, hourly\_inventory\_update\#*.

**Gestión de dependencias**  
La integridad de los datos depende estrictamente del orden de ejecución. Se establece un modelo de dependencias *upstream* (aguas arriba) y *downstream* (aguas abajo) para asegurar que ningún proceso comience sin que sus prerrequisitos (datos disponibles, calidad validada, procesos previos,...) se hayan completado exitosamente.

Las **reglas de dependencia** que se seguirán, son las siguientes:

* **Intra-Pipeline**: *\#Ejemplo: Ejecución secuencial bloqueante (Task A \-\> Task B). Si A falla, B no se inicia\#*.  
* **Inter-Pipeline**: *\#Ejemplo: Uso de \[Ej. Sensores / Datasets / Triggers\] para desacoplar dependencias entre distintos DAGs. Se puede citar aquí que los procesos de X grupo no empiezan hasta que estén procesados los de otro grupo (ej. Facturas primero, luego ventas agrupadas por producto y sector,...)\#*.  
* **Bloqueo por Calidad**: La promoción de datos entre capas (ej. Silver a Gold) se detendrá automáticamente si las reglas de calidad *\#definidas en la sección 4.2.3\#* no son satisfactorias.

Se definirán los siguientes **triggers** para los procesos de orquestación:

*\#Ejemplos:*

* ***Basado en Tiempo (Schedule):** \*\[Ej. Cron expression: "0 2 \* \* "\] para cargas batch nocturnas.*  
* ***Basado en Eventos:** **\[Ej. Llegada de archivo a Bucket / Mensaje en PubSub\]** para cargas casi en tiempo real.*

*\#*

**Resiliencia y gestión de errores (reintentos y alertas)**

En sistemas distribuidos, los fallos transitorios (cortes de red, timeouts de APIS,...) son inevitables. Para minimizar la fatiga de alertas y la intervención manual, se define una política de auto-recuperación y escalado de notificaciones. 

La **configuración de resiliencia** propuesta incluye:

*\# Ejemplos:*

* ***Errores Transitorios:** Se aplicarán **\[Ej. 3 reintentos\]** con una estrategia de espera exponencial (exponential backoff) para dar tiempo a que el sistema externo se recupere.*  
* ***Errores Fatales:** Los fallos de código o validación de esquema no tendrán reintentos (Fail Fast) y notificarán inmediatamente.*  
* ***Canales de Alerta:***  
  * *Warning: Canal de Slack \#data-ops-logs.*  
  * *Critical: PagerDuty / Llamada al ingeniero de guardia.\#*

##  4.3. Arquitectura de Datos {#4.3.-arquitectura-de-datos}

Esta sección define la organización lógica de los datos para la cual se ha adoptado una arquitectura multicapa que sigue el patrón de arquitectura medallón para garantizar que los datos se refinen progresivamente a medida que fluyen a través del sistema.

Este enfoque permite desacoplar la extracción de la transformación, asegurando la trazabilidad (linaje), facilitando la auditoría y optimizando tanto el costes de almacenamiento como el rendimiento de las consultas de negocio.

###  4.3.1 Capa Bronze  {#4.3.1-capa-bronze}

La **capa bronce**, también conocida como **capa raw** o **landing**, ejerce de repositorio de los datos crudos. Los datos se almacenan en su formato original desde la fuente, sin modificaciones, transformaciones ni pérdidas de información. En esta capa se añaden metadatos esenciales para auditoría, linaje y reprocesamiento en forma de campos técnicos, incluyendo marcas de tiempo, origen del archivo, etc. sin alterar los datos fuente originales.

Los **principios rectores** de esta capa son los siguientes:

* **Inmutabilidad**: Los datos una vez escritos en la capa bronce, nunca se modifican.  
* **Auditabilidad**: Permite reprocesar la historia completa en caso de errores en capas superiores o cambios en la lógica de negocio.  
* **Acceso**: Restringido exclusivamente a procesos de ingeniería. No accesible para usuarios de negocio.

**Especificaciones de implementación**

* **Formato de almacenamiento:** Los datos en la capa Bronze se almacenarán como *\#Ej: Parquet / Avro / JSON/Datos estructurados en BQ\#.*

* **Estrategia y frecuencia de carga:** Los datos se cargarán *\#Ej: Carga Incremental diaria (Deltas) / Full refresh diaria / Streaming cada XX días/horas…\#*.

* **Estrategia de particionamiento:** *\#Ej: Por fecha de ingestión dt=YYY-MM-DD\#*.

* **Política de retención:** *\#Ej: Indefinida / Mover a Cold Storage tras 12 meses / Eliminar datos de usuarios inactivos por RGPD\#*.

**Contrato de Datos**

* **Gestión de cambios del esquema:** Cualquier cambio en los nombres de columnas, tipos de datos o la eliminación de campos debe ser notificado con un mínimo de *\#\[X\] días de antelación.\#* En el caso de el esquema de datos sufra una evolución, *\# describir cómo reaccionarán las capas dentro del scope del actual\#*.  
* **Semántica del Tiempo**: Se garantiza que el campo utilizado para el particionamiento *\#event\_timestamp, date o similar\#* vendrá siempre en formato *\#Formato ej. UTC\#* y no contendrá valores nulos. En caso de no registrar un campo fiable se añadirá una columna técnica *\_ingestion\_timestamp*.

*\#**Nota:** El inventario de fuentes de datos ya está detallado en el apartado 3.3.1. Capa de ingesta. No repetir aquí para no duplicar contenidos a lo largo del documento\#*

**Riesgos e incompatibilidades**

A continuación  se detallan las posibles incompatibilidades técnicas detectadas en el origen.

*\#Ejemplos:* 

* *La BBDD no tiene campo de fecha de modificación para identificar deltas.*  
* *Conectividad VPN inestable con el servidor on-premise.\#*

### 4.3.2 Capa Silver {#4.3.2-capa-silver}

La **capa silver** es aquella en la que los datos crudos se convierten en información fiable aplicando procesos de limpieza, estandarización, tipado y deduplicación. Aunque los datos ya son técnicamente correctos, mantienen una estructura similar a la de origen (3NF o normalizada) y aún no están totalmente modelados para el consumo de negocio. 

Los **principios rectores** de esta capa son los siguientes:

* **Calidad técnica**: Se eliminan duplicados y valores corruptos.  
* **Estandarización**: Nomenclaturas unificadas (ej. snake\_case) y formatos de fecha consistentes (ISO-8601).  
* **Historización**: Gestión de la dimensión tiempo y cambios en los datos.

**Especificaciones de transformación**

* **Limpieza y normalización**  
  * **Gestión de valores nulos:** *\#Reemplazar NULLs en dimensiones por 'N/A' o '-1'\#.*  
  * **Formatos:** *\#Casteo de strings a tipos numéricos/fecha correctos\#.*

* **Estrategia de deduplicación:** *\#Uso de ROW\_NUMBER() OVER (PARTITION BY id ORDER BY updated\_at DESC) para obtener el estado actual\#.*

* **Gestión de Historia (SCD):** *\#Añadir tantas entidades/campos como se vayan a historizar\#*  
  * *\#Nombre entidad (tabla, vista, endpoint,...): SCD Tipo 2 (Vigencia de fechas) / Tipo 1 (Sobreescritura) / Snapshot periódico\#*.

* **Cálculo de deltas**: *\#Ej: Identificación de registros nuevos vs. modificados\#*.

**Reglas de negocio en Capa Silver**  
En la capa Silver solo se permiten implementar Reglas de Negocio Universales. Una regla es universal si aplica a todos los consumidores de datos de la organización sin excepción. Si una regla excluye datos que podrían ser útiles para otro departamento (ej. borrar pedidos "cancelados" que Logística necesita analizar, aunque Ventas no los cuente), esa regla NO debe aplicarse en Silver, sino en Gold.

*\#**Nota:** En esta tabla sólo se detallarán reglas universales. Quedan, por tanto, excluídas aquellas para el cálculo de KPIs como agrupaciones muy específicas o filtrados de negocio (filtros que restringen datos al común de los usuarios de negocio)\#*

| Tipo de regla | Descripción |
| :---- | :---- |
| *Limpieza técnica* | *TRIM de espacios, formatos de fecha, deduplicación técnica* |
| *Filtrado universal* | *Excluir registros de prueba, datos corruptos irrecuperables o fuera de alcance temporal histórico de la empresa* |
| *Estandarización* | *Mapeo de códigos de país (ES → ESP), conversión de divisas a moneda corporativa,...* |

*\#**Nota:** Las dependencias de procesamiento en la Capa Silver se detallan en la sección 4.2.4 Estrategia de orquestación a grandes rasgos para evitar duplicaciones de la misma información a lo largo del documento.\#*

### 4.3.3 Capa Gold {#4.3.3-capa-gold}

La capa **gold** es aquella capa que actúa como “Fuente de la Verdad” para la organización. En ella, los datos se reestructuran y agregan en modelos dimensionales orientados a procesos de negocio y entidades, no a sistemas informáticos operacionales. Está optimizada para el consumo de datos  orientados para el rendimiento de lectura y la facilidad de uso en herramienta de BI y análisis.

Los **principios rectores** de esta capa son los siguientes:

* **Usabilidad**: Esquemas intuitivos (estrella, copo de nieve) fáciles de entender por analistas.  
* **Consistencia**: Las métricas y KPIs se calculan aquí una sola vez para evitar discrepancias entre departamentos.  
* **Rendimiento:** Uso de tablas desnormalizadas y agregadas para minimizar *joins* costosos en tiempo de consulta.

**Modelo de datos** 

* **Enfoque de modelado:** *\#Ej: Kimball (Esquema de Estrella) / OBT (One Big Table) / …\#*.

* **Entidades principales**

  * **Tablas de hechos:** Las tablas de hechos contienen métricas numéricas y claves foráneas. El detalle de las tablas de hechos diseñadas para este proyecto puede localizarse en este [documento anexo](https://docs.google.com/spreadsheets/d/1a-BbsINzYzLjqkY9rKDfOkaXGfBa_0d-uBt2QUGGbmE/edit?usp=drive_link) \- Pestaña **Capa Gold Hechos**.

  * **Tablas de dimensiones:** Las tablas de dimensiones contienen atributos descriptivos. El detalle de las tablas de hechos diseñadas para este proyecto puede localizarse en este [documento anexo](https://docs.google.com/spreadsheets/d/1a-BbsINzYzLjqkY9rKDfOkaXGfBa_0d-uBt2QUGGbmE/edit?usp=drive_link)  \- Pestaña **Capa Gold Dimensiones**.

*\#En el caso de necesitar hacer alguna vista materializada que afecte a toda la compañía para acelerar consultas o usarla como vista auxiliar, definirlas a continuación añadiendo el siguiente apartado que se deja a modo de ejemplo. También se puede añadir una pestaña adicional al* [documento anexo](https://docs.google.com/spreadsheets/d/1a-BbsINzYzLjqkY9rKDfOkaXGfBa_0d-uBt2QUGGbmE/edit?usp=drive_link)  *para dichas vistas.\#*

*\#Ejemplo*

* **Vistas materializadas:** Vistas con agregaciones pre-calculadas para acelerar los dashboards.

\#

### 4.3.4 Capa Platinum {#4.3.4-capa-platinum}

*\#En el caso de no necesitar este apartado, se puede eliminar\#*

La **capa platinum** o capa de exposición está dedicada a las necesidades específicas de integración o exportación que requieren formatos rígidos o listos para consumir fuera del entorno analítico. En general, contiene tablas totalmente desnormalizadas preparadas para alimentar sistemas de terceros o casos de uso muy específicos asegurando el rendimiento en la capa de lectura.

| Informe /Dashboard  | Origen datos | Formato salida | Actualización |
| ----- | ----- | ----- | ----- |
| *\#Ej. Nombre del Informe / Dashboard\#* | *\#Ej. Joins entre Fact\_Ventas y Dim\_Productos de capa Gold\#* | *\#Ej. Vista Materializada en BigQuery / Tabla plana\#* | *\#Ej. Todas las mañanas a las 07:00 UTC \+1\#* |

## 4.4. Modelo de datos físico y optimización {#4.4.-modelo-de-datos-físico-y-optimización}

Este apartado detalla la implementación física del modelo definido en la Capa Gold. Aquí se visualizan las relaciones entre las entidades listadas anteriormente, se define la estrategia de gestión histórica y las configuraciones de rendimiento.

### 4.4.1. Diagrama de Entidad-Relación (ERD) {#4.4.1.-diagrama-de-entidad-relación-(erd)}

En esta sección se desarrolla la representación visual del modelo de datos físico. Su objetivo es facilitar la comprensión de las relaciones entre las entidades, definir la cardinalidad de los cruces (1:N, N:N) y visualizar la estructura de claves (Primary Keys / Foreign Keys).

Este diagrama (link *\#añadir link al Shared Drive donde se comparta la imagen de alta calidad\#*) sirve como referencia principal para los desarrolladores y analistas a la hora de construir *queries* y navegar por el modelo de datos.

*\#Insertar aquí el diagrama visual ERD del modelo de datos que debe mostrar las claves primarias (PKs) y las relaciones (FKs) entre las tablas de Hechos y Dimensiones listadas en el documento anexo de la [sección 4.3.3.](#4.3.3-capa-gold).* 

***Nota:** Revisar que ambos documentos (diagrama y anexo) sean fiel reflejo el uno del otro.\#*

![][image2]

### 4.4.2. Estrategia de Historización (SCD) {#4.4.2.-estrategia-de-historización-(scd)}

Los datos maestros de negocio no son estáticos sino que  evolucionan con el tiempo. Esta sección define la estrategia de SCD (Slowly Changing Dimensions) que se aplicará para gestionar estos cambios.

El objetivo es establecer explícitamente cuándo se debe sobrescribir un dato (actualización simple) y cuándo se debe generar una nueva versión del registro para preservar la integridad histórica de los informes pasados.

**Estrategias aplicables**

A continuación se definen los patrones estándar a utilizar en el proyecto:

* **SCD Tipo 1 (Sobreescritura):**  
  * **Comportamiento:** El dato nuevo reemplaza al antiguo. No se guarda historia.  
  * **Uso:** Corrección de errores tipográficos, cambios irrelevantes para el análisis histórico o para reducir volumen en tablas no críticas.  
  * **Impacto***:* Se pierde el valor anterior permanentemente.

* **SCD Tipo 2 (Versionado de Filas):**  
  * **Comportamiento:** Se crea un nuevo registro para el mismo ID de negocio, marcando el anterior como "cerrado" mediante fechas de vigencia.  
  * **Uso:** Atributos críticos donde es necesario conocer el valor exacto en un momento pasado.  
  * **Impacto***:* Permite reconstruir la historia ("Time Travel"), pero aumenta el volumen de almacenamiento.

**Definición por Entidad**

*\#Especificar en la siguiente tabla qué estrategia se aplica a cada dimensión o grupo de tablas.\#*

| Entidad / Tabla  | Estrategia | Atributos críticos | Justificación |
| ----- | ----- | ----- | ----- |
| *\#dim\_cliente\#* | *Tipo 2* | *DirecciónSegmentoEstado\_Civil* | *Necesario para analizar ventas por la geografía real del cliente en el momento de la compra* |
| *\#dim\_producto\#* | *Tipo 1* | *DescripciónCategoría* | *Si cambia la descripción queremos que se actualice todo el histórico para mantener consistencia de catálogo* |

**Implementación Técnica (SCD Tipo 2\)**

Para las tablas con estrategia SCD Tipo 2, se añadirán obligatoriamente las siguientes columnas de auditoría al modelo físico:

* **valid\_from** (TIMESTAMP): Fecha y hora en la que el registro se hizo efectivo.  
* **valid\_to** (TIMESTAMP): Fecha y hora en la que el registro dejó de ser válido (o NULL / 9999-12-31 si es el actual).  
* **is\_current** (BOOLEAN): Indicador rápido (TRUE/FALSE) para filtrar la versión vigente.  
* **sk\_id** (Surrogate Key): Clave primaria técnica (hash o autoincremental) única para cada versión, ya que el ID de negocio se repetirá.

*\#Los nombres de estos campos técnicos podrán variar según el estándar de nomenclatura definido por el arquitecto del proyecto.\#*

### 4.4.3 Estrategia de particionamiento y clustering {#4.4.3-estrategia-de-particionamiento-y-clustering}

Esta sección define la estrategia física de almacenamiento para:

* **Particionamiento:** Dividir las tablas grandes en segmentos lógicos (generalmente por tiempo) para habilitar el *partition pruning*, una técnica de lectura en la que se evita la lectura de particiones de datos irrelevantes en una consulta con la consiguiente ganancia en rendimiento y ahorro en coste.

* **Clustering:** Organizar físicamente los datos dentro de cada partición para acelerar filtros de alta granularidad y operaciones de JOIN. Esta técnica ofrece ventajas significativas en términos de ahorro de costes y mejora del rendimiento en consultas para campos críticos de uso habitual en dashboards como filtros.

**Estrategia a implementar**

*\#Detallar la configuración para las tablas volumétricas (Facts y Logs). Las tablas de dimensiones pequeñas (\< 1GB) generalmente no requieren esta estrategia. En algunas ocasiones sólo es necesario el particionamiento y no el clustering. Evaluar siguiendo [buenas prácticas de Google](https://docs.cloud.google.com/bigquery/docs/manage-partition-cluster-recommendations).\#*

| Entidad / Tabla  | Campo de Partición | Granularidad | Campo de Clustering | Justificación |
| ----- | ----- | ----- | ----- | ----- |
| *fact\_ventas* | *fecha\_ticket* | *Día* | *id\_tiendacategoria* | *Las consultas financieras siempre se filtran por fecha. El clustering acelera el análisis por tienda específica y producto.* |
| *logs\_web* | *ingestion\_time* | *Hora* | *session\_iduser\_id* | *Volumen masivo. Se requiere partición horaria para cargas incrementales eficientes. Clustering vital para trazar usuarios.* |
| *fact\_inventario* | *fecha\_snapshot* | *Mes* | *id\_productoid\_almacen* | *Los reportes de stock son mensuales. Particionar por día generaría demasiados fragmentos pequeños.* |

**Guía de Diseño**

Para la selección de claves, se han seguido los siguientes principios:

* **Particionamiento (baja cardinalidad)**  
  * Se utiliza siempre un campo de fecha (DATE o TIMESTAMP) o un campo de muy baja cardinalidad (ej. Región).  
  * **Anti-patrón:** Nunca particionar por campos de alta cardinalidad (ej. User\_ID), ya que degradaría el rendimiento de escritura.

* **Clustering (alta cardinalidad)**  
  * Se utilizan campos frecuentes en las cláusulas WHERE (que no sean la fecha) y en las condiciones de JOIN.  
  * El orden de las columnas de clustering importa: se colocan primero las de menor cardinalidad (menos valores únicos).

    

* **Gestión de Ciclo de Vida (expiración de particiones)** *\#Opcional\#*  
  * Las tablas temporales o de staging tienen configurada una caducidad de partición de *\#7 días\#* para auto-eliminarse y ahorrar costes de almacenamiento.

# **5\. Seguridad, gobierno y cumplimiento** {#5.-seguridad,-gobierno-y-cumplimiento}

En esta sección se define el marco integral de seguridad y gobernanza del proyecto. Su objetivo es garantizar que la plataforma de datos sea segura por diseño, cumpla con las regulaciones vigentes y ofrezca mecanismos de control robustos sobre el acceso y uso de la información.

## 5.1. Organización de recursos y jerarquía {#5.1.-organización-de-recursos-y-jerarquía}

Esta sección desarrolla la estructura lógica y administrativa de los recursos en la nube. Una jerarquía bien diseñada es fundamental para garantizar el aislamiento de entornos, simplificar la imputación de costes por centro de coste y facilitar la herencia de políticas de seguridad desde la organización hacia los proyectos individuales

*\#Representar en el siguiente diagrama la estructura de organización, folders y proyectos\#*

*\#Ejemplo*

```shell
Organization: cliente.com
├── Folder: Production
│   └── Project: prod-data-platform
├── Folder: Non-Production
│   ├── Project: dev-data-platform
│   └── Project: qa-data-platform
└── Folder: Shared
    └── Project: shared-logging
```

**Estrategia de etiquetado (tags)**

Para garantizar la gobernanza, la imputación correcta de costes y la automatización de operaciones, se define un esquema de etiquetado obligatorio para todos los recursos desplegados en la nube. Estas etiquetas (metadatos clave-valor) permiten agrupar lógicamente recursos que pueden estar dispersos en diferentes proyectos o regiones, facilitando auditorías de seguridad y reportes financieros.

A continuación se definen las etiquetas que deben aplicarse vía Infraestructura como Código:

| Clave | Valores permitidos | Propósito / Uso | Obligatoriedad |
| ----- | ----- | ----- | ----- |
| *environment* | *dev, uat, prd* | *Identificar la criticidad del entorno y aplicar reglas automáticas de firewall* | *Obligatorio* |
| *cost\_center* | *código\_numérico* | *Imputación de la facturación cloud al departamento financiero correspondiente* | *Obligatorio* |
| *owner* | *Email equipo* | *Identificar al responsable técnico del recurso para incidencias o mantenimiento* | *Obligatorio* |
| *application* | *Nombre App* | *Agrupar todos los recursos que pertenecen a una misma solución lógica* | *Opcional* |

**Reglas de Aplicación**

* **Nomenclatura**: Todas las claves (*keys*) deben escribirse en minúsculas y usar guiones bajos (snake\_case).  
* **Herencia**: En la medida de lo posible, los recursos heredarán los tags definidos a nivel de Proyecto o Carpeta.  
* **Cumplimiento**: Se implementarán políticas de organización que impedirán el despliegue de recursos que no contengan las etiquetas marcadas como "Obligatorias".

## 5.2. Gestión de identidades y accesos a datos {#5.2.-gestión-de-identidades-y-accesos-a-datos}

En esta sección se detalla cómo se gestionan los usuarios y las cargas de trabajo, aplicando estrictamente el **principio de mínimo privilegio** y la **separación de funciones** a fin de imitar el daño potencial si una cuenta se ve comprometida por un atacante o por un error accidental. En este sentido:

* Sólo se asignará a cada identidad los permisos estrictamente necesarios para desempeñar su cometido.

* No se asignarán permisos a nivel de usuario individual, sino a través de grupos de seguridad y roles específicos por entorno.

* Se utilizarán cuentas de servicio (service accounts) específicas por microservicio, evitando el uso de roles Editor o Owner genéricos.

### 5.2.1 Estrategia de autenticación {#5.2.1-estrategia-de-autenticación}

En esta sección se definen los mecanismos técnicos para verificar la identidad de los actores. Se distingue radicalmente entre el acceso humano (usuarios) y el acceso programático (service accounts).

**Usuarios**

* **Federación:** La gestión de usuarios se centraliza vía *\#G SUITE / AZURE AD/Okta\#*. No se crean usuarios locales en la base de datos o consola cloud.

* **MFA:** Se requiere Autenticación Multifactor (MFA) obligatoria para cualquier acceso a la consola de administración.

**Service Accounts**

* **Identidad por microservicio:** Se creará una service account por componente. Se prohíbe compartir identidades entre distintos pipelines.  
* **Acceso keyless (sin claves)**: Se prohíbe la generación y descarga de claves estáticas (.json). En su lugar se deberá usar:

  * Workload Identity: Para recursos dentro de la red del proveedor cloud.  
  * Workload Identity Federation: Para recursos externos (GitHub Actions, servidores On-Premise).  
* **Naming convention**: *\#sa-proyecto-funcion-Entorno (Ej: sa-data-ingest-prod)\#*.

### 5.2.2. Matriz de roles y permisos {#5.2.2.-matriz-de-roles-y-permisos}

En esta sección se definen los perfiles de acceso estándar. Se distingue entre permisos sobre el **Plano de Control** (Infrastructura: creación de buckets, tablas, encender máquinas,...) y el **Plano de Datos** (Contenido: lectura de tablas, ver información sensible,...).

| Rol  | Entorno | Plano Control | Plano Datos |
| :---- | :---- | :---- | :---- |
| *Data Engineer* | *dev* | *Admin:  \#recurso\#* | *Read/Write: especificar \#rol GCP\# a \#recurso\#* |
| *Data Engineer* | *prod* | *Viewer: \#recurso\#* | *Deny: Sin acceso a datos* |

### 

### 5.2.3. Gestión de secretos y credenciales {#5.2.3.-gestión-de-secretos-y-credenciales}

En esta sección se detalla la estrategia para proteger información sensible y eliminar su presencia en código fuente.

* **Almacenamiento:** Uso obligatorio de un gestor de secretos centralizado. En este caso se empleará *\#Secret Manager / Hashicorp Vault / …\#*.

* **Inyección:** Los secretos se inyectan en las aplicaciones como variables de entorno volátiles en tiempo de ejecución. Bajo ninguna circunstancia la información sensible será introducida de forma explícita en código o almacenada en variables de entorno sin cifrar.

* **Política de rotación**  
  * **Automática**: Rotación de credenciales de *\#herramienta/servicio\#* cada *\#XX días\#*.  
  * **Manual**: Rotación inmediata ante sospecha de compromiso.

**Detalle de secretos y credenciales**

| Secret ID  | Tipo | Descripción / Uso | Estrategia de rotación | Consumidores (servicios) |
| :---- | :---- | :---- | :---- | :---- |
| *sec-prod-sql-erp-pass* | *Credencial BBDD* | *Contraseña del usuario de lectura para la BBDD Oracle del ERP* | *Automática (90 días)* | *Pipeline ingest\_erp\_daily* |
| *sec-prod-ssh-sftp-key* | *SSH key (RSA)* | *Clave privada para acceder al servidor SFTP de proveedores* | *Manual (Anual)* | *Cloud Function fetch\_files* |

### 5.2.4. Seguridad granular del dato {#5.2.4.-seguridad-granular-del-dato}

En esta sección se detallan las políticas de seguridad granular para restringir la visibilidad de datos sensibles dentro de un mismo dataset o tabla, garantizando el cumplimiento de normativas de privacidad (GDPR) y políticas internas. Se define primero la taxonomía de etiquetas de seguridad (policy tags), luego su aplicación a las columnas sensibles (CLS/Enmascaramiento) y finalmente la lógica de filtrado de filas (RLS).

**Taxonomía de etiquetas de seguridad (policy tags)**

En esta sección definimos las taxonomías o categorías de datos sensibles que se definirán como *policy tags* en BigQuery y los grupos autorizados para ver el dato real sin enmascarar:

| Tag ID  | Nivel de sensibilidad | Descripción | Roles con permiso de desenmascaramiento |
| :---- | :---- | :---- | :---- |
| *pii\_email* | *Alta* | *Direcciones de correo electrónico de clientes o empleados* | *Data StewardMarketing admin* |
| *pii\_financial* | *Restrigida* | *Datos bancarios (IBAN) o números de tarjeta* | *Finance managerBilling System SA* |
| *hr\_salary* | *Confidencial* | *Datos salariales y bonificaciones* | *HR DirectorPayroll SA* |
| *geo\_location* | *Media* | *Coordenadas GPS exactas del usuario* | *Logistics Lead* |

Para gestionar el **desenmascarado dinámico**, se utilizarán los siguientes **roles nativos** de BigQuery/Data Catalog sobre las *policy tags.* Es importante distinguir entre el usuario que ve el dato enmascarado (con diferentes técnicas)  y el que tiene permiso para ver el dato limpio (texto plano).

| Nivel de acceso | Rol IAM | Comportamiento visual | Caso |
| :---- | :---- | :---- | :---- |
| *Sin acceso* | *Ninguno* | *Access Denied* | *Usuarios que no deben saber ni que el dato existe.* |
| *Acceso enmascarado* | *roles/bigquerydatapolicy.maskedReader* | *Ve el dato ofuscado según la regla (ej. \*\*\*\*\*).* | *Analistas, Desarrolladores, Data Scientists.* |
| *Acceso Total* | *roles/datacatalog.categoryFineGrainedReader* | *Ve el dato real en texto plano.* | *Sistemas de facturación, RRHH, Data Stewards.* |

Los roles con permiso de desenmascaramiento definidos en la tabla de policy tags anterior tendrán asignado el rol de roles/datacatalog.categoryFineGrainedReader. En este caso podrán ver los datos sin restricción alguna. En caso de querer aplicar alguna política de enmascaramiento, éstas se definirán en la siguiente sección.  
   
**Seguridad a nivel de columna (CLS \- Column Level Security)**

En esta sección se detalla el mapeo de columnas específicas y *policy tags* definidas anteriormente con su correspondiente estrategia de ofuscación para usuarios no autorizados.

| Tabla / Vista | Columna | Policy Tag Aplicado | Estrategia de enmascaramiento |
| :---- | :---- | :---- | :---- |
| *dim\_clientes* | *email* | *pii\_email* | *Partial mask (mostrar sólo dominio)* |
| *fact\_nominas* | *salario\_bruto* | *hr\_salary* | *Nullify (convertir a NULL)* |
| *fact\_pagos* | *iban* | *pii\_financial* | *HASH (SHA256) \- irreversible* |
| *dim\_empleados* | *dni* | *pii\_generic* | *Full mask* |

En este caso los usuarios que puedan tener acceso a los **datos enmascarados**, tendrán que tener asignado el rol de roles/bigquerydatapolicy.maskedReader.

**Seguridad a nivel de fila (RLS \- Row Level Security)**

En esta sección se detalla la lógica de filtrado dinámico (WHERE clause implícito) basada en los atributos del usuario que consulta en BigQuery.

| Tabla / Vista | Perfil usuario | Lógica de filtrado (pseudocógido) | Justificación |
| :---- | :---- | :---- | :---- |
| *fact\_ventas* | *Store Manager* | *WHERE store\_id \= USER\_ATRIBUTE(‘store\_id’)* | *Un gerente sólo puede ver las ventas de su propia tienda* |
| *dim\_empleados* | *Empleado (self)* | *WHERE employee\_id \= CURRENT\_USER\_EMAIL()* | *Un empleado sólo puede ver su propia ficha de datos* |
| *fact\_margen* | *Data Analyst* | *WHERE region \<\> ‘HR\_Corporate’* | *Los analistas no tienen acceso a datos de la sede central* |
| *todas* | *Admin* | *TRUE (sin filtro)* | *Acceso global para administradores* |

### 

### 5.2.4. Protocolo de acceso de emergencia (*glass breaker*) {#5.2.4.-protocolo-de-acceso-de-emergencia-(glass-breaker)}

En condiciones normales de operación, ningún desarrollador o ingeniero tiene acceso directo de lectura/escritura a los datos productivos. Sin embargo, ante incidencias de severidad crítica que detienen la operación del negocio, se requiere un mecanismo de excepción controlado para otorgar permisos elevados de forma temporal. Este protocolo se conoce como *glass breaker*.

**Flujo de Activación**

* **Solicitud:** El ingeniero abre un ticket de incidente declarando la urgencia y solicitando acceso al proyecto de producción.  
* **Aprobación:** Un *Data Owner* o *Tech Lead* aprueba explícitamente la solicitud (vía JIRA/ServiceNow o herramienta IAM).  
* **Elevación de Privilegios:**  
  * Se asigna temporalmente al usuario el rol de *\#definir rol custom\#*.  
  * Este rol otorga permisos de: *\#revisar lista roles IAM asignados en el rol custom anterior\#*.  
2. **Ventana de Tiempo:** El acceso expira automáticamente tras *\#XX horas\#*.  
3. **Auditoría Post-Mortem:**  
   * Todas las consultas y comandos ejecutados durante la sesión quedan marcados en los logs de auditoría.  
   * Se requiere un reporte obligatorio justificando qué se tocó y por qué.

| Permiso | Rol Estándar | Rol “Glass breaker” | Riesgo asociado |
| :---- | :---- | :---- | :---- |
| *Ver Datos PII* | *Bloqueado (masked)* | *Visible (unmasked)* | *Exposición de datos sensibles* |
| *Borrar tablas* | *Denegado* | *Permitido* | *Pérdida de datos (requiere backup)* |
| *Despegar código* | *Sólo vía CI/CD* | *Directo (hotfix)* | *Desviación de versiones (code drift)* |

### 

## 5.3. Estrategias de cifrado {#5.3.-estrategias-de-cifrado}

Este apartado detalla las medidas criptográficas implementadas para garantizar que los datos sean ininteligibles para cualquier actor no autorizado, protegiendo la confidencialidad e integridad de la información en todo momento.

### 5.3.1. Cifrado en tránsito {#5.3.1.-cifrado-en-tránsito}

* **Política**: Todo dato que se mueve a través de una red (sea pública o interna) debe viajar por un canal seguro.  
* **Protocolo**: *\#Se fuerza el uso de TLS 1.2 o superior para todas las conexiones.\#*  
* **Implementación**:  
  * **APIs y Web:** *\#HTTPS obligatorio (HSTS activado)\#.*  
  * **Bases de Datos**: *\#Conexiones JDBC/ODBC forzadas con SSL (sslmode=require)\#*.  
  * **Interconexión:** *\#Los túneles VPN/Interconnect utilizan IPsec para cifrar el tráfico entre On-Premise y la Nube\#*.

### 5.3.2. Cifrado en reposo {#5.3.2.-cifrado-en-reposo}

* **Política:** Todo dato almacenado en disco (Bases de datos, Data Lakes, Discos de VM, Backups) se cifra automáticamente antes de escribirse en el medio físico.  
* **Algoritmo:** *\#Estándar de la industria AES-256 (Advanced Encryption Standard)\#.*  
* **Cobertura:** El cifrado es transparente y se aplica a:  
  * *\#Archivos en Object Storage (Buckets).*  
  * *Tablas en Data Warehouse.*  
  * *Logs y archivos temporales ("spill to disk")\#*.

###  5.3.3. Gestión de claves de cifrado (KMS) {#5.3.3.-gestión-de-claves-de-cifrado-(kms)}

En esta sección se detalla quién posee y gestiona las claves que cifran los datos siendo de vital importancia para el cumplimiento regulatorio (GDPR/Soberanía del dato).

| Tipo de dato | Estrategia de claves | Descripción técnica | Justificación |
| :---- | :---- | :---- | :---- |
| *Datos estándar* | *GMEK* | *La nube gestiona y rota las claves automáticamente. El cliente no tiene control directo.* | *Simplicidad operativa y coste cero. Suficiente para datos no sensibles* |
| *Datos Sensibles (PII/Financiero)* | *CMEK* | *El cliente crea y custodia las claves en el KMS. La nube solo las usa con permiso explícito.* | *Requisito regulatorio. Permite el "Crypto-shredding" (borrado lógico instantáneo revocando la clave).* |
| *Secretos (Passwords)* | *Secret Manager* | *Claves específicas para credenciales, rotadas automáticamente.* | *Evitar hardcoding en aplicaciones.* |

## 

## 5.4. Seguridad de red y perímetro {#5.4.-seguridad-de-red-y-perímetro}

En esta sección se describe cómo se aísla y protege la infraestructura de datos a nivel de red detallando la topología de la nube privada virtual (VPC/VNet), la segmentación en subredes para reducir la superficie de ataque y los mecanismos de filtrado de tráfico (Firewalls, ACLs) que implementan una política de denegación por defecto (deny-by-default).

### 5.4.1. Arquitectura de red {#5.4.1.-arquitectura-de-red}

La arquitectura de red define la topología de red que alojará la plataforma en la cual se prioriza el uso de subredes privadas para los componentes de almacenamiento y procesamiento de datos, restringiendo la exposición a internet únicamente a los puntos de entrada necesarios (balanceadores de carga, hosts de bastiones,...).

**Especificaciones de red**

* **VPC/VNet CIDR**: *\#Rango de IP Global (Ej. 10.0.0.0/16)\#*  
* **Región principal**: *\#Región (ej. europe-west1)\#*  
* **Zonas de disponibilidad**: *\#Número (Ej. 3 zonas para alta disponiblidad)\#*

**Esquema de subredes**  
*\#Eliminar o reemplazar el esquema de subredes\#*

```shell
VPC: 10.0.0.0/16 (prod-data-platform-vpc)
├── Public Subnet 1: 10.0.1.0/24 (eu-west-1a) - NAT Gateway, Load Balancers
├── Public Subnet 2: 10.0.2.0/24 (eu-west-1b) - NAT Gateway, Load Balancers
├── Private Subnet 1: 10.0.10.0/24 (eu-west-1a) - App Servers, Lambda
├── Private Subnet 2: 10.0.11.0/24 (eu-west-1b) - App Servers, Lambda
├── Data Subnet 1: 10.0.20.0/24 (eu-west-1a) - Databases, Redshift
└── Data Subnet 2: 10.0.21.0/24 (eu-west-1b) - Databases, Redshift
```

### 5.4.2. Conectividad híbrida {#5.4.2.-conectividad-híbrida}

*\#Este apartado aplica si existe conexión con data centers on-premise. Si es 100% Cloud nativo, se puede eliminar\#*

En esta sección se detalla la extensión segura de la red corporativa hacia la nube. Se especifica el mecanismo de interconexión utilizado para garantizar que el tráfico entre el entorno on-premise y la nube no transite por la internet pública sin protección.

**Configuración de enlace**

* **Tipo de conexión**: *\#Ejemplos*  
  * *Opción A (Baja latencia / Alto caudal): Línea dedicada (Google Cloud Interconnect).*  
  * *Opción B (Coste eficiente): VPN Site-to-Site (IPSec) a través de internet\#*   
* **Ancho de banda provisionado**: *\#1 Gbps\#*  
* **Redundancia**: *\#Sí/No (Ej. Configuración Activo/Pasivo con failover automático).\#*

**Routing y DNS**

* **Protocolo:** *\#Ej. Se utilizará BGP (Border Gateway Protocol) para el intercambio dinámico de rutas.\#*   
* **Resolución de nombres:** *\#Ej. Se configurará Cloud DNS como DNS Forwarder para permitir la resolución de nombres de dominio internos desde la nube.\#*

###  5.4.3. Seguridad de red y controles {#5.4.3.-seguridad-de-red-y-controles}

En esta sección se detalla la implementación de controles de perímetro y segmentación interna aplicando el principio de defensa en profundidad, combinando firewalls sin estado (NACLs) y con estado (Security Groups) para micro-segmentar el tráfico.

**Firewalls y filtrado**

* **Security Groups (Firewalls de instancia):**  
  * *\#Ejemplo  \- Política: Denegar todo el tráfico entrante por defecto.\#*  
  * *\#Ejemplo \- Regla: Permitir tráfico al puerto 5432 (PostgreSQL) en la subnet “Data” sólo si proviene de la aplicación “Data”.\#*  
* **Network ACLs (Firewall de Subred)**:  
  * *\#Ejemplo \- Se utilizarán como capa adicional de seguridad para bloquear IPs maliciosas conocidas o aislar subredes completas en caso de incidente.\#*  
* **WAF (Web Application Firewall)**:  
  * *\#Ejemplo \- Estado: Activado / Desactivado.\#*  
  * *\#Ejemplo \- Alcance: Protege los puntos de acceso públicos (API Gateway, Dashboard de BI) contra ataques comunes (OWASP Top 10, SQL injection, XSS).\#*

**Whitelisting y acceso**

* **Acceso Administrativo:** *\#Ejemplo: Restringido a través de VPN Corporativa o Bastion Host. No se permite SSH/RDP directo desde Internet.\#*  
* **Whitelisting:**   
  * *\#IP\_Oficina (Acceso desarrolladores)\#*  
  * *\#IP\_Proveedor\_ETL (IPs de Fivetran, Airbyte,...).\#*

**Estrategia de segmentación (*tiering*)**

*\#Ejemplo: Se implementa una estrategia de 3 capas para aislar los datos:*

* ***Capa Presentación (Public):** Única capa expuesta a internet (vía Load Balancer). Solo acepta tráfico HTTPS (443).*  
* ***Capa Aplicación (Private):** Solo acepta conexiones desde la Capa Presentación. Aquí residen los servidores de procesamiento.*  
* ***Capa de Datos (Isolated):** El nivel más protegido. Solo acepta conexiones SQL/API desde la Capa Aplicación. Sin acceso a internet (salvo vía NAT para actualizaciones controladas).*

*\#*

## 5.5. Gobierno del dato {#5.5.-gobierno-del-dato}

Esta sección detalla los mecanismos automatizados para el descubrimiento de información sensible, la monitorización de la calidad y la gestión del ciclo de vida, asegurando que los datos sean localizables, comprensibles, fiables, seguros y auditables.

### 5.5.1. Descubrimiento y clasificación {#5.5.1.-descubrimiento-y-clasificación}

En esta sección se describen los procesos de escaneo automático a llevar a cabo para evitar la exposición accidental de datos sensibles a fin de inspeccionar los repositorios de datos en busca de patrones de información personal o confidencial.

**Estrategia de Data Loss Prevention**

* **Herramienta**: Sensitive Data Protection.  
* **Frecuencia de escaneo**: *\#Escaneo continuo en la ingesta / Escaneo semanal en reposo\#*.  
* **Acciones Automatizadas**:  
  * **Detección**: El sistema identifica patrones de *\#DNI, Tarjeta de Crédito, Email\#*.  
  * **Etiquetado**: Se aplica automáticamente un Policy Tag a la columna detectada en función del infotipo. *\#Detallar en una tabla si fuera necesario\#*  
  * **Alerta**: Se notifica al equipo de Seguridad si se detecta PII en un entorno no autorizado.  *\#Detallar el grupo de seguridad afectado\#*.

* **InfoTypes Monitorizados**: Se configuran reglas para detectar, entre otros: *\#CREDIT\_CARD\_NUMBER, EMAIL\_ADDRESS, IBAN\_CODE, PHONE\_NUMBER, NATIONAL\_ID\#*.

### 5.5.2. Gestión de metadatos y catálogo de datos {#5.5.2.-gestión-de-metadatos-y-catálogo-de-datos}

A continuación se presenta la estrategia para centralizar el conocimiento técnico y operativo de los activos de datos usando el Catálogo de Datos (Dataplex) para facilitar la búsqueda y el enriquecimiento de metadatos, evitando silos de conocimiento.

**Estrategia de Catalogación**

* **Herramienta**: Data Catalog (Dataplex)  
* **Alcance**: Indexación automática de metadatos de *\#BigQuery, Pub/Sub, GCS\#*.

**Enriquecimiento de metadatos**  
Se utilizarán plantillas de etiquetas (conocidas como *aspect types* en Dataplex) para añadir contexto de negocio a las tablas técnicas.

| Aspect type | Atributos | Aplicabilidad | Obligatoriedad |
| :---- | :---- | :---- | :---- |
| *Gobierno* | *Data owner (email)Clasificación (confidencial, interno)* | *Nivel tabla* | *Obligatorio gold y silver* |
| *Detalle ETL* | *Frecuencia cargaScript git* | *Nivel tabla* | *Opcional (automático)* |
| *Compliance* | *Tiene PII (SI/NO)Regulación (GDPR)* | *Nivel columna* | *Obligatorio (si hay PII)* |

**Organización del catálogo**  
Los activos se agruparán lógicamente según su dominio o sistema origen para facilitar la búsqueda y el control de accesos usando *entry groups*.

| Entry group | Descripción | Contenido esperado |
| :---- | :---- | :---- |
| *analytical\_warehouse* | *Entrada nativas de BigQuery* | *Tablas y vistas (Bronze, Silver, Gold, Platinum)* |
| *bi\_dashboards* | *Activos de visualización* | *Dashboard de Looker* |
| *raw\_files\_zone* | *Archivos no estructurados* | *PDFs, imágenes en GCS* |

### 

**Definición de tipos de entrada**  
Además de las entradas nativas (tablas), se definirán *custom entry types* para catalogar recursos que no se descubren automáticamente pero son críticos para el linaje y gobierno.

| Entry type (ID) | Descripción | Aspectos obligatorios (aspect types) |
| :---- | :---- | :---- |
| *generic\_table* | *Tablas estándar de BigQuery* | *Schema, Resource utilization* |
| *looker\_dashboard* | *Cuadros de mando de BI* | *Dashboard owner, business criticality, URL* |
| *dbt\_model* | *Transformación lógica SQL* | *Code repo link, last run status, SQL logic* |
| *ml\_model* | *Modelos de machine learning* | *Model version, training date, accuracy score* |

**Automatización de Metadatos**  
Para garantizar que el catálogo se mantenga sincronizado con la realidad de los datos, se adopta un enfoque de metadata as code. La documentación y el etiquetado no se realizarán manualmente en la consola, sino que se definirán como código dentro de los pipelines de transformación.

* **Implementación Técnica**:

  * **Definición**: Los atributos de los *Entry Types* y los valores de los *Aspects* se declararán explícitamente en los archivos de configuración de la herramienta de transformación:  
    *\#Ejemplo dbt: Uso de propiedades meta y tags en los archivos schema.yml. Se utilizarán paquetes (ej. dbt-google-datacatalog-tag-manager) para propagar estos cambios a Dataplex en cada despliegue\#.*

    *\#Ejemplo Dataform: Uso del bloque config { bigquery: { labels: ... } } y documentación de columnas en los archivos .sqlx\#*.

* **Propagación (CI/CD)**: Durante el despliegue del pipeline (CD), el sistema aplicará automáticamente los cambios de metadatos en Dataplex. Si un desarrollador añade una columna nueva o cambia una definición de negocio en el código, el Catálogo se actualizará automáticamente sin intervención humana.

###  5.5.3. Glosario de negocio {#5.5.3.-glosario-de-negocio}

El glosario actúa como la capa semántica que traduce los nombres técnicos de las columnas a terminología de negocio comprensible vinculando cada término empresarial con los activos físicos de datos que lo contienen.

* **Herramienta**: Dataplex business glossary.  
* **Responsabilidad**: Data Stewards mapean los términos a las columnas físicas.

*\#Añadir la siguiente tabla (si es pequeña) o eliminar la tabla y vincular a este documento un Sheets donde aparezca el grueso de los términos de negocio a tener en cuenta\#*

| Término de negocio | Definición aprobada | Mapeo a activo físico |
| ----- | :---- | :---- |
| *Cliente activo* | *Cliente con al menos una compra en los últimos 365 días* | *dim\_clientes.is\_active* |

### 5.5.4.Linaje de datos y trazabilidad {#5.5.4.linaje-de-datos-y-trazabilidad}

El linaje del dato es la capacidad de rastrear y visualizar el flujo de la información a través de toda la plataforma. Esta sección define la estrategia para garantizar la trazabilidad extremo a extremo (*End-to-End*), desde el sistema origen hasta los cuadros de mando de consumo.

Disponer de un linaje actualizado es crítico para dos procesos operativos: el **análisis de Impacto** y el **análisis de Causa Raíz**. La estrategia de captura de linaje incluye:

* **Nivel de Granularidad:** Se requiere linaje a *\#nivel de columna/nivel de tabla\#* para los datos críticos y PII, permitiendo saber exactamente qué campos alimentan un KPI.  
* **Herramienta:** Se utilizará *\#\[Ej. dbt docs / DataHub / Atlan / Google Dataplex (Data Catalog)\#* como repositorio central de metadatos.  
* **Visualización**: El grafo de linaje se consultará centralizadamente en *\#BigQuery/Dataform/Dataplex/dbt\#*.

### 5.5.5. Perfilado estadístico y calidad del dato {#5.5.5.-perfilado-estadístico-y-calidad-del-dato}

En esta sección se detalla los tests de perfilado estadístico y calidad de datos que se llevarán a cabo para asegurar la aptitud de los datos para el negocio a lo largo del tiempo.

**Matriz de configuración de perfilado estadístico del dato**

Se generarán estadísticas descriptivas automáticas sobre las tablas principales de la *\#capa Gold\#* para detectar anomalías en la distribución de los datos. Para llevar a cabo el perfilado de datos se usarán los jobs de data profiling de Dataplex.

| Entidad / Tabla | Campo / Columna | Métrica | Frecuencia | Umbral de alerta |
| ----- | :---- | :---- | :---- | :---- |
| *fact\_ventas* | *Tabla completa* | *Volumen* | *Diaria* | *Cambio \> 20% vs media 7 días* |
| *dim\_clientes* | *email* | *% nulos* | *Diaria* | *\>1% de nulos* |
| *fact\_pagos* | *total\_amount* | *Distribución (promedio máximo)* | *Semanal* | *Max \> 3 desviaciones estándar* |

**Matriz de configuración de reglas de calidad del dato**

Se definen las reglas deterministas que validarán el cumplimiento de las 6 dimensiones de calidad del dato (integridad, unicidad, consistencia, validez, precisión, frescura) sobre las tablas principales de la *\#capa Gold\#* para detectar anomalías en la calidad del dato. Se usará para ello *\#herramienta (assertions de Dataform, DQ jobs de Dataplex,...)\#*.

| Dimensión | Objeto (tabla.campo) | Lógica de validación | Severidad | Frecuencia | Acción |
| ----- | :---- | :---- | :---- | :---- | :---- |
| *Unicidad* | *dim\_clientes.id* | *COUNT(DISTINCT id) \= COUNT (id)* | *Crítica* | *Diaria* | *Cuarentena* |
| *Completitud* | *fact\_ventas.transaction\_id* | *IS NOT NULL* | *Crítica* | *Diaria* | *Fallo del pipeline* |
| *Validez* | *dim\_clientes.email* | *Regex: ^\[^@\]+@\[^@\]+\\.\[^@\]+$ (Formato Email)* | *Alta* | *Semanal*  | *Aviso (warning)* |

### 

**Severidad**

* **Crítica**: El dato es inutilizable.  
* **Alta**: Afecta a reportes importantes.  
* **Media**: Dato sucio pero no rompe el sistema.

**Acción automática**

* **Cuarentena**: Separa las filas que no cumplen la condición para revisión manual y carga el resto.  
* **Aviso (warning)**: Sólo avisa, carga todos los datos con riesgo de introducir datos sucios.  
* **Fallo del pipeline**: Detiene todo el proceso ETL protegiendo la capa Gold.

**Acuerdos de nivel de servicio (SLA)**

*\#Se pueden definir SLAs principalmente para métricas de calidad del dato pero opcionalmente también se pueden incluir alertas por fallos detectados en el perfilado de datos\#*

A continuación, se definen los siguientes objetivos de calidad para los dominios críticos:

| Dimensión | Métrica / KPI | Objetivo (SLA) | Acción ante incumplimiento |
| ----- | :---- | :---- | :---- |
| *Frescura* | *Tiempo desde el evento hasta disponibilidad en BI* | *\< 4 horas* | *Alerta a Chat ingeniería* |
| *Completitud* | *% de registros con campos obligatorios informados* | *\> 99,5%* | *Reporte con incidencia a Data Steward* |
| *Validez* | *% de registros que cumplen formatos estándar (ISO)* | *100%* | *Cuarentena automática de registros* |

### 5.5.6. Políticas de ciclo de vida {#5.5.6.-políticas-de-ciclo-de-vida}

Este apartado define las reglas de gestión del ciclo de vida de la información para equilibrar los costes de almacenamiento, el rendimiento de las consultas y los requisitos de cumplimiento legal.

Se establecen políticas automatizadas para mover los datos entre diferentes clases de almacenamiento o eliminarlos permanentemente cuando ya no aportan valor al negocio o expira su período de retención legal.

**Definición de Niveles de Almacenamiento**

* **Hot (Caliente):** Almacenamiento de alto rendimiento y coste más elevado. Para datos consultados frecuentemente (últimos 12-24 meses).  
* **Cold / Archive (Frío):** Almacenamiento de bajo coste y acceso lento (recuperación en horas). Para datos históricos que se guardan solo por auditoría legal.  
* **Delete (Borrado):** Eliminación física irreversible.

**Matriz de políticas de ciclo de vida**

| Capa / Tipo de Dato | Período de retención | Acción al vencimiento | Destino / Política final | Justificación |
| ----- | :---- | :---- | :---- | :---- |
| Capa bronze | 12 meses | Archivar | Mover a Cold Storage por 4 años más y luego borrar | *Los datos crudos permiten reprocesar la historia (Replay), pero rara vez se consultan tras un año.* |
| *Capa silver y gold* | *3 años* | *Mantener / Archivar* | *Mantener en capa hot si hay consultas de tendencias de largo plazo* | *El análisis de tendencias suele requerir ventanas de 3 a 5 años.* |
| *Datos Personales (PII) de ex-clientes* | *5 años (tras baja)* | *Borrado seguro* | *Crypto-shreadding o sobreescritura* | *Cumplimiento estricto de GDPR (Plazo de responsabilidad civil).* |
| *Backups de BBDD* | *30 días* | *Borrado físico* | *Rotación automática* | *Recuperación ante desastres (DRP). No usar backups como histórico.* |

Las políticas arriba descritas se configurarán mediante reglas nativas de la nube  *\#Google Cloud Storage Object Lifecycle / BigQuery Partition Expiration\#* para asegurar que la ejecución sea automática y no dependa de intervención humana.

## 5.6. Cumplimiento y normativas {#5.6.-cumplimiento-y-normativas}

Este apartado identifica el marco legal, regulatorio y los estándares de industria que impactan directamente en el diseño técnico de la solución. El objetivo del mismo es mapear cada requisito normativo con un Control Técnico Compensatorio específico, demostrando que la arquitectura no solo es funcional, sino que cumple con las obligaciones de seguridad, privacidad y soberanía del dato vigentes.

### 5.6.1. Residencia y soberanía del dato {#5.6.1.-residencia-y-soberanía-del-dato}

En cumplimiento con las normativas de soberanía de datos (específicamente GDPR en la UE), este apartado define explícitamente la ubicación física de la infraestructura de almacenamiento y procesamiento.

| Tipo de recurso | Región cloud | Ubicación física | Justificación |
| ----- | ----- | ----- | ----- |
| *Data warehouse* | *europe-west1* | *Bélgica (UE)* | *Jurisdicción primaria de los datos* |
| *Disaster recovery* | *europe-west3* | *Frankfurt (UE)* | *Redundancia geográfica intra-UE* |
| *Google Analytics (SaaS)* | *N/A* | *Unión Europea* | *Configuración forzada a servidores EU* |

**Restricciones de Transferencia**

*\#Añadir si resulta pertinente\#*

*\#Ejemplos*

* ***Políticas de la organización**: Se ha implementado una política de restricción de recursos (Resource Location Restriction) a nivel de organización que impide técnicamente el despliegue de servicios en regiones no listadas arriba (ej. bloquea despliegues en us-central1).*

* ***Transferencias Internacionales:** No se realizarán transferencias de datos personales fuera de la UE. En caso de necesidad técnica crítica (ej. soporte 24/7 Follow-the-Sun), se requerirá la firma previa de Cláusulas Contractuales Tipo (SCC) y una Evaluación de Impacto de Transferencia (TIA).*

*\#*

### 5.6.2. Matriz de cumplimiento normativo {#5.6.2.-matriz-de-cumplimiento-normativo}

En esta sección se detalla el mapeo de los requisitos legales y estándares de industria aplicables.

**Normativas Aplicables**  
*\#Incluir el listado de las normativas (leyes) o estándares/certificaciones de industria aplicables o exigibles por contrato\#*

*\# Ejemplos*

* ***GDPR (RGPD)***   
* ***HIPAA***  
* ***ISO 27001***  
* ***SOC 2***  
* ***PCI-DSS***

| Normativa | Requisito | Control  |
| :---- | :---- | :---- |
| *GDPR (RGPD)* | *Art. 32 \- Seguridad del tratamiento* | *Implementación de Cifrado AES-256 en reposo (BD) y TLS 1.2+ en tránsito.* |
| *GDPR (RGPD)* | *Art. 17 \- Derecho de supresión ("Derecho al olvido")* | *Scripts de purgado automático o endpoints de API para anonimizar/borrar datos de usuario a petición.* |
| *GDPR (RGPD)* | *Art. 25 \- Privacidad desde el diseño* | *Configuración de privacidad por defecto (checkboxes desmarcados) y minimización de datos en la ingesta.* |
| *EU AI Act* | *Art. 50 \- Obligaciones de transparencia (Sistemas de IA)* | *Marcado de agua o avisos visibles en la UI indicando que el contenido/decisión fue generado por IA.* |
| *EU AI Act* | *Art. 10 \- Gobierno de datos y gestión (Sistemas de alto riesgo)* | *Validación de sesgos en los datasets de entrenamiento y registro (logging) de la trazabilidad del modelo.* |
| *PCI-DSS v4.0* | *Req. 3 \- Protección de datos de cuenta almacenados* | *Tokenización del PAN (Primary Account Number) y prohibición estricta de almacenar el CVV/CVC.* |
| *DORA* | *Cap. II \- Gestión del riesgo TIC (Sector Financiero)* | *Plan de Recuperación ante Desastres (DRP) probado y copias de seguridad inmutables (WORM) contra ransomware.* |
| *LSSI-CE (Esp/UE)* | *Art. 22.2 \- Cookies y almacenamiento local* | *Banner de consentimiento granular (bloqueo preventivo de scripts de terceros hasta aceptar).* |
| *ISO 27001 (Estándar)* | *A.12.6.1 \- Gestión de vulnerabilidades técnicas* | *Escaneos de seguridad automatizados (SAST/DAST) en el pipeline de CI/CD antes de desplegar.* |

### 5.6.3. Auditoría  y evidencias {#5.6.3.-auditoría-y-evidencias}

*\#Sólo rellenar si es legalmente necesario por contrato\#*

Para facilitar las auditorías externas e internas, la plataforma está configurada para generar y retener automáticamente las siguientes evidencias de cumplimiento.

| Evidencia | Frecuencia generación | Retención | Repositorio / Acceso |
| ----- | ----- | ----- | ----- |
| *Informe de accesos a PII* | *Mensual* | *1 año* | *Bucket seguridad (sólo lectura auditor)* |
| *Reporte escaneo vulnerabilidad* | *Semanal (CICD)* | *6 meses* | *Dashboard seguridad* |
| *Certificado de borrado* | *Por solicitud* | *5 años* | *Base de datos de compliance* |

# **6\. Estrategia operativa (DevOps)** {#6.-estrategia-operativa-(devops)}

Esta sección define el marco operativo que garantiza la agilidad, la estabilidad y la calidad del desarrollo. Se adopta una filosofía DataOps, aplicando prácticas de ingeniería de software (control de versiones, pruebas automáticas, CI/CD) al ciclo de vida de los datos, con el objetivo de reducir el tiempo de entrega y minimizar los errores en producción.

## 6.1. Estándares y prácticas de ingeniería {#6.1.-estándares-y-prácticas-de-ingeniería}

### 6.1.1. Convenciones de nomenclatura {#6.1.1.-convenciones-de-nomenclatura}

El objetivo de estas convenciones es garantizar la consistencia, la predictibilidad y la fácil identificación de los recursos a lo largo de todo el ciclo de vida del proyecto.

#### 6.1.1.1 Recursos cloud (infrastructura) {#6.1.1.1-recursos-cloud-(infrastructura)}

* **Patrón general:**  {environment}\_{project}\_{resource-type}\_{purpose}\_{number}  
* **Restricciones:** Se prioriza el uso de minúsculas y guiones medios para recursos de red/almacenamiento, y guiones bajos donde el proveedor no admita guiones medios (ej. BigQuery).

**Diccionario de abreviaturas**

| Tipo | Abreviatura | Descripción |
| ----- | ----- | ----- |
| *Environment* | *dev, stg, prod* | *Entorno de despliegue* |
| *Storage* | *gcs* | *Object storage bucket* |
| *Compute* | *vm, gke, func, run* | *Recursos de cómputo* |
| *Data* | *bq, sql, red* | *Bases de datos* |
| *Network* | *vpc, sb, fw* | *Networking* |
| *Messaging* | *Ps (PubSub), kafka, topic* | *Colas y mensajería* |

#### 6.1.1.2 Objetos de Datos {#6.1.1.2-objetos-de-datos}

* **Estándar**: Se impone estrictamente *\#snake\_case (minúsculas y guiones bajos)\#*, usando nombres descriptivos en *\#idioma\#* evitando palabras reservadas en SQL.

* **Patrón de tablas: ** *\#{layer\_prefix}\_{entity}\_{granularity}\#*

* **Patrón de columnas:** \#snake\_case/camel\_case…\#. 

**Diccionario de abreviaturas**

| Capa | Prefijo | Descripción |
| ----- | ----- | ----- |
| *Bronze* | *raw\_* | *Data crudo* |
| *Silver* | *stg\_* | *Dato limpio y normalizado* |
| *Gold (dim)* | *dim\_* | *Tabla maestra de entidad* |
| *Gold (fact)* | *fact\_* | *Tabla transaccional métrica* |
| *Vistas* | *vw\_* | *Lógica de negocio encapsulada* |

## 6.2. Infraestructura como código (IaC) {#6.2.-infraestructura-como-código-(iac)}

En este diseño se adopta un enfoque estricto de infrastructura como código, esto es, el aprovisionamiento, configuración y gestión de los recursos en la nube (buckets, datasets, permisos IAM, redes,...) se realiza exclusivamente mediante archivos de definición legibles por máquina, y nunca mediante configuración manual en la consola del proveedor cloud.

Este enfoque garantiza la reproducibilidad de los entornos, la auditoría de cambios y facilita la recuperación ante desastres.

### 6.2.1. Estrategia y herramientas {#6.2.1.-estrategia-y-herramientas}

*\#Modificar si existiera otra herramienta o principios\#*

* **Herramienta Estándar**: Se utilizará Terraform como herramienta de orquestación agnóstica a la nube.  
* **Lenguaje**: HCL (HashiCorp Configuration Language).  
* **Principio de Inmutabilidad**: Se prohíben los cambios manuales ("Hotfixes") en la infraestructura productiva. Si se requiere un cambio, se modifica el código, se hace commit y se redesplegará mediante el pipeline.

### 6.2.2. Gestión del Estado {#6.2.2.-gestión-del-estado}

El archivo de estado (terraform.tfstate) es el mapeo que vincula el código con la realidad en la nube. Dado que contiene información sensible, se aplican las siguientes reglas:

* **Backend Remoto**: El estado NO se guarda en local ni en el repositorio Git. Se almacena en un Bucket de almacenamiento seguro con versionado activado.  
* **Bloqueo de estado**: Se implementa un mecanismo de bloqueo (nativo en GCS) para impedir que dos ingenieros o pipelines intenten modificar la infraestructura simultáneamente y corrompan el estado.  
* **Cifrado**: El archivo de estado está cifrado en reposo.

### 6.2.3. Modularización y reutilización {#6.2.3.-modularización-y-reutilización}

Para evitar la duplicación de código y garantizar el cumplimiento de estándares se utilizará una arquitectura basada en módulos.

* **Módulos Raíz**: Definen la arquitectura específica de cada entorno.  
* **Módulos Reutilizables** **(compartidos)**: Librería de componentes pre-configurados y securizados.

*\#Añadir un apartado convenciones de nomenclatura si aplica en la [sección 6.1.1](#6.1.1.-convenciones-de-nomenclatura)\#*

## 

## 6.3. Estrategia de CI/CD y gestión de versiones {#6.3.-estrategia-de-ci/cd-y-gestión-de-versiones}

La automatización del ciclo de vida del desarrollo es fundamental para garantizar entregas fiables. Este apartado define cómo se gestiona el código fuente, cómo colaboran los desarrolladores y cómo se promocionan los cambios entre entornos de forma segura y auditada.

## 6.3.1. Control de versiones {#6.3.1.-control-de-versiones}

* **Plataforma**: *\#GitHub / GitLab / Bitbucket / Azure DevOps*\#  
* **Estrategia de repositorios**: *\#Elegir una de las siguientes\#*  
  * Opción 1: Monorepo \- Todo en un repositorio  
  * Opción 2: Multi Repo \- Repositorio por componente  
* **Convención de nomenclatura**: *\#Elegir cómo será el estándar\#*

Se recomienda seguir el estándar [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) para automatizar el versionado semántico y la generación de Changelogs.

###  6.3.2. Estrategia de branching (flujo de trabajo) {#6.3.2.-estrategia-de-branching-(flujo-de-trabajo)}

Dado que los proyectos de datos requieren iteración continua se adopta el modelo *\#GitHub Flow / Gitflow/ Trunk-Based Development\#*. *\#Detallar en qué consiste el modelo elegido y modificar el diagrama adjunto\#*.

![][image3]

**Estructura de ramas**

```shell
main (producción) 
├── develop (integración) 
│ ├── feature/nueva-funcionalidad 
│ ├── feature/otra-funcionalidad 
│ └── hotfix/fix-critico 
└── release/v1.2.0
```

**Propósito y políticas de protección**

* **main**: *\#Contiene el código productivo verificado. Protegida, requiere PR aprobado, no permite force push\#*  
* **develop**: *\#Entorno de integración para nuevas funcionalidades. Protegida, requiere PR aprobado\#*  
* **feature branches**: *\#Ramas temporales para desarrollos específicos que se eliminan tras el merge exitoso. Sin protección, se borran tras merge\#*

### 6.3.3. Pipeline de CI/CD {#6.3.3.-pipeline-de-ci/cd}

* **Herramienta**: *\#GitHub Actions / GitLab CI / Jenkins / Azure DevOps / Cloud Build*\#.  
* **Enfoque:** *\#Pipeline as Code, La definición del pipeline reside en el propio repositorio (ej. archivo .yaml)\#.*

**Matriz de etapas del pipeline**

| Stage | Trigger | Acciones | Objetivo |
| :---- | :---- | :---- | :---- |
| *Build & CI* | *Push a cualquier rama* | *Lint, unit tests, security scan* | *Asegurar que el código nuevo es limpio, seguro y no rompe la lógica básica* |
| *Delivery* | *Merge a develop o main* | *Plan/Dry run* | *Validar que los cambios se pueden desplegar técnicamente sin errores* |
| *Release* | *Aprobación manual o tag* | *Deploy prod: Aplicar cambios de IaCDocs generation: actualizar documentación de linaje y catálogo* | *Puesta en valor para el usuario final* |

## 6.4. Observabilidad {#6.4.-observabilidad}

En esta sección describimos la estrategia de monitorización a implementar en la que no sólo se vigila la salud de los servidores sino también la salud del dato, el rendimiento de los pipelines y el coste acumulado. El objetivo de esos sistemas es la detección de anomalías (retrasos, caída de volumen, esquemas rotos) antes de que impacten en los informes de negocio, basándose en los tres pilares de la observabilidad: Métricas, Logs y Trazas.

### 6.4.1. Definición de métricas {#6.4.1.-definición-de-métricas}

Para evaluar objetivamente la salud de la plataforma, se definen una serie de métricas clave (KPIs). Estas métricas establecen la línea base del rendimiento normal y sirven de disparador para las alertas definidas posteriormente. Las métricas se clasifican en tres dimensiones: **Operativas** (rendimiento del pipeline), de **Calidad** (fiabilidad del dato) y de **Infraestructura/Coste** (eficiencia).

#### 6.4.1.1 Métricas operativas {#6.4.1.1-métricas-operativas}

Estas métricas miden el rendimiento y la fiabilidad del proceso de movimiento de datos.

| Métrica | Definición | Umbral de alerta |
| :---- | :---- | :---- |
| *Latencia de ingesta (lag)* | *Tiempo transcurrido desde que el dato se genera en origen hasta que está disponible en la capa Gold.* | *\> 2 horas* |
| *Tasa de error* | *Porcentaje de ejecuciones de DAGs o Jobs fallidos respecto al total en una ventana de tiempo.* | *\> 5% en 1 hora* |
| *Duración del pipeline* | *Tiempo total de ejecución de un flujo crítico (End-to-End).* | *\> 120% del promedio semanal* |
| *Frescura* | *Tiempo transcurrido desde la última actualización exitosa de una tabla crítica.* | *\> 24 horas (para cargas diarias)* |

#### 

#### 6.4.1.2 Métricas de calidad del dato {#6.4.1.2-métricas-de-calidad-del-dato}

Estas métricas miden la fiabilidad y usabilidad de la información almacenada.

| Métrica | Definición | Umbral de alerta |
| :---- | :---- | :---- |
| *Volumen de registros* | *Cantidad de filas ingestadas comparada con periodos anteriores (detección de caídas silenciosas).* | *Desviación \> 20% vs media de 7 días* |
| *Tasa de nulos* | *Porcentaje de valores nulos en columnas obligatorias/críticas.* | *\>0% en PKs, \>5% en columnas opcionales* |
| *Integridad de esquema* | *Detección de cambios no controlados (columnas borradas, cambios de tipo).* | *Cualquier cambio (booleano)* |
| *Duplicados* | *Número de registros que violan la clave primaria (PK)* | *\>0 registros* |

#### 6.4.1.2 Métricas de infrastructura {#6.4.1.2-métricas-de-infrastructura}

Estas métricas miden la saturación del sistema y la eficiencia financiera.

| Métrica | Definición | Umbral de alerta |
| :---- | :---- | :---- |
| *Uso de slots/cómputo* | *Cantidad de unidades de computación (ej. BigQuery Slots / vCPUs) utilizadas concurrentemente* | *\>80% de la cuota asignada* |
| *Bytes procesados* | *Volumen de datos escaneados por consultas SQL (proxy de coste).* | *Queries unitarias \>1 TB* |
| *Coste diario proyectado* | *Gasto acumulado del vía vs presupuesto diario asignado* | *\>100% del presupuesto* |

### 6.4.2. Estrategia de monitorización y dashboards {#6.4.2.-estrategia-de-monitorización-y-dashboards}

A continuación, se detallan las herramientas y paneles de control que permitirán visualizar el estado del sistema en tiempo real. El objetivo de los mismos es la centralización de la información técnica y de negocio en una vista unificada.

**Stack de monitorización**

* **Herramienta principal**: *\#Google Cloud Monitoring / Datadog / Prometheus \+ Graphana\#*.  
* **Gestión de errores**: *\#Google Error Reporting / Sentry\#* para agrupación automática de stack traces.

**Dashboards clave**

| Dashboard | Descripción y propósito | Métricas Clave |
| :---- | :---- | :---- |
| *Pipelines health* | *Visión general del estado de los flujos de datos.* | *Tasa de éxito/fallo de DAGs, duración de job, retraso (lag) en ingesta.* |
| *Data quality* | *Monitorización de la fiabilidad del dato.* | *% de nulos, registros duplicados, tests de dbt fallidos, frescura del dato.* |
| *Infrastructura* | *Salud de recursos de cómputo.* | *Uso de CPU/RAM en K8s, slots consumidos en BQ, IOPS de disco.* |
| *FinOps / Costes* | *Control de gasto acumulado.* | *Coste diario por servicio, conste por consulta SQL, proyección a fin de mes.* |

### 6.4.3. Estrategia de logging y auditoría {#6.4.3.-estrategia-de-logging-y-auditoría}

En esta sección se define una estrategia de centralización y retención de logs que cumpla con los requisitos legales y operativos y que agilice el diagnóstico de incidencias y la auditoría de seguridad.

**Configuración de logs**

* **Centralización**: Todos los componentes enviarán sus logs a *\#destino (ej. Cloud Logging / Elasticsearch)\#*.  
* **Formato**: Se impone el uso de Structured Logging (JSON) para facilitar consulta y el filtrado automático (evitar texto plano).  
* **Nivel de log**:  
  * **Producción**: INFO (Operativa normal) y ERROR.  
  * **Dev/Staging** *\#Revisar nombre de entornos\#*: DEBUG (Para trazabilidad profunda).

**Retención y ciclo de vida**

Se implementará una arquitectura de almacenamiento de logs por niveles (*tiering*) para optimizar costes:

* **Hot storage (consulta inmediata)**: Retención de *\#X días\#* en la herramienta de  monitorización para la depuración rápida de errores recientes.  
* **Cold storage (auditoría/histórico)**: Exportación automática (log sink) a *\#destino (ej. GCS Archive)\#* con una retención de *\#X años\#* para cumplimiento normativo y análisis forense.

**Nota:** Se configurará un log sink agregado para capturar eventos de auditoría (cloudaudit.googleapis.com) y volcarlos en un bucket inmutable (*lock bucket*) para garantizar la seguridad forense.

###  6.4.4. Matriz de alertas y respuestas {#6.4.4.-matriz-de-alertas-y-respuestas}

Para evitar la *fatiga por alertas* (ignorar avisos por exceso de ruido), se define una matriz de severidad clara basada en las métricas anteriores. Solo las incidencias que requieren acción humana inmediata despertarán al ingeniero; el resto se registrarán para revisión pasiva.

**Política de notificación**

* **Canales:** *\#Lista de canales (ejemplo. Slack data-alerts, PagerDuty, Mail corporativo,...\#*  
* **Automatización:** *\#Ejemplo: Siempre que sea posible, las alertas intentarán una auto-remediación (reintento automático) antes de escalar a un humano.\#*

**Matriz de severidad**

| Severidad | Escenario (condiciones) | Destinatarios | SLA Respuesta |
| :---- | :---- | :---- | :---- |
| *CRITICAL (P1)* | *Pipeline core fallido tras reintentos.Integridad de datos comprometida en capa Gold.Coste diario \> 150% del umbral.* | *Llamada telefónica al ingeniero de guardia \+ manager* | *\< 15 min* |
| *WARNING (P2)* | *Retraso de carga no crítica (latencia \> 2h)Calidad de datos degradada (warning tests)Uso de recursos al 80%* | *Slack (@channel) \+ email al equipo de ingeniería* | *\< 4 horas (horario laboral)* |
| *INFO (P3)* | *Carga diaria finalizada OKDespliegue a producción exitosoBackup realizado* | *Slack (log channel) \- sin notificación activa* | *N/A* |

# **7\. Estrategia de validación y pruebas** {#7.-estrategia-de-validación-y-pruebas}

El propósito de esta sección es definir el marco de trabajo para garantizar que la arquitectura implementada cumple con los requisitos funcionales, técnicos y de calidad del dato definidos previamente. El enfoque se basa en una estrategia de *data testing* que cubre desde la ingesta hasta el consumo final, asegurando la integridad, seguridad y rendimiento del stack tecnológico.

## 7.1. Pruebas unitarias {#7.1.-pruebas-unitarias}

Este apartado describe la fase de validación de las funciones de transformación y lógica de negocio a nivel atómico para asegurar que cada pieza (SQL, Python, IaC) funcione de forma aislada.

Las pruebas unitarias se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña Pruebas Unitarias) para simplificar el presente documento.

## 7.2. Pruebas de integración {#7.2.-pruebas-de-integración}

Este apartado describe la fase de validación de los componentes de la solución propuesta en conjunto dentro de los pipelines, verificando la conectividad y el flujo de datos entre las distintas capas.

Las pruebas unitarias se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña Pruebas de Integración) para simplificar el presente documento.

## 7.3. Pruebas de calidad del dato {#7.3.-pruebas-de-calidad-del-dato}

En este apartado se detallan aquellas pruebas que más allá de la funcionalidad técnica aseguran que el contenido de la arquitectura de datos es confiable. Se centran en el cumplimiento de los contratos de datos y las expectativas de negocio sobre la información.

Las pruebas de calidad del dato se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña Calidad del dato).

## 7.4. Pruebas de carga y rendimiento {#7.4.-pruebas-de-carga-y-rendimiento}

En este apartado se detallan las pruebas que validan el comportamiento de la arquitectura diseñada bajo condiciones de estrés, grandes volúmenes de datos y concurrencia. El objetivo es asegurar que las estrategias de particionamiento y clústering definidas en la [sección 4.4.3](#4.4.3-estrategia-de-particionamiento-y-clustering) son efectivas.

Las pruebas de carga y rendimiento se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña Pruebas de carga).

## 7.5. Pruebas de seguridad y acceso {#7.5.-pruebas-de-seguridad-y-acceso}

En este apartado se describen las pruebas de validación de los controles de seguridad definidos en la [Sección 5](#5.-seguridad,-gobierno-y-cumplimiento), asegurando que la información sensible está protegida y que sólo los roles autorizados pueden acceder a los datos correspondientes.

Las pruebas de seguridad y acceso se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña Seguridad y Acceso).

## 7.6. Pruebas de aceptación de usuario (UAT) {#7.6.-pruebas-de-aceptación-de-usuario-(uat)}

En este apartado se detallan las pruebas para llevar a cabo la última fase de validación donde los usuarios de negocio confirman que los casos de uso descritos en el apartado 2.3 resuelven sus necesidades y que el modelo de datos es útil para el análisis final.

Las pruebas de aceptación de usuario (UAT) se detallan en el siguiente [documento](https://docs.google.com/spreadsheets/d/1wJgx3ql0A97BH3bMd4Ud3F7PPprVQK617WE3kPT-ngk/edit?usp=drive_link) (pestaña UAT).

# **8\. Estrategia FinOps** {#8.-estrategia-finops}

Esta sección detalla la estrategia para garantizar la sostenibilidad económica del proyecto. Se definen las estimaciones de costes, los mecanismos de control presupuestario y la gestión de límites de recursos (cuotas) para evitar sorpresas en la facturación y paradas de servicio por agotamiento de capacidad.

## 

## 8.1. Estimación de costes {#8.1.-estimación-de-costes}

A continuación se detalla la estimación del coste mensual esperado de la solución en producción, desglosados por los costes fijos (licencias, instancias reservadas,...) y variables (almacenamiento, computación bajo demanda,...).

Esta estimación se basa en la [calculadora oficial de GCP](https://cloud.google.com/products/calculator?hl=en) y otros proveedores (*\#Ejemplo [Fivetran](https://fivetran.com/pricing-estimator)\#*) y asume un crecimiento de datos del 10% anual. 

| Servicio | Métrica de cobro | Consumo estimado | Coste estimado (€/mes) |
| :---- | :---- | :---- | :---- |
| *Almacenamiento (GCS)* | *GB/mes (Clase standard)* | *5 TB* | *\~ 100€* |
| *Cómputo ETL (Dataflow)* | *vCPU/hora \+ memoria* | *50 horas/día* | *\~300€* |
| *BigQuery* | *TB procesados (analysis)* | *100 TB* | *\~500€* |
| *Orquestador (Composer)* | *Instancia/hora* | *24x7 (Small)* | *\~300€* |

**Disclaimer:** Esta estimación no es un presupuesto cerrado y existen variables fuera del control de la ingeniería (volumen de datos futuro, consultas masivas por usuarios, subidas de precio del proveedor) que pueden alterar la factura. Se recomienda la revisión mensual y ajuste de presupuestos.

### 8.1.1. Estrategia de precios y ediciones (BigQuery Editions) {#8.1.1.-estrategia-de-precios-y-ediciones-(bigquery-editions)}

*\#Incluir este apartado si se quiere optar por BigQuery Editions para controlar costes de consultas.\#*

Para mitigar la volatilidad de precios del modelo on-demand (pago por TB procesado), este proyecto opta por el uso de BigQuery Editions. Este modelo basa la facturación en la capacidad de cómputo reservada (Slots/Hora) en lugar del volumen de datos leídos.  Esta estrategia permite establecer un techo máximo de gasto, garantizando que, independientemente de cuántas consultas se lancen o cuán ineficientes sean, el coste por hora nunca superará el límite de capacidad definido.

*\#Seleccionar las ediciones que se usarán en el proyecto y detallar más abajo para qué en específico. Revisar si ha habido cambios en las condiciones de las mismas en la página oficial de GCP.\#*

| Edición | Características clave | Caso de uso en proyecto |
| :---- | :---- | :---- |
| *Standar* | *Coste más bajo. Sin caché de resultados. Sólo SQL estándar.* | *\#SI/NO\# (ideal para cargas ETL nocturnas no críticas)* |
| *Enterprise* | *Rendimiento equilibrado. Incluye ML, caché y gestión de cargas.* | *\#SI/NO\# (recomendado para producción y data warehouse general)* |
| *Enterprise Plus* | *Máximo rendimiento, cumplimiento estricto (HIPAA/PCI), Disaster recovery avanzado* | *\#SI/NO\# (sólo para casos críticos de banca o salud)* |

**Configuración de Autoscaling**

Se configurará una reserva de slots con autoescalado para optimizar el ratio coste/rendimiento:

* **Baseline Slots (Mínimo)**: *\#Ej. 0 Slots\#*. No se paga nada si no hay consultas ejecutándose.  
* **Max Autoscaling Slots (Techo de Gasto)**: *\#Ej. 400 Slots\#*.

Esto crea un "cortafuegos" financiero. El sistema escalará recursos si es necesario, pero nunca gastará más allá de los 400 slots por hora, aunque se lance una consulta masiva. Si la demanda supera los 400 slots, las consultas se pondrán en cola siendo más lentas pero no serán más caras.

**Estimación de Ahorro**

Se estima que el uso de la edición *\#Standard/Enterprise\#* junto con el compromiso de uso de *\#1 año (Committed Use Discount)\#* reducirá la factura de cómputo en un *\#Ej. 20-40%\#* respecto al modelo *on-demand*.

## 8.2. Política de presupuestos y gobernanza financiera {#8.2.-política-de-presupuestos-y-gobernanza-financiera}

Habiendo definido las herramientas de monitorización y los KPIs financieros en el apartado [6.4. Observabilidad](#6.4.-observabilidad), esta sección establece las reglas de negocio que regirán el control del gasto. Aquí se definen los límites presupuestarios aprobados, la estrategia de imputación de costes y el protocolo de actuación ante desviaciones.

**Definición de presupuestos**

| Ámbito | Presupuesto mensual  | Acción al superar el 100% |
| :---- | :---- | :---- |
| *Producción* | *1500€* | *Alerta a management (no detener el servicio)* |
| *Desarrollo* | *300€* | *Detención automática de recursos no críticos* |
| *Sandbox / POC* | *100€* | *Notificación al propietario* |

**Protocolo de actuación ante desviaciones**

Si las alertas definidas en el apartado [6.4.4 (Matriz de Severidad)](#6.4.4.-matriz-de-alertas-y-respuestas) se activan, se procederá según el siguiente protocolo:

*\# Ejemplo*

* ***Nivel 1 (Aviso 50-80%)**: Revisión pasiva por parte del Tech Lead.*  
* ***Nivel 2 (Aviso 90%)**: Auditoría inmediata de las consultas más costosas (vía Dashboard FinOps definido en la sección [6.4.2](#6.4.2.-estrategia-de-monitorización-y-dashboards)) para identificar ineficiencias.*  
* ***Nivel 3 (\>100%)**: Requiere aprobación explícita del Product Owner para ampliar la cuota o, en su defecto, reducción de la retención de datos o frecuencia de carga.*

*\#*

**Estrategia de asignación de costes**

Para garantizar que el gasto pueda atribuirse a un centro de coste o proyecto, se impone la siguiente política de etiquetado obligatorio en la infraestructura (IaC):

*\#Ejemplos*

* ***Etiqueta** centro\_coste: (Ej. Marketing, Logística, IT\_Común).*  
* ***Etiqueta** entorno: (Ej. pro, pre, dev).*  
* ***Etiqueta** servicio: (Ej. data-lake, etl-pipeline, bi-tool).\#*

**Nota**: Los recursos que no cumplan con estas etiquetas serán detectados por las políticas de la nube y marcados para su revisión o eliminación (si aplica).

**Estrategia de Análisis de Costes en BigQuery**  
*\#Determinar si aplica o se construirá\#* Se desplegará un dashboard financiero conectado a INFORMATION\_SCHEMA. JOBS\_BY\_PROJECT para monitorizar el coste exacto por consulta (total\_bytes\_billed) y atribuir costes a usuarios o procesos específicos.

## 8.3. Gestión de límites de consumo y cuotas {#8.3.-gestión-de-límites-de-consumo-y-cuotas}

En esta sección se definen los controles que bloquearán la ejecución de procesos no controlados para evitar costos no esperados debidos a errores humanos (i.e. queries mal formadas) o problemas técnicos (i.e. bucles infinitos en funciones). A diferencia de las alertas de presupuesto que sólo notifican, estos controles bloquearán la ejecución del proceso si supera el umbral definido.

### 8.3.1. Límites de coste por usuario y proyecto {#8.3.1.-límites-de-coste-por-usuario-y-proyecto}

A continuación se definen las restricciones configuradas a nivel de servicio para limitar la cantidad de recursos que un usuario o proceso puede consumir en un tiempo determinado.

| Servicio | Nivel de aplicación | Límite configurado | Justificación |
| :---- | :---- | :---- | :---- |
| *BigQuery* | *Por usuario* | *1 TB/día* | *Evita que un analista lance accidentalmente consultas masivas que disparen el coste* |
| *BigQuery* | *Por Service Account* | *Sin límite* | *Los procesos automáticos críticos no deben bloquearse, pero se monitorizan.* |
| *BigQuery* | *Por proyecto* | *2000 slots (si aplica flat rate)* | *Asegura que un proyecto de desarrollo no consuma toda la capacidad de cómputo de la organización.* |
| *BigQuery* | *Por Query* | *5 TB máximo por consulta* | *Bloquea inmediatamente cualquier consulta única que intente escanear tablas gigantescas sin filtros de partición.* |
| *Cloud Functions/Run* | *N/A* | *50 instancias concurrentes como máximo* | *Evitar escalado infinito en caso de ataque DDoS o bucle de reintentos* |
| *GCS* | *N/A* | *7 días de TTL (time-to-live) para tablas temporales* | *Reducir costes de almacenamiento temporal* |

### 8.3.2. Cuotas técnicas del proveedor (capacity planning) {#8.3.2.-cuotas-técnicas-del-proveedor-(capacity-planning)}

En esta sección se identifican las cuotas de servicio del proveedor (GCP) que podrían actuar como límite físico y se planifica la solicitud de aumento de las mismas antes del despliegue para evitar interrupciones del servicio.

| Servicio | Cuota / Límite | Uso estimado (Pico) | ¿Requiere aumento? |
| :---- | :---- | :---- | :---- |
| *BigQuery API* | *Queries concurrentes (100)* | *20* | *No* |
| *BigQuery Query* | *Slots/CPU (2000 slots)* | *500 slots* | *No* |
| *Cloud Functions* | *Instancias concurrentes* | *150* | *Sí (solicitar 500\)* |
| *IPs estáticas* | *IP regionales (8)* | *10* | *Sí (solicitar 20\)* |

# 

# **9\. Conclusiones y próximos pasos** {#9.-conclusiones-y-próximos-pasos}

El presente diseño cubre los requisitos establecidos y ofrece una base sólida para la implementación de la plataforma del dato de *\#Cliente\#*.

**Próximos pasos inmediatos**

1. Aprobación formal de este documento por parte del *\#Cliente\#*.  
2. Desarrollo del **Roadmap** de implementación con el estudio de la brecha entre la situación AS IS y TO BE, el detalle, estimación y temporalización de las actividades a desarrollar así como el dimensionamiento del equipo y costes de construcción y mantenimiento.

| About Devoteam  Devoteam is a tech consulting firm specialised in cloud, cybersecurity, data, and sustainability. Tech Native for over 25 years, Devoteam guides businesses through sustainable digital transformation to unlock their full potential. With over 10,000 employees in more than 25 countries across Europe, the Middle East, and Africa, Devoteam is committed to putting technology at the service of people. To realise this vision, we partner with the top cloud platforms in the world, Microsoft Azure, Google Cloud, and AWS.  |
| :---- |

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,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>

[image3]: <data:image/png;base64,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>