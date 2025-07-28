# Proyecto_Modelos_Predictivos
Título: **Predicción de Retrasos en Vuelos Comerciales utilizando Modelos de Clasificación”**
Este es un proyecto final para la materia de Modelos Predictivos de la Maestría de Análisis de Datos en la Universidad Tecnológica de Panamá
## Presentación
- Elaborado por: Angiel Fernández
- Profesor: Juan Marcos Castillo, PhD

## Este Repositorio contiene:
- Trabajo Final
- Excel de Las Variables total del dataset con su descripción
- Excel de las Evaluaciones de los Modelos
- Carpeta con los Dataset Originales
- Códigos del Proyecto
- Story Telling

## Problematica
La puntualidad en los vuelos es un aspecto clave para el buen funcionamiento del sector aeronáutico. No solo afecta la eficiencia operativa de aerolíneas y aeropuertos, sino también la experiencia de los pasajeros, quienes dependen cada vez más de un servicio confiable y predecible.
A partir de esto, surge la siguiente pregunta que da origen a este proyecto: ¿Podemos anticipar si un vuelo se retrasará, utilizando únicamente los datos disponibles antes del despegue?
Responder esta pregunta permitiría desarrollar un sistema que clasifique los vuelos en dos categorías: a tiempo (0) o retrasado (1). Para este estudio, se considerará como “retrasado” cualquier vuelo cuya salida se postergue más de 15 minutos, siguiendo criterios estándar en la industria.
  
## Dataset
- Fuente: [2015 Flight Delays and Cancellations - Kaggle](https://www.kaggle.com/datasets/usdot/flight-delays)
- Tamaño de la muestra: 500,000 registros seleccionados aleatoriamente.
- Variables utilizadas:
  - `YEAR`, `MONTH`, `DAY`, `DAY_OF_WEEK`
  - `AIRLINE`, `ORIGIN_AIRPORT`, `DESTINATION_AIRPORT`
  - `SCHEDULED_DEPARTURE`, `DISTANCE`, `SCHEDULED_ARRIVAL`,  `SCHEDULED_TIME`
  - `DELAYED`: Variable objetivo (`delayed` o `on time`)
     
 ## Modelos Probados
Se probaron varios modelos:

- Regresión Logística
- Random Forest
- Hist Gradient Boosting
- LightGBM
- XBoost
- CatBoost
- Random Forest

Técnicas de balanceo aplicadas:
- Ninguno 
- class_weight='balanced'
- Undersampling
- SMOTE (Synthetic Minority Over-sampling)

## Instrucciones
-Se debe correr en primera instancia el archivo ProyectoMP_EDA_Limpieza.ipynb, cargando el dataset flight.csv, este a su vez generará el dataset df_limpio.
- Acto seguido se debe correr el limpieza_adicional.ipynb, el cual generará el dataset df_final.csv el cual será usado para la evaluacion de los modelos.
- Con el df_final.py ya se pueden probar los diferentes archivos .ipynb que contienen los modelos, estan divididos de la siguiente manera:
- 1. Archivos unbalance_gs.ipynb, class_balance_gs.ipynb, undersampling_gs.ipynb y smote_gs.ipynb (cada uno una tecnica de balanceo diferente); cada archivo contiene la evaluación de los modelos Árbol de Decisión, Lightgbm, Regresión Lógistica y Hist gradient boost.
  2. En el archivo Random_Forest.ipynb se encuentra la evaluación del modelo random forest con sus tecnicas de balanceo correspondientes.
  3. En el archivo LightunOHE, Catboost, XGoost.ipynb se encuentran a su vez la evaluacion de estos tres modelos sin la utilizacion de OHE con sus tecnicas de balance correspondiente.

## Evaluación
Métricas evaluadas:
- Accuracy
- Precision
- Recall
- F1-Score
- Matriz de Confusión
- AUC-ROC

- Dado el desbalance de clases, se priorizó **recall** y **F1-score** de la clase minoritaria.
