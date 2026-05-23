# ConnectaTel-Analysis
Análisis de comportamiento del cliente y segmentación comercial en Python para ConnectaTel.
# 📊 ConnectaTel: Análisis de Comportamiento del Cliente y Segmentación Estratégica

Este repositorio contiene un proyecto integral de **Análisis de Datos (Data Analytics)** enfocado en evaluar el comportamiento de los clientes y los patrones de consumo de **ConnectaTel**, una empresa de telecomunicaciones ficticia en Latinoamérica, con registros históricos consolidados hasta el año 2024.

El objetivo principal es transformar datos crudos de uso y perfiles de usuarios en **insights ejecutivos** y **recomendaciones comerciales accionables** orientadas a mitigar el *churn* (fuga de clientes), optimizar el ARPU (ingresos promedio por usuario) y estructurar campañas eficaces de *up-selling*.

---

## 🚀 Estructura del Proyecto

El análisis se desarrolló completamente en Python dentro de un Jupyter Notebook y se divide en las siguientes etapas clave:

1. **Exploración y Diagnóstico Inicial:** Identificación de la estructura de datos, formatos, consistencia operativa y detección de valores faltantes/sentinels.
2. **Limpieza y Calidad de Datos:** Tratamiento avanzado de valores nulos (verificación de mecanismos de pérdida como MAR - *Missing At Random* para duraciones y mensajes) y corrección de valores atípicos (`-999` en edad).
3. **Ingeniería de Características:** Agrupación y pivoteo de la tabla de consumo (`usage`) para consolidar métricas métricas históricas personalizadas por cada usuario (minutos consumidos, total de textos enviados, llamadas totales).
4. **Análisis de Distribuciones y Outliers:** Implementación de gráficos estadísticos (histogramas, KDE, boxplots) segmentados por tipo de plan actual (**Básico vs. Premium**).
5. **Segmentación Multidimensional de Clientes:**
   - **Por Uso:** Clasificación algorítmica en *Bajo uso*, *Uso medio* y *Alto uso*.
   - **Por Edad:** Clasificación demográfica para entender preferencias generacionales.
6. **Insight Ejecutivo y Recomendaciones:** Traducción de hallazgos estadísticos en estrategias puras de negocio.

---

## 📊 Principales Hallazgos (Insights de Negocio)

* **Concentración en el Plan Básico:** El **64.9%** de los clientes se encuentra en el plan más económico, representando una oportunidad masiva para estrategias de migración escalonada.
* **Segmento Dorado de Alto Uso:** Un **6.95%** de la base de datos exhibe consumos extremadamente altos (llamadas/mensajes largos), convirtiéndose en el público objetivo ideal para un plan Ultra-Premium con soporte VIP.
* **Oportunidad Demográfica:** Los **Adultos Mayores representan el 30.55%** de la base analizada. Sus distribuciones demuestran que consumen paquetes de voz tradicionales más que datos intensivos, abriendo la puerta a productos nicho.
* **Simetría Operativa:** El consumo general (llamadas de 3-6 minutos o 2.5-5 mensajes por sesión) presenta un sesgo a la derecha idéntico en ambos planes, lo que sugiere que muchos usuarios Premium están subutilizando sus beneficios o que usuarios Básicos sufren penalizaciones por excedentes.

---

## 🎯 Recomendaciones Estratégicas Redactadas

Para impactar el negocio, el análisis propone tres estrategias directas y accionables:

1. **Estrategia Senior (Fidelización del 30.55%):** Lanzar el *"Plan Conectados Senior"* a **$10/mes**, enfocado en 500 minutos de voz nacionales, soporte simplificado vía WhatsApp y números frecuentes ilimitados.
2. **Blindaje High-Value (Retención del 6.95%):** Crear el plan *"Connecta Max Premium"* (**$35-$40/mes**) con datos/minutos ilimitados y roaming básico, ofreciendo un upgrade directo con 50% de descuento el primer mes para evitar la fuga a la competencia.
3. **Campaña de Up-selling Intermedio (Migración del 64.9%):** Diseñar un *"Plan Puente"* a **$15/mes** ofreciendo una prueba gratuita de 2 meses a los usuarios del plan Básico. La fricción de baja manual posterior asegura tasas históricas de conversión superiores al 20%.

---

## 🛠️ Tecnologías Utilizadas

* **Python 3.x**
* **Pandas** (Estructuración, limpieza, agregaciones y uniones de datos)
* **NumPy** (Operaciones lógicas y manejo de arrays)
* **Matplotlib & Seaborn** (Visualizaciones avanzadas, histogramas de densidad y boxplots de detección de anomalías)

---

## 📂 Datasets Analizados

* `plans.csv`: Datos de las tarifas vigentes, minutos/GB incluidos y costos marginales por excedente.
* `users.csv`: Información demográfica del cliente (edad, ciudad, fecha de alta, plan activo y estatus de churn).
* `usage.csv`: Bitácora detallada de interacciones en tiempo real (tipo de servicio, duración, caracteres de texto y fecha).

---
*Análisis desarrollado como parte del proyecto de evaluación de comportamiento del cliente de ConnectaTel (2024).*
Cómo reproducir el proyecto", que indique cómo ejecutar el notebook. Por ejemplo:

## ▶️ Cómo ejecutar el proyecto

1. Clona este repositorio
2. Instala las dependencias: `pip install pandas numpy matplotlib seaborn`
3. Abre el notebook `connectatel_analysis.ipynb` en Jupyter
4. Ejecuta las celdas en orden
