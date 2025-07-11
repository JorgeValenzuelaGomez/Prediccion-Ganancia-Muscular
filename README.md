# Prediccion-Porcentaje de grasa
Proyecto final del curso introducción a la Inteligencia Artificial - Universidad de OHiggins

Nombres: Jorge Valenzuela, Carlos Moreno

Definición del problema

El porcentaje de grasa corporal es una de las métricas más relevantes para evaluar la salud y la composición corporal de una persona. A diferencia del peso o el índice de masa corporal (IMC), el porcentaje de grasa entrega una visión más precisa sobre el estado físico, permitiendo identificar riesgos metabólicos o cardiovasculares, incluso en personas con peso aparentemente normal.

Este proyecto tiene como objetivo construir un modelo de aprendizaje supervisado que permita predecir el porcentaje de grasa corporal de una persona (Body Fat) en base a sus características físicas, como la edad, peso, altura, y medidas antropométricas (por ejemplo, circunferencia de abdomen, muñeca, cadera, entre otras). La predicción se realizará utilizando técnicas de regresión.

Plan de acción 

El dataset seleccionado es un conjunto de datos real que contiene mediciones de 252 hombres adultos. Las variables incluyen edad, altura, peso, densidad corporal y circunferencias de distintas partes del cuerpo, como el abdomen, pecho, brazo, muslo, rodilla y tobillo. El valor a predecir (BodyFat) fue obtenido mediante un método confiable: hidrodensitometría.

Se utilizarán distintos modelos de regresión supervisada para predecir el porcentaje de grasa corporal. Se comenzará con una regresión lineal múltiple como modelo base y se evaluarán posteriormente otros algoritmos como árbol de decisión y random forest para comparar el rendimiento.

La evaluación del modelo se realizará dividiendo el conjunto de datos en entrenamiento y prueba, utilizando métricas como el error absoluto medio (MAE), el error cuadrático medio (MSE) y el coeficiente de determinación (R²). Además, se implementará validación cruzada para asegurar la robustez de los resultados.

Justificación del modelo

La regresión lineal múltiple fue seleccionada como punto de partida por su simplicidad, interpretabilidad y capacidad para modelar relaciones lineales entre la variable objetivo y múltiples predictores. Esto permite establecer una base comprensible desde la cual evaluar mejoras posteriores.

También se emplearán modelos basados en árboles, como el árbol de decisión y random forest. Estos modelos permiten capturar relaciones no lineales y manejar interacciones complejas entre variables sin necesidad de transformar los datos.

Como ventajas, estos modelos son fáciles de entrenar, ofrecen buen desempeño con datos estructurados y permiten interpretar la importancia de cada variable. Entre sus limitaciones está el riesgo de sobreajuste en modelos complejos como random forest, y la menor capacidad explicativa de los árboles en comparación con regresión lineal simple.

La elección de estos modelos es pertinente para un problema de predicción continua como este, y todos ellos fueron revisados durante el curso, cumpliendo con los lineamientos del proyecto.

Dataset y fuente
Se utilizó el Body Fat Prediction Dataset, el cual contiene 252 registros con 15 variables, incluyendo medidas como densidad corporal, edad, peso, altura y distintas circunferencias. El dataset fue obtenido desde la plataforma Kaggle, publicado por el usuario "fedesoriano" bajo licencia abierta.

Metodología aplicada (paso a paso)

Primero se cargó el dataset desde Kaggle, que contiene mediciones físicas de personas junto con su porcentaje de grasa corporal. Se revisó la estructura del archivo utilizando los métodos head, info y describe, lo que permitió tener una visión general de los datos y detectar posibles problemas.

Luego, se realizó un análisis exploratorio utilizando una matriz de correlación. Esta herramienta ayudó a identificar qué variables tenían mayor relación con la variable objetivo, que en este caso es BodyFat. Se observó que abdomen, chest y hip tenían alta correlación positiva, lo que sirvió como orientación para el proceso de selección de variables.

A continuación, se prepararon los datos para el modelo. Se eliminaron variables irrelevantes y se normalizaron las variables numéricas mediante la técnica de escalamiento estándar usando StandardScaler. Posteriormente, los datos se dividieron en conjuntos de entrenamiento y prueba con la función train_test_split.

Para predecir el porcentaje de grasa corporal, se entrenaron tres modelos de regresión: regresión lineal, árbol de decisión y bosque aleatorio. Cada uno fue evaluado utilizando métricas como error absoluto medio (MAE), error cuadrático medio (MSE) y coeficiente de determinación (R2).

Finalmente, se compararon los resultados obtenidos por cada modelo. Random Forest fue el que mostró el mejor desempeño general, con un R2 de 0.6512, y los menores errores MAE y MSE. Estos resultados se visualizaron mediante gráficos de barras comparativos y una gráfica que muestra los valores reales versus los valores predichos, lo que permitió validar visualmente la calidad de las predicciones.

Resultados obtenidos
Tras evaluar los tres modelos entrenados, se observaron los siguientes resultados:
Regresión Lineal: obtuvo un MAE de 3.35, MSE de 19.41 y un R2 de 0.5827.
Árbol de Decisión: presentó un desempeño inferior, con un MAE de 5.12, MSE de 37.51 y R2 de 0.1936.
Random Forest: fue el modelo que obtuvo el mejor rendimiento general, alcanzando un MAE de 3.32, MSE de 16.23 y un R2 de 0.6512.
Estos resultados se visualizaron en un gráfico comparativo que muestra claramente la superioridad del modelo Random Forest en términos de precisión. Además, se generó una gráfica de dispersión que compara los valores reales con los valores predichos, evidenciando una alineación aceptable en la mayoría de los casos.

Conclusiones

Se concluye que el modelo de Random Forest es el más adecuado para predecir el porcentaje de grasa corporal en este conjunto de datos, ya que logró los mejores resultados en todas las métricas evaluadas. Además, se comprobó que variables como abdomen y pecho son fuertes predictores del BodyFat, lo que refuerza la importancia del análisis exploratorio inicial.

El proceso seguido permitió aplicar paso a paso técnicas reales de machine learning, desde la exploración de datos hasta la comparación de modelos. A pesar de tratarse de un dataset pequeño, se logró una predicción razonablemente precisa, lo que demuestra que una buena preparación de los datos y una selección adecuada de modelos pueden generar buenos resultados incluso en proyectos sencillos.


