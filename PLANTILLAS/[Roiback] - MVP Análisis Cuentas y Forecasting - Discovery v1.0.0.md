# 

# 

# \#\#Cliente\#\# \- \#\#Proyecto\#\#

## 

## Discovery

**Hoja de control**

**Control de documentación**

|  |  |
| :---- | :---- |
| **Document Code** | \#\#Cliente\#\#- \#\#Proyecto\#\# \- Entregable Discovery |
| **Preparado por:** | \#\#Nombre técnico Devoteam\#\# |
| **Fecha** | \#\#dd/mm/yyyy\#\# |

**Control de versiones**

| Versión | Autor | Fecha | Comentarios |
| :---- | :---- | :---- | :---- |
| v1.0 | Data Accelerator | 8 Dec 2025 | Versión funcional entregable Discovery |
|  |  |  |  |
|  |  |  |  |

**Control de revisión y aprobación**

|  | Nombre | Fecha | Firma |
| :---- | :---- | :---- | :---- |
| **Revisado por** |  |  |  |
| **Aprobado por** |  |  |  |

# 

## Índice

[**Instrucciones de uso de esta plantilla	5**](#instrucciones-de-uso-de-esta-plantilla)

[**1\. Introducción y contexto	6**](#1.-introducción-y-contexto)

[1.1. Propósito del documento	6](#1.1.-propósito-del-documento)

[1.2 Contexto de Negocio	6](#1.2-contexto-de-negocio)

[1.3 Metodología y stakeholders involucrados	7](#1.3-metodología-y-stakeholders-involucrados)

[**2\.  Definición de objetivos y requisitos	8**](#2.-definición-de-objetivos-y-requisitos)

[2.1 Objetivos Estratégicos de Negocio	8](#2.1-objetivos-estratégicos-de-negocio)

[2.2. Casos de uso prioritarios	8](#2.2.-casos-de-uso-prioritarios)

[2.3. Requisitos del Sistema	9](#2.3.-requisitos-del-sistema)

[2.3.1. Requisitos funcionales	9](#2.3.1.-requisitos-funcionales)

[2.3.2. Requisitos técnicos (no funcionales)	10](#2.3.2.-requisitos-técnicos-\(no-funcionales\))

[**3\. Análisis de la arquitectura y plataforma actual (AS-IS)	11**](#3.-análisis-de-la-arquitectura-y-plataforma-actual-\(as-is\))

[3.1. Visión general de la arquitectura	11](#3.1.-visión-general-de-la-arquitectura)

[3.2. Stack tecnológico	12](#3.2.-stack-tecnológico)

[3.2.1. Fuentes de datos	12](#3.2.1.-fuentes-de-datos)

[3.2.2. Almacenamiento de datos	13](#3.2.2.-almacenamiento-de-datos)

[3.2.3. Ingesta de datos	13](#3.2.3.-ingesta-de-datos)

[3.2.4. Procesamiento y transformación	14](#3.2.4.-procesamiento-y-transformación)

[3.2.5. Orquestación y automatización	14](#3.2.5.-orquestación-y-automatización)

[3.2.6. Modelado y Arquitectura de datos	14](#3.2.6.-modelado-y-arquitectura-de-datos)

[3.2.7. Computing y Networks	15](#3.2.7.-computing-y-networks)

[3.2.8. Explotación de datos (BI & AI/ML)	16](#3.2.8.-explotación-de-datos-\(bi-&-ai/ml\))

[3.3. Análisis de flujos de datos	16](#3.3.-análisis-de-flujos-de-datos)

[3.3.1. Patrones de ingesta y latencia	16](#3.3.1.-patrones-de-ingesta-y-latencia)

[3.3.2. Trazabilidad y ciclo de vida (end-to-end)	17](#3.3.2.-trazabilidad-y-ciclo-de-vida-\(end-to-end\))

[**4\. Gobierno, seguridad y operaciones	17**](#4.-gobierno,-seguridad-y-operaciones)

[4.1. Seguridad y Gestión de identidades (IAM)	17](#4.1.-seguridad-y-gestión-de-identidades-\(iam\))

[4.1.1. Análisis de roles y permisos	17](#4.1.1.-análisis-de-roles-y-permisos)

[4.1.2. Gestión de credenciales	18](#4.1.2.-gestión-de-credenciales)

[4.2. Organización de Recursos Cloud	18](#4.2.-organización-de-recursos-cloud)

[4.3. Gobierno y Calidad del Dato	18](#4.3.-gobierno-y-calidad-del-dato)

[4.3.1. Catálogo de Datos y Glosario	19](#4.3.1.-catálogo-de-datos-y-glosario)

[4.3.2. Linaje del dato	19](#4.3.2.-linaje-del-dato)

[4.3.3. Calidad y perfilado del dato	19](#4.3.3.-calidad-y-perfilado-del-dato)

[4.3.4. Seguridad del Dato (fine-grained access)	19](#4.3.4.-seguridad-del-dato-\(fine-grained-access\))

[4.4. Fundamentos de ingeniería y DevOps	20](#4.4.-fundamentos-de-ingeniería-y-devops)

[4.4.1. Organización del Código (Git)	20](#4.4.1.-organización-del-código-\(git\))

[4.4.2. Ciclo de Vida y Despliegue	20](#4.4.2.-ciclo-de-vida-y-despliegue)

[4.4.3. Infraestructura como Código (IaC)	20](#4.4.3.-infraestructura-como-código-\(iac\))

[4.4.4. Estándares y Buenas Prácticas	21](#4.4.4.-estándares-y-buenas-prácticas)

[4.5. Monitorización y Alertas	21](#4.5.-monitorización-y-alertas)

[4.5.1. Observabilidad técnica	21](#4.5.1.-observabilidad-técnica)

[4.5.2. Alertas y protocolos	21](#4.5.2.-alertas-y-protocolos)

[**5\. Análisis de costes y Eficiencia	21**](#5.-análisis-de-costes-y-eficiencia)

[5.1. Orígenes del Gasto	22](#5.1.-orígenes-del-gasto)

[5.2. Oportunidades de optimización	22](#5.2.-oportunidades-de-optimización)

[5.2.1. Análisis de Queries Costosas	22](#5.2.1.-análisis-de-queries-costosas)

[5.2.2. Análisis de uso de slots	23](#5.2.2.-análisis-de-uso-de-slots)

[5.2.3. Análisis de almacenamiento (lógico vs físico)	24](#5.2.3.-análisis-de-almacenamiento-\(lógico-vs-físico\))

[**6\. Hallazgos principales y recomendaciones	25**](#6.-hallazgos-principales-y-recomendaciones)

[6.1. Resumen de fortalezas de la arquitectura actual	25](#6.1.-resumen-de-fortalezas-de-la-arquitectura-actual)

[6.2. Identificación de puntos de dolor	25](#6.2.-identificación-de-puntos-de-dolor)

[6.3. Recomendaciones y puntos de mejora	26](#6.3.-recomendaciones-y-puntos-de-mejora)

[**About Devoteam	28**](#about-devoteam)

# **Instrucciones de uso de esta plantilla** {#instrucciones-de-uso-de-esta-plantilla}

**Esta página debe eliminarse antes de la entrega del documento al cliente**.

- Usar siempre fuente **Montserrat Normal** (en estilo estándar o negrita, según convenga) con **tamaño 10.5** e **interlineado de 1.15** en bloques de texto.

- Respetar los **formatos de título** (Heading 1, Heading 2 y Heading 3 con sus respectivos tamaños de fuente) definidos en este documento.

- Tened cuidado de no modificar la fuente o espaciado por accidente al copiar y pegar desde otros orígenes.

- La **orientación** del documento será siempre **vertical** y se deberán respetar los márgenes del documento evitando en todo momento que las imágenes, diagramas o tablas excedan dichos márgenes.

- Una vez finalizado el documento **regenerar el índice** y comprobar formatos ya que suelen alterarse cambiando la fuente a otra que no es Montserrat.

- Los comentarios añadidos con *\#\#sombreado gris y en cursiva\#\#* deben **eliminarse o reemplazarse** por el texto adecuado ya que son ejemplos ilustrativos o notas con referencias a documentos externos. En todo caso, se debe revisar que no exista ningún comentario con este formato en el momento de la entrega a Cliente. *\#\#sombreado rosa y en cursiva\#\#*  se encuentra la explicación de qué rellenar en las secciones, eliminar después de rellenar

- Los links a los documentos de anexos (checklist, inventario de recursos o similares) deberán clonarse desde sus respectivas plantillas del [Shared Drive del Acelerador](https://drive.google.com/drive/folders/1VYaRYObi9oXvUWdEs05b_CJVBtz3XCi2?usp=sharing) y hacer una copia editable en la carpeta del cliente, para así vincularlos a este documento.

# **1\. Introducción y contexto** {#1.-introducción-y-contexto}

## 1.1. Propósito del documento {#1.1.-propósito-del-documento}

El objetivo de este documento es **formalizar y consolidar los hallazgos** obtenidos durante la fase de *Discovery* del proyecto *\#\#Nombre del Proyecto\#\#*.  Su finalidad es presentar un análisis integral del estado actual (*AS IS*) de la infraestructura de datos, la arquitectura y procesos operativos de *\#\#Cliente\#\#* que permita anticipar desafíos técnicos y eliminar suposiciones.

Este entregable actúa como **herramienta de diagnóstico** orientada a:

* **Garantizar la alineación estratégica**: Unificar la visión y expectativas de todos los stakeholders (técnicos y de negocio) validando el alcance inicial frente a las necesidades reales detectadas, gestionando posibles desviaciones.

* **Formalizar y priorizar objetivos:** Identificar los objetivos y casos de uso estratégicos, transformándolos en requisitos priorizados según la urgencia y el valor indicados por el cliente.

* **Mapear el ecosistema actual:** Proporcionar visibilidad sobre las fuentes de datos, flujos de información y sistemas existentes, en el contexto de los procesos de negocio que soportan.

* **Diagnosticar puntos de dolor y brechas**: Identificar de forma explícita las ineficiencias técnicas, silos de información o limitaciones de la infraestructura actual que están impactando en la agilidad o la toma de decisiones de negocio.

* **Detectar oportunidades de mejora**: Proponer líneas de acción estratégicas y recomendaciones de alto nivel basadas en la evidencia encontrada, que servirán como punto de partida para la fase de diseño y la creación de un roadmap de implementación.

En esencia, este documento es fundamental para garantizar que la solución final no solo sea técnicamente viable y escalable, sino que aporte un valor tangible y medible al negocio, respondiendo eficazmente a los desafíos y oportunidades identificadas.

## 1.2 Contexto de Negocio  {#1.2-contexto-de-negocio}

*\#\#Breve introducción al Cliente:* 

* ***Actividad y contexto de negocio del cliente:** A qué se dedican, tipo de negocio que desarrollan, servicios que proveen,organización empresarial (si es un grupo de empresas).*  
* ***Contexto operativo:** Desafíos que enfrenta, necesidades detectadas, problemas que estos desafíos le provocan (no incluir puntos de dolor en detalle ya que se especifican en un apartado concreto posteriormente).*  
* ***Objetivos estratégicos:** Objetivos que persiguen a alto nivel.*  
* *Argumentar las necesidades por las que se pone en contacto con Devoteam*

*\#\#*

## 1.3 Metodología y stakeholders involucrados {#1.3-metodología-y-stakeholders-involucrados}

La metodología empleada durante la fase de Discovery se ha centrado en la **recopilación sistemática de información** y la colaboración estrecha con el equipo de *\#\#Cliente\#\#*. El proceso inició con la revisión del [checklist de documentación técnica](https://docs.google.com/spreadsheets/d/1-mmH0ZEud3mSHIVyFdpabpkaq1aAoFKdyRWk-wTI-jc/edit?usp=sharing) solicitado en el kick-off y se profundizó mediante sesiones de trabajo iterativas.

El análisis se ha estructurado en torno a los siguientes **ejes de trabajo**:

* **Levantamiento de requisitos**: Identificación de objetivos de negocio, requisitos funcionales y priorización de casos de uso.

* **Auditoría de Datos**: Revisión de las fuentes existentes, analizando su volumetría, frecuencia de actualización, calidad y políticas de gobierno/acceso.

* **Análisis de Arquitectura**: Evaluación del stack tecnológico actual, flujos de datos y almacenamiento para identificar ineficiencias y puntos de dolor.

* **Evaluación Estratégica**: Análisis de costes, detección de cuellos de botella y definición de recomendaciones clave.

1.3.1 Sesiones de Trabajo

A continuación, se detallan las sesiones conjuntas de trabajo realizadas para la recopilación y validación de la información:

| Fecha | Objetivo de la sesión | Asistentes | Referencia |
| ----- | ----- | ----- | ----- |
| dd/mm/yyyy | \#\#Tópico 1\#\# | \#\#Asistente\#\# | \#\#Link a minuta\#\# |
| dd/mm/yyyy | \#\#Tópico 2\#\# | \#\#Asistente\#\# | \#\#Link a minuta\#\# |

1.3.1 Stakeholders involucrados

En el desarrollo del presente documento y durante la ejecución de la fase de *Discovery*, que ha tenido una duración de \#\#Nº de días\#\# días, han participado los siguientes perfiles tanto de Devoteam y \#\#Cliente\#\#:

| Empresa | Nombre | Rol / Cargo | Contacto |
| ----- | ----- | ----- | ----- |
| Devoteam | \#\#técnico\#\# | Data Engineer | \#\#tecnico@devoteam.com\#\# |
| \#\#Cliente\#\# | \#\#XXXX\#\# | Head of Data | xx.xx@cliente.com |

Tras el cierre de la fase de Discovery, se procederá a la entrega y revisión de este documento de hallazgos, el cual requerirá la aprobación formal por parte de ambos equipos.

# **2\.  Definición de objetivos y requisitos** {#2.-definición-de-objetivos-y-requisitos}

En esta sección se detallan las necesidades identificadas durante las sesiones de Discovery, traduciendo la estrategia de negocio de *\#\#Cliente\#\#* en casos de uso concretos y requisitos técnicos que guiarán la arquitectura de datos.

## 2.1 Objetivos Estratégicos de Negocio {#2.1-objetivos-estratégicos-de-negocio}

En esta sección, se enumeran los objetivos macro de negocio que este proyecto de datos debe habilitar o acelerar:

*\#\#Seguir el formato de bulletpoints por objetivo con formato en negrita y describir a alto nivel lo que se persigue desde el punto de vista de negocio*

* ***Objetivo 1\. Democratización del Dato**: Facilitar el acceso a datos certificados a los equipos de marketing para reducir la dependencia del equipo de IT.\#\#*  
* ***Objetivo 2\. Optimización Operativa**: Reducir los tiempos de generación de informes regulatorios de T+1 a tiempo real (NRT).*  
* ***Objetivo 3\. Descripción**: …\#\#*

## 2.2. Casos de uso prioritarios {#2.2.-casos-de-uso-prioritarios}

Se han identificado y priorizado los siguientes casos de uso iniciales, los cuales servirán de guía para validar la arquitectura propuesta:

| ID | Caso de uso | Descripción breve  | Consumidor | Prioridad |
| ----- | ----- | ----- | ----- | ----- |
| *UC-01* | *\#\#Ej. Dashboard de Ventas\#\#* | *\#\#Visualización consolidada de ventas por región y producto\#\#* | *\#\#Dirección Comercial\#\#* | *Alta* |
| *UC-02* | *\#\#Modelo de Churn\#\#* | *\#\#Dataset preparado para entrenamiento de modelos de fuga de clientes\#\#* | *\#\#Data Science\#\#* | *Media* |

## 2.3. Requisitos del Sistema {#2.3.-requisitos-del-sistema}

Los objetivos estratégicos y casos de uso descritos en las secciones precedentes se traducen en los siguientes requisitos funcionales y técnicos (no funcionales) que guiarán la definición del alcance y el diseño de la solución final, asegurando que la arquitectura propuesta por Devoteam resuelva los problemas claves y/o habilite nuevas funcionalidades para *\#\#Cliente\#\#*.

###  2.3.1. Requisitos funcionales  {#2.3.1.-requisitos-funcionales}

Los **requisitos funcionales** representan el *“qué”* del proyecto, definiendo el comportamiento y las capacidades que la plataforma debe ofrecer a los usuarios finales y a la organización. Se centran por tanto, en las necesidades del negocio, describiendo las funcionalidades necesarias para garantizar el gobierno, la accesibilidad y la confianza en la información, independientemente de la tecnología que se utilice por debajo.

A continuación, se detallan los **requisitos funcionales** identificados:

*\#\# Seguir el formato de bulletpoints por requisito funcional  organizados en torno a títulos en negrita y agrupando los requisitos de la misma tipología o tópico y describiendo lo que se persigue con dichos requisitos. Ejemplo:*

* ***Conectividad e Ingesta:***  
  * *Capacidad para conectar e ingerir datos de fuentes heterogéneas (APIs REST, Bases de datos Relacionales, ficheros planos CSV/Excel).*  
  * *Soporte para mecanismos de carga incremental (CDC \- Change Data Capture) para minimizar el impacto en los sistemas origen.*  
* ***Procesamiento y Lógica de Negocio:***  
  * *Implementación de reglas de negocio para el cálculo de KPIs críticos (ej. Margen Neto, LTV, Churn Rate) asegurando consistencia histórica.*  
  * *Anonimización o enmascaramiento de datos sensibles (PII) antes de su almacenamiento en capas de consumo.*  
* ***Almacenamiento e Historicidad:***  
  * *Capacidad para historificar los cambios en los datos maestros (SCD Tipo 2\) para permitir análisis de "foto a fecha".*  
  * *Retención de datos crudos (raw data) inmutables para permitir reprocesamientos futuros o auditorías.*  
* ***Consumo y Accesibilidad:***  
  * *Disponibilidad de los datos en estructuras optimizadas para analítica (ej. Modelo Estrella o One Big Table) consultables vía SQL.*  
  * *Capacidad para exponer datasets certificados a herramientas de visualización (ej. PowerBI, Tableau, Looker) sin intermediarios manuales.\#\#*

###  2.3.2. Requisitos técnicos (no funcionales) {#2.3.2.-requisitos-técnicos-(no-funcionales)}

Los **requisitos técnicos** representan el “cómo” del proyecto, definiendo el marco tecnológico, la arquitectura y los estándares de ingeniería necesarios para soportar las funcionalidades de negocio. Se centran en la infraestructura y la calidad del software, definiendo cómo se deben construir, asegurar y optimizar las soluciones en el entorno de la nube (GCP) para garantizar el rendimiento, escalabilidad y mantenimiento a futuro.

A continuación, se detallan los **requisitos técnicos (no funcionales)** identificados:

*\#\# Seguir el formato de bulletpoints por requisito técnico organizados en torno a títulos en negrita y agrupando los requisitos de la misma tipología o tópico y describiendo lo que se persigue con dichos requisitos. Ejemplo:*

* ***Escalabilidad y Rendimiento**:*  
  * ***Desacoplamiento**: La arquitectura debe desacoplar el almacenamiento del cómputo para permitir el escalado independiente de recursos según la carga de trabajo.*  
  * ***Latencia de Datos**: El sistema debe garantizar una disponibilidad del dato (Data Freshness) acorde al SLA definido (ej. Batch diario antes de las 08:00 AM o Near-Real-Time con latencia \< 5 min).*  
  * ***Tiempos de Respuesta**: Las consultas analíticas estándar no deben exceder los \#\#X\#\# segundos de ejecución para garantizar una buena experiencia de usuario en los dashboards.*

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
  * ***Etiquetado (Tagging)**: Todos los recursos deben incluir etiquetas de facturación (ej. centro de coste, entorno, proyecto) para permitir un análisis FinOps granular.  \#\#*

# 

# **3\. Análisis de la arquitectura y plataforma actual (AS-IS)**  {#3.-análisis-de-la-arquitectura-y-plataforma-actual-(as-is)}

En esta sección se describe el estado actual de la infraestructura tecnológica y los flujos de datos de *\#\#Cliente\#\#*. El objetivo es comprender las fortalezas, debilidades y dependencias existentes para informar el diseño de la futura arquitectura.

## 3.1. Visión general de la arquitectura {#3.1.-visión-general-de-la-arquitectura}

La arquitectura actual se compone de una combinación de servicios *\#\#on-premise / en el proveedor Cloud X (GCP, AWS, Azure)\#\#*. A continuación, se presenta un diagrama de alto nivel que ilustra los principales componentes y cómo interactúan entre sí.

*\#\#Insertar aquí Diagrama de arquitectura AS-IS de alto nivel \- [Usar las plantillas provistas en Lucidchart](https://lucid.app/lucidchart/1e7860c8-a29b-4262-9413-44dccb320701/edit?viewport_loc=-3529%2C-596%2C8514%2C4806%2C0_0&invitationId=inv_49e1e952-1c05-4449-93b8-9c0d5b884c19)\#\#*

**Descripción de la topología**

*\#\#Describir a alto nivel lo que se ilustra en el diagrama de arquitectura de la situación AS IS. Ejemplo: Se observa una arquitectura tipo Data Warehouse tradicional donde las fuentes de datos vuelcan datos batch a un staging area en GCS,...\#\#*

\#\#**Nota para el equipo de Discovery (eliminar):** Para el uso de herramientas de descubrimiento automático como Asset Inventory, se necesitarán [permisos adicionales](https://docs.google.com/document/d/13uir1j-sD4c72lXmhLx_X3FI4pUmiPJnSVZ5gmbJAeQ/edit?usp=drive_link) y habrá que informar o requerir al cliente los mismos (si fuera posible). Estos permisos deberían eliminarse tras su uso\#\#

\#\#**Nota para el equipo de Discovery (eliminar)**: Para el listado exhaustivo de los servicios y componentes descubiertos se dispone de la plantilla [\[Template\] Inventario de recursos descubiertos](https://docs.google.com/spreadsheets/u/0/d/14CH4-j3OeSWCYkWHzswKdCXA6nZ-c3Wfsw7Ec891IWI/edit) donde se tendrá que rellenar todos los elementos descubiertos\#\#

## 3.2. Stack tecnológico {#3.2.-stack-tecnológico}

A continuación, se detalla el análisis cualitativo de cada dominio funcional de la plataforma, evaluando las herramientas desplegadas y su configuración. Para consultar el listado exhaustivo de todos los activos descubiertos y sus metadatos técnicos, refiérase al anexo [\[Template\] Inventario de recursos descubiertos](https://docs.google.com/spreadsheets/u/0/d/14CH4-j3OeSWCYkWHzswKdCXA6nZ-c3Wfsw7Ec891IWI/edit).

### 3.2.1. Fuentes de datos {#3.2.1.-fuentes-de-datos}

En esta sección se realiza el inventario de los sistemas externos, bases de datos y aplicaciones (ERP, CRM) desde donde se extrae la información.

* **Tipología de fuentes**:  
  * **Bases de datos relacionales**: *\#\#Ejemplo: Oracle On-premise (Finanzas), SQL Server (Marketing),...\#\#*  
  * **APIs y SaaS:** *\#\#Ej: Salesforce, Google Analytics 4, Facebook Ads, APIs de terceros.\#\#*  
  * **Archivos y FTP:** *\#\#Ej: volcados de Mainframe en servidor SFTP, excels manuales en SharePoint.\#\#*  
  * **Eventos:** *\#\#Ej: Webhooks, Logs de aplicaciones móviles.\#\#*

* **Conectividad:** \#\#Describir cómo se accede. Ej: Conexión vía VPN Site-to-Site a on-premise; acceso público a APIs con autenticación OAuth2.\#\#

* **Filtros aplicados en las tablas origen**: *\#\#Describir si se usan filtros o cruces con otras tablas de origen y hacer referencia al Sheets de inventario de recursos descubiertos en la pestaña de fuentes de datos\#\#*

* **Volumetría histórica y deltas diarias:** \#\#Indicar que las volumetrías de las tablas origen se indican en el Sheets de inventario de recursos descubiertos en la pestaña de fuentes de datos\#\#.

**Observaciones y Diagnóstico:**

* \#\#Análisis del consultor. Ej: Gran dependencia de archivos manuales (Excel) propensos a errores humanos. La conexión a la base de datos Oracle on-premise sufre cortes intermitentes por restricciones de ancho de banda en la VPN.\#\#

  ### 3.2.2. Almacenamiento de datos {#3.2.2.-almacenamiento-de-datos}

En esta sección se evalúan las soluciones de persistencia y bases de datos donde reside la información:

* **Servicios e Infraestructura**:   
  * *\#\#Listar servicios identificados. Ej: Google Cloud Storage (Standard/Nearline), BigQuery (Tablas nativas/Externas), PostgreSQL en Cloud SQL, Oracle Exadata On-Premise.\#\#*

* **Observaciones y Diagnóstico**:  
* *\#\#Análisis del consultor. Ej: El uso de BigQuery como Data Warehouse centralizado facilita la escalabilidad. Sin embargo, se detecta una fragmentación de datos en silos (buckets de GCS sin estructura clara) y ausencia de políticas de ciclo de vida (Lifecycle Management), lo que incrementa los costes de almacenamiento.\#\#*

  ### 3.2.3. Ingesta de datos {#3.2.3.-ingesta-de-datos}

En esta sección se realiza el análisis de los mecanismos y herramientas utilizados para mover los datos desde los sistemas origen hacia la plataforma (EL/ETL).

* **Herramientas de Ingesta:**  
  * *\#\#Listar servicios (un item por servicio). Ej: Pub/Sub (Streaming), Kafka, Fivetran (SaaS), Transfer Appliance, Scripts Python custom, Cloud Functions.\#\#*

* **Tipología de Ingesta:**  
  * *\#\#Describir métodos. Ej: Ingesta Batch diaria vía JDBC desde Oracle; Ingesta Streaming de eventos de clickstream; Carga de ficheros planos desde SFTP con Cloud Functions; uso de herramientas SaaS como Fivetran;...\#\#*

* **Observaciones y Diagnóstico:**  
* *\#\#Análisis del consultor. Ej: La ingesta depende excesivamente de scripts manuales (crontab) que fallan silenciosamente. No existe un patrón de 'Backpressure' para la ingesta en streaming, lo que provoca pérdida de mensajes en picos de carga.\#\#*

  ### 3.2.4. Procesamiento y transformación {#3.2.4.-procesamiento-y-transformación}

En esta sección se realiza la evaluación de las herramientas y la lógica aplicada para limpiar, normalizar y enriquecer los datos.

* **Frameworks y Herramientas:**  
  * *\#\#Listar servicios (un ítem por servicio). Ej: Dataflow (Apache Beam), Dataproc (Spark), dbt (SQL based), Procedimientos almacenados en BigQuery, Pandas en Cloud Run.\#\#*

* **Lenguajes y Paradigmas:**  
  * *\#\#Ej: SQL (predominante), Python, Scala. Procesamiento Batch vs. Micro-batch. Paradigma ETL o ELT\#\#*

* **Observaciones y Diagnóstico:**  
  * *\#\#Análisis del consultor. Ej: La lógica de transformación está "hardcodeada" dentro de las herramientas de orquestación, lo que dificulta el testeo unitario. Se recomienda migrar la lógica SQL a un framework como dbt para gestionar versiones y documentación.\#\#*

    ### 3.2.5. Orquestación y automatización {#3.2.5.-orquestación-y-automatización}

En esta sección se realiza el análisis de la capa de control que orquesta, monitoriza y gestiona las dependencias entre tareas.

* **Herramientas de Orquestación:**  
  * *\#\#Listar servicios. Ej: Google Cloud Composer (Airflow), Workflows, Control-M, Jenkins, Cron jobs dispersos.\#\#*  
* **Gestión de Dependencias:**  
  * *\#\#Describir madurez. Ej: DAGs configurados en Airflow con gestión automática de reintentos (Retries) y sensores.\#\#*  
* **Observaciones y Diagnóstico:**  
  * *\#\#Análisis del consultor. Ej: Existe una fragmentación en la orquestación: algunos procesos corren en Control-M (Legacy) y otros en Composer (Cloud), sin visibilidad cruzada. Los fallos en los pipelines no generan alertas accionables, requiriendo revisión manual diaria.\#\#*

    ### 3.2.6. Modelado y Arquitectura de datos {#3.2.6.-modelado-y-arquitectura-de-datos}

En esta sección se presenta un estudio de la organización lógica de la información, metodologías de modelado y patrones de arquitectura de datos implementados.

* **Patrón de Arquitectura de Datos:**  
* **Estructura de Capas:** *\#\#Identificar si existe una separación lógica clara. Ej: Arquitectura Medallón (Bronce/Raw → Plata/Curated → Oro/Enriched).\#\#*

* **Enfoque de Almacenamiento:** *\#\#Ej: Data Lakehouse (ficheros estructurados con gobierno), Data Warehouse tradicional, Data Mesh (dominios descentralizados).\#\#*

* **Metodología de Modelado (Capa de Consumo):**  
  * **Esquema:** *\#\#Describir la técnica de modelado para la explotación. Ej: Modelo Dimensional Kimball (Esquema en Estrella con Hechos y Dimensiones), Modelo Inmon (3NF), Data Vault 2.0, o One Big Table (OBT) para rendimiento en BigQuery.\#\#*

* **Observaciones y Diagnóstico**:  
* *\#\#Análisis del consultor. Ej: Se observa una implementación teórica de arquitectura Medallón, pero en la práctica la capa 'Plata' se salta a menudo, conectando PowerBI directamente a datos crudos (Bronce), lo que genera problemas de rendimiento y lógica duplicada. El modelo dimensional está bien definido pero las Dimensiones no son conformadas (compartidas) entre diferentes áreas de negocio.\#\#*

  ### 3.2.7. Computing y Networks {#3.2.7.-computing-y-networks}

En esta sección se refleja el estado de la infraestructura de cómputo subyacente y configuración de red base que soporta la plataforma de datos.

* **Servicios de Cómputo:**  
  * *\#\#Listar servicios. Ej: GKE (Google Kubernetes Engine) para microservicios, Compute Engine (VMs) para cargas legacy, Dataproc (Hadoop/Spark gestionado).\#\#*  
* **Configuración de Red:**  
  * *\#\#Ej: Shared VPC (VPC Compartida), Interconnect dedicado con On-Premise, Cloud VPN, Cloud NAT para salida a internet controlada.\#\#*  
* **Observaciones y Diagnóstico:**  
  * *\#\#Análisis del consultor. Ej: El clúster de GKE está sobredimensionado para la carga de trabajo actual (muchos nodos ociosos). La red es segura (Private Google Access habilitado), pero las reglas de firewall en el proyecto de desarrollo son excesivamente permisivas (allow-all), lo que representa un riesgo de seguridad latente.\#\#*

    ### 3.2.8. Explotación de datos (BI & AI/ML) {#3.2.8.-explotación-de-datos-(bi-&-ai/ml)}

En esta sección se detallan las herramientas de consumo final, visualización y ciencia de datos utilizadas por los usuarios de negocio.

* **Herramientas de BI y Reporting:**  
  * *\#\#Ej: Looker (Enterprise BI), Power BI, Tableau, Excel, Looker Studio.\#\#*  
* **Capacidades de ML/AI:**  
  * *\#\#Ej: Vertex AI, Notebooks gestionados (Workbench), Modelos custom en VMs, APIs de visión/lenguaje (SaaS).\#\#*  
* **Observaciones y Diagnóstico:**  
  * *\#\#Análisis del consultor. Ej: Existe una proliferación de herramientas de BI (Shadow IT) donde cada departamento usa una licencia diferente, generando métricas inconsistentes. En cuanto a ML, los modelos no están productivizados (falta MLOps), ejecutándose manualmente desde los portátiles de los Data Scientists sin control de versiones.\#\#*

  ## 3.3. Análisis de flujos de datos {#3.3.-análisis-de-flujos-de-datos}

En este apartado se evalúa la dinámica de movimiento de la información a través de la plataforma. Se analiza la naturaleza de los flujos en relación a la frecuencia de actualización de los datos y su latencia así como la trazabilidad del dato desde su origen hasta su consumo final.

### 3.3.1. Patrones de ingesta y latencia {#3.3.1.-patrones-de-ingesta-y-latencia}

En esta sección se realiza el análisis de los mecanismos de entrada de datos y los tiempos de disponibilidad (SLA) actuales.

* **Tipología de Flujos**:  
  * *\#\#Describir la distribución. Ej: El 90% de los flujos son Batch (cargas masivas nocturnas). Existe un componente minoritario de Streaming para la telemetría de la App Móvil.\#\#*  
* **Frecuencia y Latencia:**  
  * *\#\#Describir la frescura del dato. Ej: Los datos financieros tienen una latencia de T+1 (disponibles al día siguiente a las 8:00 AM). Los datos operativos se actualizan cada 15 minutos (Micro-batch).\#\#*  
* **Observaciones:**  
  * *\#\#Diagnóstico sobre la idoneidad. Ej: La frecuencia diaria es insuficiente para el equipo de Marketing, que requiere datos intra-día para ajustar campañas. Los procesos Batch nocturnos a menudo exceden la ventana de mantenimiento, retrasando los reportes matutinos.\#\#*

    ### 3.3.2. Trazabilidad y ciclo de vida (end-to-end) {#3.3.2.-trazabilidad-y-ciclo-de-vida-(end-to-end)}

En esta sección se describe de forma técnica la secuencia de etapas y transformaciones que atraviesa la información a través de las distintas capas de la arquitectura.

* **Secuencia de procesamiento estándar**:

  * *\#\#Describir el pipeline estándar. Ej: Los datos se extraen vía JDBC y se depositan en GCS (Raw Zone). Posteriormente, se limpian con Dataflow y se cargan en BigQuery (Staging) y de ahí se transforman con SQL en Dataform y se exponen en Vistas Materializadas.\#\#*

* **Puntos de Ruptura y Complejidad:**

  * *\#\#Identificar dónde se pierde la traza o se complica el flujo. Ej: El flujo es transparente hasta llegar a BigQuery, pero luego se pierde la trazabilidad debido a cientos de 'Scheduled Queries' no documentadas que crean tablas temporales sin dueño claro (Spaghetti Data).\#\#*

* **Gestión de Dependencias y acoplamiento**:

  * *\#\#Ej: Existe un alto acoplamiento entre los sistemas origen y el DWH; si cambia una columna en el ERP, se rompen los pipelines de ingesta, ya que no existe un contrato de datos (Data Contract) ni validación de esquema en la entrada.\#\#*

# **4\. Gobierno, seguridad y operaciones** {#4.-gobierno,-seguridad-y-operaciones}

Mientras la sección anterior describe los componentes tecnológicos, esta sección analiza los cimientos operativos de la plataforma. Se evalúa la estructura organizativa en la nube, los controles de seguridad, la madurez en el gobierno del dato y las prácticas de ingeniería (DevOps).

## 4.1. Seguridad y Gestión de identidades (IAM) {#4.1.-seguridad-y-gestión-de-identidades-(iam)}

A continuación se exponen la gestión actual de accesos y roles. 

### 4.1.1. Análisis de roles y permisos {#4.1.1.-análisis-de-roles-y-permisos}

En esta sección se evalúa la granularidad y pertinencia de los permisos asignados.

* **Observaciones**  
* *\#\#Ej: La gestión de permisos se realiza a nivel de proyecto. Se observa un uso excesivo de roles básicos como 'Propietario' (Owner) y 'Editor' (Editor) en lugar de roles predefinidos más específicos, lo que aumenta la superficie de ataque.\#\#*

  ### 4.1.2. Gestión de credenciales {#4.1.2.-gestión-de-credenciales}

En esta sección se realiza el análisis del ciclo de vida de las claves de acceso.

* **Observaciones:**  
  * *\#\#Ej: Las aplicaciones utilizan correctamente Cuentas de Servicio (Service Accounts), pero las claves JSON se rotan manualmente y, en algunos casos, se han detectado credenciales 'hardcodeadas' en el código fuente, lo que supone un riesgo crítico de seguridad.\#\#*

  4.1.3. Principio de Mínimo Privilegio

En esta sección se realiza la verificación de si los usuarios tienen solo los permisos estrictamente necesarios para realizar las tareas que tienen asignadas.

* **Observaciones:**  
  * *\#\#Ej: El principio no se aplica de forma consistente. Los desarrolladores tienen permisos de Editor en entornos de Producción para depurar errores, cuando deberían tener solo acceso de lectura o visualización de logs.\#\#*

## 4.2. Organización de Recursos Cloud {#4.2.-organización-de-recursos-cloud}

En esta sección se realiza el análisis de la estructura jerárquica que sustenta el despliegue de servicios.

* **Jerarquía de Carpetas y Proyectos:**  
* *\#\#Ej: La estructura de carpetas y proyectos en la organización de GCP sigue las buenas prácticas, con una separación clara a nivel de proyecto para cada entorno (dev, staging, prod), lo que facilita la imputación de costes y el aislamiento.\#\#*

  ## 4.3. Gobierno y Calidad del Dato {#4.3.-gobierno-y-calidad-del-dato}

Esta sección analiza los pilares de la confianza en la información: el marco de políticas, roles y responsabilidades sobre cómo se gestiona, accede y protege la información.

### 4.3.1. Catálogo de Datos y Glosario {#4.3.1.-catálogo-de-datos-y-glosario}

* **Herramientas:** *\#\# (Si aplica) Ej. Dataplex, Data Catalog.\#\#*  
* **Madurez:**  
  * *\#\#Ej: (Si aplica) No existe una herramienta centralizada de catálogo de datos. La documentación sobre las tablas y métricas clave reside en documentos de Confluence desactualizados y dispersos. Esto genera desconfianza en los reportes finales.\#\#*

    ### 4.3.2. Linaje del dato {#4.3.2.-linaje-del-dato}

* **Trazabilidad:**  
* *\#\#Ej: (Si aplica) No hay capacidades de linaje de datos automatizadas. Actualmente es imposible trazar el origen de una métrica en un informe de BI hasta su fuente original sin realizar una ingeniería inversa manual del código SQL.\#\#*

  ### 4.3.3. Calidad y perfilado del dato {#4.3.3.-calidad-y-perfilado-del-dato}

* **Procesos de Calidad:**  
* *\#\#Ej: (Si aplica) Existen algunos tests de calidad (dbt tests) en el pipeline de BigQuery para verificar nulos y unicidad, pero no hay un proceso formal de monitorización ni alertas (Data Observability) cuando la calidad de los datos se degrada silenciosamente.\#\#*

* **Procesos de perfilado del dato:**  
* *\#\#Ej: (Si aplica) Existen algunos jobs de perfilado del dato para la determinación de estadísticos (longitud de cadenas de texto, frecuencia de los valores,...)\#\#*

  ### 4.3.4. Seguridad del Dato (fine-grained access) {#4.3.4.-seguridad-del-dato-(fine-grained-access)}

En esta sección se detalla el uso de políticas de acceso granular para datos sensibles (PII).

* **Políticas aplicadas:**

  * **RLS (row-level security):** *\#\#Describir las policies que se usan a nivel de BigQuery a qué tablas aplica, qué filtros se usa y qué grupos tienen acceso a cada segregación de datos\#\#*

  * **CLS (column-level security):** *\#\#Ej: Detallar si existen [policy tags](https://docs.cloud.google.com/bigquery/docs/column-level-security-intro) definidas en BigQuery, a qué columnas aplican, si están activas y si existen reglas o roles de IAM definidos sobre ellas de enmascaramiento  columnas con datos sensibles (fine-grained reader role).\#\#*

## 4.4. Fundamentos de ingeniería y DevOps {#4.4.-fundamentos-de-ingeniería-y-devops}

En el siguiente apartado se explican los fundamentos de ingeniería que sustentan la metodología DevOps y su aplicación en el ciclo de vida del desarrollo de software.

### 4.4.1. Organización del Código (Git)  {#4.4.1.-organización-del-código-(git)}

* **Estructura de Repositorios**:  
  * *\#\#Ej: El código está centralizado en repositorios de GitLab. Sin embargo, múltiples proyectos de Dataflow conviven en un único 'monorepo' gigante sin una estructura modular clara, lo que complica la gestión de dependencias y versiones.\#\#*

### 4.4.2. Ciclo de Vida y Despliegue {#4.4.2.-ciclo-de-vida-y-despliegue}

* **Madurez de Automatización:**  
* *\#\#Ej: Se utiliza un [flujo](https://blog.damavis.com/branching-en-git-github-flow-gitflow-y-trunk-based-development/) de GitFlow/GitHub flow/Trunk-based (si aplica). Existe un pipeline de CI/CD con GitLab CI/GitHub actions/Azure DevOps/Cloud Build que despliega automáticamente a los entornos de dev y staging, pero el despliegue a producción sigue siendo un proceso manual propenso a errores humanos. Describir si existen triggers o automatizaciones en el pipeline de CI/CD.\#\#*

### 4.4.3. Infraestructura como Código (IaC)  {#4.4.3.-infraestructura-como-código-(iac)}

* **Gestión y aprovisionamiento:**  
  * *\#\#Ej: Actualmente la creación de recursos (Buckets S3, instancias EC2/VMs, Datasets de BigQuery) se realiza manualmente a través de la consola del proveedor cloud ("ClickOps"). No existe un repositorio de Terraform o CloudFormation que defina el estado deseado, lo que ha provocado configuraciones dispares entre los entornos de Desarrollo y Producción (Configuration Drift).\#\#*

  * *\#\#Ej: Se utiliza Terraform para el despliegue de recursos base, pero el estado se almacena en local en los equipos de los desarrolladores en lugar de en un backend remoto con bloqueo (e.g., S3 \+ DynamoDB / Azure Storage), lo que genera riesgos de corrupción y dificulta el trabajo colaborativo.\#\#*

### 4.4.4. Estándares y Buenas Prácticas {#4.4.4.-estándares-y-buenas-prácticas}

* **Convenciones:**  
  * *\#\#Ej: Se ha detectado inconsistencia en el nombrado de tablas. La referencia recomendada para futuras nomenclaturas será: \[Link a glosario de nomenclatura/guía de estilo\].\#\#*

## 4.5. Monitorización y Alertas {#4.5.-monitorización-y-alertas}

Esta sección analiza los sistemas de monitorización y alertas, componentes clave  para la capacidad de respuesta ante incidentes y control operativo.

### 4.5.1. Observabilidad técnica {#4.5.1.-observabilidad-técnica}

* **Herramientas y Dashboards:**  
  * *\#\#Ej: Se utiliza Cloud Monitoring. Existen dashboards básicos de uso de CPU, pero faltan paneles de negocio que indiquen si los datos se han cargado a tiempo.\#\#*

### 4.5.2. Alertas y protocolos {#4.5.2.-alertas-y-protocolos}

* **Alertas de Facturación**:  
  * *\#\#Ej: Describir si existen alertas de presupuesto configuradas, cuáles son los budgets que disparan las alertas, quién recibe y por qué canal dichas alertas, y cuál es el protocolo de actuación ante la detección de un pico de gasto inesperado.\#\#*

* **Protocolo de Respuesta**:  
  * *\#\#Ej: Las alertas se envían a un canal de Slack/Teams/Mail general que nadie revisa (fatiga de alertas). No existe una rotación de guardias (on-call) formalizada ni una cadena de escalado definida para incidentes críticos fuera de horario.\#\#*

### 

# **5\. Análisis de costes y Eficiencia** {#5.-análisis-de-costes-y-eficiencia}

En esta sección se desglosa el análisis de costes de la plataforma actual, basado en la auditoría realizada sobre los servicios principales (*\#\#indicar servicios analizados \- eg. BigQuery, Cloud Run,...\#\#*).

*\#\#**Nota para los técnicos (eliminar)**: Las consultas SQL base utilizadas para este análisis están disponibles en [link](https://docs.google.com/document/d/190LwFhvh15R_3TtvZBDLxZY2Um-nfKY1gyJPHBnmAtA/edit?usp=drive_link)\#\#*

## 5.1. Orígenes del Gasto {#5.1.-orígenes-del-gasto}

Para investigar los generadores de coste, se ha analizado el historial de trabajos (jobs) a través de las vistas de metadatos (**INFORMATION\_SCHEMA.JOBS\_BY\_PROJECT**).

Esta tabla contiene información detallada sobre todos los jobs ejecutados en BigQuery incluyendo las queries, con los bytes que ha tenido que leer y quienes han sido los autores de estas queries.

*\#\#Reemplazar la siguiente imagen por una real del cliente auditado mostrando la distribución de costes por usuario y service account. En este ejemplo se ocultan datos sensibles de otro cliente: En el caso real, mostrar cuentas de email afectadas o anonimizadas si es necesario.\#\#*

![][image1]

Se identifican \#\#especificar usuarios clave que generan mayor sobrecoste\#\#:

* **\#\#Usuario 1\#\#:** \#\#Indicar el origen de las consultas y su objetivo\#\#.  
* **\#\#Usuario 2\#\#:** \#\#Indicar el origen de las consultas y su objetivo\#\#.  
* …

## 5.2. Oportunidades de optimización {#5.2.-oportunidades-de-optimización}

A continuación se detallan las ineficiencias detectadas y el potencial del ahorro.

### 5.2.1. Análisis de Queries Costosas {#5.2.1.-análisis-de-queries-costosas}

*\#\#**Nota para los técnicos (eliminar)**: Enlace a query para análisis: [\[DATA ACC\] Análisis Bigquery v1.0.0](https://docs.google.com/document/u/0/d/190LwFhvh15R_3TtvZBDLxZY2Um-nfKY1gyJPHBnmAtA/edit)\#\#*

Se ha detectado que el *\#\#X%\#\#* del coste de cómputo se concentra en un número reducido de consultas recurrentes.

* **Actividades más pesadas**:  
  * *\#\#Proceso 1: Descripción del proceso y el dataset afectado\#\#.*  
  * *\#\#Proceso 2: Descripción del proceso y el dataset afectado\#\#.*  
  * *\#\#...\#\#*

* **Diagnóstico y Recomendación:**  
  * *\#\#Ej: Analizando las consultas anteriores, se observa que (insertar casuística  por la que se está produciendo mayor gasto). Se podría optimizar el consumo de estas consultas, (detallar cómo se podría mejorar el rendimiento y gastos) (e.g. usando particiones, clustering, limitando el scope de las queries, eliminando columnas redundantes de la consulta, usando incrementales, refrescando tabla de manera incremental,...)\#\#*.

  ### 5.2.2. Análisis de uso de slots {#5.2.2.-análisis-de-uso-de-slots}

Se ha analizado el consumo de slots en las regiones activas para determinar si el modelo de precios actual (Bajo demanda vs. Editions/Reservas) es el óptimo.

*\#\#**Nota para los técnicos (eliminar)**: Enlace a query para análisis: [\[DATA ACC\] Análisis Bigquery v1.0.0](https://docs.google.com/document/u/0/d/190LwFhvh15R_3TtvZBDLxZY2Um-nfKY1gyJPHBnmAtA/edit)\#\#*

*\#\#Cliente\#\#* está ejecutando jobs en *\#\#introducir regiones donde se encuentren jobs\#\#* y por tanto se analizó cada región por separado para conocer si es más económico reservar capacidad en BigQuery o usar un modelo bajo demanda.

*\#Modificar tabla acorde a los resultados del Cliente\#\#*

| Región | Bytes procesados últimos 30 días | Uso medio de slots últimos 30 días |
| :---- | :---- | :---- |
| US | 3745 Tebibyte | 337 |
| EU | 6396 Tebibyte | 567 |
| europe-west2 | 58 Tebibyte | 31 |
| us-east5 | 2 Tebibyte | 0.02 |
| El resto de regiones tiene un uso muy bajo y se han descartado para el análisis. |  |  |

A partir de la tabla anterior podemos hacer un cálculo teórico comparando el coste actual (on-demand) frente a una tarifa plata (Edition Enterprise) basada en el uso medio.

*\#Modificar tabla acorde a los resultados del Cliente\#*

| Región | Coste mensual bajo demanda | Coste teórico usando reserva de capacidad (edición enterprise) | Potencial de impactar positivamente en el billing |
| :---- | :---- | :---- | :---- |
| US | € 21113 | € 16014 | Bajo |
| EU | € 77281 | € 26943 | Alto |
| europe-west2 | € 401 | € 1473 | Muy Bajo |
| us-east5 | € 5.5 | € 0.95 | Muy Bajo |

***Nota**: La fórmula usada para calcular el coste es uso\_medio\_slots x 30 x 24 x 0.066€*

* **Conclusiones:**  
  * *\#\#Ej: Siempre que la latencia y la residencia del dato lo permitan, se recomienda consolidar las cargas de trabajo en la región EU para aprovechar las economías de escala y contratar una reserva de capacidad (Edition), lo que reduciría la factura en aprox. un 60%.*

  * Siempre que no existan otros impedimentos, se recomienda localizar los jobs en las multiregiones de EEUU o de EU, dado que son las más baratas tanto por byte escaneado como almacenado.\#\#

### 5.2.3. Análisis de almacenamiento (lógico vs físico) {#5.2.3.-análisis-de-almacenamiento-(lógico-vs-físico)}

*\#\#**Nota para los técnicos (eliminar)**: Enlace a query para análisis: [\[DATA ACC\] Análisis Bigquery v1.0.0](https://docs.google.com/document/u/0/d/190LwFhvh15R_3TtvZBDLxZY2Um-nfKY1gyJPHBnmAtA/edit)\#\#*

En BigQuery, el modelo de facturación de almacenamiento físico (basado en bytes comprimidos) suele ser más económico que el lógico (bytes sin comprimir) para datos con alta cardinalidad o texto. El modelo lógico suele ser el estándar por defecto y en el caso de *\#\#Cliente\#\#* usa almacenamiento *\#\#físico / lógico\#\#*.

*\#Modificar tabla acorde a los resultados del Cliente\#*

| Región | Coste actual con almacenamiento lógico (€/mes) | Coste calculado aplicando almacenamiento físico (€/mes) | Potencial ahorro calculado si se aplica almacenamiento físico (€/mes) |
| :---- | :---- | :---- | :---- |
| US | € 13413 | € 6839 | € 6573 |
| EU | € 14213 | € 4669 | € 9544 |

La elección del tipo de almacenamiento puede hacerse a nivel de dataset, por lo que si aplicamos el almacenamiento físico sólo en aquellos datasets donde el beneficio sea superior a 10€ mensuales el potencial ahorro sería el siguiente:

*\#Modificar tabla acorde a los resultados del Cliente\#*

| Región | Coste actual con almacenamiento lógico (€/mes) | Coste calculado aplicando almacenamiento físico (€/mes) | Potencial ahorro calculado si se aplica almacenamiento físico (€/mes) |
| :---- | :---- | :---- | :---- |
| US | € 13413 | € 6839 | € 6573 |
| EU | € 14213 | € 4669 | € 9544 |

# **6\. Hallazgos principales y recomendaciones** {#6.-hallazgos-principales-y-recomendaciones}

A continuación se resumen las principales fortalezas y deficiencias detectadas en la arquitectura actual así como aquellas oportunidades clave de optimización.  El objetivo es proporcionar una visión de alto nivel sobre la madurez del ecosistema de datos actual.

## 6.1. Resumen de fortalezas de la arquitectura actual {#6.1.-resumen-de-fortalezas-de-la-arquitectura-actual}

*\#\#Enumerar aquellos puntos relevantes en bulletpoints y de la forma más ejecutiva posible (sintetizado)*

* ***Centralización del Dato:** Existencia de un repositorio único de verdad (Data Lake / Data Warehouse) que reduce la dispersión de la información crítica.*  
* ***Segregación de Cargas:** Separación efectiva entre cargas de trabajo transaccionales y analíticas, evitando impactos en el rendimiento de los sistemas operacionales*  
* *… \#\#*

## 6.2. Identificación de puntos de dolor {#6.2.-identificación-de-puntos-de-dolor}

*\#\#Hacerlo en bulletpoints y lo más ejecutivo posible\#\#*

* **Técnicos**:  
  * *\#\#**Calidad del dato**: Ausencia de validaciones automáticas en la ingesta, provocando duplicidad, nulos o formatos inconsistentes en capas finales\#\#*  
  * *\#\#**Latencia de procesamiento**: Tiempos de ejecución de pipelines ETL excesivos que retrasan la disponibilidad de los datos para la toma de decisiones diaria (SLA de datos no cumplido).\#\#*  
* **Operativos**:  
  * *\#\#**Gestión de Incidencias:** Falta de trazabilidad (Lineage) y alertas proactivas; el equipo de datos se entera de los errores cuando negocio reclama el dato\#\#*  
  * *\#\#**Procesos Manuales:** Necesidad de relanzar procesos manualmente o corregir datos "a mano" frecuentemente.\#\#*  
* **Seguridad**:  
  * *\#\#**Control de Accesos (RBAC):** Permisos de acceso a datos demasiado amplios; falta de granularidad a nivel de fila/columna para datos sensibles\#\#*  
  * *\#\#**Protección de Datos (PII):** Datos de Información Personal (PII) expuestos en entornos de desarrollo o sin ofuscar/encriptar en reposo.\#\#*  
* **Coste**:  
  * *\#\#**Ineficiencia en Consultas:** Consultas analíticas no optimizadas (escaneos completos de tablas, joins cartesianos) que disparan el consumo de cómputo.\#\#*  
  * *\#\#**Almacenamiento de Datos Fríos:** Retención indefinida de históricos de datos sin acceso frecuente en capas de almacenamiento de alto coste.\#\#*  
  * ***\#\#Recursos no optimizados:** Clusters de procesamiento encendidos 24/7 para cargas de trabajo que son por lotes (batch) y puntuales.\#\#*

## 6.3. Recomendaciones y puntos de mejora {#6.3.-recomendaciones-y-puntos-de-mejora}

A continuación,  presentamos un análisis orientado a la eficiencia del ciclo de vida del dato. El objetivo es proponer acciones de redimensionamiento, refactorización de código y mejora en la gobernanza.

*\#\#Indicación de recursos que podrían mejorarse, están obsoletos, podrían mejorarse, recomendaciones de uso de herramientas…*

*Ejemplo:*

* ***Optimización de Procesamiento y Almacenamiento***  
  * *Estrategias de Particionado: Reestructurar grandes tablas factos utilizando claves de partición \[e.g., Fecha, Región\] para reducir el volumen de datos escaneados y el coste de las consultas.*  
  * *Formatos de Archivo Optimizados: Migrar almacenamiento de datos crudos (CSV/JSON) a formatos columnares y comprimidos (Parquet/Avro/Delta) para mejorar rendimiento de lectura y reducir espacio.*  
  * *Ciclo de Vida del Dato: Implementar políticas de archivado automático para mover datos con antigüedad mayor a \[X años\] a capas de almacenamiento "frío" (Archive tier).*

* ***Modernización y Calidad***  
  * *Implementación de Data Quality Gates: Integrar librerías de calidad \[e.g., Great Expectations, dbt tests\] que frenen pipelines defectuosos antes de ensuciar el Data Warehouse.*  
  * *Orquestación Avanzada: Migrar de \[Herramienta actual/Cron\] a orquestadores modernos \[e.g., Airflow, Prefect, Dagster\] para gestionar dependencias y reintentos automáticos.*  
  * *Separación Cómputo/Almacenamiento: Desacoplar estos recursos para permitir escalar la potencia de cálculo sin necesidad de migrar datos ni pagar almacenamiento extra.*

* ***Gobierno y Herramientas***  
  * *Catálogo de Datos: Desplegar una herramienta de catálogo \[e.g., DataHub, Glue Catalog\] para documentar definiciones de negocio y facilitar el autoservicio.*  
  * *FinOps para Datos: Etiquetar recursos por proyecto/caso de uso para identificar las consultas o modelos más costosos y optimizarlos.*  
  * *Enmascaramiento Dinámico: Implementar políticas de seguridad que ofusquen datos sensibles en tiempo real según el rol del usuario que consulta.*

*\#\#*

## 

| About Devoteam  Devoteam is a tech consulting firm specialised in cloud, cybersecurity, data, and sustainability. Tech Native for over 25 years, Devoteam guides businesses through sustainable digital transformation to unlock their full potential. With over 10,000 employees in more than 25 countries across Europe, the Middle East, and Africa, Devoteam is committed to putting technology at the service of people. To realise this vision, we partner with the top cloud platforms in the world, Microsoft Azure, Google Cloud, and AWS. |
| :---- |

[image1]: <data:image/png;base64,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>