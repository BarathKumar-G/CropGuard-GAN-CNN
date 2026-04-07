# CropGuard: GAN-Enhanced CNN for Crop Disease Detection

CropGuard is an experiment-driven deep learning project focused on improving crop disease detection using Convolutional Neural Networks (CNNs) and Generative Adversarial Networks (GANs).

The project specifically addresses class imbalance in agricultural datasets, where certain disease classes have significantly fewer samples, leading to poor model performance.

---

## Problem Statement

In real-world agricultural datasets:

- Healthy leaf images are abundant  
- Rare disease classes have very few samples  

This imbalance causes deep learning models to:

- Perform well on majority classes  
- Perform poorly on minority classes  

---

## Objective

- Detect crop diseases from leaf images using CNN  
- Identify and address class imbalance  
- Improve recall of minority classes  
- Evaluate effectiveness of synthetic data  

---

## Approach

### 1. Data Preparation

- Used PlantVillage dataset  
- Resized images and split into train/validation/test sets  
- Analyzed class distribution  

### 2. Baseline CNN Model

- Trained a CNN model (ResNet18) on imbalanced dataset  
- Observed strong overall accuracy but weak minority class recall  

### 3. GAN-Based Data Generation

- Trained a DCGAN on a selected minority class (Potato___healthy)  
- Generated synthetic images to increase data diversity  

### 4. Data Balancing Strategy

Combined:

- Original dataset  
- Augmented real images  
- GAN-generated synthetic images  

### 5. Retraining

- Retrained CNN on balanced dataset  
- Compared performance before and after balancing  

---

## Results

| Metric | Before | After |
|------|--------|-------|
| Potato Healthy Recall | ~0.14 | ~0.5 |

**Key Outcome:**

- Improved detection of underrepresented classes  
- Demonstrated effectiveness of targeted data balancing  

---

## Technologies Used

- Python  
- PyTorch  
- Torchvision  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Google Colab  

---

## Key Learnings

- High accuracy does not guarantee good performance across all classes  
- Class imbalance significantly impacts recall  
- GAN-generated data can help improve minority class performance  
- Combining augmentation + synthetic data is more effective than using GAN alone  

---

## Limitations

- GAN-generated images were not perfectly realistic  
- Improvement depends on GAN quality  
- Only one class was enhanced for experimentation  

---

## Future Work

- Extend GAN augmentation to multiple minority classes  
- Use advanced GAN architectures (StyleGAN, CycleGAN)  
- Deploy model using a web interface (Streamlit)  
- Optimize hyperparameters for better performance  