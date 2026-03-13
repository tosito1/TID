# Tratamiento Inteligente de Datos (TID)

Este repositorio contiene las prácticas realizadas en la asignatura **Tratamiento Inteligente de Datos** del Máster en Ingeniería Informática.

El objetivo del proyecto es aplicar técnicas de **análisis exploratorio, minería de datos y machine learning** sobre distintos tipos de datasets reales: datos financieros, deportivos, clínicos, tráfico, texto y series temporales.

A lo largo de las prácticas se implementa el ciclo completo de un proyecto de **Data Science**:

1. Exploración y visualización de datos
2. Limpieza y preparación de datos
3. Ingeniería de características
4. Aplicación de algoritmos de minería de datos
5. Entrenamiento de modelos de machine learning
6. Evaluación y comparación de resultados

Las prácticas utilizan principalmente **KNIME Analytics Platform** y **Python** para el análisis avanzado de datos.

---

# Tecnologías utilizadas

Lenguajes

* Python

Herramientas

* KNIME Analytics Platform
* Google Colab

Librerías

* pandas
* scikit-learn
* statsmodels
* scipy
* xgboost
* yfinance

Conceptos de Data Science

* Exploratory Data Analysis (EDA)
* Feature Engineering
* Clustering
* Association Rules
* Machine Learning
* Natural Language Processing
* Time Series Forecasting

---

# Práctica 1 — Análisis Exploratorio de Datos

Herramienta utilizada: **KNIME Analytics Platform**

## Descripción

Se realizó un análisis exploratorio profundo sobre dos datasets reales:

* Base de datos financiera de clientes bancarios
* Estadísticas deportivas de jugadores de la NBA

El objetivo fue comprender la estructura de los datos, detectar patrones y extraer insights mediante técnicas estadísticas y visualización avanzada.

## Conceptos aprendidos

### Preprocesamiento de datos

* Tipificación correcta de variables numéricas y categóricas
* Renombrado y filtrado de variables para facilitar el análisis
* Segmentación de datos mediante filtros por filas y columnas

### Análisis estadístico

* Media, desviación estándar, asimetría y curtosis
* Identificación de outliers mediante diagramas de caja
* Correlación de Pearson entre variables

### Visualización de datos

* Diagramas de barras, pie charts y scatter plots
* Visualización multivariable con colores por categoría
* Análisis multidimensional mediante **parallel coordinates**

## Aplicaciones

* **Análisis financiero:** relación entre nivel educativo, ingresos y uso de productos financieros
* **Sports Analytics:** clasificación de jugadores NBA en roles funcionales según su rendimiento

---

# Práctica 2 — Preparación y Tratamiento de Datos

## Descripción

Esta práctica se centró en la fase más crítica del pipeline de datos: **la preparación y limpieza del dataset** antes del modelado.

Se aplicaron múltiples técnicas para mejorar la calidad de los datos y analizar cómo estos cambios afectan al rendimiento de un modelo de clasificación basado en árboles de decisión.

## Conceptos aprendidos

### Tratamiento de valores perdidos

* Identificación de columnas con alto porcentaje de nulos
* Imputación mediante media o moda
* Imputación basada en algoritmos predictivos

### Discretización de variables

Transformación de variables continuas en rangos categóricos utilizando:

* **CAIM (Class-Attribute Interdependence Maximization)**

### Reducción de dimensionalidad

* Eliminación de variables redundantes mediante correlación
* **PCA (Principal Component Analysis)** para reducir dimensiones conservando el 95% de la información
* **Backward Feature Elimination** para seleccionar las variables más relevantes

### Balanceo de datos

* Muestreo aleatorio
* **SMOTE** para generar instancias sintéticas de clases minoritarias

### Modelado

* Clasificación mediante **C4.5 Decision Tree**
* Evaluación mediante matriz de confusión y accuracy

## Casos de uso

* Perfilado de vehículos para seguros
* Predicción de riesgo clínico en cáncer cervical
* Predicción de gravedad en accidentes de tráfico

---

# Práctica 3 — Market Basket Analysis

## Descripción

Se realizó un análisis de **Market Basket Analysis** utilizando el algoritmo **Apriori** para descubrir patrones de compra en supermercados.

El objetivo fue identificar combinaciones frecuentes de productos y generar reglas de asociación.

## Conceptos aprendidos

### Transformación de datos

