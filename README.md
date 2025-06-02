# 🦁🐯 Multi-Class Animal Recognition 🐶🦓

## 🚀 Deep Learning Project for Animal Image Classification

---

## 📌 Overview

Welcome to the **Multi-Class Animal Recognition** project — a deep learning-based classification system designed to recognize and categorize multiple types of animals from images using Convolutional Neural Networks (CNNs). This project is a practical application of modern computer vision techniques tailored to wildlife conservation, smart zoos, automated animal monitoring, and educational tools.

---

## 🎯 Objectives

- Build a robust CNN model for multi-animal image classification.
- Preprocess and augment image data for enhanced model generalization.
- Evaluate performance through metrics and training visualizations.
- Leverage popular deep learning libraries like TensorFlow and Keras.

---

## 📦 Dataset Summary

The dataset used for this project is publicly available on **Kaggle**:

🔗 **Dataset Link**: [Animal Image Dataset (90 Different Animals)](https://www.kaggle.com/datasets/iamsouravbanerjee/animal-image-dataset-90-different-animals)

### 🧬 Description

This dataset is a curated collection of high-resolution animal images across **90 unique categories**, suitable for training and evaluating **multi-class image classification models**. It includes a wide range of species, providing intra-class variability and inter-class similarity — making it a compelling benchmark for CNN-based models.

### 🔍 Key Technical Highlights

- 🧾 **Multi-class, Single-label Classification Task**: Each image is labeled with exactly one class out of 90 possible categories.
- 🖼️ **Image Format**: Primarily `.jpg` files with varying dimensions and quality; preprocessing includes resizing to 224x224 and normalization to [0, 1].
- 📐 **Resolution Variability**: Original images have non-uniform resolutions, requiring dynamic resizing and augmentation strategies.
- 🧪 **Data Distribution**: While generally balanced, some long-tail class distributions exist — making it suitable for experimenting with weighted loss functions or focal loss.
- 🔄 **Noisy Labels**: A few images contain minor label noise or class ambiguity, making it useful for testing model robustness and regularization techniques.
---
## 🧠 Model Summary

This project implements a **custom Convolutional Neural Network (CNN)** architecture, enhanced using **MobileNetV2** through **transfer learning**, tailored for multi-class animal image classification. The model design strikes a balance between training efficiency and classification accuracy, particularly when dealing with high-resolution visual data.

MobileNetV2 is chosen for its lightweight architecture, enabling fast convergence while leveraging powerful pre-trained features from ImageNet. It is well-suited for applications that require real-time performance or resource-efficient deployment.

### 🏗️ Architecture Overview

- 📸 **Input Layer**: Preprocessed RGB images resized to **224x224x3**, the standard input size for MobileNetV2.
- 🧠 **Base Model**: Pretrained **MobileNetV2** loaded with `imagenet` weights and `include_top=False` to remove the original classifier.
- ❄️ **Frozen Layers**: Convolutional layers of MobileNetV2 are frozen to preserve low-level visual features.
- 🔄 **Dropout & BatchNormalization**: Integrated to regularize the model and prevent overfitting.
- 🧮 **Custom Fully Connected Layers**: Additional dense layers are added on top of MobileNetV2 to specialize the model for classifying **6 animal categories**.
- 🔚 **Output Layer**: A final `Dense` layer with **ReLu activation** outputs probability distributions over the classes.

## 🎯 Model Evaluation on Validation Set

**Validation Loss:** 0.608  
**Validation Accuracy:** 84.8%

---

*This model confidently classifies diverse animal species with an impressive 84.8% accuracy on unseen data — making it a powerful tool for wildlife monitoring, smart zoos, and automated animal recognition!* 🦁🐯🐶🦓

