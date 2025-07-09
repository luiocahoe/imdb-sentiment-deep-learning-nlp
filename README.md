# IMDB Sentiment Analysis con Deep Learning y Transformers

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/luiocahoe/imdb-sentiment-deep-learning-nlp/blob/main/notebooks/imdb_lstm.ipynb)

Este repositorio contiene el desarrollo de varios modelos de deep learning para análisis de sentimiento en reseñas de películas utilizando el dataset IMDB. Se exploran arquitecturas clásicas como LSTM, variantes con atención, modelos bidireccionales y modelos basados en Transformers (BERT), incluyendo experimentos de optimización y comparación de resultados.

---

## Estructura del repositorio

```
imdb-sentiment-deep-learning-nlp/
├── imdb_sentiment.ipynb
├── imdb_sentiment.html
└── README.md
```
---

## Descripción del proyecto

El objetivo es comparar el rendimiento de distintos enfoques de deep learning para clasificación binaria de sentimientos en texto. Se incluyen:

- **LSTM clásico:** Modelo secuencial con embedding y capa LSTM.
- **LSTM + Atención:** Añade mecanismo de self-attention y normalización.
- **LSTM Bidireccional + Atención:** Incorpora contexto pasado y futuro.
- **BERT Small y Large:** Modelos preentrenados de Transformers finetuneados.
- **BERT congelado:** Encoder congelado para eficiencia computacional.
- **Optimización:** Experimentos con tasas de aprendizaje y regularización.

---

## Resultados principales

| Modelo               | Accuracy Test |
|----------------------|:------------:|
| LSTM                 |   0.85796    |
| LSTM ATT             |   0.83540    |
| LSTM ATT MOD         |   0.88768    |
| BERT small           |   0.83736    |
| BERT large           |   0.88450    |
| BERT congelado       |   0.66390    |
| BERT optimizado      |   0.84440    |

---

## Cómo ejecutar

1. **Clona el repositorio**
    ```
    git clone https://github.com/tu_usuario/imdb-sentiment-deep-learning-nlp.git
    cd imdb-sentiment-deep-learning-nlp
    ```

2. **Ejecuta los notebooks**
    - Abre los notebooks en Jupyter o Google Colab.
    - Descarga el dataset IMDB usando los scripts o el loader de Keras.

---

## Créditos

- **Dataset:** IMDB Movie Reviews (Keras Datasets)
- **Modelos BERT:** TensorFlow Hub

---

## Notas

- Para ejecutar modelos BERT grandes, se recomienda disponer de GPU.
- Incluye ejemplos de cómo evitar el *catastrophic forgetting* y optimizar el entrenamiento.