* Conversión de datasets relacionales a formato transaccional
* Manipulación avanzada de strings para generar listas de productos

### Minería de datos

* Algoritmo **Apriori** para identificar itemsets frecuentes
* Generación de reglas de asociación

### Métricas de evaluación

* Support
* Confidence
* Lift

## Aplicaciones

* Diseño de estrategias de **cross-selling**
* Optimización del layout de supermercados
* Segmentación de clientes basada en patrones de compra

---

# Práctica 4 — Clustering y Análisis No Supervisado

## Descripción

Se aplicaron técnicas de **clustering** para descubrir estructuras ocultas en datasets sin etiquetas.

Casos de estudio:

* Clasificación de vinos según propiedades químicas
* Segmentación de jugadores NBA según rendimiento

## Algoritmos utilizados

* Clustering jerárquico
* **K-Means**
* **DBSCAN**

## Conceptos aprendidos

* Distancias Euclidianas y Manhattan
* Métodos de enlace (single, average, complete)
* Interpretación de dendrogramas
* Detección de outliers mediante clustering basado en densidad

## Resultados

* Reconstrucción automática de categorías de vinos
* Identificación de roles de jugadores NBA mediante clustering

---

# Práctica 5 — Sistema Predictivo de Rendimiento Deportivo

## Descripción

Se desarrolló un sistema predictivo para clasificar el rendimiento de jugadores NBA.

Se crearon métricas personalizadas de rendimiento ofensivo y defensivo combinando múltiples estadísticas.

## Feature Engineering

Creación de variables derivadas:

* Rendimiento ofensivo
* Rendimiento defensivo

Posteriormente se discretizaron en categorías:

* Excelente
* Bueno
* Promedio
* Bajo

## Modelos entrenados

* Random Forest
* Naive Bayes
* K-Nearest Neighbors

## Resultados

El modelo **Random Forest** obtuvo la mayor precisión para este dataset.

---

# Práctica 6 — Predicción de Accidentes Mortales

## Descripción

Se construyeron modelos de machine learning para predecir si un accidente de tráfico resultará en víctimas mortales.

Dataset:

* 28,390 registros reales de accidentes

## Algoritmos evaluados

* Decision Tree
* Naive Bayes
* Support Vector Machine
* K-Nearest Neighbor

## Evaluación

* Cross Validation (10-fold)
* Curvas ROC
* AUC

## Resultados

* **Decision Tree:** mejor recall para detectar accidentes mortales
* **Naive Bayes:** mejor accuracy global

---

# Práctica 8 — Procesamiento de Lenguaje Natural (NLP)

## Descripción

Se desarrolló un sistema de análisis de sentimiento capaz de clasificar automáticamente reseñas de películas de IMDb como **positivas o negativas**.

## Procesamiento de texto

* Tokenización
* Part-of-Speech Tagging
* Bag of Words
* TF-IDF

## Modelos aplicados

* Árboles de decisión para clasificación
* **K-Means** para clustering de opiniones

## Aplicaciones

* Análisis automático de opiniones de clientes
* Descubrimiento de temáticas ocultas en textos

---

# Práctica 9 — Predicción de Series Temporales

Herramientas:

* Python
* Google Colab

Dataset:

* Precios históricos de acciones de **Tesla (TSLA)** desde 2018 hasta 2024

## Procesamiento de series temporales

* Medias móviles
* Descomposición estacional
* Normalización Min-Max

## Procesamiento de señales

* Transformada de Fourier para eliminar ruido

## Modelos entrenados

* Linear Regression
* Random Forest Regressor
* Support Vector Regression
* XGBoost

## Resultados

El modelo **Linear Regression** obtuvo el mejor rendimiento tras el preprocesamiento de la serie temporal.

---

# Conclusiones del proyecto

Este proyecto cubre múltiples áreas del **Tratamiento Inteligente de Datos**:

* análisis exploratorio de datos
* preparación y limpieza de datasets
* minería de datos
* clustering
* machine learning supervisado
* procesamiento de lenguaje natural
* análisis de series temporales

A través de estas prácticas se desarrolló experiencia en la aplicación de técnicas avanzadas de análisis de datos sobre **datasets reales de diferentes dominios** como finanzas, deporte, medicina, tráfico, comercio y mercados financieros.

---

# Autor

Tosé
Máster en Ingeniería Informática
