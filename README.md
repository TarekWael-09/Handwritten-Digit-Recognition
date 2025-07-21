# 🧠 Handwritten Digit Recognition with TensorFlow/Keras

A deep learning project to classify handwritten digits using the MNIST dataset. This project demonstrates loading, training, evaluating, and visualizing a neural network built with TensorFlow/Keras.

---

## 🚀 Features

* Load and preprocess MNIST dataset
* Neural network architecture for classification
* Interactive prediction on single test samples
* Visualize:

  * Model accuracy and loss
  * Model prediction on test image
* Clean code and simple explanation

---

## 📊 Dataset

**MNIST Handwritten Digits**

* 70,000 grayscale images (28x28 pixels)

  * 60,000 for training
  * 10,000 for testing
* 10 classes (digits from 0 to 9)

---

## ⚙️ Getting Started

### Prerequisites

* Python 3.7 or later
* `pip` or other package manager

### 🔧 Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/handwritten-digit-recognition.git
cd handwritten-digit-recognition
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the classifier:

```bash
python mnist_classifier.py
```

---

## 🧠 Model Architecture

```
Input Image (28x28x1)
        ↓
Conv2D (64 filters, 3x3) → ReLU → MaxPooling2D (2x2)
        ↓
Conv2D (64 filters, 3x3) → ReLU → MaxPooling2D (2x2)
        ↓
Conv2D (64 filters, 3x3) → ReLU → MaxPooling2D (2x2)
        ↓
Flatten
        ↓
Dense (64) → ReLU
        ↓
Dense (32) → ReLU
        ↓
Dense (10) → Softmax
```

| Layer (type)         | Output Shape       | Param # |
| -------------------- | ------------------ | ------- |
| conv2d\_21 (Conv2D)  | (None, 26, 26, 64) | 640     |
| activation\_46       | (None, 26, 26, 64) | 0       |
| max\_pooling2d\_21   | (None, 13, 13, 64) | 0       |
| conv2d\_22 (Conv2D)  | (None, 11, 11, 64) | 36,928  |
| activation\_47       | (None, 11, 11, 64) | 0       |
| max\_pooling2d\_22   | (None, 5, 5, 64)   | 0       |
| conv2d\_23 (Conv2D)  | (None, 3, 3, 64)   | 36,928  |
| activation\_48       | (None, 3, 3, 64)   | 0       |
| max\_pooling2d\_23   | (None, 1, 1, 64)   | 0       |
| flatten\_8 (Flatten) | (None, 64)         | 0       |
| dense\_25 (Dense)    | (None, 64)         | 4,160   |
| activation\_49       | (None, 64)         | 0       |
| dense\_26 (Dense)    | (None, 32)         | 2,080   |
| activation\_50       | (None, 32)         | 0       |
| dense\_27 (Dense)    | (None, 10)         | 330     |
| activation\_51       | (None, 10)         | 0       |

**Total Parameters:** 81,066 (316.66 KB)
**Trainable Parameters:** 81,066
**Non-trainable Parameters:** 0

---

## 📈 Performance

The model achieved strong performance on the MNIST test dataset:

* **Test Loss:** 0.0579
* **Test Accuracy:** 98.33%

This indicates that the model generalizes well and effectively classifies handwritten digits with high precision.

---

## 🔍 Example Prediction

After training, you can enter a test index (0–9999):

```bash
Choose a test index (0–9999): 1543
```

Visual Output:

* **Expected**: `5`
* **Predicted**: `5`

---

## 📝 License

This project is open source and available under the MIT License.
