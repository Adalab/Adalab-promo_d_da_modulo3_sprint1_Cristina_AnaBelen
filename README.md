# Adalab-promo_d_da_modulo3_sprint1_Cristina_AnaBelen


Este repositorio contiene los ejercicios referentes al módulo 3, sprint 1 del bootcamp Data Analyst de Adalab.

Las librerías que se manejan son:
    -[NumPy](https://numpy.org/)
    -[Pandas](https://pandas.pydata.org/)
    -[Matplotlib](https://matplotlib.org/)
    -[Seaborn](https://seaborn.pydata.org/)
    -[Scikit Learn](https://scikit-learn.org/stable/index.html)

Los contenidos de este módulo son:
    - Regresión lineal fundamentos
    - Introducción a Maching Learning
    - Test estadísticos
    - Covarianza y correlación
    - Asunciones
    - Normalización
    - Estandarización
    - ANOVA
    - Encoding
    - Intro Regresión lineal
    - regresión lineal métricas
    - Decision Tree
    - Random forest
    - Regresión logística - EDA
    - Regresión logística - Ajuste
    - Regresión logística - Métricas
    - Regresión logística - Decision Tree
    - Regresión logística - Random Forest

El repositorio está organizado en tres carpetas:
    - Datos: contiene los archivos de trabajo y los que se han ido generando durante el módulo.
    - Regresión lineal: archivos de trabajo de los contenidos de regresión lineal.
    - Regresión logística: archivos de trabajo de los contenidos de regresión logística y una carpeta denominada "data" con los archivos de trabajo.

MODELO DE ML BASADO EN REGRESIÓN LINEAL

    - Se seleccionó el dataset "supermarket" que contiene datos de tres supermercados de Myanmar. 
    - Realizamos EDA, eliminamos columnas redundantes, seleccionamos "Rating" como variable respuesta, categorizamos columnas y terminamos la exploración con la visualización de gráficas. 
    - Comprobamos la simetría de la variable respuesta y las relaciones entre variables.
    - Comprobamos asunciones para las variables predictoras de cara a la aplicación de regresión lineal. 
    - Se intentó la normalización con el método Box-cox de la variable respuesta sin éxito. No obstante, por razón meramente práctica, se continua con el modelo (estandarización de variables predictoras y realización de ANOVA). 
    - Realizamos codificación de variables categóricas aplicando distintos métodos también a efectos de práctica. 
    - Creamos un primer modelo de regresión lineal sin obtener resultados. 
    - Corroboramos con las métricas que el modelo no predice el rating. 
    - Realizamos un nuevo modelo aplicando Decision Tree. De nuevo sin éxito.
    - Realizamos otro modelo aplicando Random Forest también sin resultados. 

    De esta parte del trabajo concluímos que ninguno de los modelos es válido para predecir la variable respuesta seleccionada. Pensamos que no tenemos variables predictoras que sirvan para predecir esta variable. Investigamos otros resultados a través de Kaggle y encontramos conclusiones semejantes a las nuestras.

    Al haber mirado otros trabajos relativos a este dataset, decidimos probar con otra variable respuesta, en una aproximación modificada de un caso. Elegimos como variable respuesta "Total" y eliminamos columnas redudantes. 
    Realizamos un Decision Tree con el que tampoco obtenemos resultados al igual que con el Random Forest.

MODELO DE ML BASADO EN REGRESIÓN LOGÍSTICA

    - Se seleccionó el dataset "card_transdata" que contiene 1.000.000 de registros y trata del fraude en compras con tarjeta de crédito. La predicción de este fraude será el objeto del modelo y "fraude" la variable respuesta.
    - Realizamos EDA y visualización de datos. El dataset no contiene nulos ni duplicados. Todas las columnas son de tipo "float". Las variables que consideramos categóricas, incluida la variable respuesta, se cambian en este momento a tipo "category". 
    - Procesamos datos aplicando el método RobustScaler a las columnas numéricas. Utilizamos este método por la existencia de outliers que hemos decidido no eliminar tras valorarlos en el primer análisis. Aplicamos el método get-dummies para el encoding de la variable "user_pin_number" que es la variable categórica que consideramos no tiene orden. Las que sí tienen orden las dejamos como están. 
    - Aplicamos el SMOTETomek para el desbalanceo de los datos de la variable respuesta. Tras aplicar el método, comprobamos que nos está generando nulos. Parece estar realizando el upsampling pero el downsampling solo de forma parcial. A partir de aquí, dividimos el ejercicio en diferentes aproximaciones:

            1. Eliminamos los duplicados generados y continuamos con el modelo para ver las métricas.
            2. Eliminamos el get_dummies realizado y probamos a realizar el SMOTETomek antes de dividir datos en train y test. Esto sigue generando nulos. 
            3. Retrocedimos al inicio y no realizamos el cambio de las variables a tipo "category".  De esta manera trabajamos con el dataset original con la única modificación de la estandarización de las tres variables consideradas inicialmente numéricas a las que se les realiza el RobustScaler. Estas variables son: distance_from_home, distance_from_last_transaction, ratio_to_median_purchase_price. 
    
     




