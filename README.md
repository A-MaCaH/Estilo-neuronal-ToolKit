# 🧠 Neural Style Transfer Toolkit

This repository contains a set of tools and tutorials for working with neural style transfer, including spatial control, stylized data augmentation, and style analysis with dimensionality reduction techniques.

This project is inspired by my master's thesis "Neural style transfer in small medical image sets". Although it is not the exact code used in the thesis, much of the inspiration and concepts come from it.

The project is divided into three main parts:

## 1. 📘 Tutorial: Neural Style Transfer and Spatial Control

An interactive notebook (Jupyter Notebook) that explains the fundamentals of neural style transfer using PyTorch, including:

*   Feature extraction with VGG19
  <img src="https://github.com/user-attachments/assets/274b4ee6-3285-4533-9de5-0b7e72debd6b" width="512">

*   Calculation of content and style losses (Gram matrices)
  <img src="https://github.com/user-attachments/assets/be70582a-f4ec-48eb-8081-704d44fbee88" width="512">
  <img src="https://github.com/user-attachments/assets/25e38410-7c04-450f-93ed-d40c7d285813" width="512">

*   Optimization to generate an image that combines content and style
<div style="display: flex; gap: 10px;">

  <div style="flex: 1;">
    <h4>🧠 Gift de Gradientes</h4>
    <img src="https://github.com/user-attachments/assets/d4a823bb-8e33-4910-9f8d-2b2287c09545" width="224">
  </div>

  <div style="flex: 1;">
    <h4>🖼️ Gift de resultado</h4>
    <img src="https://github.com/user-attachments/assets/5cbe44d5-825f-4d6f-8a6a-b3f14e2638e0" width="224">
  </div>

</div>

*   Spatial style control, applying different styles in specific regions of the image
  

This tutorial is designed to be educational and easy to modify, ideal for students and developers who want to understand the inner workings of neural style.

## 2. 🧪 Data Augmentation with Neural Style (building)

This module allows generating augmented datasets using neural styles. It takes a class-structured folder as input (one folder per class with images inside) and generates a specific number of stylized images per class. Ideal for classification or robustness tasks with convolutional neural networks.

**Input:**

```
dataset/
  ├── class1/
  │    ├── img1.jpg
  │    └── ...
  ├── class2/
       └── ...
```

**Configurable parameters:**

*   Number of output images per class
*   List of styles (image or folder)
*   Output dimensions
*   Random or fixed style per class

**Output:**
A new set of stylized images per class, ready for training.

## 3. 🧬 Style Extraction and Analysis (building)

This program has two modes:

### a. Style Extraction

Extracts style representations (Gram matrices) from a folder of images using a pre-trained VGG network. Style vectors are stored for each image, facilitating their reuse or later analysis.

### b. Style Analysis

Allows visualizing the similarity between styles using:

*   Dimensionality reduction (PCA, t-SNE, UMAP)
*   Euclidean distance matrix
*   Correlation matrix

These visualizations allow:

*   Exploring the structure of the style space
*   Identifying groups of similar styles
*   Evaluating the diversity of a set of styles

## 📂 Repository Structure

```

```

## 🛠️ Requirements

*   Python 3.8
*   PyTorch
*   torchvision
*   scikit-learn
*   matplotlib
*   seaborn
*   tqdm


## 📚 Referencias

* [TensorFlow Style Transfer Tutorial](https://github.com/tensorflow/docs/blob/master/site/en/tutorials/generative/style_transfer.ipynb)
* [Doodle: Style Transfer Tool](https://github.com/gargimahale/Doodle)
* [Exploring the Structure of the Style Space](https://arxiv.org/pdf/1611.07865v2)
* [CS231n Style Transfer Project](https://tomhenighan.com/pdfs/cs231n-project.pdf)


## 🖼️ Imágenes de Ejemplo

* Contenido: [Xolo de la UNAM](https://www.gaceta.unam.mx/wp-content/uploads/2021/08/xolodes.jpg)
* Estilo: [Henri-Edmond Cross – Puntillismo](https://mymodernmet.com/wp/wp-content/uploads/2022/04/Henri-Edmond-Cross-puntillismo.jpeg)
