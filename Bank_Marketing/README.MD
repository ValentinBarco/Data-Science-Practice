# 📊 Bank Marketing Dataset

Este proyecto utiliza datos de campañas de marketing directo realizadas por una entidad bancaria portuguesa, con el objetivo de **predecir si un cliente suscribirá (o no) un depósito a plazo fijo**.

---

## ✅ 1. Origen del Dataset

- **Creado por:**  
  Paulo Cortez (Universidad do Minho)  
  Sérgio Moro (ISCTE-IUL)  
  Año: 2012

- **Referencia académica:**  
  Moro, S., Laureano, R., & Cortez, P. (2011).  
  *Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology.*  
  European Simulation and Modelling Conference (ESM'2011), pp. 117–121.

---

## ✅ 2. Descripción General

Los datos provienen de campañas de marketing por teléfono. En muchos casos se realizaron múltiples intentos con el mismo cliente para determinar si contrataría o no un depósito a plazo.

Se incluyen **dos archivos**:

- **`bank-full.csv`**  
  - 45,211 registros  
  - Ordenados temporalmente (2008–2010)

- **`bank.csv`**  
  - 4,521 registros  
  - 10% del dataset completo, seleccionado aleatoriamente  
  - Útil para probar modelos más pesados (ej. SVM)

**Variable objetivo:**  
`y` → Indica si el cliente suscribió un depósito (`yes` / `no`)

---

## ✅ 3. Estructura del Dataset

**Total de atributos:** 16 variables explicativas + 1 variable objetivo.

### 📌 Variables de cliente:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 1  | age       | numérico  | Edad |
| 2  | job       | categórico | Tipo de empleo |
| 3  | marital   | categórico | Estado civil |
| 4  | education | categórico | Nivel educativo |
| 5  | default   | binario    | ¿Crédito en default? |
| 6  | balance   | numérico   | Balance anual promedio (€) |
| 7  | housing   | binario    | ¿Tiene crédito hipotecario? |
| 8  | loan      | binario    | ¿Tiene préstamo personal? |

### 📌 Variables del último contacto:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 9  | contact   | categórico | Medio de contacto |
| 10 | day       | numérico   | Día del último contacto |
| 11 | month     | categórico | Mes del contacto |
| 12 | duration  | numérico   | Duración del llamado (segundos) |

### 📌 Variables de historial de campaña:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 13 | campaign  | numérico  | N° de contactos en la campaña actual |
| 14 | pdays     | numérico  | Días desde el último contacto previo |
| 15 | previous  | numérico  | N° de contactos previos |
| 16 | poutcome  | categórico| Resultado de campaña anterior |

### ✅ Variable objetivo:
| Nº | Variable | Tipo   | Descripción |
|----|----------|--------|-------------|
| 17 | y        | binario| ¿Suscribió depósito a plazo? |

---

## ✅ 4. Tareas posibles con este dataset

✔️ Modelos de clasificación binaria  
✔️ Análisis exploratorio (EDA)  
✔️ Balanceo de clases  
✔️ Feature engineering  
✔️ Comparación de algoritmos (Logistic Regression, Random Forest, SVM, etc.)  
✔️ Métricas: Accuracy, ROC-AUC, Precision, Recall, F1

---

## ✅ 5. Valores faltantes

✅ No hay valores missing reportados.

---

## ✅ 6. Objetivo del problema

Desarrollar un modelo capaz de **predecir si un cliente contratará un depósito a plazo (`y = yes`)** a partir de sus datos personales, historial financiero y características de contacto.

---

Si querés una versión para filmina, Jupyter Notebook o presentación, avisame y te lo adapto al formato que necesites.
