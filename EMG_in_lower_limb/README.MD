# 🦵 EMG Dataset in Lower Limb

Este ejercicio está basado en un conjunto de datos de electromiografía (EMG) de la pierna, que incluye registros de actividad muscular y goniometría durante distintos movimientos. Fue recolectado en sujetos sanos y con alteraciones de rodilla. Es ideal para trabajar procesamiento de señales, segmentación, extracción de características y clasificación.

---

## 📄 Descripción del Dataset

Cada archivo de datos contiene registros de señales EMG y goniometría para un sujeto realizando uno de los siguientes ejercicios:

- **Sitting** (sentarse o levantarse)
- **Standing** (mantenerse de pie)
- **Walking** (caminar)

Las señales fueron adquiridas a una frecuencia de muestreo de **1000 Hz** con 5 canales:

| Columna | Canal | Músculo / Medición      | Descripción                                         |
|---------|--------|--------------------------|-----------------------------------------------------|
| 0       | Ch1    | Rectus Femoris (RF)      | Señal EMG del músculo recto femoral                |
| 1       | Ch2    | Biceps Femoris (BF)      | Señal EMG del bíceps femoral                       |
| 2       | Ch3    | Vastus Medialis (VM)     | Señal EMG del vasto medial                         |
| 3       | Ch4    | Semitendinosus (ST)      | Señal EMG del semitendinoso                        |
| 4       | Ch5    | Goniometría (FX)         | Ángulo de la rodilla durante el movimiento         |

Cada archivo suele contener 5 repeticiones del mismo movimiento.

---

## 🧪 Ejercicios propuestos para el EMG Dataset in Lower Limb

### ✅ Ejercicio 1 - Visualización de señales  
**Objetivo**: familiarizarse con los datos crudos.

- Leer los archivos de señal por sujeto.  
- Graficar las señales EMG (Ch1–Ch4) y el canal de goniometría (Ch5).  
- Ver cómo cambian las señales entre ejercicios: sentarse, pararse y caminar.  
- Identificar visualmente las repeticiones de movimiento.  

📌 **Bonus**: marcar los picos de activación muscular y los ciclos articulares en la goniometría.

---

### ✅ Ejercicio 2 - Segmentación de eventos  
**Objetivo**: dividir las señales por repeticiones (ej. ciclos de marcha o flexiones).

- Usar el canal de goniometría (Ch5) para detectar ciclos de movimiento.  
- Crear ventanas de tiempo por repetición de movimiento.  
- Extraer segmentos por cada repetición de ejercicio por sujeto.  

📌 **Tip**: podés usar `scipy.signal.find_peaks()` para detectar transiciones.

---

### ✅ Ejercicio 3 - Extracción de características EMG  
**Objetivo**: transformar señales crudas en vectores útiles.

- Calcular features típicas por ventana:
  - RMS (root mean square)  
  - Media absoluta  
  - Varianza  
  - Willison Amplitude  
  - Zero Crossing Rate  
- Concatenar features por canal para representar cada repetición.  

📌 **Bonus**: comparar si hay diferencias entre sujetos sanos y con patologías.

---

### ✅ Ejercicio 4 - Clasificación de tipo de ejercicio  
**Objetivo**: identificar si la actividad fue caminar, sentarse o pararse.

- Etiquetar cada segmento con su clase (`sitting`, `standing`, `walking`)  
- Usar modelos como:
  - k-NN  
  - Random Forest  
  - SVM  
- Evaluar con matriz de confusión y F1-score.  

📌 **Extra**: aplicar reducción de dimensionalidad (PCA, t-SNE) para visualizar los clusters.

---

### ✅ Ejercicio 5 - Detección de sujetos con patología  
**Objetivo**: construir un clasificador para detectar alteraciones en sujetos.

- Agrupar sujetos en dos clases: **sanos** y **con alteraciones**  
- Usar los features EMG para entrenar un modelo  
- Evaluar si hay patrones claros que distinguen ambos grupos  

📌 **Discusión**: ¿qué músculos muestran más diferencia entre grupos?

---

### 💡 ¿Tenés otra idea?
Si se te ocurre otro enfoque, análisis o modelo que quieras probar, ¡adelante! Este dataset es ideal para experimentar y explorar distintas estrategias de análisis de señales, clasificación o visualización. Podés proponer tu propio enfoque, siempre y cuando lo justifiques técnicamente.

---
