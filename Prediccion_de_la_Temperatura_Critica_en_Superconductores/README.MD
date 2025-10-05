# 🧪 Superconductors Critical Temperature Prediction

Este proyecto utiliza datos de **21.263 superconductores** con **81 propiedades físico-químicas** para predecir su **temperatura crítica (Tc)** —la temperatura por debajo de la cual el material se vuelve superconductor.

---

## 📂 Dataset

El dataset está compuesto por dos archivos principales:

| Archivo       | Descripción |
|---------------|-------------|
| `train.csv`   | Contiene 81 features para cada superconductor, más la temperatura crítica en la columna 82. |
| `unique_m.csv` | Incluye la fórmula química desglosada de cada material. Las últimas dos columnas contienen la Tc y la fórmula original. |

📌 **Cantidad de instancias:** 21.263  
📌 **Cantidad de features numéricos:** 81  
📌 **Variable objetivo:** `critical_temperature` (regresión)  
📌 **Valores faltantes:** No reportados  

---

## 🧠 Objetivo del proyecto

Desarrollar un modelo de Machine Learning que **prediga la temperatura crítica (Tc)** de un superconductor a partir de sus propiedades físico-químicas, y analizar **qué factores influyen más en su comportamiento superconductor**.

---

## 🧩 Tareas posibles con este dataset

✔️ Modelos de **regresión supervisada** (Linear Regression, Random Forest, XGBoost, Redes Neuronales, etc.)  
✔️ **EDA** de propiedades físico-químicas  
✔️ **Feature Importance / Interpretabilidad científica**  
✔️ **Clusterización** para identificar familias de materiales similares  
✔️ **Diseño de nuevos materiales** simulando combinaciones extremas de features

---

## 📌 Referencia académica

> **A data-driven statistical model for predicting the critical temperature of a superconductor**  
> *K. Hamidieh (2018), Computational Materials Science*

Dataset original obtenido desde:  
🔗 http://supercon.nims.go.jp/index_en.html

---

## 🚀 Posibles extensiones

- Generar **ranking de materiales con mayor potencial para alta superconductividad**
- Crear un **recomendador de nuevos superconductores hipotéticos**
- Visualizar las fórmulas químicas de los materiales más prometedores