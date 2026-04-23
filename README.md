# Deep Learning with PyTorch — CNN & Neural Networks

> MSc Data Science — Applied Machine Learning and Deep Learning (MS4S16)  
> University of South Wales · 2023–2024

---

## Overview

A collection of deep learning experiments using PyTorch — covering CNNs, Neural Networks, Backpropagation, Gradient Descent, and MNIST classification. Built as part of my MSc coursework.

---

## Notebooks

| Notebook | Topic | Key Result |
|----------|-------|------------|
| `cnn_image_classifier.ipynb` | Basic CNN → Improved CNN with Batch Normalisation | **65.8% accuracy** (up from 51%) |
| `simple_neural_network.ipynb` | Feedforward NN from scratch | — |
| `pytorch_autograd_gradient_descent.ipynb` | Autograd, gradient computation, gradient descent | — |
| `pytorch_basics.ipynb` | PyTorch tensors, operations, fundamentals | — |
| `gradient_descent_programming.ipynb` | Gradient descent — parameter optimisation | — |
| `mnist_cnn.ipynb` | MNIST digit classification — Convolutional NN | — |
| `mnist_simple_nn.ipynb` | MNIST digit classification — Simple NN | — |

---

## Key Experiments — CNN Image Classifier

### Architecture Evolution

**Basic CNN:**
- 2 Conv layers (8, 16 filters) + MaxPool + 2 FC layers
- SGD, lr=0.01, 10 epochs
- **Accuracy: 51.5%**

**Improved CNN (with Batch Normalisation):**
- Same architecture + BatchNorm1d after each FC layer
- SGD, lr=0.01, 15 epochs, batch size 75
- **Accuracy: 65.8%**

### Learning Rate Experiments

| Learning Rate | Accuracy |
|---------------|----------|
| 0.00000001 | 29.8% — too slow to converge |
| 0.01 ✅ | **65.8%** — optimal |
| 10 | 59% — overshooting |

**Conclusion:** Learning rate is the single most impactful hyperparameter. Too low → fails to converge. Too high → overshoots. lr=0.01 was optimal here.

---

## Tech Stack

- **Framework:** PyTorch, torchvision
- **Training:** SGD, CrossEntropyLoss, BatchNorm
- **Evaluation:** Confusion Matrix (sklearn), Accuracy
- **Visualisation:** Matplotlib

---

## Setup

```bash
pip install torch torchvision scikit-learn matplotlib tqdm
jupyter notebook cnn_image_classifier.ipynb
```

---

*University of South Wales · MSc Data Science · MS4S16 Applied ML & Deep Learning*
