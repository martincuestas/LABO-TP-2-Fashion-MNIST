# Clasificación de Imágenes — Fashion MNIST

**Trabajo Práctico II — Laboratorio de Datos, Licenciatura en Ciencias de Datos, UBA (FCEyN) — 2025**  
**Autores:** Martín Iván Cuestas, Julián Nakasone, Dante Poli

## Descripción

Análisis exploratorio y entrenamiento de modelos de clasificación sobre el dataset
Fashion MNIST, compuesto por 70.000 imágenes de prendas de vestir de 28×28 píxeles.

## Contenido

### Análisis Exploratorio
- Identificación de píxeles informativos mediante análisis de varianza por clase
- Visualización de imágenes promedio y mapas de varianza por prenda
- Comparación de patrones de píxeles entre grupos de prendas similares

### Clasificación Binaria — kNN
- Clases: T-shirt/Top (0) vs. Bag (8)
- Selección de los 100 atributos más discriminativos por varianza
- Comparación de distancias Euclidean y Manhattan para k = 1…30
- **Mejor modelo:** k = 5, distancia Euclidean → **accuracy: 98.71%**

### Clasificación Multiclase — Decision Tree
- 10 clases, validación con k-fold estratificado
- Selección de atributos por comparación de varianza entre todos los pares de clases
- Comparación de criterios Gini vs. Entropy y profundidades 1…10
- **Mejor modelo:** Entropy, profundidad 10, 82 atributos → **accuracy en holdout: 80.09%**
- Trade-off: reducción de 118 a 82 atributos con pérdida de solo 0.38%

## Tecnologías

Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn

## Estructura

- `TP2.ipynb` — Notebook principal con análisis y modelos
- `informe.pdf` — Informe completo con desarrollo y conclusiones
