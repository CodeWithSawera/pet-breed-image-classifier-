# Pet Breed Image Classifier (Oxford-IIIT Pet Dataset)

This repository contains a PyTorch-based image classification model trained to recognize 37 pet breeds from the Oxford-IIIT Pet Dataset.

## 1. Model and Training Setup
* **Dataset:** Oxford-IIIT Pet Dataset (37 distinct pet breeds).
* **Architecture:** ResNet34 (Pretrained on ImageNet) with fine-tuning. ResNet34 was chosen because it provides an optimal balance between high classification accuracy and fast training times on Google Colab T4 GPU.
* **Data Splitting:** Clean split maintaining separate training, validation, and test sets to prevent data leakage.

## 2. Test Results & Metrics
* **Overall Test Accuracy:** Evaluated and reported on the independent test set.
* **Per-Breed Performance:** Precision and recall metrics calculated per breed using Scikit-learn classification reports.
* **Confusion Matrix:** Visualized using Seaborn to highlight inter-class confusion among visually similar breeds.

## 3. Generalisation Check (Out-of-Dataset Evaluation)
* Tested the model on at least 30 external photos collected from outside the training dataset (personal photos and web images).
* **Generalisation Accuracy:** Evaluated and reported based on real-world test images.

## 4. Failure Case Analysis
* **Picked Wrong Prediction:** Analyzed one specific misclassification instance where visually similar breeds were confused due to overlapping patterns and facial structures.
* **Reason:** Lighting variations, background clutter, or ambiguous pose alignment.

## 5. Future Improvements
* Implement data augmentation techniques (random cropping, color jitter) to improve robustness.
* Experiment with deeper architectures like EfficientNet for higher feature extraction capability.
