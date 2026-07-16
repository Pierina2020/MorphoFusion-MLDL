# MorphoFusion-MLDL

Código fuente del sistema MorphoFusion-MLDL para la clasificación del nivel de rendimiento deportivo en atletas universitarios a partir de variables morfológicas, empleando técnicas de Machine Learning, Deep Learning e interpretabilidad mediante SHAP.

## Contenido del repositorio

- `MorphoFusion_MLDL_codigo.ipynb`: notebook principal con el procesamiento de datos, entrenamiento de modelos, evaluación e interpretabilidad.
- `requirements.txt`: librerías necesarias para ejecutar el código.
- `dataset_limpio_morphofusion_mldl.csv`: conjunto de datos limpio y anonimizado usado para el modelado.

## Modelos evaluados

Se evaluaron modelos de Machine Learning y Deep Learning:

- Regresión Logística
- SVM
- Random Forest
- XGBoost
- MLP
- CNN1D
- Attention

## Modelo final

El modelo seleccionado fue Regresión Logística, debido a que presentó el mejor equilibrio entre accuracy, balanced accuracy, F1-score y MCC en el conjunto de prueba.

## Privacidad de datos

El conjunto de datos fue anonimizado antes de su publicación. No se incluyen nombres, apellidos ni información personal identificable de los deportistas evaluados.
