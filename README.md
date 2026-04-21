# Comparative Analysis of Pre-trained CNN Models for Custom Image Classification

## Project Overview

This project presents a comparative analysis of three pre-trained Convolutional Neural Network (CNN) architectures for custom multi-class image classification using transfer learning.

The study evaluates the performance of:

- VGG16
- ResNet50
- MobileNetV2

The models were trained and tested on a custom image dataset containing 20 classes with at least 200 images per class.

Performance was evaluated using:

- Accuracy and Loss
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- AUC Score
- Grad-CAM Explainability

---

## Objectives

This project aims to:

- Apply transfer learning using pre-trained CNN models
- Compare model performance using standard evaluation metrics
- Analyze classification errors using confusion matrices
- Evaluate discriminative ability using ROC and AUC
- Interpret model decisions using Grad-CAM
- Identify the best-performing model for deployment

---

## Dataset Structure

```bash
ImageDataset/
├── Class1/
├── Class2/
├── Class3/
...
├── Class20/
```

- Total Classes: 20  
- Images per Class: 200+  
- Total Images: 4,000+  

---

## Pre-trained Models Used

| Model | Type | Purpose |
|------|------|---------|
| VGG16 | Deep CNN | Baseline model |
| ResNet50 | Residual CNN | High-performance model |
| MobileNetV2 | Lightweight CNN | Efficient deployment model |

---

## Technologies Used

- Python
- TensorFlow / Keras
- Scikit-learn
- NumPy
- Matplotlib
- Google Colab
- GitHub

---

## Methodology

### 1. Data Preparation

- Dataset collection
- Directory organization
- Train-validation split

### 2. Data Preprocessing

- Image resizing (224x224)
- Rescaling
- Batch processing

### 3. Transfer Learning

- Freeze pre-trained base layers
- Add custom classification head
- Train models for 10 epochs

### 4. Evaluation

Metrics used:

- Accuracy
- Loss
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC Curve
- AUC

### 5. Explainability

Grad-CAM was applied to:

- VGG16
- ResNet50
- MobileNetV2

---

## Results Summary

| Model | Test Accuracy | Precision | Recall | F1-Score | AUC |
|------|---------------|-----------|--------|----------|-----|
| VGG16 | XX.XX | XX.XX | XX.XX | XX.XX | XX.XX |
| ResNet50 | XX.XX | XX.XX | XX.XX | XX.XX | XX.XX |
| MobileNetV2 | XX.XX | XX.XX | XX.XX | XX.XX | XX.XX |

*(Replace with actual results.)*

---

## Visualizations

### Accuracy and Loss Curves

Add screenshots in:

```bash
results/accuracy_plots/
```

---

### Confusion Matrices

Add outputs in:

```bash
results/confusion_matrices/
```

---

### ROC Curves

Add outputs in:

```bash
results/roc_curves/
```

---

### Grad-CAM Heatmaps

Add outputs in:

```bash
results/gradcam/
```

---

## Repository Structure

```bash
├── README.md
├── LW5_CNN_Comparison.ipynb
├── dataset/
├── results/
│   ├── confusion_matrices/
│   ├── roc_curves/
│   ├── gradcam/
│   └── accuracy_plots/
└── saved_models/
```

---

## Key Findings

- ResNet50 achieved the highest classification performance.
- MobileNetV2 showed efficient performance with lower computational cost.
- Grad-CAM revealed meaningful feature attention across models.
- Transfer learning significantly improved training efficiency.

---

## Future Improvements

Possible enhancements:

- Fine-tune deeper layers
- Increase dataset size
- Apply data augmentation
- Optimize hyperparameters
- Test EfficientNet or DenseNet architectures

---

## Real-World Applications

This system can be applied to:

- Medical image classification
- Plant disease detection
- Object recognition
- Smart agriculture
- Mobile and web-based AI applications

---

## Google Colab Notebook

Open in Google Colab:

```python
(Add your Colab link here)
```

---

## GitHub Repository

Repository link:

```bash
(Add your GitHub repository link here)
```

---

## Authors

Name: Your Name  
Course: Bachelor of Science in Information Technology  
Subject: Computer Vision / Deep Learning Laboratory  
Institution: Caraga State University

---

## License

This project is for academic and educational purposes.

MIT License
