# 🌍 Predicción de la Calidad del Agua (WB_CLEAR)

Este proyecto utiliza datos del Banco Mundial sobre la **calidad del agua (nutrientes y sales)** para realizar un análisis exploratorio y desarrollar modelos de machine learning que permitan **predecir el estado del agua por país**.

## 📁 Datos utilizados

- Dataset base: `WB_CLEAR_WIDEF.csv`
- Fuente: [World Bank – CLEAR dataset](https://databank.worldbank.org/source/climate-economic-analysis-for-resilience)
- Año de referencia: **2020**
- Indicador principal: `Water quality - nutrients, salts range`  
  *(Valores negativos indican peor calidad del agua)*

### 🧾 Descripción de columnas

| Nombre de columna       | Descripción                                                                 |
|-------------------------|------------------------------------------------------------------------------|
| `FREQ`                  | Código de frecuencia de la observación (por ejemplo, A = Anual)             |
| `FREQ_LABEL`            | Etiqueta de frecuencia (por ejemplo, "Annual")                              |
| `REF_AREA`              | Código ISO del país (por ejemplo, ARG = Argentina)                          |
| `REF_AREA_LABEL`        | Nombre completo del país                                                     |
| `INDICATOR`             | Código del indicador utilizado internamente                                 |
| `INDICATOR_LABEL`       | Descripción completa del indicador (aquí siempre refiere a calidad de agua) |
| `URBANISATION`          | Código de urbanización (por ejemplo, _T = Total)                             |
| `URBANISATION_LABEL`    | Etiqueta de urbanización (por ejemplo, Total, Urbano, Rural)                |
| `UNIT_MEASURE`          | Código de la unidad de medida (por ejemplo, WQ_RANGE)                        |
| `UNIT_MEASURE_LABEL`    | Descripción de la unidad de medida                                           |
| `DATABASE_ID`           | ID de la base de datos que provee la información                            |
| `DATABASE_ID_LABEL`     | Nombre de la base de datos (por ejemplo, CLEAR – Climate and Economic...)   |
| `UNIT_MULT`             | Multiplicador de unidad (generalmente 0 = unidades base)                    |
| `UNIT_MULT_LABEL`       | Etiqueta del multiplicador                                                   |
| `COMMENT_OBS`           | Comentarios sobre la observación (por ejemplo, rango de valores)            |
| `OBS_STATUS`            | Código del estado de la observación                                          |
| `OBS_STATUS_LABEL`      | Descripción del estado (por ejemplo, "Normal value")                         |
| `OBS_CONF`              | Código de nivel de confianza                                                 |
| `OBS_CONF_LABEL`        | Descripción del nivel de confianza (por ejemplo, "Public")                   |
| `2020`                  | **Valor de calidad del agua para el año 2020** (más negativo = peor calidad) |

## 🎯 Objetivos

1. Visualizar la distribución de la calidad del agua en el mundo.
2. Identificar los países con peor situación hídrica.
3. Enriquecer el dataset con variables socioeconómicas externas (PBI, poblacion, etc.).
4. Entrenar modelos de machine learning para predecir la calidad del agua.
5. Evaluar qué factores influyen más en la calidad del recurso hídrico.



## 💡 Preguntas guía para estudiantes

- ¿Qué regiones presentan los mayores niveles de contaminación hídrica?
- ¿Qué limitaciones tiene este análisis?

## 🛠 Requisitos

- Python 3.x
- pandas, numpy, matplotlib, seaborn, scikit-learn
- plotly (para mapas interactivos)

## 📌 Autor

Valentin Barco

