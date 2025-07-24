# Proyecto_Modelos_Predictivos
Este es un proyecto final para la materia de Modelos Predictivos de la Maestría de Análisis de Datos en la Universidad Tecnologica de Panamá
## Presentación
- Elaborado por:Angiel Fernández
- Profesor: Juan Marcos Castillo, PhD
## Este repositorio contine lo siguiente:
- La propuesta
- Avances
- Trabajo Final
- Excel de Las Variables total del dataset con su descripción
- Excel de las Evaluaciones de los Modelos
- Carpeta con los Dataset Originales
- Codigos del Proyecto
- Story Telling
## Dataset
- Fuente: [2015 Flight Delays and Cancellations - Kaggle](https://www.kaggle.com/datasets/usdot/flight-delays)
- Tamaño de la muestra: 500,000 registros seleccionados aleatoriamente.
- Variables utilizadas:
  - `YEAR`, `MONTH`, `DAY`, `DAY_OF_WEEK`
  - `AIRLINE`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`
  - `SCHEDULED_DEPARTURE`, `DISTANCE`, `SCHEDULED_ARRIVAL`,  `SCHEDULED_TIME`
  - `DELAYED`: Variable objetivo (`delayed` o `on time`)
 ## Modelos Probados
Se probaron varios clasificadores con técnicas de balanceo de clases:

- Regresión Logística
- Random Forest
- Gradient Boosting
- LightGBM
- XBoost
- CatBoost
- Random Forest

Técnicas de balanceo aplicadas:
- Ninguno 
- class_weight='balanced'
- Undersampling
- SMOTE (Synthetic Minority Over-sampling)

## Evaluación
Métricas evaluadas:
- Accuracy
- Precision
- Recall
- F1-Score
- Matriz de Confusión
- AUC-ROC

- Dado el desbalance de clases, se priorizó **recall** y **F1-score** de la clase minoritaria.
