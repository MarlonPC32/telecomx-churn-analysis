# Telecom X — Análisis de Evasión de Clientes (Churn)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![pandas](https://img.shields.io/badge/pandas-data-green)
![matplotlib](https://img.shields.io/badge/matplotlib-viz-yellow)
![Jupyter](https://img.shields.io/badge/Jupyter-notebook-orange)

Exploratory data analysis of customer churn for Telecom X using Python.

> Companion to **[telecomx-churn-prediction](https://github.com/MarlonPC32/telecomx-churn-prediction)**, where this analysis feeds a full ML pipeline (Logistic Regression, Random Forest).

## Descripción del Proyecto

En este proyecto trabajé analizando el problema de evasión de clientes (Churn) en Telecom X. La empresa enfrenta una tasa considerable de cancelación de servicios y el objetivo principal fue entender qué factores influyen en que los clientes decidan irse.

Realicé un proceso completo de análisis de datos: extracción de la información, limpieza y transformación, y análisis exploratorio para identificar patrones y comportamientos relevantes.

La idea es generar insights que ayuden a la empresa a tomar decisiones más informadas para reducir la evasión.

## Tecnologías Utilizadas

- Python
- Pandas
- Matplotlib
- Seaborn
- Google Colab

## Proceso del Análisis

### 1. Extracción de datos

Los datos fueron obtenidos desde una API en formato JSON.

### 2. Limpieza y transformación de datos

- Normalización de columnas anidadas
- Conversión de variables al tipo de dato adecuado
- Revisión y manejo de valores nulos
- Creación de variables derivadas (ej. `Cuentas_Diarias`) para facilitar el análisis

### 3. Análisis exploratorio de datos

- Distribución general de clientes con churn vs. clientes que permanecen
- Comparación de churn según variables categóricas
- Exploración de variables numéricas relacionadas con el comportamiento de los clientes

### 4. Visualización de datos

Gráficos de barras, diagramas de caja (boxplots) y mapas de correlación para identificar tendencias y relaciones entre variables.

## Principales Insights

- Los clientes con contratos de corto plazo muestran mayor tendencia a cancelar
- Los clientes con menor tiempo de permanencia tienen mayor probabilidad de churn
- Existen diferencias entre métodos de pago asociadas con la evasión
- El gasto mensual muestra comportamientos distintos entre clientes que permanecen y los que cancelan

## Recomendaciones

- Incentivar contratos de mayor duración para mejorar la retención
- Desarrollar estrategias de fidelización enfocadas en clientes nuevos
- Analizar con mayor profundidad los métodos de pago relacionados con churn
- Explorar modelos predictivos que identifiquen clientes en riesgo antes de que cancelen → ver [telecomx-churn-prediction](https://github.com/MarlonPC32/telecomx-churn-prediction)

## Cómo ejecutar el proyecto

```bash
pip install pandas matplotlib seaborn
```

Abrir `TelecomX_Churn_Analysis.ipynb` en Jupyter o Google Colab y ejecutar las celdas en orden.

## Autor

**Marlon P. Crespo** — proyecto realizado como parte del desafío **Telecom X – Análisis de Datos** del programa **Oracle Next Education (ONE)**.
[LinkedIn](https://www.linkedin.com/in/marlonpc)
