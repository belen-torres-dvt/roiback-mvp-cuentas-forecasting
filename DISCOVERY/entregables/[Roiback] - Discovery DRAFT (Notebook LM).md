#### OBTENIDO CON NOTEBOOK LM

##Roiback## - ##MVP Cuentas y forecasting##
Discovery
Hoja de control Control de documentación |  |  | | ------ | ------ | | Document Code | Roiback- MVP Cuentas y forecasting - Entregable Discovery | | Preparado por: | Data Accelerator / Devoteam | | Fecha | 30/04/2026 |
Control de versiones | Versión | Autor | Fecha | Comentarios | | ------ | ------ | ------ | ------ | | v1.0 | Data Accelerator | 30/04/2026 | Versión funcional entregable Discovery |
Control de revisión y aprobación |  | Nombre | Fecha | Firma | | ------ | ------ | ------ | ------ | | Revisado por |  |  |  | | Aprobado por |  |  |  |
Índice
1. Introducción y contexto 1.1. Propósito del documento 1.2 Contexto de Negocio 1.3 Metodología y stakeholders involucrados 2. Definición de objetivos y requisitos 2.1 Objetivos Estratégicos de Negocio 2.2. Casos de uso prioritarios 2.3. Requisitos del Sistema 2.3.1. Requisitos funcionales 2.3.2. Requisitos técnicos (no funcionales) 3. Análisis de la arquitectura y plataforma actual (AS-IS) 3.1. Visión general de la arquitectura 3.2. Stack tecnológico 3.2.1. Fuentes de datos 3.2.2. Almacenamiento de datos 3.2.3. Ingesta de datos 3.2.4. Procesamiento y transformación 3.2.5. Orquestación y automatización 3.2.6. Modelado y Arquitectura de datos 3.2.7. Computing y Networks 3.2.8. Explotación de datos (BI & AI/ML) 3.3. Análisis de flujos de datos 3.3.1. Patrones de ingesta y latencia 3.3.2. Trazabilidad y ciclo de vida (end-to-end) 4. Gobierno, seguridad y operaciones 4.1. Seguridad y Gestión de identidades (IAM) 4.1.1. Análisis de roles y permisos 4.1.2. Gestión de credenciales 4.2. Organización de Recursos Cloud 4.3. Gobierno y Calidad del Dato 4.3.1. Catálogo de Datos y Glosario 4.3.2. Linaje del dato 4.3.3. Calidad y perfilado del dato 4.3.4. Seguridad del Dato (fine-grained access) 4.4. Fundamentos de ingeniería y DevOps 4.4.1. Organización del Código (Git) 4.4.2. Ciclo de Vida y Despliegue 4.4.3. Infraestructura como Código (IaC) 4.4.4. Estándares y Buenas Prácticas 4.5. Monitorización y Alertas 4.5.1. Observabilidad técnica 4.5.2. Alertas y protocolos 5. Análisis de costes y Eficiencia 5.1. Orígenes del Gasto 5.2. Oportunidades de optimización 5.2.1. Análisis de Queries Costosas 5.2.2. Análisis de uso de slots 5.2.3. Análisis de almacenamiento (lógico vs físico) 6. Hallazgos principales y recomendaciones 6.1. Resumen de fortalezas de la arquitectura actual 6.2. Identificación de puntos de dolor 6.3. Recomendaciones y puntos de mejora

