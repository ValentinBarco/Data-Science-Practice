# 📧 Clasificación de Correos Electrónicos como SPAM o NO SPAM

Este ejercicio utiliza el dataset **Spambase** para construir un modelo de machine learning que identifique si un correo electrónico es spam o no, en base a su contenido textual.

---

## 📁 Descripción del Dataset

Cada fila del dataset representa un correo electrónico. El objetivo es predecir si fue clasificado como **spam (1)** o **no spam (0)**.

### 🔢 Estructura de los Datos

- **48 atributos** `word_freq_X`: Porcentaje de palabras que coinciden con la palabra `X`.  
- **6 atributos** `char_freq_X`: Porcentaje de caracteres que coinciden con el caracter `X`.
- **3 atributos relacionados a mayúsculas**:
  - `capital_run_length_average`
  - `capital_run_length_longest`
  - `capital_run_length_total`
- **1 atributo objetivo**:
  - `spam`: valor `1` si es spam, `0` si es correo legítimo.

---

## 🎯 Objetivo del Ejercicio

Construir un modelo de **clasificación binaria** para detectar correos no deseados (spam) aplicando técnicas de machine learning.

---

## 🧪 Actividades Sugeridas

### 1. Exploración de Datos
- Visualización de la distribución de la clase `spam`
- Análisis de correlación entre variables

### 2. Preprocesamiento
- Detección y tratamiento de valores faltantes
- Normalización si es necesaria

### 3. Entrenamiento de Modelos
- División del dataset en training y test (por ejemplo 80/20)
- Entrenamiento con al menos dos modelos:
  - Regresión logística
  - Árboles de decisión o Random Forest
  - Naive Bayes
  - k-Nearest Neighbors
  - Redes neuronales (opcional)

### 4. Evaluación
- Matriz de confusión
- Métricas: precisión, recall, F1-score
- Análisis de importancia de variables

---

## 📚 Recursos

- Dataset: [Spambase - UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/spambase)
- Lectura recomendada:  
  *Cranor, L.F. & LaMacchia, B.A. (1998). “Spam!” Communications of the ACM, 41(8):74-83.*

---

## ⚠️ Consideraciones

- Evitar falsos positivos es clave: marcar un correo válido como spam puede ser muy problemático.
- Algunas palabras como `george` o números como `650` pueden estar asociadas a correos legítimos por cómo se construyó el dataset.



