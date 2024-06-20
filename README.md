
# 🎮 Análisis de Dataset de Ventas de Videojuegos

## Descripción

Este dataset contiene una lista de videojuegos con ventas superiores a 100,000 copias, obtenidos mediante scraping de vgchartz.com.

### Atributos

- **Ranking**: Ranking de ventas totales.
- **Nombre**: Nombre del videojuego.
- **Plataforma**: Plataforma de lanzamiento del juego (por ejemplo, PC, PS4, etc.).
- **Año**: Año de lanzamiento del juego.
- **Género**: Género del juego.
- **Editora**: Editorial del juego.
- **Ventas NA**: Ventas en América del Norte (en millones).
- **Ventas EU**: Ventas en Europa (en millones).
- **Ventas JP**: Ventas en Japón (en millones).
- **Otras Ventas**: Ventas en el resto del mundo (en millones).
- **Ventas Globales**: Ventas totales en todo el mundo.

## Bibliotecas Utilizadas

\```python
import os  # para manejo de rutas de archivo
import numpy as np  # álgebra lineal
import pandas as pd  # procesamiento de datos
import warnings  # filtros de advertencia

# Bibliotecas de visualización
import matplotlib.pyplot as plt
import seaborn as sns
import plotly.graph_objects as go

# Bibliotecas de Machine Learning
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.metrics import confusion_matrix, classification_report, accuracy_score, r2_score
from sklearn.model_selection import cross_val_score

# Modelos de Machine Learning
from sklearn.linear_model import Ridge, LinearRegression
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import RandomForestRegressor
from sklearn.neighbors import KNeighborsRegressor
\```

## Fases del Análisis

1. **Vista Previa de los Datos**
2. **Detección de Duplicados**
3. **Preprocesamiento de Datos**
4. **Análisis Exploratorio de Datos (EDA)**
5. **Manejo de Valores Atípicos**
6. **División de Datos (Entrenamiento | Prueba)**
7. **Modelado**

## Conclusiones

### Hallazgos Clave

1. La mayoría de los juegos se produjeron para la plataforma DS, seguida por PS2.
2. Los géneros más populares son Acción y Deportes; Puzzle es el menos popular.
3. La editora más destacada es Electronic Arts.
4. La mayoría de los juegos se produjeron entre 2002 y 2016, con un pico alrededor de 2010.
5. Los juegos de Acción son los más frecuentemente publicados.
6. Las ventas alcanzaron su punto máximo entre 2005 y 2010, con ventas más bajas en los años 1980 y 1990.

### Mejores Modelos

Los modelos que mejor rendimiento mostraron fueron la Regresión Ridge y la Regresión Lineal.
