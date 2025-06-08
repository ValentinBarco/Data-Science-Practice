# 🔬 Clasificación de Lesiones Gastrointestinales a partir de Videos Colonoscópicos

Este ejercicio está basado en un conjunto de datos reales que contiene características extraídas de videos colonoscópicos. El objetivo es construir un modelo de machine learning capaz de predecir si una lesión gastrointestinal debe ser resecada o no, utilizando información obtenida mediante dos tipos de iluminación: luz blanca (WL) y narrow-band imaging (NBI).

---

## 📄 Descripción del Dataset

Cada una de las 76 lesiones fue registrada dos veces (una con luz blanca y otra con NBI), y se extrajeron **1396 características por lesión**:

- **Textura (2D):**  
  - 166 AHT (Gabor invariantes)  
  - 256 LBP rotacionalmente invariantes

- **Color (2D):**  
  - 16 Color Naming  
  - 13 Discriminative Color  
  - 7 Hue  
  - 7 Opponent  
  - 33 Color Gray-Level Co-occurrence Matrix

- **Forma (3D):**  
  - 100 shapeDNA  
  - 100 KPCA

📌 Cada archivo contiene:
- Fila 1: nombre de la lesión
- Fila 2: tipo de lesión (`1 = hiperplásica`, `2 = serrated`, `3 = adenoma`)
- Fila 3: tipo de luz (`1 = WL`, `2 = NBI`)
- A partir de la fila 4: vectores de características (698 por cada tipo de luz)

---

## 🎯 Objetivo del Ejercicio

Construir un modelo de clasificación supervisada que determine si una lesión requiere **resección (maligna)** o **no requiere resección (benigna)**.

### Clases:
- `0`: Hiperplásica (benigna – no se reseca)
- `1`: Adenoma o Serrated Adenoma (maligna – se reseca)

---

## 🧪 Actividades

### ✅ 1. Exploración de Datos
- Cargar el dataset y verificar las dimensiones
- Revisar el balanceo de clases
- Visualizar patrones con PCA o t-SNE

### ✅ 2. Preparación del Dataset
- Concatenar las características WL + NBI (1396 features por lesión)
- Crear una columna de clase binaria
- Normalizar o escalar las características

### ✅ 3. Entrenamiento del Modelo
- Modelos sugeridos:
  - Random Forest
  - SVM
  - XGBoost
  - Logistic Regression
- Validación: **Leave-One-Out Cross Validation (LOOCV)**

### ✅ 4. Evaluación
- Calcular las siguientes métricas:
  - **Accuracy**
  - **Sensibilidad (Recall)** – importante minimizar falsos negativos
  - **Especificidad**
  - **Matriz de confusión**
  - **AUC-ROC**

### ✅ 5. Interpretación de Resultados
- ¿Qué modelo obtuvo mejor rendimiento?
- ¿Qué errores son más comunes?
- ¿Cuál es la implicancia clínica de cada tipo de error?

---

## 📈 Comparación con Resultados Humanos

Podés usar el archivo `ground_truth.xlsx` para comparar tu modelo con las predicciones de médicos:

- 4 médicos expertos
- 3 médicos principiantes
- Resultados histopatológicos

📌 Extra: comparar sensibilidad/especificidad del modelo contra humanos.

---

## 💡 Extensiones Opcionales

- Realizar clasificación multiclase (`hiperplásica`, `adenoma`, `serrated`)
- Evaluar la importancia de cada tipo de características (textura, color, forma)
- Aplicar reducción de dimensionalidad con PCA o `SelectKBest`

---

## 🧠 Preguntas para Reflexionar

- ¿Qué implicancia clínica tiene un falso negativo?
- ¿Es mejor un modelo con alta sensibilidad o alta especificidad en este caso?
- ¿Conviene entrenar modelos por separado para WL y NBI?

---

