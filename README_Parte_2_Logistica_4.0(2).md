# Orquestación de IA y Asistentes Virtuales en Logística 4.0

## 📋 Descripción del Proyecto -- Parte 2

Evolución del proyecto de automatización logística enfocado en
desarrollar una Intelligent Supply Chain Control Tower, integrando
información de transitarias *inbound* y navieras para mejorar la
visibilidad, el seguimiento de embarques y el análisis del rendimiento
de proveedores.

Esta segunda fase incorpora procesos de analítica operacional mediante
**n8n, JavaScript y PostgreSQL**, transformando los datos logísticos
consolidados en indicadores para el control de rutas, carriers y
operaciones semanales.

## ⚙️ Arquitectura del Flujo de Automatización (Workflow)

El sistema implementa dos workflows complementarios para el
procesamiento y análisis de información logística:

### Integración de Datos -- Carrier Performance Analytics

-   **Trigger Programado (*Schedule Trigger*):** Ejecución automática de
    la sincronización de información.
-   **Extracción de Datos (*Google Sheets*):** Lectura de registros
    procedentes de diferentes operadores logísticos.
-   **Unificación (*Merge*):** Consolidación de las fuentes de
    información de los carriers.
-   **Depuración (*Filter*):** Filtrado de registros para evitar
    información no válida.
-   **Procesamiento (*Code in JavaScript*):** Normalización y
    transformación de los datos logísticos.
-   **Registro (*PostgreSQL*):** Almacenamiento centralizado de los
    embarques.
-   **Evaluación de Proveedores (*Carrier Performance*):** Generación de
    indicadores de rendimiento por operador.

### 2. Dashboard Semanal -- Intelligent Control Tower

-   **Extracción de Embarques (*PostgreSQL*):** Consulta centralizada de
    los registros logísticos.
-   **Análisis de Volumen (*QTY Embarques*):** Seguimiento de la
    cantidad de embarques.
-   **Matriz de Rutas (*Route Matrix*):** Análisis de rutas según POL,
    POD, volumen y carrier dominante.
-   **Análisis de Tránsito (*Transit Analysis*):** Cálculo del tránsito
    medio y retraso medio por ruta.
-   **Clasificación de Riesgos (*Route Risk*):** Identificación de rutas
    con niveles de riesgo bajo, medio y alto.
-   **Control de Estados (*QTY Estatus*):** Consolidación de los estados
    operativos de los embarques.
-   **Reporte Semanal (*Weekly Report*):** Generación de indicadores de
    seguimiento y alertas por destino.
-   **Registro de Indicadores (*PostgreSQL / Google Sheets*):**
    Almacenamiento de los resultados para su consulta y seguimiento.

## 🚀 Funcionalidades Principales

-   **Integración Multicarrier:** Consolidación de información
    procedente de diferentes operadores logísticos.
-   **Carrier Performance:** Evaluación de proveedores mediante volumen
    de envíos, retrasos, porcentaje de retrasos y tiempo medio de
    espera.
-   **Route Matrix:** Análisis de rutas marítimas según origen, destino,
    carrier y comportamiento del tránsito.
-   **Route Risk Classification:** Clasificación de riesgos operativos
    según el retraso medio de las rutas.
-   **Shipment Monitoring:** Seguimiento de embarques y distribución por
    estados operativos.
-   **Weekly Control Tower:** Consolidación de indicadores y alertas
    semanales.
-   **Operational Analytics:** Transformación de registros logísticos en
    información útil para la toma de decisiones.

## 📊 Indicadores y Reglas de Control

### Clasificación de Riesgo de Rutas

-   **Bajo:** Retraso medio de hasta 1 día.
-   **Medio:** Retraso medio superior a 1 y hasta 3 días.
-   **Alto:** Retraso medio superior a 3 días.

### Alertas de Bloqueo Semanal

-   **Verde:** Porcentaje de bloqueo igual o inferior al 15%.
-   **Amarillo:** Porcentaje de bloqueo superior al 15% y hasta el 30%.
-   **Rojo:** Porcentaje de bloqueo superior al 30%.

## 🧠 Evolución hacia Inteligencia Artificial -- Roadmap

La arquitectura actual incorpora automatización, integración de datos y
analítica basada en reglas. Las siguientes capacidades representan una
evolución futura del proyecto:

-   **Predictive ETA:** Predicción de fechas estimadas de llegada y
    posibles retrasos.
-   **AI Anomaly Detection:** Identificación de comportamientos anómalos
    en tiempos, costes y operaciones.
-   **AI Logistics Assistant:** Asistente inteligente para consultar
    información de embarques, carriers y rutas mediante lenguaje
    natural.
-   **Predictive Route Analytics:** Análisis predictivo del
    comportamiento de las rutas.
-   **Intelligent Decision Support:** Recomendaciones para priorizar
    incidencias y mejorar la toma de decisiones operativas.
-   **Power BI Integration:** Visualización de indicadores y tendencias
    mediante dashboards ejecutivos.

## 🛠️ Tecnologías Utilizadas

-   **Automatización y Flujos:** n8n / Workflow Orchestration.
-   **Procesamiento:** JavaScript / Data Transformation.
-   **Base de Datos:** PostgreSQL.
-   **Fuentes de Información:** Google Sheets.
-   **Business Intelligence:** Power BI.
-   **Control de Versiones:** Git / GitHub.
-   **Entorno Logístico:** Supply Chain Management / Maritime Inbound /
    Carrier Management.

## 🎯 Valor Estratégico del Proyecto

-   Centralización de información logística procedente de múltiples
    operadores.
-   Reducción de tareas manuales de consolidación de datos.
-   Mayor visibilidad del rendimiento de los carriers.
-   Identificación de rutas con mayores retrasos.
-   Seguimiento estructurado de embarques y estados operativos.
-   Generación de indicadores para el control semanal.
-   Preparación de una arquitectura de datos para futuras aplicaciones
    de Inteligencia Artificial en Logística 4.0.

------------------------------------------------------------------------

*Desarrollado por Larry Steven Pineda Fonseca*
