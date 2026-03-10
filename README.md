# telecomx-churn-analysis
Exploratory data analysis of customer churn for Telecom X using Python.

# Telecom X - Análisis de Evasión de Clientes (Churn)

## Descripción del Proyecto

En este proyecto trabajé analizando el problema de evasión de clientes (Churn) en Telecom X. La empresa enfrenta una tasa considerable de cancelación de servicios y el objetivo principal fue tratar de entender qué factores pueden estar influyendo en que los clientes decidan irse.

Para abordar el problema, realicé un proceso completo de análisis de datos. Esto incluyó la extracción de la información, la limpieza y transformación de los datos, y finalmente un análisis exploratorio para poder identificar patrones y comportamientos relevantes.  

La idea detrás de este análisis es obtener una mejor comprensión del comportamiento de los clientes y generar insights que puedan ayudar a la empresa a tomar decisiones más informadas para reducir la evasión.

---

## Tecnologías Utilizadas

Durante el desarrollo del proyecto utilicé las siguientes herramientas:

- Python  
- Pandas  
- Matplotlib  
- Seaborn  
- Google Colab  

---

## Proceso del Análisis

El análisis se desarrolló siguiendo varias etapas típicas dentro de un flujo de trabajo de ciencia de datos.

### 1. Extracción de datos
- Los datos fueron obtenidos desde una API y estaban en formato JSON.

### 2. Limpieza y transformación de datos
En esta etapa preparé el dataset para que pudiera ser analizado correctamente:

- Normalización de columnas que venían anidadas.
- Conversión de variables al tipo de dato adecuado.
- Revisión y manejo de valores nulos.
- Creación de nuevas variables derivadas, como `Cuentas_Diarias`, para facilitar el análisis.

### 3. Análisis exploratorio de datos
Una vez preparado el dataset, realicé un análisis exploratorio para empezar a identificar patrones:

- Distribución general de clientes con churn vs. clientes que permanecen.
- Comparación de churn según diferentes variables categóricas.
- Exploración de variables numéricas relacionadas con el comportamiento de los clientes.

### 4. Visualización de datos
Para apoyar el análisis utilicé diferentes visualizaciones:

- Gráficos de barras
- Diagramas de caja (boxplots)
- Mapas de correlación

Estas visualizaciones ayudaron a identificar tendencias y relaciones entre variables.

---

## Principales Insights

A partir del análisis se pudieron observar algunos patrones interesantes relacionados con la evasión de clientes:

- Los clientes con contratos de corto plazo muestran una mayor tendencia a cancelar el servicio.
- Los clientes con menor tiempo de permanencia tienen una probabilidad más alta de churn.
- Existen algunas diferencias entre métodos de pago que podrían estar asociadas con la evasión.
- El gasto mensual también muestra comportamientos distintos entre los clientes que permanecen y los que terminan cancelando el servicio.

---

## Recomendaciones

Basado en los resultados obtenidos, algunas posibles acciones que la empresa podría considerar son:

- Incentivar contratos de mayor duración para mejorar la retención de clientes.
- Desarrollar estrategias de fidelización enfocadas en clientes nuevos.
- Analizar con mayor profundidad los métodos de pago que parecen estar más relacionados con churn.
- Explorar la creación de modelos predictivos que permitan identificar clientes con riesgo de cancelación antes de que ocurra.

---

## Autor

Proyecto realizado como parte del desafío **Telecom X - Análisis de Datos** del programa **Oracle Next Education (ONE)**.
