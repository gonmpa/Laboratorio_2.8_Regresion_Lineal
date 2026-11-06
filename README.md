# Laboratorio 2.8: Modelos de Regresión Lineal Simple y Múltiple 📈

Este repositorio contiene el desarrollo del cuaderno de la **Actividad 2.8**, enfocado en la aplicación, evaluación y diagnóstico de modelos predictivos de **Regresión Lineal Simple y Múltiple**. El objetivo principal del proyecto no es solo obtener predicciones, sino evaluar críticamente la validez de los modelos mediante el análisis de residuos y pruebas de multicolinealidad.

## 🗂️ Estructura del Proyecto

El análisis se divide en dos grandes bloques prácticos utilizando conjuntos de datos extraídos automatizadamente desde Kaggle:

### Bloque 1: Regresión Lineal Simple (Breast Cancer Wisconsin)
Se entrenaron modelos bidimensionales para predecir características morfológicas de núcleos celulares.
* **Modelo 1 (Radio vs Perímetro):** Demostración de un ajuste lineal perfecto, validado por un $R^2$ de 0.99 y una dispersión aleatoria u homocedástica de los residuos.
* **Modelo 2 (Radio vs Área):** Un caso de estudio crítico. A pesar de tener un $R^2$ alto (0.98), el **análisis de residuos** reveló una forma parabólica (curvatura en U), demostrando empíricamente una violación al supuesto de linealidad (la relación real es cuadrática). 
* **Conclusión clave:** El $R^2$ por sí solo no garantiza la validez de un modelo; la inspección visual de los residuos es obligatoria.

### Bloque 2: Regresión Lineal Múltiple (FIFA 19 Player Stats)
Se construyó un modelo multidimensional para predecir el **Valor de Mercado** (`Value_num`) y el rendimiento general (`Overall`) de los jugadores basándose en múltiples atributos (Edad, Potencial, Salario, etc.).
* **Limpieza de Datos:** Transformación algorítmica de variables financieras en formato texto (ej. "€80M", "€450K") a valores numéricos continuos (flotantes).
* **Diagnóstico de Multicolinealidad:** Uso de la librería `statsmodels` para calcular el **Factor de Inflación de la Varianza (VIF)**, previniendo el *Data Leakage* y el solapamiento entre variables predictoras.
* **Análisis de Heterogeneidad:** Segmentación del rendimiento del modelo entre subgrupos (Arqueros vs Jugadores de Campo), demostrando cómo el contexto del negocio (rol táctico) afecta la precisión algorítmica.

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3
* **Manipulación de Datos:** `pandas`, `numpy`
* **Modelamiento Automático (Machine Learning):** `scikit-learn` (`LinearRegression`, `train_test_split`, `r2_score`, `mean_absolute_error`, `mean_squared_error`)
* **Estadística Avanzada:** `statsmodels` (Cálculo de VIF)
* **Visualización:** `matplotlib`, `seaborn`
* **Descarga de Datos:** `kagglehub`

## 🚀 Cómo ejecutar este proyecto

1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/gonmpa/Laboratorio_2.8_Regresion_Lineal.git](https://github.com/gonmpa/Laboratorio_2.8_Regresion_Lineal.git)
