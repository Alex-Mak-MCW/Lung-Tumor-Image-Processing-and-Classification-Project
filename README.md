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
