# CropGuard: GAN-Enhanced CNN for Crop Disease Detection

CropGuard is a deep learning–based smart agriculture system designed to detect plant diseases from leaf images and improve rare disease recognition using synthetic data generation.  
The project combines **Convolutional Neural Networks (CNNs)** for image classification and **Generative Adversarial Networks (GANs)** for dataset balancing, creating a complete end-to-end pipeline for accurate and scalable crop disease detection.

---

## Problem Statement

Early identification of crop diseases is critical for preventing yield loss, reducing pesticide overuse, and supporting sustainable farming.

However, real-world agricultural datasets are **highly imbalanced**, where:

- Healthy leaf images are abundant  
- Rare disease samples are extremely limited  

This imbalance causes deep learning classifiers to perform poorly on **minority disease classes**, leading to unreliable predictions in practical scenarios.

---

## Project Objective

The primary goal of CropGuard is to:

- Detect crop diseases from leaf images using deep learning  
- Address dataset imbalance through **GAN-generated synthetic diseased images**  
- Improve **rare disease recall and overall classification performance**  
- Provide a simple deployment interface for real-time disease prediction  

---

## Core Approach

### 1. Data Preparation
- Public agricultural image datasets (e.g., PlantVillage) are collected.
- Images are resized, normalized, and split into **train, validation, and test** sets.
- Exploratory analysis is performed to quantify **class imbalance**.

### 2. Baseline CNN Classification
- A Convolutional Neural Network is trained on the **original imbalanced dataset**.
- Evaluation metrics such as **accuracy, precision, recall, F1-score, and confusion matrix** are recorded.
- This establishes the **baseline performance** and highlights poor detection of rare diseases.

### 3. Synthetic Data Generation with GAN
- A **Deep Convolutional GAN (DCGAN)** is trained on diseased leaf images.
- The generator learns disease texture, color variation, and lesion patterns.
- New **realistic synthetic diseased images** are produced for minority classes.

### 4. Dataset Balancing and Retraining
- Real and synthetic images are combined to create a **balanced training dataset**.
- The CNN is retrained using this balanced data.
- Performance is compared against the baseline model to measure improvement.

### 5. Deployment Interface
- A lightweight prediction interface allows users to:
  - Upload a leaf image  
  - Receive disease classification results in real time  

---

## Key Features

- Deep learning–based **crop disease classification**
- **GAN-driven synthetic image generation** for minority classes
- Quantitative **performance comparison before and after balancing**
- Visualization of **class distribution, confusion matrices, and results**
- Simple **deployment-ready prediction interface**

---

## Evaluation Metrics

Model performance is assessed using:

- **Accuracy** – Overall prediction correctness  
- **Precision & Recall** – Class-wise reliability  
- **F1-Score** – Balanced performance measure  
- **Confusion Matrix** – Error distribution visualization  

Special focus is given to **recall improvement in rare disease classes** after GAN-based balancing.

---

## Technologies Used

- **Python**
- **PyTorch / TensorFlow** for CNN and GAN implementation  
- **NumPy, Pandas, Matplotlib, Seaborn** for data analysis and visualization  
- **Streamlit** for deployment interface  

---

## Expected Outcomes

- Improved detection of **rare crop diseases**
- Demonstration that **synthetic data enhances deep learning performance**
- A complete **end-to-end smart agriculture prototype**
- Foundation for **AI-assisted precision farming tools**

---

## Future Enhancements

- Apply **Diffusion Models** for higher-quality synthetic image generation  
- Extend to **mobile deployment** for real field usage  
- Integrate **treatment recommendation systems** based on detected disease  
- Train on **real-world field images** beyond controlled datasets  

---

## License

This project is intended for **academic and research purposes only**.
