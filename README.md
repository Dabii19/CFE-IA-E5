# CFE-IA-E5

Este proyecto utiliza el **dataset Breast Cancer Wisconsin (Diagnostic)** de Kaggle para predecir si un tumor es **Benigno (0)** o **Maligno (1)** a partir de características clínicas.

## Objetivo
Entrenar un modelo de clasificación que estime el diagnóstico de un tumor en función de variables clínicas y realizar predicciones con valores ingresados manualmente.

## Datos:
**Variables utilizadas:**
- `radius_mean`: promedio del radio de las células  
- `perimeter_mean`: promedio del perímetro de las células  
- `area_mean`: promedio del área de las células  
- `diagnosis`: variable objetivo (0 = Benigno, 1 = Maligno)  

## Pasos realizados

### 1. Carga y preprocesamiento de datos
- Se cargó el dataset `data.csv`.  
- Se reemplazó la variable objetivo `diagnosis` para codificar: **B = 0, M = 1**.  
- Se seleccionaron las variables más influyentes según el mapa de calor (`radius_mean`, `perimeter_mean`, `area_mean`).  
- Se aplicó `StandardScaler` para normalizar los datos.  

### 2. Creación de gráficos e implementación del modelo KNN
- Se creó un **mapa de calor** para observar las correlaciones entre las variables y el diagnóstico.  
- Se generaron **gráficos de dispersión** (`radius_mean vs perimeter_mean` y `radius_mean vs area_mean`) para visualizar la separación entre tumores benignos y malignos.  
- Se realizaron **histogramas** para analizar la distribución de `radius_mean` y `area_mean` según el diagnóstico.  
- Se entrenó un modelo **KNeighborsClassifier** con `k=3`.  

### 3. Ingreso manual de datos y predicción
- Se ingresan valores manuales de `radius_mean`, `perimeter_mean` y `area_mean`.  
- El modelo predice si el tumor es **Benigno (0)** o **Maligno (1)**.  

### 4. Resultados
- Con valores bajos como [[12.5, 80.0, 500.0]] en este orden (radius_mean, perimeter_mean, area_meanel) los resultados son 0
- Con valores altos como [[20.0, 130.0, 1200.0]] en este orden (radius_mean, perimeter_mean, area_meanel) los resultados son 1
