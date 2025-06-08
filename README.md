# 🧠 Neural Style Transfer Toolkit

Este repositorio contiene un conjunto de herramientas y tutoriales para trabajar con transferencia de estilo neuronal, incluyendo control espacial, aumento de datos estilizados y análisis de estilos con técnicas de reducción de dimensionalidad.

Este proyecto está inspirado en mi tesis de maestría "Transferencia de estilo neuronal en pequeños conjuntos de imágenes médicas". Aunque no es el código exacto utilizado en la tesis, gran parte de la inspiración y los conceptos provienen de ella.

El proyecto está dividido en tres partes principales:

## 1. 📘 Tutorial: Transferencia de Estilo Neuronal y Control Espacial

Un cuaderno interactivo (Jupyter Notebook) que explica los fundamentos de la transferencia de estilo neuronal utilizando PyTorch, incluyendo:

*   Extracción de características con VGG19
*   Cálculo de pérdidas de contenido y estilo (matrices de Gram)
*   Optimización para generar una imagen que combine contenido y estilo
*   Control espacial de estilo, aplicando diferentes estilos en regiones específicas de la imagen

Este tutorial está diseñado para ser educativo y fácil de modificar, ideal para estudiantes y desarrolladores que quieran entender el funcionamiento interno del estilo neuronal.

## 2. 🧪 Aumento de Datos con Estilo Neuronal

Este módulo permite generar datasets aumentados mediante estilos neuronales. Toma como entrada una carpeta estructurada por clases (una carpeta por clase con imágenes dentro) y genera un número específico de imágenes estilizadas por clase. Ideal para tareas de clasificación o robustez con redes convolucionales.

**Entrada:**

```
dataset/
  ├── class1/
  │    ├── img1.jpg
  │    └── ...
  ├── class2/
       └── ...
```

**Parámetros configurables:**

*   Número de imágenes de salida por clase
*   Lista de estilos (imagen o carpeta)
*   Dimensiones de salida
*   Estilo aleatorio o fijo por clase

**Salida:**
Un nuevo conjunto de imágenes estilizadas por clase, listo para entrenamiento.

## 3. 🧬 Extracción y Análisis de Estilos

Este programa tiene dos modos:

### a. Extracción de Estilos

Extrae representaciones de estilo (matrices de Gram) desde una carpeta de imágenes usando una red VGG preentrenada. Se almacenan los vectores de estilo para cada imagen, facilitando su reutilización o análisis posterior.

### b. Análisis de Estilos

Permite visualizar la similitud entre estilos utilizando:

*   Reducción de dimensionalidad (PCA, t-SNE, UMAP)
*   Matriz de distancias euclidianas
*   Matriz de correlaciones

Estas visualizaciones permiten:

*   Explorar la estructura del espacio de estilos
*   Identificar grupos de estilos similares
*   Evaluar diversidad de un conjunto de estilos

## 📂 Estructura del Repositorio

```
├── tutorial/
│   └── neural_style_transfer.ipynb      # Parte 1: Tutorial
├── augment/
│   └── stylized_data_generator.py       # Parte 2: Aumento de datos
├── style_extractor/
│   ├── extract_styles.py                # Parte 3a: Extracción
│   └── analyze_styles.py                # Parte 3b: Análisis
└── README.md
```

## 🛠️ Requisitos

*   Python 3.8+
*   PyTorch
*   torchvision
*   scikit-learn
*   matplotlib
*   seaborn
*   UMAP (opcional)
*   tqdm

## 🧪 Aplicaciones

*   Aumento de datos para modelos de visión por computadora
*   Estudio del espacio de estilos artísticos
*   Experimentación educativa sobre estilo neuronal

## Referencias

Aquí puedes listar los artículos, libros o recursos que fueron importantes para tu trabajo.
