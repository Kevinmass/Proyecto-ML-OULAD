# Roadmap — Sistema Inteligente de Análisis y Predicción del Desempeño Académico en Educación Virtual

# Objetivo General

Construir un sistema de Machine Learning capaz de:

- Analizar comportamiento estudiantil en plataformas virtuales
- Detectar estudiantes en riesgo de abandono
- Predecir desempeño académico
- Descubrir perfiles de estudiantes
- Explicar factores que afectan el rendimiento
- Visualizar métricas e insights mediante dashboards interactivos

Dataset utilizado:
Open University Learning Analytics Dataset (OULAD)

---

# Arquitectura General

Raw CSVs
↓
Integración de tablas
↓
Preprocesamiento
↓
EDA + Visualizaciones
↓
Feature Engineering
↓
Modelos Supervisados
↓
Modelos No Supervisados
↓
Evaluación
↓
Dashboard Final

---

# EPIC 1 — Comprensión y Arquitectura del Dataset

## Objetivo
Comprender completamente:
- relaciones entre tablas
- tipos de variables
- claves
- temporalidad
- granularidad de datos

## Tareas
- Analizar estructura relacional
- Identificar joins
- Construir diccionario de datos
- Crear mapa conceptual del dataset
- Detectar missing values

## Tablas involucradas
- studentInfo
- studentVle
- studentAssessment
- assessments
- vle
- courses
- studentRegistration

## Entregables
- Documento de arquitectura del dataset
- Diagrama relacional simplificado
- Diccionario de variables

## Visualizaciones
- Entity Relationship Diagram
- Heatmap de missing values
- Distribución de tipos de variables

---

# EPIC 2 — Integración y Preprocesamiento

## Objetivo
Construir datasets limpios y listos para Machine Learning.

## Tareas
- Limpieza de datos
- Eliminación de duplicados
- Tratamiento de nulls
- Conversión de tipos
- Encoding de variables categóricas
- Escalado/normalización
- Integración de tablas

## Datasets derivados

### Dataset Demográfico
studentInfo

### Dataset Conductual
studentVle + vle

### Dataset Académico
studentAssessment + assessments

### Dataset Maestro
Integración completa

## Feature Engineering

### Features de engagement
- total_clicks
- avg_clicks_per_week
- early_activity

### Features académicas
- mean_score
- submission_ratio
- late_submissions

### Features temporales
- activity_trend
- inactivity_periods
- days_since_last_access

## Entregables
- Dataset limpio
- Dataset integrado
- Pipeline reproducible

## Visualizaciones
- Histogramas
- Boxplots
- Correlation heatmaps
- Timeline charts

---

# EPIC 3 — Análisis Exploratorio de Datos (EDA)

## Objetivo
Descubrir patrones relevantes antes del modelado.

## Preguntas clave
- ¿Qué factores afectan abandono?
- ¿Cómo usan la plataforma los alumnos exitosos?
- ¿Existe relación entre actividad y rendimiento?
- ¿Qué perfiles demográficos tienen mayor riesgo?

## Visualizaciones

### Distribución de resultados académicos
- Pass
- Fail
- Withdrawn

### Actividad vs desempeño
- Boxplots
- Violin plots

### Evolución temporal
- Actividad semanal
- Tendencia de engagement

### Correlaciones
- Heatmaps

### Análisis demográfico
- Edad
- Región
- Educación
- Género

### Sankey diagrams
Demografía → comportamiento → resultado

## Entregables
- Notebook EDA
- Insights accionables
- Hipótesis para modelos

---

# EPIC 4 — Machine Learning Supervisado

## Objetivo
Predecir:
- abandono
- aprobación
- rendimiento académico

## Problema principal recomendado
Clasificación:
Withdrawn vs Non-Withdrawn

## Modelos

### KNN
- efecto de K
- sensibilidad al escalado

### Logistic Regression
- interpretabilidad
- probabilidades

### SVM
- kernels lineales y RBF
- separación no lineal

### Decision Trees
- reglas interpretables
- feature importance

### Naive Bayes
- baseline probabilístico

## Evaluación

### Métricas
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

## Visualizaciones

### ROC Curves
Comparación de modelos

### Confusion Matrices

### Precision-Recall Curves

### Feature Importance

### Visualización de árboles

### Decision boundaries usando PCA

## Entregables
- Modelos entrenados
- Benchmark comparativo
- Modelo óptimo seleccionado

---

