# Zuber: Análisis de Viajes en Chicago

Este proyecto practicum consiste en un análisis de datos para **Zuber**, una nueva empresa de viajes compartidos que se lanza en Chicago. El objetivo principal es comprender las preferencias de los pasajeros y el impacto de factores externos, como el clima, en los viajes.

## 🎯 Objetivos del Proyecto

*   Identificar las 10 empresas de taxis con mayor número de viajes en Chicago.
*   Determinar los barrios más populares como destinos finales de viajes.
*   Probar la hipótesis de que la duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare cambia en los sábados lluviosos.

## 📊 Descripción de los Datasets

El proyecto utiliza tres conjuntos de datos principales:

1.  **`project_sql_result_01.csv`**:
    *   `company_name`: nombre de la empresa de taxis.
    *   `trips_amount`: el número de viajes para cada empresa de taxis el 15 y 16 de noviembre de 2017.
2.  **`project_sql_result_04.csv`**:
    *   `dropoff_location_name`: barrios de Chicago donde finalizaron los viajes.
    *   `average_trips`: el promedio de viajes que terminaron en cada barrio en noviembre de 2017.
3.  **`project_sql_result_07.csv`**: Datos sobre viajes desde el Loop hasta el Aeropuerto O'Hare.
    *   `start_ts`: fecha y hora de la recogida.
    *   `weather_conditions`: condiciones climáticas en el momento en el que comenzó el viaje.
    *   `duration_seconds`: duración del viaje en segundos.

## 🛠️ Herramientas Utilizadas

*   **Python 3**
*   **Pandas**: Para la manipulación y limpieza de datos.
*   **Matplotlib & Seaborn**: Para la creación de visualizaciones estéticas e informativas.
*   **Scipy**: Específicamente el módulo `stats` para realizar pruebas de hipótesis estadísticas.

## 🚀 Flujo de Trabajo

### 1. Análisis Exploratorio de Datos (EDA)
Se analizaron los datos de las empresas y barrios para identificar patrones de demanda.
*   Se identificó a **Flash Cab** como la empresa líder con una diferencia significativa sobre la competencia.
*   El barrio **Loop** resultó ser el destino más frecuente, seguido de River North y Streeterville.

### 2. Visualización de Datos
Se crearon gráficos de barras para representar visualmente el Top 10 de empresas por cantidad de viajes y el Top 10 de barrios por promedio de llegadas.

### 3. Prueba de Hipótesis
Se realizó una prueba t de Student independiente para comparar la duración de los viajes en diferentes condiciones climáticas.
*   **Hipótesis Nula (H₀)**: La duración promedio de los viajes desde el Loop hasta el Aeropuerto Internacional O'Hare es la misma en los sábados lluviosos que en los sábados de buen clima.
*   **Hipótesis Alternativa (H₁)**: La duración promedio de los viajes difiere según las condiciones climáticas.

## 💡 Conclusiones Principales

1.  **Dominio de Mercado**: Flash Cab domina el mercado de taxis en Chicago durante el periodo analizado.
2.  **Concentración Urbana**: La actividad de viajes se concentra fuertemente en el centro financiero y turístico (Loop, River North).
3.  **Impacto del Clima**: Se rechazó la hipótesis nula, concluyendo que **el clima lluvioso aumenta significativamente la duración de los viajes**, probablemente debido al tráfico y las condiciones de la carretera.

## ⚙️ Cómo Ejecutar
1. Clone este repositorio.
2. Asegúrese de tener instaladas las dependencias: `pip install pandas matplotlib seaborn scipy`.
3. Ejecute el notebook `Recopilacion y Almacenamiento de Datos.ipynb` en un entorno de Jupyter.

---
*Proyecto desarrollado como parte del bootcamp de análisis de datos de TripleTen.*