--------------------------------------------------------------------------------
1. Introducción y contexto
1.1. Propósito del documento
El objetivo de este documento es formalizar y consolidar los hallazgos obtenidos durante la fase de Discovery del proyecto MVP Cuentas y forecasting. Su finalidad es presentar un análisis integral del estado actual (AS IS) de la infraestructura de datos, la arquitectura y procesos operativos de Roiback que permita anticipar desafíos técnicos y eliminar suposiciones.
1.2 Contexto de Negocio
Roiback es una empresa enfocada en soluciones para la venta directa de cadenas hoteleras y hoteles independientes
. Su principal objetivo de negocio es hacer crecer el canal directo del usuario (vía web oficial y motor de reservas), reduciendo así la fuerte dependencia en intermediarios como Booking.com o Expedia
. Gestionan los sistemas de aproximadamente 600 cuentas y 2200 hoteles activos
.
A nivel operativo, el equipo de analistas de cuentas de Roiback (DCS - Direct Channel Specialists) tiene el desafío de gestionar el rendimiento de ventas
. El problema principal radica en que el proceso de análisis, diagnóstico de anomalías y supervisión de ventas está muy poco estandarizado, es altamente tedioso, manual y subjetivo, y la información se encuentra muy dispersa entre distintas herramientas
. Además, el modelo actual es muy reactivo: las anomalías se detectan revisando métricas pasadas cuando las ventas ya han caído
.
1.3 Metodología y stakeholders involucrados
1.3.1 Sesiones de Trabajo | Fecha | Objetivo de la sesión | Asistentes | Referencia | | ------ | ------ | ------ | ------ | | 28/04/2026 | Discovery Inicial - Modelos, métricas y negocio | Devoteam y Roiback | [Roiback] - MVP - Discovery – 2026_04_28 | | 29/04/2026 | Discovery 2 - Casos de uso y arquitectura fuente | Devoteam y Roiback | [Roiback] - MVP - Discovery 2 – 2026_04_29 | | 30/04/2026 | Semanal - Cuentas y forecasting | Devoteam y Roiback | Roiback - MVP Cuentas y forecasting - Semanal |
1.3.2 Stakeholders involucrados | Empresa | Nombre | Rol / Cargo | | ------ | ------ | ------ | | Devoteam | Urbano Llamas | Equipo Proyecto | | Devoteam | Belén Torres | Data Engineer | | Devoteam | Daniel Acosta | Equipo Proyecto | | Devoteam | Juan Ezquerro | DevOps/Infra | | Devoteam | Jose Ortuño | Equipo Proyecto | | Roiback | Ana Martín | Equipo Proyecto | | Roiback | Otelo Pons | Technical Lead/Data | | Roiback | Irene Soler | DCS (Direct Channel Specialist) |
2. Definición de objetivos y requisitos
2.1 Objetivos Estratégicos de Negocio
Optimización Operativa: Reducir el esfuerzo manual y el tiempo invertido en los análisis diarios de rendimiento, haciéndolos mucho más eficientes
.
Estandarización y Gobierno del Dato: Definir un modelo de indicadores y métricas comunes para que toda la organización hable el mismo idioma y tenga una interpretación clara y compartida
.
Gestión Proactiva: Modificar el flujo de trabajo hacia un modelo proactivo y anticipativo, donde los fallos se detecten mediante alertas tempranas en lugar de análisis reactivos
.
Escalabilidad: Poder realizar este análisis de forma escalable sobre las más de 600 cuentas y 2200 propiedades, detectando problemas incluso a nivel específico de un único hotel dentro de una cadena
.
2.2. Casos de uso prioritarios
ID
Caso de uso
Descripción breve
Consumidor
Prioridad
UC-01
Sistema de Alertas Tempranas
Recepción de notificaciones proactivas (ej. vía Slack) en caso de caídas anómalas de ventas, con enlaces para completar la información
.
DCS (Account Managers)
Alta
UC-02
Dashboard Integral de Reunión
Panel unificado para presentar el análisis de un cliente integrando alertas históricas y un resumen automático de IA sobre tráfico, ventas, año anterior y presupuestos
.
DCS (Account Managers)
Alta
UC-03
Analítica Conversacional
Uso de un agente conversacional para que el equipo de marketing recupere agrupaciones de datos limpios y tendencias rápidamente (ej. top de extras más vendidos)
.
Data / Marketing
Media
2.3. Requisitos del Sistema
2.3.1. Requisitos funcionales
Diccionario de Datos Estandarizado: Generación de un marco común para asegurar que todos utilizan fórmulas idénticas al analizar el negocio (por ejemplo, definir claramente cómo se debe calcular el "porcentaje de cancelación")
.
Centralización del Diagnóstico: Capacidad para unificar métricas provenientes de la ventana de reservas (Booking Window), la ventana de estancias futuras (Travel Window), tráfico web, conversión, disponibilidad, paridad de precios y cancelaciones en un único entorno de análisis
.
Comparativas Dinámicas Consolidadas: Posibilidad de visualizar métricas como TTV o Roomnights comparando tramos dinámicos de tiempo de forma simultánea (ej. últimos 7 días vs últimas 4 semanas vs mismo periodo exacto del año anterior)
.
Modelado de Agrupaciones (Clustering): Capacidad del sistema para generar automáticamente clusters o segmentos de propiedades "similares" que faciliten la comparativa de mercado basándose en estacionalidad, destino u otros criterios algorítmicos
.
2.3.2. Requisitos técnicos (no funcionales)
Motor de Anomalías Machine Learning: Despliegue de un algoritmo predictivo (ej. uso de modelos ARIMA) ajustado a las particularidades, vacaciones de origen/destino y picos naturales de cada hotel individual, ya que las caídas porcentuales no impactan igual a cadenas diferentes
.
Plataforma de Gobernanza: Empleo de una herramienta técnica de metadatos y glosarios (como Google Dataplex) para mantener centralizado el diccionario semántico para los departamentos
.
Infraestructura DWH Moderna: Estructuración y modelado dentro de Google BigQuery garantizando los entornos unificados requeridos para servir herramientas visuales sin que exista "Shadow IT" local
.
3. Análisis de la arquitectura y plataforma actual (AS-IS)
3.1. Visión general de la arquitectura
Se observa una arquitectura donde existe almacenamiento consolidado, pero el acceso de negocio se encuentra tremendamente fragmentado. Los datos principales residen en BigQuery, pero no hay un gobierno central para la ingesta del usuario. Los DCS analizan métricas saltando entre la exportación manual a Excel, un portal BI propio desarrollado por Roiback, herramientas de QlikSense y docenas de cuadros de mando aislados en Data Studio construidos por usuarios sin directrices comunes
.
3.2. Stack tecnológico
3.2.1. Fuentes de datos
Motor de Reservas (Producción Interna): Sistemas propios de Roiback desde donde se recuperan todas las reservas, transacciones e información de cancelaciones
.
Google Analytics 4 (GA4): Analítica digital para estudiar tanto el tráfico global de la web como las búsquedas internas y disponibilidad dentro del motor de reservas
.
Fuentes Externas de Paridad: Integraciones y cruces manuales con plataformas externas como The Hotels Network (THN) y Google Hotels (GHA) para supervisar la disparidad de precios contra competidores u OTAs
.
CRM: Salesforce utilizado como base de datos interna para guardar metadatos de los hoteles y las cuentas (no del cliente final)
.
3.2.2. Almacenamiento de datos
Google BigQuery: El dato principal reside en BigQuery. Las interacciones transaccionales se encuentran alojadas en una única tabla de reservas consolidadas que agrupa toda la información de la reserva, mientras que los eventos de GA4 se agrupan en tablas agregadas
.
3.2.3. Ingesta de datos
La integración con Google Analytics se produce mediante las transferencias nativas (BigQuery Data Transfer / Exportación automática) hacia GCP, introduciendo tablas de eventos base divididas por cuenta y día
.
3.2.4. Procesamiento y transformación
No aplica.
3.2.5. Orquestación y automatización
No aplica.
3.2.6. Modelado y Arquitectura de datos
No aplica.
3.2.7. Computing y Networks
No aplica.
3.2.8. Explotación de datos (BI & AI/ML)
QlikSense: Para uso interno avanzado y creación automatizada de informes en PDF o PPT
.
Looker Studio (Data Studio): Numerosos paneles auto-gestionados por distintos usuarios y departamentos
.
Portal BI propietario: Solución ad-hoc para que los clientes finales auditen sus hoteles
.
3.3. Análisis de flujos de datos
3.3.1. Patrones de ingesta y latencia
Los datos de eventos web se envían en exportaciones base estructuradas de forma diaria por Google mediante exportación por día y cuenta, procesándose miles de ellas para generar una tabla consolidada
.
3.3.2. Trazabilidad y ciclo de vida (end-to-end)
No aplica.
4. Gobierno, seguridad y operaciones
4.1. Seguridad y Gestión de identidades (IAM)
4.1.1. Análisis de roles y permisos
No aplica.
4.1.2. Gestión de credenciales
No aplica.
4.2. Organización de Recursos Cloud
No aplica.
4.3. Gobierno y Calidad del Dato
Actualmente existe una grave deficiencia en la capa de gobernanza y calidad. Diferentes usuarios calculan y definen métricas críticas a su manera.
4.3.1. Catálogo de Datos y Glosario
Herramientas: Ninguna desplegada actualmente. Se planea evaluar la implantación de Dataplex.
Madurez: Muy baja. No hay acuerdo común en definiciones elementales como el "porcentaje de cancelación" entre el equipo de ventas, analítica y finanzas. Esto genera frustración y desajustes numéricos en reportes internos y ante los clientes
.
4.3.2. Linaje del dato
No aplica.
4.3.3. Calidad y perfilado del dato
No aplica.
4.3.4. Seguridad del Dato (fine-grained access)
No aplica.
4.4. Fundamentos de ingeniería y DevOps
4.4.1. Organización del Código (Git)
Se ha validado la utilización futura de repositorios mediante GitLab para la gestión y versionado de todo el trabajo analítico de la nueva solución
.
4.4.2. Ciclo de Vida y Despliegue
No aplica.
4.4.3. Infraestructura como Código (IaC)
No aplica.
4.4.4. Estándares y Buenas Prácticas
No aplica.
4.5. Monitorización y Alertas
4.5.1. Observabilidad técnica
No aplica.
4.5.2. Alertas y protocolos
El proceso de diagnóstico actual se fundamenta en un flujo puramente visual, subjetivo y a posteriori
. No existen reglas automatizadas que avisen de irregularidades severas o picos inesperados
. Todo el trabajo depende del rastreo manual de cada cuenta hotelera.
5. Análisis de costes y Eficiencia
5.1. Orígenes del Gasto
No aplica.
5.2. Oportunidades de optimización
5.2.1. Análisis de Queries Costosas
No aplica.
5.2.2. Análisis de uso de slots
No aplica.
5.2.3. Análisis de almacenamiento (lógico vs físico)
No aplica.
6. Hallazgos principales y recomendaciones
6.1. Resumen de fortalezas de la arquitectura actual
Materia Prima Disponible en GCP: Ya se ha consolidado exitosamente el repositorio analítico central (BigQuery), teniendo trazabilidad en crudo tanto sobre los eventos digitales de usuario con GA4 como en los flujos completos de reservas de hoteles (Booking vs Cancelaciones)
.
Nivel de Conocimiento del Negocio Profundo: El equipo ha logrado documentar de manera extensiva una matriz de diagnóstico de 11 pasos sumamente rica (Booking Window, Travel Window, Paridad, Demanda, Campañas, etc.) que fundamenta de manera perfecta el modelo futuro
.
6.2. Identificación de puntos de dolor
Operativos (Procesos Reactivos y Subjetivos): El diagnóstico actual recae exclusivamente en personal intentando navegar por plataformas inconexas
. Los problemas de ventas se abordan después de que se solidifiquen métricas malas porque no hay notificaciones de tiempo real
.
Gobierno de Datos (Ausencia de Estandarización): Dependencia de una capa semántica inexistente. Los analistas (Shadow IT) desarrollan sus propios Data Studios lo que lleva a resultados incongruentes en métricas tan vitales como la producción y cancelación de cuentas, rompiendo la confianza de la métrica
.
Escalabilidad: Al gestionar el canal directo para cientos de cadenas y más de 2000 propiedades
, el análisis manual es imposible de escalar en profundidad sin dejar de dar soporte óptimo a hoteles secundarios
.
6.3. Recomendaciones y puntos de mejora
Implementación Inmediata de Gobernanza y Capa Semántica: Centralizar el modelado de datos y desplegar la suite de Dataplex como solución única y dorada (Golden Record) para definiciones como tasas de cancelación o TTV. Los reportes, tanto en Looker como Qlik, deberán beber exclusivamente de este modelo y lenguaje unificado
.
Despliegue de Analítica Predictiva para Alertas: Implementar procesos basados en Machine Learning que asimilen la variabilidad estacional y de mercado de cada cadena hotelera individualmente para gatillar alertas proactivas ante la desviación inminente, reduciendo tiempos de acción de días a horas
.
Automatización del Framework de 11 Pasos: Reemplazar el análisis visual transversal de los Account Managers construyendo dashboards centralizados que vinculen de forma nativa la paridad (GHA/THN), la búsqueda en web (GA4) y las reservas on the books (Sistema Propio) reduciendo enormemente la carga operativa del área de cuentas