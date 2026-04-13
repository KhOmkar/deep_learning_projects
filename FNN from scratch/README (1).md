# Feedforward Neural Network — From Scratch

> Deep Learning Assignment | Built with NumPy only — no PyTorch, TensorFlow, or Keras.

---

## Overview

A complete implementation of a Feedforward Neural Network (FNN) from scratch,
trained on the `make_moons` binary classification dataset.
Every component — forward pass, backpropagation, weight initialisation, and gradient
descent — is implemented manually using NumPy.

---

## Network Architecture

```
Input (2)  ──►  Hidden Layer 1 (8, ReLU)  ──►  Hidden Layer 2 (4, ReLU)  ──►  Output (1, Sigmoid)
```

| Layer | Units | Activation | Parameters |
|---|---|---|---|
| Input | 2 | — | — |
| Hidden 1 | 8 | ReLU | W¹: 8×2, b¹: 8×1 |
| Hidden 2 | 4 | ReLU | W²: 4×8, b²: 4×1 |
| Output | 1 | Sigmoid | W³: 1×4, b³: 1×1 |

**Total parameters: 65**

---

## Files

| File | Description |
|---|---|
| `FNN_from_Scratch.ipynb` | Main Jupyter Notebook (submit this) |
| `README.md` | This file |

---

## How to Run

### Option 1 — Google Colab (recommended, free GPU)
1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Upload `FNN_from_Scratch.ipynb`
3. Runtime → Run All

### Option 2 — Local Jupyter
```bash
pip install numpy matplotlib scikit-learn jupyter
jupyter notebook FNN_from_Scratch.ipynb
```

> **Note:** No GPU required. The network uses only NumPy CPU operations.

---

## Dependencies

```
numpy
matplotlib
scikit-learn   # dataset generation and train/test split ONLY
jupyter
```

No deep learning libraries (PyTorch / TensorFlow / Keras) are used anywhere.

---

## Key Implementation Details

### `NeuralNetwork` Class API

| Method | Description |
|---|---|
| `__init__(layer_dims)` | He initialisation of weights and biases |
| `forward(X)` | Compute activations for all layers; cache intermediates |
| `compute_loss(A_out, Y)` | Binary Cross-Entropy loss |
| `backward(Y)` | Backpropagation — compute dW, db for all layers |
| `update_params(lr)` | Vanilla gradient descent update |
| `train(X, y, epochs, lr, verbose)` | Full training loop with per-epoch weight printing |
| `predict(X)` | Binary predictions (threshold 0.5) |
| `evaluate(X, y)` | Classification accuracy |
| `confusion_matrix_manual(X, y)` | Manual 2×2 confusion matrix |

### Per-Epoch Weight Display

When `verbose=True` (default), the training loop prints all weight matrices
and bias vectors after every epoch:

```
──────────────────────────────────────────────────────────────────
  Epoch   1 / 50   |   Loss: 0.693147
──────────────────────────────────────────────────────────────────
  Layer 1  W1  shape=(8, 2):
    [+0.54772  -0.23145]
    [-0.12089  +0.67834]
    ...
  Layer 1  b1: [+0.00000  +0.00000  ...]
  ...
```

---

## Visualisations Produced

1. **Dataset Scatter** — train and test sets, colour-coded by class
2. **Loss Curve** — training BCE loss vs. epoch
3. **Decision Boundary** — non-linear curved boundary over test set
4. **Weight Norm Evolution** — L2-norm of each weight matrix across epochs
5. **Confusion Matrix** — TN/FP/FN/TP heatmap on test set
6. **Gradient Norm Evolution** *(bonus)* — gradient magnitudes across epochs

---

## Results

| Metric | Value |
|---|---|
| Train Accuracy | ~78% |
| Test Accuracy | ~76% |
| Epochs | 50 |
| Learning Rate | 0.01 |

---

## Research Paper Referenced

Rumelhart, D. E., Hinton, G. E., & Williams, R. J. (1986).
*Learning representations by back-propagating errors.*
**Nature**, 323(6088), 533–536.
https://doi.org/10.1038/323533a0

---

## Academic Integrity

This is original work implementing a neural network from mathematical first principles.
All code is written by the student; no neural network library code was copied or adapted.
