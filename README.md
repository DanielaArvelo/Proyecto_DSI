# 🧠 Predicción del Riesgo de Agotamiento (Burnout Risk) en Empleados

## 📝 Descripción

Este proyecto consiste en el análisis de un *dataset* de encuestas de salud mental en el lugar de trabajo. El objetivo principal es **identificar y predecir los factores más influyentes** que llevan a un empleado a un alto **Riesgo de Agotamiento (Burnout)**.

Se implementan técnicas de Aprendizaje Automático (Machine Learning) para construir un modelo de clasificación robusto, complementado con un exhaustivo Análisis Exploratorio de Datos (EDA) para generar *insights* accionables y estratégicos.

## ⭐ Características y Fases del Proyecto

### 1. Análisis Exploratorio de Datos (EDA)
* **Limpieza de Datos:** Manejo y estandarización de variables (nulos, tipos de datos como `BurnoutLevel`, etc.).
* **Visualización:** Análisis de la correlación entre el apoyo del gerente, la satisfacción laboral y el impacto del estilo de trabajo (remoto/presencial) en el riesgo de agotamiento.
* **Conclusión:** Identificación de tendencias y perfiles de riesgo en la población de empleados.

### 2. Preprocesamiento de Datos para ML
* Uso de **Pipelines** y **ColumnTransformer** de Scikit-learn para aplicar transformaciones consistentes.
* Imputación de valores faltantes (mediana/moda), escalado de variables numéricas con **StandardScaler** y codificación categórica con **OneHotEncoder**.
* Limpieza y eliminación final de columnas redundantes (100% NaN) para garantizar la solidez de los datos.

### 3. Modelado y Predicción
* **Modelo Base (Interpretabilidad):** **Regresión Logística**, utilizado para determinar la dirección e intensidad de la influencia de cada factor en el riesgo de *burnout*.
* **Modelo de Alto Rendimiento:** **Árbol de Decisión**, el cual demostró una **precisión del 100%** en la detección de casos de riesgo en el conjunto de prueba.
* **Métricas:** Foco en el **F1-Score** y **AUC-ROC** para asegurar una alta confiabilidad en la predicción de la clase de riesgo.

## 🛠️ Tecnologías utilizadas

* **Lenguaje:** Python
* **Análisis y Manipulación de Datos:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (LogisticRegression, DecisionTreeClassifier, ColumnTransformer, Pipelines)

## 📂 Estructura del repositorio

* **mental_health_workplace_survey.csv:** Archivo CSV original de la encuesta. 
* **ProyectoDS_ParteI_Arvelo.ipynb:** Notebook completo con EDA, Preprocesamiento y Modelado.

## 📈 Principales Hallazgos y Recomendaciones

El análisis de los coeficientes de la Regresión Logística y el rendimiento de los modelos revelaron los siguientes *insights* clave:

* **Factor Protector Crítico:** La **Puntuación de Apoyo Gerencial** (`ManagerSupportScore`) es el factor más importante y con mayor coeficiente negativo (protector), disminuyendo significativamente el riesgo de *burnout*.
* **Roles Vulnerables:** El rol de **IT Admin** se asocia fuertemente con un mayor riesgo, lo que sugiere una carga de trabajo o estrés desproporcionados en ese puesto.
* **Recomendación de Negocio:** Se debe priorizar la **capacitación en habilidades de apoyo y liderazgo** para los gerentes y realizar **intervenciones específicas** en departamentos de alto riesgo, utilizando el modelo predictivo para el **monitoreo proactivo** de empleados.
