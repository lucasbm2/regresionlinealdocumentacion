# REGRESIÓN LINEAL EN CLASIFICACIÓN DE CÉLULAS CANCERÍGENAS

## 1.	Introducción.

Hemos querido hacer un modelo de clasificación de células para comparar con el modelo que nos entregaba el enunciado, que es el de clasificación mediante redes neuronales.

Para ello, se ha revisado la documentación oficial de Scikit-Learn, además de revisar múltiples cuadernos de Colab donde otros usuarios implementaban este modelo.

Sabíamos que este modelo no está definido para un uso tan complejo como este, pero queríamos comprobar si podría sacar resultados parecidos, ya que es un modelo mucho menos costoso en recursos.

## 2.	Implementación

Primeramente, hemos tenido que traducir las clases a números para poder entrenar este modelo, porque los datos que teníamos en el enunciado estaban enfocados al modelo de redes neuronales.

•	Así que traducimos las clases a números, creando un conjunto primero y luego volviendo a dividir los datos en entrenamiento y test.

•	Utilizamos el modelo LinearRegression de Scikit-learn.

•	Entrenamos el modelo.

•	Una vez lo hemos entrenado, redondeamos los valores a enteros, encuadrándolos entre 0, 1 y 2, como las clases que definimos en el diccionario.

•	Después, con la librería plt vamos a representar la matriz de confusión, donde podemos comprobar la precisión de nuestro modelo.

## 3.	Apuntes.

Este modelo es tan sencillo que no realiza el entrenamiento por épocas, sino como un total.

No podemos visualizar la curva de aprendizaje, como sí que hemos podido ver en el modelo del enunciado.

Y, sobre todo, este modelo no está diseñado para clasificación, pero queríamos comprobar si podría ser útil debido a su bajo coste.


## 4.	Justificación adaptar regresión a clasificación

La regresión líneal trata dos variables, una dependiente y otra independiente, como por ejemplo puede ser la relación entre horas trabajadas y sueldo mensual.

Como había 3 clases, se ha asignado un número a las clases, basándonos en que cuando una célula normal (0) se corrompe, asumimos que pasa por el estado benigno (1) al crecer, y después se vuelve maligno (2). Esto no quiere decir que en la realidad sea así, pero es la lógica que hemos empleado para utilizarlo en este caso. 

## 5.	Conclusión final.

El modelo de regresión lineal es menos conveniente para resolver el problema de clasificación que el modelo de redes neuronales, por lo que nos decantaremos por el segundo.

Al realizar una predicción de precios o estimación de costes, sí que sería un cálculo más preciso, pero en este caso que tiene más complejidad y riesgo, hemos demostrado que no es el idóneo.

