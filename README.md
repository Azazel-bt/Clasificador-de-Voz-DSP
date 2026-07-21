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
