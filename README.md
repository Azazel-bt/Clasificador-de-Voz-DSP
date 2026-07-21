# 🎙️ Clasificador de Voz mediante Procesamiento Digital de Señales y SVM

Este proyecto aplica técnicas de **Procesamiento Digital de Señales (DSP)** y **Machine Learning** en Python para analizar, procesar y clasificar archivos de audio de voz de múltiples locutores.

## 🚀 Características Principales

* **Conversión y Gestión de Audio:** Transcodificación de audio comprimido (`.opus`) a formato no comprimido (`.wav`) mediante `PyDub` y `FFmpeg` / `opus-tools`.
* **Procesamiento Digital de Señales (DSP):**
  * Extracción de características espectrales y temporales con `Librosa`.
  * Diseños de filtros digitales (Filtro Butterworth y `filtfilt` de `SciPy`) para atenuación de ruido e higiene espectral.
* **Clasificación Automática:** Entrenamiento de un modelo de Máquinas de Vectores de Soporte (**SVM**) con `Scikit-Learn` para identificar las etiquetas de los locutores.

## 🛠️ Tecnologías Utilizadas

* **Lenguaje:** Python 3
* **Librerías de Audio & DSP:** `librosa`, `pydub`, `scipy`, `numpy`, `matplotlib`
* **Machine Learning:** `scikit-learn` (`SVC`, `train_test_split`, `LabelEncoder`)
* **Herramientas del Sistema:** `ffmpeg`, `opus-tools`
  
## 📋 Sistema y resultdos 

El sistema opera mediante un flujo de procesamiento secuencial diseñado para transformar señales de audio crudas en vectores de características altamente discriminativos antes de la etapa de clasificación:
<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/9b23a2c5-6ce6-4eec-8b1d-df69a545733c" />

### 📊 Evaluación y Resultados del Modelo

Para evaluar el desempeño del clasificador se utilizó una **Matriz de Confusión**, la cual permite visualizar la precisión de la predicción frente a las etiquetas reales del dataset (*Astro*, *Cala*, *Carlos*, *Mich*):

#### 📈 Análisis de la Matriz de Confusión:
<p align="center">
  <img width="533" height="438" alt="image" src="https://github.com/user-attachments/assets/27c96e25-9157-4e14-8a69-9f7210b51140" />
</p>

* **Alta Precisión en Clases Principales:** El modelo demuestra un desempeño sobresaliente en la identificación de la mayoría de las categorías (destacando *Astro* con un 100% de aciertos en sus muestras de prueba).
* **Diagonal Dominante:** La concentración de la mayor densidad de muestras sobre la diagonal principal confirma la efectividad de la extracción de características basadas en MFCC y el filtrado previo.
* **Métricas Globales:**
  * **Exactitud (Accuracy):** ~92.8%
  * **Pérdida (Loss):** ~0.26
* **Robustez frente al Ruido:** Gracias al filtrado pasabanda Butterworth previo a la etapa de feature extraction, el modelo reduce significativamente los solapamientos entre clases con registros de voz de tono similar.





## 📋 Estructura del Código

El proyecto está desarrollado completamente en un Jupyter Notebook (`Proyecto_Señales.ipynb`), el cual cubre las siguientes fases:

1. **Instalación y Configuración del Entorno:** Descarga de librerías y utilidades de sistema para tratamiento de archivos multimedia.
2. **Carga y Conversión de Señales:** Proceso automatizado para leer archivos `.opus` y guardarlos como `.wav`.
3. **Filtrado y Análisis de Frecuencia:** Procesamiento con filtros IIR/Butterworth y representación temporal/espectral.
4. **Extracción de Características y Entrenamiento:** Vectorización de características de voz y evaluación de un clasificador SVM.

## 💻 Cómo Ejecutar el Proyecto

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/Azazel-bt/Clasificador-de-Voz-DSP.git](https://github.com/Azazel-bt/Clasificador-de-Voz-DSP.git)
