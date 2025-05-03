
## Subterráneos de la Ciudad Autónoma de Buenos Aires.

![Plano](/PlanoSubte2025.png.png)

**Análisis y Predicción del Sistema de Subterráneos de Buenos Aires**

Este proyecto tiene como objetivo el análisis exploratorio y predictivo del sistema de subterráneos de la Ciudad Autónoma de Buenos Aires, mediante la recopilación, limpieza, visualización y modelado de diversos conjuntos de datos relacionados con estaciones, líneas, accesibilidad, cantidad de viajes y precios históricos del boleto.

**Estructura del Proyecto**

El proyecto está estructurado en distintos notebooks y archivos que agrupan el análisis de datos, los conjuntos de datos (tanto originales como procesados), los modelos de predicción entrenados y las visualizaciones generadas durante el desarrollo.
Esta estructura permite mantener el flujo de trabajo ordenado, reutilizable y fácilmente escalable.

**Datasets Suministrados por el Cliente**

Para el desarrollo del presente análisis, el cliente proporcionó un conjunto de bases de datos clave que permiten estudiar el comportamiento histórico del sistema de subterráneos de la Ciudad Autónoma de Buenos Aires. A continuación se detalla cada uno de los archivos entregados:

**historico_2014.csv**
Contiene registros detallados de viajes validados por estación, molinete, franja horaria y tipo de pasajero (boleto pago, pase, franquicia, etc.) correspondientes al año 2014.
Este dataset es la base central para el análisis de patrones de uso y para los modelos de predicción.

**lineas-de-subte.csv**
Contiene información sobre la longitud (en wkt) de cada línea de subte, permitiendo incorporar una dimensión física al análisis del transporte y generar métricas normalizadas (por ejemplo, pasajeros por kilómetro).

**viajes_anual.csv**
Presenta estadísticas anuales agregadas por línea, incluyendo el total de viajes validados por año. Es útil para el análisis de tendencias a largo plazo y la comparación interanual entre líneas.

**estaciones-accesibles.csv**
Enumera las estaciones que cuentan con infraestructura de accesibilidad (como ascensores, rampas, etc.), permitiendo realizar análisis diferenciados del uso entre estaciones accesibles y no accesibles, así como su evolución a lo largo del tiempo.

**registro-historico-del-precio-del-boleto.csv**
Incluye el historial de tarifas del boleto de subte, con fechas de aplicación y valores correspondientes. Es clave para analizar la relación entre incrementos tarifarios y la demanda del servicio.


**Orden de Ejecución de los Notebooks**

A continuación, se detalla el orden sugerido en que deben ejecutarse los notebooks para garantizar una correcta carga, análisis y modelado de los datos:

1.	<u>1 ANALISIS_Precio_Boleto.ipynb</u>
Análisis del histórico de precios del boleto, comportamiento tarifario y su posible impacto en la demanda.

2.	<u>2 ANALISIS_viajes_anual.ipynb</u>
Evaluación de la evolución de los viajes anuales por línea, con visualización de tendencias y picos.

3.	<u>3 ANALISIS_PREDICCIONES_lineas-de-subte.ipynb</u>
Modelado y predicción del comportamiento de cada línea utilizando técnicas de regresión y clasificación.

4.	<u>4 ANALISIS_PREDICCIONES_estaciones_accesibles.ipynb</u>
Estudio comparativo de las estaciones accesibles y su impacto en la cantidad de pasajeros.

5.	<u>5 PLANO_estaciones_accesibles.ipynb</u>
Generación de mapas interactivos con la ubicación de estaciones accesibles utilizando Folium.

6.	<u>6 ANALISIS_PREDICCIONES_BaseUnificadaEstaciones.ipynb</u>
Integración de variables en una base unificada para su análisis global por estación.

7.	<u>7 ANALISIS_PREDICCIONES_estaciones.ipynb</u>
Análisis detallado por estación con modelos de predicción para distintos escenarios.

8.	<u>8 ANALISIS_PREDICCIONES_historico_2014.ipynb</u>
Estudio específico del histórico 2014 utilizando series temporales y regresiones clásicas.

9.	<u>9 DeepLearning_historico_2014.ipynb</u>
Aplicación de redes neuronales (MLP, GRU, CNN, LSTM) para predicción avanzada de demanda de pasajeros.


**Árbol de Archivos del Proyecto**

A continuación se presenta la estructura del proyecto en formato de árbol, organizada por carpetas temáticas:

proyecto-subte/
├── README.md                          # Documentación principal del proyecto
├── notebooks/                         # Notebooks de análisis y modelado
│   ├── 1 ANALISIS_Precio_Boleto.ipynb
│   ├── 2 ANALISIS_viajes_anual.ipynb
│   ├── 3 ANALISIS_PREDICCIONES_lineas-de-subte.ipynb
│   ├── 4 ANALISIS_PREDICCIONES_estaciones_accesibles.ipynb
│   ├── 5 PLANO_estaciones_accesibles.ipynb
│   ├── 6 ANALISIS_PREDICCIONES_BaseUnificadaEstaciones.ipynb
│   ├── 7 ANALISIS_PREDICCIONES_estaciones.ipynb
│   ├── 8 ANALISIS_PREDICCIONES_historico_2014.ipynb
│   └── 9 DeepLearning_historico_2014.ipynb
├── data/                              # Conjuntos de datos originales y procesados
│   ├── df2014.csv
│   ├── df2014DL.csv
│   ├── dfentrenamiento2014.csv
│   ├── dftarifa.csv
│   ├── historico_2014.csv
│   ├── lineas-de-subte.csv
│   ├── Longitud_Lineas.csv
│   ├── viajes_anual.csv
│   ├── estaciones-accesibles.csv
│   ├── registro-historico-del-precio-del-boleto.csv
├── modelos/                           # Modelos entrenados
│   └── gru_model.h5
├── visualizaciones/                  # Gráficos y mapas generados
│   ├── temporal_correlation.png
│   ├── temporal_patterns.png
│   ├── temporal_predictions.png
│   ├── training_history_rnn.png
│   └── mapa_accesibilidad_subte_bsas.html


**Notebooks Generados**
	•	1 ANALISIS_Precio_Boleto.ipynb
	•	2 ANALISIS_viajes_anual.ipynb
	•	3 ANALISIS_PREDICCIONES_lineas-de-subte.ipynb
	•	4 ANALISIS_PREDICCIONES_estaciones_accesibles.ipynb
	•	5 PLANO_estaciones_accesibles.ipynb
	•	6 ANALISIS_PREDICCIONES_BaseUnificadaEstaciones.ipynb
	•	7 ANALISIS_PREDICCIONES_estaciones.ipynb
	•	8 ANALISIS_PREDICCIONES_historico_2014.ipynb
	•	9 DeepLearning_historico_2014.ipynb


**Archivos de Datos y Resultados**
	•	df2014.csv, df2014DL.csv, dfentrenamiento2014.csv
	•	dftarifa.csv, historico_2014.csv
	•	lineas-de-subte.csv, Longitud_Lineas.csv, viajes_anual.csv
	•	registro-historico-del-precio-del-boleto.csv, estaciones-accesibles.csv
	•	Visualizaciones: temporal_correlation.png, temporal_patterns.png, temporal_predictions.png, training_history_rnn.png
	•	Mapa interactivo: mapa_accesibilidad_subte_bsas.html
	•	Modelo entrenado: gru_model.h5



**Herramientas Utilizadas**
	•	Lenguajes de Programación: Python, HTML
	•	Notebook: Visual Studio Code
	•	Hardware: MacBook Air M4 (24GB RAM) 10-Core CPU / 10-Core GPU

Bibliotecas Python Utilizadas
	•	Análisis de Datos: Pandas, NumPy
	•	Visualización y Análisis Geoespacial: Matplotlib, Seaborn, Plotly, Folium, Shapely
	•	Estadística: SciPy, Statsmodels
	•	Machine Learning: Scikit-learn, XGBoost
	•	Deep Learning: TensorFlow, Keras


**Pasos**

1. **Limpieza y Preparación de Datos**

Se unificaron y transformaron datos de distintas fuentes:
	•	Registros históricos del precio del boleto
	•	Cantidad de viajes anuales por línea
	•	Información sobre accesibilidad en estaciones
	•	Series temporales del período 2014–2021

Procesos realizados:
	•	Conversión de formatos de fecha y hora
	•	Normalización y homogeneización de nombres de estaciones y líneas
	•	Relleno y eliminación de valores faltantes
	•	Unificación de datasets en una base centralizada



2. **Análisis Exploratorio de Datos (EDA)**

Se identificaron patrones de comportamiento, correlaciones, tendencias temporales, y agrupamientos. Se utilizaron múltiples visualizaciones para facilitar la interpretación de datos:
	•	Evolución del precio del boleto a lo largo del tiempo
	•	Comparativa de uso de estaciones accesibles vs no accesibles
	•	Mapa interactivo de estaciones accesibles
	•	Ranking de líneas y estaciones con mayor y menor tráfico de pasajeros
	•	Análisis temporal de viajes y horas picos de uso



3. **Modelos de Predicción Tradicionales**

Se aplicaron múltiples modelos de predicción, seleccionados según la naturaleza de los datos y los objetivos analíticos:

Modelos aplicados:
	•	KMeans: detección de clusters de comportamiento
	•	Regresión Lineal y Ridge: predicción de cantidad de viajes
	•	Regresión Logística: clasificación binaria de accesibilidad
	•	Random Forest Regressor y Decision Tree Regressor: predicción no lineal y análisis de importancia de variables
	•	XGBoost (XGBRegressor, XGBRFRegressor): predicción robusta y eficiente
	•	SVR: soporte vectorial para regresión
	•	ARIMA: predicción de series temporales de viajes y tarifas

Cada modelo fue evaluado con métricas como R², RMSE y MAE. Se presentan comparativas gráficas de predicciones vs valores reales.



4. **Deep Learning**

Para abordar secuencias temporales complejas y comportamiento histórico, se implementaron modelos de redes neuronales:

Modelos de Deep Learning utilizados:
	•	MLP (Perceptrón Multicapa): aproximación inicial
	•	CNN: extracción de patrones espaciales y temporales
	•	LSTM: aprendizaje de dependencias a largo plazo
	•	GRU: versión optimizada de LSTM para datos históricos

Se entrenaron sobre el conjunto historico_2014.csv, obteniendo resultados satisfactorios en la predicción de la cantidad de pasajeros. Se presenta la evolución de la pérdida durante el entrenamiento (training_history_rnn.png) y visualizaciones de las predicciones.



5. **Porque estos modelos de Deep Learning utilizados son adecuados para el análisis del sistema de subterráneos:**

El análisis de demanda en un sistema de transporte subterráneo involucra grandes volúmenes de datos históricos, con patrones complejos, estacionales y no lineales. Además, la información puede verse influenciada por múltiples factores simultáneos: tarifas, estaciones accesibles, líneas, horarios pico, entre otros.

**Estos modelos permiten:**
	•	Capturar dependencias temporales complejas y no evidentes.
	•	Adaptarse a cambios de comportamiento o estacionalidad.
	•	Generalizar a situaciones nuevas sin necesidad de reglas explícitas.
	•	Mejorar la precisión en la predicción de la demanda, lo cual es clave para una mejor planificación y toma de decisiones.

**Modelos de Deep Learning Utilizados y Justificación**

Para abordar la predicción de patrones de uso y comportamiento en el sistema de subterráneos, se implementaron distintos modelos de Deep Learning, cada uno con ventajas particulares frente a los desafíos del problema:

	•	MLP (Perceptrón Multicapa)
Utilizado como punto de partida por su simplicidad y capacidad de aproximar funciones no lineales. Aunque no es óptimo para series temporales, permite establecer una línea base comparativa.

	•	CNN (Redes Neuronales Convolucionales)
Aplicadas para capturar patrones espaciales y temporales en los datos, especialmente útiles cuando se combinan variables estructurales (como estaciones o líneas) con variables temporales. Las CNN detectan automáticamente características relevantes sin necesidad de ingeniería manual de variables.

	•	LSTM (Long Short-Term Memory)
Diseñadas específicamente para modelar secuencias temporales largas y con dependencias a largo plazo, como las series de pasajeros por hora, día o mes. Son ideales para capturar la evolución de la demanda a lo largo del tiempo.

	•	GRU (Gated Recurrent Unit)
Variante simplificada y más eficiente de las LSTM. Mantiene una buena capacidad de modelado temporal con menor complejidad computacional, lo que lo convierte en un modelo ideal para implementaciones livianas o en entornos con recursos limitados.



6. **Visualizaciones Clave**
	•	Mapas interactivos (Folium) de accesibilidad en estaciones
	•	Gráficos temporales y de correlación de variables
	•	Predicciones de series temporales en gráficos comparativos
	•	Ranking dinámico de líneas y estaciones
	•	Análisis visual de comportamiento antes y después de subas de tarifa



7. **Conclusiones y Aclaraciones**

Para el desarrollo de este trabajo se utilizó el dataset correspondiente al histórico anual del año 2014. Este conjunto de datos sirvió como base para el análisis exploratorio, la visualización de patrones temporales y la implementación de diversos modelos de predicción, tanto tradicionales como basados en técnicas de deep learning.

Cabe destacar que la metodología, los procesos analíticos y los modelos desarrollados son perfectamente escalables y aplicables a los años posteriores. La única diferencia radica en la etapa de preparación de los datos, que puede requerir ajustes específicos dependiendo de la estructura del dataset correspondiente a cada año. Esto incluye la posible normalización de nombres de columnas (features), tratamiento de datos faltantes o duplicados, y la detección y corrección de outliers.

Este enfoque garantiza la flexibilidad y adaptabilidad del modelo ante nuevos datos, manteniendo la coherencia del análisis y la validez de las predicciones en distintos períodos históricos.

Este proyecto permite entender de forma profunda el comportamiento del sistema de subte porteño. El uso de técnicas de machine learning y deep learning no solo facilita la predicción de uso futuro, sino también la toma de decisiones en cuanto a accesibilidad, tarifas y optimización de recursos.
.

