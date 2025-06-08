# 🧠 Neural Style Transfer Toolkit

This repository contains a set of tools and tutorials for working with neural style transfer, including spatial control, stylized data augmentation, and style analysis with dimensionality reduction techniques.

This project is inspired by my master's thesis "Neural style transfer in small medical image sets". Although it is not the exact code used in the thesis, much of the inspiration and concepts come from it.

The project is divided into three main parts:

## 1. 📘 Tutorial: Neural Style Transfer and Spatial Control

An interactive notebook (Jupyter Notebook) that explains the fundamentals of neural style transfer using PyTorch, including:

*   Feature extraction with VGG19
  ![imagen](https://github.com/user-attachments/assets/274b4ee6-3285-4533-9de5-0b7e72debd6b)

*   Calculation of content and style losses (Gram matrices)
  ![imagen](https://github.com/user-attachments/assets/be70582a-f4ec-48eb-8081-704d44fbee88)
  ![imagen](https://github.com/user-attachments/assets/c6ae7510-e146-4af9-b013-1385d76b1a15)

*   Optimization to generate an image that combines content and style
![gradients](https://github.com/user-attachments/assets/d4a823bb-8e33-4910-9f8d-2b2287c09545)
![style_transfer(1)](https://github.com/user-attachments/assets/5cbe44d5-825f-4d6f-8a6a-b3f14e2638e0)

*   Spatial style control, applying different styles in specific regions of the image
  

This tutorial is designed to be educational and easy to modify, ideal for students and developers who want to understand the inner workings of neural style.

## 2. 🧪 Data Augmentation with Neural Style

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

## 3. 🧬 Style Extraction and Analysis

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
├── tutorial/
│   └── neural_style_transfer.ipynb      # Part 1: Tutorial
├── augment/
│   └── stylized_data_generator.py       # Part 2: Data Augmentation
├── style_extractor/
│   ├── extract_styles.py                # Part 3a: Extraction
│   └── analyze_styles.py                # Part 3b: Analysis
└── README.md
```

## 🛠️ Requirements

*   Python 3.8+
*   PyTorch
*   torchvision
*   scikit-learn
*   matplotlib
*   seaborn
*   UMAP (optional)
*   tqdm

## 🧪 Applications

*   Data augmentation for computer vision models
*   Study of the artistic style space
*   Educational experimentation on neural style

## References

Here you can list the articles, books, or resources that were important for your work.
