# Lung Tumor Image Processing and Classification Project

This project applies deep learning to detect and classify lung tumors into benign, malignant, or normal cases in medical images. It employs various Convolutional Neural Network (CNN) architectures, including custom CNNs, MobileNetV1, and EfficientNetB0, to achieve robust classification.

## Key Features:

1. **Data Preprocessing**:
   - Image resizing, normalization, and contrast enhancement using Contrast Limited Adaptive Histogram Equalization (CLAHE) for better feature extraction.
   - Data augmentation, generating diverse samples to improve model generalization.

2. **Model Architectures**:
   - Custom CNN with multiple convolutional and pooling layers for baseline performance.
   - Pre-trained MobileNetV1 and EfficientNetB0 models, leveraging transfer learning for enhanced accuracy.

3. **Training and Validation**:
   - Stratified train-test-validation splitting to maintain class distribution.
   - Augmented training data combined with original samples for robust model learning.

4. **Evaluation and Analysis**:
   - Comprehensive metrics including accuracy, precision, recall, F1-score, and AUC-ROC for model evaluation.
   - Visualizations such as confusion matrices, class-wise performance heatmaps, and precision-recall curves.

5. **Deployment**:
   - Models saved in Keras format for easy reloading and inference.
   - Example usage of the trained models to predict unseen test cases and verify performance consistency.

This codebase showcases a complete pipeline for medical image classification, emphasizing both reproducibility and scalability.


## Results:

### Table I. Overall Classification Performance for Each Model

| Model          | Classification Accuracy | Specificity | Sensitivity |
|----------------|--------------------------|-------------|-------------|
| CNN            | 94.85%                  | 0.9739      | 0.8762      |
| MobileNetV1    | 93.03%                  | 0.9626      | 0.7943      |
| EfficientNetB0 | 96.36%                  | 0.9810      | 0.8955      |

### Table II. Computational Resources Consumed for Each Model

| Model          | Total Parameters    | Trainable Parameters | Non-trainable Parameters |
|----------------|---------------------|-----------------------|--------------------------|
| CNN            | 494,547 (1.89 MB)  | 494,547 (1.89 MB)    | 0 (0.00 B)              |
| MobileNetV1    | 3,231,969 (12.33 MB) | 3,210,081 (12.25 MB) | 21,888 (85.50 KB)       |
| EfficientNetB0 | 4,053,444 (15.46 MB) | 4,011,421 (15.30 MB) | 42,023 (164.16 KB)      |

### Table III. Summary of Model's Performance in Each Class

| Model          | Class            | Precision | Recall | F1-Score |
|----------------|------------------|-----------|--------|----------|
| CNN            | Benign           | 0.68      | 0.68   | 0.75     |
|                | Malignant        | 0.99      | 0.99   | 0.99     |
|                | Normal           | 0.91      | 0.97   | 0.94     |
|                | Macro Average    | 0.92      | 0.88   | 0.89     |
|                | Weighted Average | 0.95      | 0.95   | 0.95     |
| MobileNetV1    | Benign           | 1.00      | 1.00   | 1.00     |
|                | Malignant        | 1.00      | 0.99   | 1.00     |
|                | Normal           | 0.84      | 1.00   | 0.91     |
|                | Macro Average    | 0.95      | 0.79   | 0.82     |
|                | Weighted Average | 0.94      | 0.93   | 0.95     |
| EfficientNetB0 | Benign           | 0.96      | 0.69   | 0.80     |
|                | Malignant        | 1.00      | 1.00   | 1.00     |
|                | Normal           | 0.92      | 0.99   | 0.95     |
|                | Macro Average    | 0.96      | 0.92   | 0.96     |
|                | Weighted Average | 0.96      | 0.96   | 0.96     |
