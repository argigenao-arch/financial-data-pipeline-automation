# End-to-End Data Pipeline & Automatización de Validación Financiera

## 📌 Situación y Problema de Negocio
En entornos financieros internacionales, el procesamiento manual de flujos de datos provenientes de múltiples unidades de negocio independientes genera cuellos de botella operacionales y aumenta el riesgo de errores en los reportes de P&L. Se requería una solución automatizada que consolidara estos flujos y garantizara la integridad del dato antes de su carga en los sistemas de Business Intelligence

## 🎯 Acciones e Hitos Técnicos

### 1. Optimización y Modelado de Consultas en SQL (MySQL)
* Implementación de **Common Table Expressions (CTEs)** y **Window Functions** (`ROW_NUMBER()`) para limpiar y particionar el histórico de transacciones masivas.
* Eliminación de subconsultas redundantes para optimizar los tiempos de ejecución en la base de datos de staging.

### 2. Script de Validación de Calidad del Dato (Python + Pandas)
* Desarrollo de un script automatizado en Python que actúa como *data gatekeeper*.
* Programación de reglas de negocio específicas para identificar anomalías en tiempo real: detección de valores negativos erróneos y alertas automáticas ante la ausencia de códigos de divisa o registros duplicados.

## 📊 Resultados e Impacto de Negocio
**Eficiencia:** Unificación de flujos de trabajo aislados en un pipeline consolidado
**Calidad:** Se logró una **reducción del 15% en los errores de procesamiento manual* garantizando datos limpios y listos para auditorías financieras.

---

## 📁 Estructura del Repositorio
* `src/pipeline.py`: Script principal de extracción, limpieza y validación en Python.
* `sql/queries_optimization.sql`: Consultas avanzadas de MySQL utilizadas para la segmentación de datos.
* `data/`: Carpeta con datos de muestra (anonimizados).
