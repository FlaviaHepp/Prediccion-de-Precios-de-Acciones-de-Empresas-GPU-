# 📈Predicción de Precios de Acciones de Empresas GPU con Econometría y Deep Learning

Este proyecto realiza un análisis integral de series temporales financieras y predicción del precio de cierre de acciones de las principales empresas del sector GPU, combinando modelos econométricos tradicionales y modelos de Deep Learning.

El estudio se centra principalmente en NVIDIA, y luego se extiende a un análisis comparativo con AMD, ASUS, INTEL y MSI.

## 🎯Objetivos del proyecto

- Analizar el comportamiento histórico del precio de las acciones de NVIDIA.
- Evaluar la estacionariedad de la serie temporal.
- Aplicar modelos econométricos clásicos (ARIMA).
- Implementar modelos de Machine Learning y Deep Learning:
- MLP (Red Neuronal Multicapa)
- RNN (Red Neuronal Recurrente)
- LSTM (Long Short-Term Memory)
- Comparar el desempeño de distintos enfoques de predicción.
- Extender el análisis a múltiples empresas del sector GPU.
- Exportar resultados de predicción para análisis posterior.

## 📁Conjunto de datos

Empresas analizadas:
- NVIDIA (1999–2023)
- AMD (1980–2023)
- ASUS (2000–2023)
- INTEL (1980–2023)
- MSI (2023–2024)

Variables principales:
- Open
- High
- Low
- Close
- Volume

Los datos corresponden a precios históricos diarios de acciones.

## 🔎Análisis exploratorio (EDA)

- Análisis descriptivo estadístico.
- Detección de valores nulos.
- Visualización de precios históricos y volúmenes.
- Análisis de correlación entre variables financieras.
- Histogramas y distribuciones.

## ⏱️Estacionariedad de la serie

- Se aplican dos pruebas estadísticas fundamentales:
- ADF (Augmented Dickey-Fuller)
- KPSS (Kwiatkowski–Phillips–Schmidt–Shin)
- Los resultados confirman que la serie original no es estacionaria, por lo que se aplican diferenciaciones para habilitar el uso de modelos ARIMA.

## 📉Modelado econométrico: ARIMA

- Análisis de ACF y PACF para determinar los parámetros del modelo.
- Modelo ajustado sobre el conjunto de entrenamiento.
- Pronóstico fuera de muestra.
- Análisis de residuos y validación del modelo.
- Visualización de valores reales vs. predichos.

## 🤖Modelos de Machine Learning y Deep Learning
🔹 MLP (Red Neuronal Multicapa)

- Selección automática del lookback usando PACF.
- Entrenamiento supervisado univariado.
- Evaluación con múltiples métricas.

🔹 RNN (Red Neuronal Recurrente)

- Modelado secuencial de dependencias temporales.
- Early stopping para evitar overfitting.
- Comparación visual entre valores reales y predichos.

🔹 LSTM

- Arquitectura profunda con memoria de largo plazo.
- Captura de dependencias temporales complejas.
- Mejor desempeño en escenarios no lineales.

## 📊Métricas de evaluación

Se utilizan métricas estándar para series temporales financieras:

- R²
- MAE
- MSE
- RMSE
- NRMSE
- WMAPE
- MAPE

Esto permite una comparación objetiva entre modelos.

## 🏢Análisis multiactivo (GPU Companies)

Para AMD, ASUS, INTEL, MSI y NVIDIA se implementa:

Regresión lineal multivariada usando:
- Open
- High
- Low
- Volume
- Evaluación individual por empresa.
- Visualización comparativa de precios históricos.
- Exportación de predicciones a archivos CSV.

## 🛠️Tecnologías utilizadas

- Python
- pandas / numpy
- matplotlib / seaborn
- statsmodels
- scikit-learn
- TensorFlow / Keras

## 📂Estructura del proyecto

├── 1.py
├── datasets/
│   ├── NVIDIA (1999 - 2023).csv
│   ├── AMD (1980 - 2023).csv
│   ├── ASUS (2000 - 2023).csv
│   ├── INTEL (1980 - 2023).csv
│   └── MSI (2023 - 2024).csv
├── outputs/
│   ├── AMD_Close_Prediction.csv
│   ├── ASUS_Close_Prediction.csv
│   ├── INTEL_Close_Prediction.csv
│   ├── MSI_Close_Prediction.csv
│   └── NVIDIA_Close_Prediction.csv
└── README.md


## 📌Resultados clave

- Los modelos clásicos (ARIMA) capturan bien la tendencia de corto plazo.
- Los modelos LSTM y RNN capturan mejor las no linealidades.
- NVIDIA presenta alta dependencia temporal y fuerte estructura secuencial.
- El enfoque híbrido permite comparar interpretabilidad vs. performance.

## ⚠️Disclaimer

Este proyecto es educativo y demostrativo.
No constituye asesoramiento financiero ni recomendaciones de inversión.

## 👤Autor

Flavia Hepp
Data Science en formación· Econometría · Machine Learning · Finanzas
