# Clasificación de Tweets durante el COVID-19 (Text Mining)

Este proyecto aplica **técnicas de Text Mining y Machine Learning** para clasificar tweets publicados durante la pandemia de COVID-19, determinando si mencionan o no una **profesión**.

---

## 📂 Dataset

- Archivo: `Twits_Profesion.csv`
- Contenido: Tweets recolectados durante la pandemia de COVID-19.
- Etiquetas: Indican si el tweet hace referencia a una profesión (`profesión`) o no (`no_profesión`).

---

## 🛠️ Metodología

1. **Preprocesamiento de Texto**
   - Eliminación de stopwords, caracteres especiales y URLs.
   - Normalización de texto (minúsculas, lematización/stemming).
   - Tokenización.

2. **Extracción de Características**
   - Representación mediante **TF-IDF** y/o **Bag of Words**.
   - Posible uso de embeddings (Word2Vec, FastText, BERT).

3. **Modelado**
   - Entrenamiento de modelos supervisados:
     - **Naive Bayes**
     - **Logistic Regression**
     - **Random Forest**
     - **SVM**
   - Comparación de desempeño entre modelos.

4. **Evaluación**
   - Métricas utilizadas:
     - Accuracy
     - Precision
     - Recall
     - F1-score
   - Validación cruzada sobre el dataset.

---

## 📊 Resultados Esperados

- Identificación automática de si un tweet menciona una profesión.
- Métricas comparativas para cada modelo entrenado.
- Posible despliegue de un clasificador en un notebook o aplicación ligera.

---

