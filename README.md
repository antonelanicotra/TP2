# TP2

•	Descripción del proyecto:
Este proyecto desarrolla un modelo de Machine Learning supervisado para clasificar individuos como fumadores o no fumadores a partir de información médica, demográfica y clínica obtenida durante exámenes de salud.
El conjunto de datos principal utilizado para el entrenamiento fue el archivo smoking_prediction - smoking_prediction.csv, mientras que las predicciones finales se realizaron sobre el archivo smoking_prediction_entrega - smoking_prediction.csv.

•	Objetivo del proyecto:
Construir un modelo de clasificación basado en Random Forest capaz de predecir:
    0: No fumador
    1: Fumador
Se utilizando variables como:
    Género
    Edad
    Altura
    Peso
    Circunferencia de cintura
    Presión arterial
    Colesterol
    HDL
    LDL
    Triglicéridos
    Hemoglobina
    Indicadores odontológicos (tartar, dental caries)


El objetivo adicional fue lograr un modelo con un desempeño adecuado, minimizando el overfitting mediante el ajuste de hiperparámetros.

•	Instrucciones para reproducir el entorno y ejecutar el código.
•	Explicación de la estructura de archivos.
•	Resumen de los experimentos realizados, pruebas, intentos y cambios tomados a lo largo del desarrollo.
•	Conclusiones principales.


El análisis exploratorio permitió comprender la estructura del conjunto de datos y detectar las variables con mayor relación respecto al hábito de fumar. Las variables hemoglobin, gender, triglyceride, HDL, LDL y waist(cm) mostraron diferencias apreciables entre fumadores y no fumadores. No se detectaron problemas significativos de calidad de datos ni valores faltantes relevantes. La variable objetivo presentó una distribución adecuada para entrenar modelos de clasificación. A partir de estos hallazgos se decidió utilizar un modelo Random Forest, capaz de capturar relaciones no lineales entre las variables y la condición de fumador del individuo