# 🏦📊 Bank Marketing Dataset

Este proyecto utiliza datos de campañas de marketing directo realizadas por una entidad bancaria portuguesa, con el objetivo de **predecir si un cliente suscribirá (o no) un depósito a plazo fijo**.

---

## 🧾 1. Origen del Dataset

👤 **Creado por:**  
Paulo Cortez (Universidad do Minho)  
Sérgio Moro (ISCTE-IUL)  
📅 Año: 2012

📚 **Referencia académica:**  
Moro, S., Laureano, R., & Cortez, P. (2011).  
*Using Data Mining for Bank Direct Marketing: An Application of the CRISP-DM Methodology.*  
📍 European Simulation and Modelling Conference (ESM'2011), pp. 117–121.

---

## ☎️ 2. Descripción General

Los datos provienen de campañas de **marketing telefónico**.  
En muchos casos se realizaron múltiples intentos por cliente.

📂 Archivos disponibles:

- 📁 **`bank-full.csv`**  
  • 45,211 registros  
  • Ordenados entre 2008 y 2010

- 📁 **`bank.csv`**  
  • 4,521 registros  
  • Muestra aleatoria del 10%  
  • Útil para modelos más pesados (ej. SVM)

🎯 **Variable objetivo:**  
`y` → ¿Suscribió un depósito a plazo? (`yes` / `no`)

---

## 🧩 3. Estructura del Dataset

🧮 **Total de variables:** 16 predictoras + 1 objetivo

### 👤 Variables del cliente:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 1  | age       | 🔢 numérico  | Edad |
| 2  | job       | 🧑‍💼 categórico | Tipo de empleo |
| 3  | marital   | 💍 categórico | Estado civil |
| 4  | education | 🎓 categórico | Nivel educativo |
| 5  | default   | ⚠️ binario    | ¿Crédito en default? |
| 6  | balance   | 💶 numérico   | Balance anual promedio (€) |
| 7  | housing   | 🏠 binario    | ¿Tiene crédito hipotecario? |
| 8  | loan      | 💳 binario    | ¿Tiene préstamo personal? |

### 📞 Variables del último contacto:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 9  | contact   | ☎️ categórico | Medio de contacto |
| 10 | day       | 📆 numérico   | Día del último contacto |
| 11 | month     | 🗓️ categórico | Mes del contacto |
| 12 | duration  | ⏱️ numérico   | Duración del llamado (segundos) |

### 🔁 Historial de campaña:
| Nº | Variable  | Tipo      | Descripción |
|----|-----------|-----------|-------------|
| 13 | campaign  | 🔢 numérico  | Nº de contactos actuales |
| 14 | pdays     | 📉 numérico  | Días desde contacto anterior |
| 15 | previous  | 🔢 numérico  | Nº de contactos previos |
| 16 | poutcome  | 🎯 categórico| Resultado de campaña previa |

### 🎯 Variable objetivo:
| Nº | Variable | Tipo   | Descripción |
|----|----------|--------|-------------|
| 17 | y        | ✅ binario | ¿Suscribió depósito a plazo? |

---

## 🛠️ 4. Tareas posibles con este dataset

✔️ Modelos de clasificación binaria  
✔️ 🔍 Análisis exploratorio (EDA)  
✔️ ⚖️ Balanceo de clases  
✔️ 🏗️ Feature Engineering  
✔️ 🤖 Comparación de algoritmos (SVM, LR, RF, etc.)  
✔️ 📈 Métricas: Accuracy, ROC-AUC, Precision, Recall, F1

---

## 🔍 5. Valores faltantes

✅ No se reportan datos faltantes.

---

## 🎯 6. Objetivo del problema

Desarrollar un modelo capaz de **predecir si un cliente contratará un depósito a plazo (`y = yes`)** a partir de sus datos personales, historial financiero y características de contacto.

