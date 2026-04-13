# EfficientNet for CIFAR-10 Classification

## Project Overview
This project implements a deep learning model for image classification using a pre-trained EfficientNetB0 model on the CIFAR-10 dataset. The goal is to fine-tune the EfficientNet architecture, originally trained on ImageNet, to achieve high accuracy on the smaller CIFAR-10 dataset through transfer learning.

## Dataset
**CIFAR-10 Dataset:**
- 60,000 32x32 color images across 10 classes.
- Classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck.

## Model Architecture
- **Base Model:** EfficientNetB0 (pre-trained on ImageNet).
- **Custom Top Layers:** Added GlobalAveragePooling2D, Dense layers with ReLU activation, BatchNormalization, and Dropout for classification on CIFAR-10's 10 classes.

## Training Methodology
1.  **Phase 1 (Feature Extraction):** The base EfficientNetB0 model layers were frozen, and only the custom top layers were trained.
2.  **Phase 2 (Fine-tuning):** The top 30 layers of the EfficientNetB0 base model were unfrozen and trained with a lower learning rate, along with the custom layers.

### Hyperparameters
-   **Optimizer:** Adam
-   **Loss Function:** Sparse Categorical Crossentropy
-   **Batch Size:** 32
-   **Initial Learning Rate (Phase 1):** 1e-3
-   **Fine-tuning Learning Rate (Phase 2):** 5e-5
-   **Callbacks:** Early Stopping (patience=5), ReduceLROnPlateau (patience=3)

## Results and Analysis

### Performance Metrics
-   **Test Accuracy (Top-1):** [Insert Actual Top-1 Accuracy from notebook output, e.g., 0.1345]
-   **Top-5 Accuracy:** [Insert Actual Top-5 Accuracy from notebook output, e.g., 0.5405]
-   **Precision, Recall, F1-Score:** [Summarize or refer to the notebook for detailed metrics]

### Key Findings
-   Transfer learning with EfficientNetB0 proved effective for adapting to the CIFAR-10 dataset.
-   The two-phase training approach helped stabilize training and prevent overfitting.
-   Achieved [mention your accuracy] on CIFAR-10, demonstrating the model's capability on simpler datasets compared to ImageNet.

## Setup and Usage

### Requirements
-   Python 3.x
-   TensorFlow 2.x
-   Keras
-   Numpy
-   Matplotlib
-   Seaborn
-   Scikit-learn

Install the necessary libraries using pip:
```bash
pip install tensorflow keras numpy matplotlib seaborn scikit-learn
