# Sistema Inteligente de Análisis y Predicción del Desempeño Académico en Educación Virtual

## Descripción del Proyecto

Este proyecto implementa un sistema integral de análisis y predicción del desempeño estudiantil utilizando técnicas de Machine Learning supervisadas y no supervisadas sobre el dataset Open University Learning Analytics Dataset (OULAD).

El objetivo principal es analizar el comportamiento de estudiantes en entornos virtuales de aprendizaje para:

- Detectar estudiantes en riesgo de abandono
- Predecir desempeño académico
- Descubrir perfiles de comportamiento
- Analizar patrones de interacción en plataformas educativas
- Visualizar métricas e insights mediante dashboards interactivos

El sistema integra datos demográficos, actividad dentro del Virtual Learning Environment (VLE), evaluaciones y resultados académicos para construir modelos predictivos e interpretables.

---

# Dataset

## Fuente

Open University Learning Analytics Dataset (OULAD)

Dataset:
https://www.kaggle.com/datasets/anlgrbz/student-demographics-online-education-dataoulad/data

## Descripción

El dataset contiene información anonimizada de estudiantes de la Open University del Reino Unido e incluye:

- Datos demográficos
- Resultados académicos
- Actividad en plataforma virtual
- Evaluaciones y entregas
- Información temporal de interacción

---

# Objetivos

## Objetivo General

Construir un sistema inteligente capaz de analizar y predecir el rendimiento estudiantil en educación virtual.

## Objetivos Específicos

- Analizar comportamiento académico y digital
- Detectar patrones asociados al abandono
- Comparar modelos de clasificación
- Implementar técnicas de clustering
- Aplicar reducción dimensional
- Construir dashboards interactivos
- Explicar decisiones del modelo mediante técnicas de interpretabilidad

---

# Tecnologías Utilizadas

| Área | Tecnología |
|---|---|
| Lenguaje | Python |
| Manipulación de datos | Pandas, NumPy |
| Visualización | Matplotlib, Seaborn, Plotly |
| Machine Learning | Scikit-learn |
| Boosting | XGBoost |
| Dashboard | Streamlit |
| Explainability | SHAP |
| Notebook | Google Colab |

---

# Estructura del Proyecto
/root/
/root/Dataset/(Copiar aca todos los dataset)
/root/Colab Notebook

---

# Dataset Utilizado

## Tablas principales

| Tabla | Descripción |
|---|---|
| studentInfo | Información demográfica y resultado final |
| studentVle | Interacciones con la plataforma |
| vle | Información sobre recursos del VLE |
| studentAssessment | Resultados de evaluaciones |
| assessments | Información de evaluaciones |
| studentRegistration | Registro y deserción |
| courses | Información de cursos |

---

# Pipeline del Proyecto

text Raw Data    ↓ Data Cleaning    ↓ Feature Engineering    ↓ EDA    ↓ Supervised Learning    ↓ Unsupervised Learning    ↓ Dimensionality Reduction    ↓ Model Evaluation    ↓ Dashboard & Visualization 

---

# Técnicas Implementadas

## Aprendizaje Supervisado

- K-Nearest Neighbors (KNN)
- Logistic Regression
- Support Vector Machines (SVM)
- Decision Trees
- Naive Bayes

## Aprendizaje No Supervisado

- K-Means Clustering

## Reducción Dimensional

- PCA (Principal Component Analysis)

## Explainable AI

- SHAP Values
- Feature Importance

---

# Variables y Features Relevantes

## Features de Engagement

- total_clicks
- avg_clicks_per_week
- early_activity
- activity_trend

## Features Académicas

- mean_score
- submission_ratio
- late_submissions

## Features Demográficas

- age_band
- gender
- highest_education
- region
- disability

---

# Visualizaciones Implementadas

- Heatmaps
- Correlation matrices
- ROC Curves
- Confusion Matrices
- PCA Scatter Plots
- Cluster Visualizations
- Radar Charts
- Timeline Charts
- Sankey Diagrams
- SHAP Summary Plots

---

# Dashboard Interactivo

El proyecto incluye un dashboard desarrollado con Streamlit para visualizar:

- KPIs generales
- Métricas de abandono
- Rendimiento académico
- Actividad en plataforma
- Comparación de modelos
- Predicciones individuales
- Clustering de estudiantes
- Explicabilidad de modelos

---

# Métricas de Evaluación

## Clasificación

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

## Clustering

- Silhouette Score
- Inertia

---

# Objetivo Principal del Modelo

El sistema busca resolver principalmente:

## Predicción temprana de abandono estudiantil

Clasificación:
- Withdrawn vs Non-Withdrawn

Y secundariamente:
- Predicción de aprobación
- Segmentación de estudiantes
- Análisis de comportamiento digital

---

# Instalación

## Clonar repositorio

bash git clone <repository_url> cd project 

## Crear entorno virtual

bash python -m venv venv 

## Activar entorno

### Windows

bash venv\Scripts\activate 

### Linux / Mac

bash source venv/bin/activate 

## Instalar dependencias

bash pip install -r requirements.txt 

---

# Ejecución

## Notebooks

Abrir notebooks desde:

bash /notebooks 

## Dashboard Streamlit

bash streamlit run dashboard/app.py 

---

# Resultados Esperados

El sistema permitirá:

- Detectar estudiantes en riesgo
- Descubrir patrones de comportamiento
- Comparar técnicas de Machine Learning
- Explicar predicciones del modelo
- Visualizar insights complejos
- Facilitar intervenciones educativas tempranas

---

# Limitaciones

- Dataset limitado a una universidad
- Posible desbalance de clases
- Dependencia de calidad de interacción digital
- Variables temporales complejas

---

# Trabajo Futuro

- Modelos temporales avanzados
- Deep Learning
- Recomendadores educativos
- Detección de anomalías
- Predicción en tiempo real
- Integración con LMS reales

---

# Uso de Inteligencia Artificial Generativa

Durante el desarrollo del proyecto se utilizaron herramientas de IA generativa para:

- Explicación de conceptos
- Asistencia en debugging
- Generación de documentación
- Sugerencias de visualización
- Revisión de arquitectura del sistema

Todas las decisiones de diseño, selección de modelos y validación fueron realizadas críticamente por el equipo de desarrollo.

---

# Autores
MASSHOLDER KEVIN
CARPINETI OCTAVIO

Proyecto desarrollado para la materia:
Sistemas Inteligentes — 2026

---

# Licencia

Uso académico y educativo.
