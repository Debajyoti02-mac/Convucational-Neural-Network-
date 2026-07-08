# 🧠 Handwritten Digit Classification using CNN (PyTorch)

A Convolutional Neural Network (CNN) built with **PyTorch** for handwritten digit recognition on the **MNIST dataset**. This project demonstrates the complete deep learning workflow, from loading data to training a CNN and monitoring experiments with Weights & Biases.

---

## 📌 Project Overview

The objective is to classify handwritten digits (0–9) from grayscale images using a Convolutional Neural Network.

The project includes:

- MNIST dataset loading
- Image preprocessing
- CNN model creation
- Model training
- Accuracy and loss tracking
- Experiment logging with Weights & Biases
- Model summary using TorchInfo
- Training visualization

---

## 🧠 CNN Architecture

```text
Input Image (1 × 28 × 28)
          │
          ▼
Conv2D (1 → 24, Kernel=2)
          │
        ReLU
          │
      MaxPool2D
          │
          ▼
Conv2D (24 → 48, Kernel=2)
          │
        ReLU
          │
      MaxPool2D
          │
          ▼
Flatten
          │
       Dropout (0.5)
          │
          ▼
Linear (1728 → 128)
          │
        ReLU
          │
          ▼
Linear (128 → 10)
          │
          ▼
Digit Prediction
```

---

## 📂 Dataset

Dataset: **MNIST**

- 60,000 Training Images
- 10,000 Test Images
- Image Size: 28 × 28
- Classes: 10 (Digits 0–9)

---

## 🛠 Technologies Used

- Python
- PyTorch
- Torchvision
- TorchInfo
- Matplotlib
- Weights & Biases (W&B)

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/MNIST-CNN.git
cd MNIST-CNN
```

Install dependencies:

```bash
pip install torch torchvision matplotlib torchinfo wandb
```

---

## ⚙️ Data Preprocessing

Images are transformed using:

- Convert image to tensor
- Normalize pixel values

```python
transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize((0.5,), (0.5,))
])
```

---

## 📈 Training Configuration

| Parameter | Value |
|-----------|------:|
| Optimizer | Adam |
| Learning Rate | 0.01 |
| Weight Decay | 0.01 |
| Loss Function | CrossEntropyLoss |
| Batch Size | 32 |
| Epochs | 10 |

---

## 📊 Experiment Tracking

The project uses **Weights & Biases (W&B)** to monitor:

- Training Loss
- Training Accuracy
- Epoch Progress

---

## 📉 Visualization

Training progress is visualized using Matplotlib.

Metrics plotted:

- Training Accuracy
- Training Loss

---

## 📦 Model Summary

The model architecture is displayed using:

```python
from torchinfo import summary

summary(model, input_size=(1, 1, 28, 28))
```

---

## 📚 Concepts Practiced

- Convolutional Neural Networks (CNN)
- Image Classification
- Convolution Layers
- ReLU Activation
- Max Pooling
- Dropout
- Fully Connected Layers
- CrossEntropyLoss
- Adam Optimizer
- Mini-batch Training
- Experiment Tracking (W&B)
- Model Visualization

---

## 🔮 Future Improvements

- Add validation loop
- Evaluate on test dataset
- Save trained model
- Load pretrained model
- Confusion Matrix
- Precision, Recall, F1-Score
- Learning Rate Scheduler
- Early Stopping
- GPU / Apple Silicon (MPS) support

---

## 👨‍💻 Author

**Debajyoti Hazra**

BCA Student | Machine Learning & Deep Learning Enthusiast

Learning and building projects in:

- Machine Learning
- Deep Learning
- Computer Vision
- Natural Language Processing
- Generative AI
- Agentic AI

---

