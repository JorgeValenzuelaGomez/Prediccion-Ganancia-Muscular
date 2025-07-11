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