# EPIC 5 — Reducción Dimensional

## Objetivo
Reducir complejidad y visualizar patrones ocultos.

## Técnicas
- PCA

## Aplicaciones
- Visualización 2D
- Mejora de clustering
- Eliminación de redundancia

## Visualizaciones

### PCA Scatter Plot
Coloreado por:
- final_result
- cluster

### Scree Plot
Varianza explicada

### PCA Loadings
Importancia de componentes

## Entregables
- Dataset reducido
- Visualizaciones PCA

---

# EPIC 6 — Aprendizaje No Supervisado

## Objetivo
Descubrir perfiles de estudiantes sin etiquetas previas.

## Técnicas

### K-Means
Segmentación principal

## Features utilizadas
- engagement
- scores
- regularidad
- actividad temprana
- entregas

## Objetivos
Detectar perfiles como:
- Alto rendimiento
- Bajo engagement
- Riesgo de abandono
- Estudiantes constantes

## Visualizaciones

### Elbow Method

### Clusters en PCA 2D

### Radar Charts por cluster

### Heatmap de centroides

## Entregables
- Clusters identificados
- Descripción de perfiles estudiantiles

---

# EPIC 7 — Interpretabilidad y Explainable AI

## Objetivo
Explicar las decisiones del sistema.

## Técnicas
- SHAP values
- Feature importance

## Preguntas clave
- ¿Por qué un estudiante fue clasificado como riesgo?
- ¿Qué variables afectan más el abandono?

## Visualizaciones
- SHAP summary plot
- Dependence plots
- Ranking de features

## Entregables
- Análisis interpretable
- Explicación de predicciones

---

# EPIC 8 — Dashboard Interactivo

## Objetivo
Construir un sistema visual e interactivo para análisis.

## Tecnología recomendada
Streamlit

## Secciones del dashboard

### 1. Overview general
KPIs:
- total estudiantes
- tasa de abandono
- tasa de aprobación
- promedio score
- actividad promedio

### 2. Demografía
- distribución de edad
- género
- región
- educación

### 3. Actividad VLE
- clicks semanales
- uso por actividad
- timelines

### 4. Predicción ML
Input:
- features estudiante

Output:
- probabilidad de abandono
- explicación SHAP

### 5. Clustering
- perfil asignado
- visualización de clusters

### 6. Comparación de modelos
- Accuracy
- Recall
- F1
- ROC-AUC

## Visualizaciones
- KPI cards
- Heatmaps
- Scatter plots interactivos
- Radar charts
- Timeline charts
- ROC interactive plots
- Sankey diagrams

## Entregables
- Dashboard funcional
- Sistema navegable
- Visualizaciones interactivas

---

# EPIC 9 — Informe y Storytelling

## Objetivo
Documentar el proyecto de forma clara y profesional.

## Estructura recomendada

### 1. Introducción
Problema y motivación

### 2. Dataset
Descripción y relaciones

### 3. Metodología
Preprocesamiento y modelos

### 4. EDA
Hallazgos principales

### 5. Modelos supervisados
Resultados y comparación

### 6. Modelos no supervisados
Clusters y perfiles

### 7. Dashboard
Descripción funcional

### 8. Recomendaciones
Aplicaciones reales

### 9. Limitaciones
Sesgos y trabajo futuro

### 10. Uso de IA generativa
Herramientas utilizadas y revisión crítica

## Entregables
- Informe PDF
- Google Colab
- Presentación oral

---

# Stack Tecnológico Recomendado

| Área | Herramienta |
|---|---|
| Manipulación de datos | Pandas |
| ML | Scikit-learn |
| Boosting | XGBoost |
| Visualización | Plotly |
| EDA | Seaborn |
| Dashboard | Streamlit |
| Explainability | SHAP |
| Notebook | Google Colab |

---

# Roadmap resumido

| Epic | Objetivo |
|---|---|
| 1 | Comprensión del dataset |
| 2 | Preprocesamiento |
| 3 | EDA |
| 4 | Clasificación supervisada |
| 5 | PCA |
| 6 | Clustering |
| 7 | Interpretabilidad |
| 8 | Dashboard |
| 9 | Informe final |

---

# Resultado Final Esperado

Un sistema inteligente capaz de:
- analizar comportamiento estudiantil
- detectar estudiantes en riesgo
- segmentar perfiles
- explicar decisiones del modelo
- visualizar insights complejos
- asistir en intervenciones tempranas educativas