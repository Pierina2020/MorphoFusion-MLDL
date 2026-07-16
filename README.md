# MorphoFusion-MLDL: Código Fuente del Sistema

Repositorio complementario del artículo de investigación orientado a la clasificación del nivel de rendimiento deportivo en atletas universitarios a partir de variables morfológicas, mediante técnicas de Machine Learning, Deep Learning e interpretabilidad con SHAP.

## Objetivo

Desarrollar un sistema computacional capaz de clasificar el nivel de rendimiento deportivo en atletas universitarios, considerando información morfológica organizada en dimensiones antropométricas, composición corporal, proporcionalidad corporal y maduración biológica.

## Dataset

El conjunto de datos utilizado estuvo conformado por 80 registros de atletas universitarios. Después del proceso de limpieza, anonimización y selección de variables, se emplearon 91 variables predictoras morfológicas y una variable objetivo binaria:

- `0`: En desarrollo
- `1`: Alto rendimiento

## Procesamiento de datos

El flujo metodológico incluyó:

- limpieza de nombres de columnas;
- eliminación de identificadores personales;
- anonimización del conjunto de datos;
- recodificación de la variable objetivo;
- eliminación de variables no predictivas;
- análisis de correlación de Pearson;
- selección de características mediante SelectKBest;
- imputación de valores faltantes;
- escalamiento mediante StandardScaler;
- partición estratificada 80/20;
- validación cruzada estratificada de 5 pliegues.

## Modelos evaluados

Se evaluaron siete modelos de clasificación.

### Machine Learning

- Regresión Logística
- SVM
- Random Forest
- XGBoost

### Deep Learning

- MLP
- CNN1D
- Attention

## Modelo final

El modelo seleccionado fue Regresión Logística, debido a que presentó el mejor equilibrio entre accuracy, balanced accuracy, F1-score y MCC en el conjunto de prueba.

## Interpretabilidad

Se utilizó SHAP para identificar las variables morfológicas con mayor influencia en la clasificación del rendimiento deportivo, permitiendo complementar el desempeño predictivo con una explicación interpretable del modelo.

## Archivos del repositorio

- `MorphoFusion_MLDL_codigo.ipynb`: notebook principal del sistema.
- `dataset_limpio_morphofusion_mldl.csv`: dataset limpio y anonimizado.
- `requirements.txt`: librerías necesarias para ejecutar el notebook.
- `README.md`: descripción general del proyecto.

## Ejecución

Para ejecutar el notebook en Google Colab:

1. Abrir `MorphoFusion_MLDL_codigo.ipynb`.
2. Instalar las dependencias indicadas en `requirements.txt`.
3. Cargar el dataset limpio.
4. Ejecutar las celdas en orden.

## Privacidad de datos

El dataset publicado fue anonimizado antes de su almacenamiento en GitHub. No se incluyen nombres, apellidos, universidad, fechas personales ni otra información que permita identificar directamente a los atletas evaluados.
