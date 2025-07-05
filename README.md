# Prediccion-Porcentaje de grasa
Proyecto final del curso introducción a la Inteligencia Artificial - Universidad de OHiggins

Nombres: Jorge Valenzuela, Carlos Moreno

Definición del problema

En el contexto del entrenamiento físico y los hábitos saludables, la composición corporal es un indicador clave del estado de salud y rendimiento. Uno de los componentes más relevantes de esta composición es el porcentaje de grasa corporal, ya que un exceso de grasa se asocia con riesgos cardiovasculares y metabólicos, mientras que niveles óptimos suelen reflejar una mejor condición física. Este proyecto tiene como objetivo construir un modelo predictivo que estime el porcentaje de grasa corporal de una persona en función de sus características físicas (edad, género, peso, altura, frecuencia cardíaca, índice de masa corporal, etc.) y sus hábitos de vida (tipo de entrenamiento, duración de la sesión, ingesta de agua, frecuencia de entrenamiento, nivel de experiencia, entre otros). La predicción se realizará utilizando técnicas de regresión, buscando obtener una estimación continua y precisa de la variable objetivo Fat_Percentage.

Plan de acción 

El dataset utilizado para este proyecto corresponde a un conjunto de datos sintético que simula el registro de miembros de un gimnasio, incluyendo tanto características físicas como hábitos de entrenamiento. Contiene un total de 973 registros y 15 columnas, entre las que se destacan:
Edad, género, peso, altura, índice de masa corporal (BMI)
Porcentaje de grasa corporal (Fat_Percentage)
Tipo de entrenamiento, duración de la sesión, frecuencia semanal
Nivel de experiencia, frecuencia cardíaca, ingesta de agua
Calorías quemadas por sesión
La variable objetivo a predecir es Fat_Percentage, ya que representa un indicador clave del estado físico general de la persona y se encuentra influenciado por múltiples factores disponibles en el conjunto de datos.
El modelo seleccionado para este proyecto será una regresión lineal múltiple, por su simplicidad, interpretabilidad y utilidad como punto de partida en problemas de regresión. Posteriormente se evaluará también el uso de modelos no lineales como árboles de decisión y random forest, que permiten capturar relaciones más complejas y no lineales entre variables.
La estrategia de evaluación consiste en dividir el dataset en un conjunto de entrenamiento y otro de prueba. Se utilizarán métricas como el Error Absoluto Medio (MAE), el Error Cuadrático Medio (MSE) y el coeficiente de determinación (R²) para medir el rendimiento de los modelos. Además, se aplicará validación cruzada para asegurar la robustez de los resultados.

Justificación del modelo

El modelo principal seleccionado es la regresión lineal múltiple, ya que permite predecir una variable continua como el porcentaje de grasa corporal en función de múltiples variables independientes. Su implementación es sencilla, es fácilmente interpretable y sirve como línea base para comparar con otros modelos más complejos.
Además, se considerarán modelos no lineales como árboles de decisión y random forest, los cuales pueden capturar interacciones y relaciones no lineales entre variables, lo que resulta útil en contextos donde los hábitos y características físicas pueden combinarse de manera compleja.
Entre las ventajas de los modelos seleccionados se encuentran su facilidad de entrenamiento, su capacidad de interpretación (en el caso de la regresión) y su buen desempeño con datos mixtos (en el caso de los árboles). Como limitación, la regresión lineal puede no capturar correctamente relaciones no lineales, y los modelos de árboles pueden sobreajustar si no se controlan adecuadamente los hiperparámetros.
La elección de estos modelos es pertinente, ya que se alinean con la naturaleza del problema (predicción de una variable numérica) y con los contenidos revisados en el curso.
