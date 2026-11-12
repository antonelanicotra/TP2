•   Descripción del proyecto:
        Este proyecto desarrolla un modelo de Machine Learning supervisado para clasificar individuos como fumadores o no fumadores a partir de información médica, demográfica y clínica obtenida durante exámenes de salud.
        El conjunto de datos principal utilizado para el entrenamiento fue el archivo smoking_prediction - smoking_prediction.csv, mientras que las predicciones finales se realizaron sobre el archivo smoking_prediction_entrega - smoking_prediction.csv.

•   Objetivo del proyecto:
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

•   Instrucciones para reproducir el entorno y ejecutar el código.
        Ejecutar las notebooks en el siguiente orden:
            01_Lectura_y_Discovery.ipynb
            02_EDA.ipynb
            03_Preprocesamiento.ipynb
            04_Entrenamiento_y_Optimizacion.ipynb
            05_Guardo_Modelo.ipynb
            06_Predicciones.ipynb
            07_Validaciones.ipynb
        Cada notebook utiliza los resultados generados en la etapa anterior utilizando la instruccion %run
        
•   Explicación de la estructura de archivos.
        TP2/
        │
        ├── Datos/
        │   ├── OTROS
        │   └── Originales
        │         └── smoking_prediction.csv
        │         └── smoking_prediction_entrega.csv
        │   └── Procesados
        ├── Notebooks/TP2
        │   ├── 01_Lectura_y_Discovery.ipynb
        │   ├── 02_EDA.ipynb
        │   ├── 03_Preprocesamiento.ipynb
        │   ├── 04_Entrenamiento_y_Optimizacion.ipynb
        │   ├── 05_Guardo_Modelo.ipynb
        │   └── 06_Predicciones.ipynb
        │   └── 07_Validaciones.ipynb
        │
        ├── README.md
    01_Lectura_y_Discovery.ipynb: Instalación e Importación de librerías, Carga de datasets, Verificación de datos (Dimensiones. Tipos de datos. Valores nulos).
    02_EDA.ipynb: Distribuciones, Correlaciones, Heatmap, Boxplot.
    03_Preprocesamiento.ipynb: Separación de variables predictoras y variable objetivo, identificacion de variables categóricas, Aplicación de OneHotEncoder, guardo el dataset procesado en TP2/DATOS/Procesados/Procesado.csv, Train/Test.
    04_Entrenamiento_y_Optimizacion.ipynb: Entrenamiento del modelo Random Forest, Construcción del Pipeline, Entrenamiento, Predicciones y Metricas.
    05_Guardo_Modelo.ipynb: Entreno y guardo el modelo en TP2/DATOS/OTROS/modelo_random_forest_smoking.pkl
    06_Predicciones.ipynb: Cargo nuevos datos, Genero predicciones, obtengo probabilidad, predigo el archivo sin "Smoking" y guardo con las predicciones en TP2/DATOS/Procesados/personas_clasificadas.csv
    07_Validaciones.ipynb: Cargo el archivo con "SMOKING" y genero el codigo de barra de los fumadores y no fumadores, Cargo el archivo generado en el punto anterior y genero el mismo codigo de barras, a modo de poder comparar ambos resultados.

•   Resumen de los experimentos realizados, pruebas, intentos y cambios tomados a lo largo del desarrollo.
    Métricas utilizadas: Accuracy, Precision, Recall, F1-Score , Matriz de Confusion
    Comparación entre: Conjunto de entrenamiento y Conjunto de prueba.

•   Conclusiones principales.
       Durante el desarrollo de este proyecto se construyó un modelo de Machine Learning capaz de predecir si una persona es fumadora o no fumadora utilizando información demográfica y clínica contenida en el dataset analizado.
       A través del EDA se identificaron las características generales de la población estudiada, la distribución de la variable objetivo y posibles relaciones entre las variables predictoras y la condición de fumador.
       Posteriormente se realizó el preprocesamiento de los datos, incluyendo la transformación de variables categóricas mediante One-Hot Encoding y la preparación de los conjuntos de entrenamiento y prueba.
       Como modelo de clasificación se utilizó Random Forest Classifier, con lo cual se obtuvo un accuracy aproximado del 83% sobre el conjunto de entrenamiento y del 75% sobre el conjunto de prueba. Esto evidencian un overfitting moderado, lo que indica que el modelo es capaz de generalizar adecuadamente sobre datos no vistos.
       El modelo entrenado fue almacenado mediante Joblib, permitiendo reutilizarlo posteriormente para realizar predicciones sobre nuevos registros sin necesidad de volver a entrenar el algoritmo.


