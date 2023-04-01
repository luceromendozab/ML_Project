# Machine Learning para Predecir Precios de Diamantes

![portada](https://github.com/Ironhack-Data-Madrid-Enero-2021/W7-Kaggle_competition/blob/main/images/PORTADA.jpg)

## Descripción

Este proyecto tiene como objetivo utilizar técnicas de aprendizaje automático (machine learning) para predecir los precios de los diamantes en función de sus características. Para ello, se utilizará un conjunto de datos que contiene información sobre varios diamantes, como el peso en quilates, el color, la claridad y la forma.

## Datos 
Los datos utilizados en este proyecto son dos DataFrame , uno llamano "train.csv" que utilizaremos para entrenar nuestro modelo y otro llamado "test.csv" que utilizaremos para predecir los precios de los diamantes segun sus características.

El conjunto de datos incluye las siguientes columnas:

Carat: El peso del diamante en quilates.
Cut: La calidad de corte del diamante (Fair, Good, Very Good, Premium, Ideal).
Color: El color del diamante, desde J (más amarillo) hasta D (más blanco).
Clarity: La claridad del diamante, desde I1 (peor) hasta IF (mejor).
Depth: La profundidad total del diamante, medida desde la mesa hasta el culet como un porcentaje del diámetro total.
Table: El ancho de la mesa del diamante, como un porcentaje del diámetro total.
Price: El precio del diamante en dólares estadounidenses.
X, Y, Z: Las dimensiones del diamante en milímetros.

## Preprocesamiento de Datos
Antes de entrenar cualquier modelo de aprendizaje automático, es necesario preprocesar los datos. En este caso, se realizarán las siguientes tareas de preprocesamiento:

Eliminar las columnas X, Y y Z, ya que el peso del diamante (carat) es suficiente para representar su tamaño.
Convertir las variables categóricas (Cut, Color y Clarity) en variables numéricas usando codificación one-hot_encoding y ordinal encoding.


## Modelado 

Se utilizarán varios modelos de aprendizaje automático para predecir los precios de los diamantes. Estos incluyen:

- Regresión lineal: un modelo lineal simple que intenta encontrar una relación lineal entre las variables de entrada y la variable de salida (precio).
- Árbol de decisión: un modelo no lineal que divide los datos en varias ramas y hojas, donde cada hoja representa una predicción.
- Random Forest: un modelo que combina múltiples árboles de decisión y promedia sus predicciones.

## Evaluación 
Para evaluar la precisión de cada modelo, se utilizará el modelo que mejor tenga el MSE.

- Error cuadrático medio (MSE): una medida de la diferencia entre las predicciones del modelo y los valores reales. Cuanto menor sea el MSE, mejor será el modelo.

## Conclusiones

- La calidad del preprocesamiento de datos es fundamental para obtener buenos resultados en el modelado. En este proyecto, la eliminación de las columnas X, Y , Z, depth% , table  y la codificación one-hot y ordinal de las variables categóricas ayudaron a mejorar la precisión de los modelos.

- La gestión de outliers es importante para evitar que valores extremos en los datos distorsionen las predicciones del modelo. En este proyecto, se utilizaron técnicas como el análisis de caja para identificarlos. ??????

- La codificación ordinal asigna valores numéricos a las categorías en función de su orden natural, por lo que puede reflejar cierta relación de orden entre las categorías.????

- En cuanto a la codificación one-hot es una técnica útil para convertir variables categóricas en variables numéricas para su uso en modelos de aprendizaje automático. Sin embargo, puede aumentar el tamaño del conjunto de datos, lo que puede ser problemático en conjuntos de datos grandes.?????

- Se demostró que el modelo de Random Forest produjeron resultados mejores. Esto se concluyo debido a su metrica MSE que era la más baja de todas. 

![portada](https://github.com/Ironhack-Data-Madrid-Enero-2021/W7-Kaggle_competition/blob/main/images/PORTADA.jpg)

- En general, este proyecto demuestra cómo la aplicación de técnicas de Machine Learning puede ser útil para predecir precios de diamantes, lo que puede ser útil para la industria joyera y para los consumidores que buscan comprar diamantes a precios justos.

## Librerias utilizadas 

- Pandas: utilizada para la manipulación y análisis de datos en el DataFrame que contiene las características de los diamantes y sus precios.

- NumPy: utilizada para la manipulación de matrices y cálculos numéricos en el preprocesamiento de los datos.

- Matplotlib: utilizada para la visualización de datos y gráficos de distribución de las variables.

- Seaborn: utilizada para la visualización de distribuciones de variables y correlaciones entre ellas.

- Scikit-learn: utilizada para la implementación de los modelos de machine learning, selección de características y evaluación del rendimiento de los modelos.

- Pickle: utilizada para guardar el modelo final entrenado y su uso posterior para hacer predicciones en nuevos datos.