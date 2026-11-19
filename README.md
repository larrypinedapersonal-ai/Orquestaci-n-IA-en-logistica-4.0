# Orquestación de IA y Asistentes Virtuales en Logística 4.0

## 📋 Descripción del Proyecto
Proyecto de automatización y gestión logística avanzada enfocado en optimizar la cadena de suministro internacional (*supply chain*), unificando procesos para transitarias *inbound* y navieras mediante flujos automatizados de datos.

## ⚙️ Arquitectura del Flujo de Automatización (Workflow)
El sistema implementa un pipeline automatizado en **n8n** para el procesamiento masivo de registros:
* **Trigger Programado (*Schedule Trigger*):** Ejecución automática de procesos periódicos de sincronización.
* **Extracción de Datos (*Get rows*):** Lectura centralizada desde múltiples fuentes y bases de datos de navieras/transitarias (más de 20,000 registros procesados simultáneamente).
* **Unificación y Filtrado (*Merge & Filter*):** Combinación inteligente de bases de datos de entrada y depuración de registros.
* **Procesamiento a Medida (*Code in JavaScript*):** Transformación de datos mediante código personalizado para adaptar los formatos logísticos.
* **Registro Automatizado (*Append row*):** Consolidación final en la base de datos central.

## 🚀 Funcionalidades Principales
* **Integración de Bases de Datos:** Sincronización y unificación de datos clave de navieras y transitarias.
* **Gestión de Proveedores y Planificación:** Coordinación automatizada de la cadena de suministro.
* **Control de Facturación y Comunicaciones:** Seguimiento centralizado mediante automatizaciones conectadas a Gmail.

## 🛠️ Tecnologías Utilizadas
* **Automatización y Flujos:** n8n / Orquestación de Nodos Lógicos.
* **Procesamiento:** JavaScript, Bases de Datos relacionales y Hojas de cálculo sincronizadas.
* **Gestión:** SAP (MM, SD), Power BI.
* **Control de Versiones:** Git / GitHub.

---
*Desarrollado por Larry Steven Pineda Fonseca*
