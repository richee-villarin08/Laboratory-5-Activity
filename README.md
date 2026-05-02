# 📚 Laboratory 5: Comparative Analysis of Pre-trained CNN Models

---

## 🚀 Project Overview

This project presents a comprehensive comparison of several state-of-the-art **Convolutional Neural Network (CNN)** architectures for a custom image classification task. Using **Transfer Learning**, models were trained on a dataset with 20 classes. Additionally, **Grad-CAM** was applied to visualize and explain how models make decisions based on image features.

---

## 🧠 Models Used

* **Xception** (Feature Extraction)
* **DenseNet121** (Feature Extraction)
* **NASNetMobile** (Lightweight / Mobile-Optimized)
* **ResNet101** (Deep Residual Learning)
* **EfficientNetB3** (Scaling Optimized)

---

## 📊 Performance Summary

| Model          | Train Accuracy | Train Loss | Validation Accuracy | Validation Loss |
| -------------- | -------------- | ---------- | ------------------- | --------------- |
| Xception       | 77.47%         | 0.8400     | 83.30%              | 0.7437          |
| DenseNet121    | 70.67%         | 1.0425     | 83.30%              | 0.7892          |
| NASNetMobile   | 66.52%         | 1.1863     | 75.75%              | 0.9951          |
| ResNet101      | 10.88%         | 2.9005     | 10.83%              | 2.8986          |
| EfficientNetB3 | 6.38%          | 2.9720     | 5.96%               | 2.9670          |

---

## 📝 Guide Questions & Reflection

### A. Model Performance

**1. Which pre-trained model achieved the highest accuracy? Why?**
**Answer:**
Xception achieved the highest performance with **77.47% training accuracy** and **83.30% validation accuracy**. This is likely due to its use of **depthwise separable convolutions**, which efficiently capture both spatial and channel-wise features in complex datasets.

**2. Which model had the lowest performance? What could be the reason?**
**Answer:**
EfficientNetB3 showed the lowest performance (**5.96% validation accuracy**). This may be due to:

* Model complexity being too high for the dataset size
* Mismatch in preprocessing (EfficientNet has its own normalization requirements)
* Insufficient training epochs or improper fine-tuning

**3. How did loss values compare across models?**
**Answer:**

* Xception and DenseNet121 showed **steady loss reduction**, indicating effective learning
* NASNetMobile showed moderate improvement
* ResNet101 and EfficientNetB3 had **high and stagnant loss**, suggesting poor convergence

---

### B. Evaluation Metrics

**4. Why is accuracy not enough to evaluate a model?**
**Answer:**
Accuracy alone cannot capture the full performance of a model. In multi-class classification:

* A model may perform well overall but fail in specific classes
* It does not show **false positives vs false negatives**
* Metrics like **Precision, Recall, and F1-score** provide deeper insight

**5. Which model had the best F1-score? What does it indicate?**
**Answer:**
Xception likely achieved the best F1-score, indicating a strong balance between:

* **Precision** (correct positive predictions)
* **Recall** (capturing all relevant instances)

---

### C. Confusion Matrix Analysis

**6. Which classes were frequently misclassified?**
**Answer:**
Classes with **similar visual characteristics** (e.g., color, shape, or texture) were commonly misclassified, such as similar plant or object categories.

**7. What patterns did you observe in the confusion matrix?**
**Answer:**

* High diagonal values indicate correct predictions
* Off-diagonal clusters show confusion between similar classes
* Some classes dominate predictions, suggesting bias

---

### D. ROC and AUC

**8. Which model had the highest AUC score?**
**Answer:**
Xception achieved the highest AUC score.

**9. What does AUC tell us about model performance?**
**Answer:**
AUC (Area Under the Curve) measures how well a model distinguishes between classes:

* **1.0 = perfect classification**
* Values closer to 1 indicate better performance
* In multi-class problems, higher AUC reflects stronger classification capability

---

### E. Explainability (Grad-CAM)

**10. What did Grad-CAM reveal about model decision-making?**
**Answer:**
Grad-CAM produced heatmaps highlighting regions influencing predictions. It shows whether the model focuses on:

* Relevant objects (e.g., main subject)
* Irrelevant background areas

**11. Did the model focus on relevant image regions?**
**Answer:**

* Xception and DenseNet121 focused on meaningful regions
* ResNet101 showed scattered attention, explaining poor performance

**12. Which model produced the most meaningful heatmaps?**
**Answer:**
Xception and DenseNet121 generated the most localized and accurate heatmaps.

---

### F. Model Comparison & Improvement

**13. Which model would you recommend for deployment? Why?**
**Answer:**
Xception is recommended due to:

* Highest accuracy
* Stable learning behavior
* Good explainability results

**14. How can you further improve your best-performing model?**
**Answer:**

* Apply **fine-tuning** (unfreeze top layers)
* Use **data augmentation** (rotation, flipping, zoom)
* Increase training epochs
* Optimize hyperparameters

---

### G. Real-World Application

**15. How can your model be applied in real-world scenarios?**
**Answer:**

* Plant or object identification apps
* Agricultural automation systems
* Biodiversity monitoring tools
* Image-based classification systems

**16. What are the risks of deploying an inaccurate model?**
**Answer:**

* Misclassification of critical objects (e.g., toxic vs safe plants)
* Incorrect decision-making
* Reduced trust in AI systems

**17. How can this system be integrated into a mobile/web app?**
**Answer:**

* Convert model to **TensorFlow Lite** (mobile deployment)
* Use **TensorFlow.js** for web applications
* Integrate with a frontend for real-time predictions

---

## 📦 Conclusion

This project demonstrates how different **pre-trained CNN models** perform on a custom dataset. Among all tested models, **Xception** provided the best balance of accuracy, stability, and interpretability. Through evaluation metrics and Grad-CAM visualization, we gained deeper insight into model behavior, enabling better decisions for deployment and future improvements.

---


## Google Colab Notebook

Open in Google Colab:

```python
((https://colab.research.google.com/drive/129_lbR6iiYDh1rIbYarmeaeLUuPDgIUo?usp=sharing))
```


---

## Authors

Name: Richee G. Villarin 
Course: Bachelor of Science in Information Technology  
Subject: Computer Vision / Deep Learning Laboratory  
Institution: Caraga State University

---

## License

This project is for academic and educational purposes.
