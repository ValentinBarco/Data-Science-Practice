# 🛢️ Segmentación Litológica y Detección de Reservorios

Este proyecto tiene como objetivo aplicar técnicas de análisis de datos y machine learning no supervisado sobre registros de pozo (well logs) para:

1. **Segmentar los tipos de suelo** según sus propiedades petrofísicas.
2. **Calcular propiedades derivadas clave**, como volumen de lutitas, porosidad efectiva y módulos elásticos.
3. **Identificar los segmentos con mayor potencial como reservorios de hidrocarburos**, tanto convencionales como no convencionales.

---

## 📌 Descripción general del flujo de trabajo

1. **Lectura y exploración del dataset** de registros de pozo.
2. **Segmentación litológica inicial** utilizando K-Means sobre variables como densidad aparente (RHOB), porosidad (NPHI) y gamma ray (GR).
3. **Cálculo de propiedades derivadas**, entre ellas:
   - Volumen de lutitas (Vsh)
   - Porosidad combinada (ΦND)
   - Velocidades sísmicas (Vp, Vs)
   - Módulos elásticos (E, G, K)
   - Impedancia acústica (Z) y reflectividad (R)
4. **Nueva segmentación** con las propiedades derivadas para identificar zonas con buena calidad de reservorio.
5. **Comparación y combinación de segmentaciones** para evaluar cuáles zonas presentan:
   - Alta porosidad
   - Bajo contenido de arcilla
   - Buena respuesta mecánica
   - Potencial productivo como reservorio
6. **Análisis final y visualización de intervalos favorables.**


## 🧠 Nivel de dificultad

**Media.**  
El desafío requiere encadenar distintos pasos: desde la segmentación de litologías hasta el cálculo de propiedades físicas complejas y una segunda segmentación basada en esos nuevos atributos. El análisis también requiere **criterio geológico** para interpretar correctamente los resultados y definir zonas favorables para explotación.

---

## 💼 Dataset

El dataset fue extraído de [Kaggle](https://www.kaggle.com/datasets/madhuraatmarambhagat/geological-logging-dataset/data) y contiene más de 18.000 mediciones de registros de pozo, utilizadas en la competencia FORCE 2020. Cada fila corresponde a un punto a lo largo de un pozo con valores de:
- GR (Gamma Ray)
- RHOB (Densidad aparente)
- NPHI (Porosidad por neutrones)
- PEF (Factor fotoeléctrico)
- DTC (Tiempo de tránsito sónico)
- DEPTH_MD (profundidad medida)

---

## ✅ Resultado esperado

- Una clasificación clara de los tipos de roca (lutitas, areniscas, calizas).
- Un conjunto de propiedades derivadas bien calculadas.
- Una identificación de al menos un **intervalo con potencial como reservorio**.
- Visualizaciones que respalden la interpretación (crossplots, curvas, perfiles por profundidad).
