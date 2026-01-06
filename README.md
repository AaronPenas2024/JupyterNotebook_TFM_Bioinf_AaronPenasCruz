# TFM – Evaluación automática de la ejecución de ejercicios de rehabilitación mediante sensores wearables

Este repositorio contiene el código fuente y los datos procesados utilizados en el Trabajo Final de Máster desarrollado en el Máster Universitario en Ingeniería Biomédica (UOC).

El objetivo del proyecto es evaluar la corrección en la ejecución de ejercicios de rehabilitación a partir de señales de electromiografía de superficie (sEMG) y unidades de medición inercial (IMU), utilizando modelos de aprendizaje automático supervisado y una estrategia de validación independiente por sujeto.

---

## Estructura del repositorio

- `readData.ipynb`  
  Lectura del dataset original, procesamiento inicial de los datos y construcción del conjunto de características.

- `statisticalAnalysis.ipynb`  
  Análisis exploratorio y estadístico de las características extraídas.

- `modelTraining.ipynb`  
  Entrenamiento y evaluación de los modelos de clasificación mediante validación Leave-One-Subject-Out (LOSO), así como análisis de interpretabilidad mediante SHAP.

- `features_trials_imu_emg.csv`  
  Dataset de características extraídas a partir de señales IMU y sEMG.

- `features_with_meta_and_target.csv`  
  Dataset de características con metadatos y variable objetivo.

- `features_model_ready.csv`  
  Dataset final utilizado para el entrenamiento de los modelos.

- `results_loso_baselines.csv`  
  Resultados agregados de las métricas obtenidas mediante validación LOSO.

- `modelo_rf_sle.joblib`  
  Modelo Random Forest entrenado para el ejercicio Seated Leg Extension (SLE).

---

## Dataset

El conjunto de datos original **no se incluye** en este repositorio debido a restricciones de tamaño y condiciones de uso.

El dataset puede obtenerse a partir de su fuente original:

Kansnes, P. et al. (2025). *A Knee Rehabilitation Exercises Dataset for Postural Assessment using Wearable Devices*. Scientific Data.

Una vez descargado, el dataset debe almacenarse localmente y adaptarse la ruta correspondiente en el cuaderno `readData.ipynb`.

---

## Entorno de trabajo y dependencias

El proyecto se ha desarrollado en Python utilizando JupyterLab a través de la distribución Anaconda.

Las principales librerías utilizadas son:
- numpy
- pandas
- scikit-learn
- matplotlib
- seaborn
- shap
- joblib

---

## Reproducibilidad

El pipeline completo de procesamiento, entrenamiento y evaluación está documentado en los cuadernos incluidos en este repositorio. Ejecutando los cuadernos en el orden indicado es posible reproducir los resultados presentados en la memoria del TFM.

---

## Autor

Aaron Peñas Cruz  
Trabajo Final de Máster – Universitat Oberta de Catalunya (UOC)
