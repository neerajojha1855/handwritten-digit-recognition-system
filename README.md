# ✍️ Handwritten Digit Recognition System

A deep learning application that recognizes handwritten digits (0–9) in real time using a Convolutional Neural Network (CNN) trained on the MNIST dataset. Draw a digit on the canvas and the model predicts it instantly.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange?logo=tensorflow)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 Features

- **CNN Model** — Trained on 60,000 MNIST images with ~99% test accuracy
- **Interactive GUI** — Draw digits on a Tkinter canvas and get instant predictions
- **Confidence Score** — Displays the predicted digit along with its confidence percentage
- **Lightweight** — Minimal dependencies, runs entirely on CPU

---

## 🏗️ Project Structure

```
├── model.py               # Trains the CNN model and saves it as mnist_h5.keras
├── digit_recognizer.py    # GUI application for real-time digit recognition
├── requirements.txt       # Python dependencies
├── .gitignore             # Git ignore rules
└── README.md              # Project documentation
```

---

## 🧠 Model Architecture

The CNN model is built using Keras Sequential API:

| Layer              | Details                          |
|--------------------|----------------------------------|
| Conv2D             | 32 filters, 3×3 kernel, ReLU     |
| Conv2D             | 64 filters, 3×3 kernel, ReLU     |
| MaxPooling2D       | 2×2 pool size                    |
| Dropout            | 25%                              |
| Flatten            | —                                |
| Dense              | 256 units, ReLU                  |
| Dropout            | 50%                              |
| Dense (Output)     | 10 units, Softmax                |

- **Optimizer:** Adadelta
- **Loss Function:** Categorical Crossentropy
- **Epochs:** 10 | **Batch Size:** 128

---

## 🚀 Getting Started

### Prerequisites

- Python 3.x
- Windows OS (required for `pywin32` screen capture)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/neerajojha1855/handwritten-digit-recognition-system.git
   cd handwritten-digit-recognition-system
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🎯 Usage

### Step 1 — Train the Model

```bash
python model.py
```

This trains the CNN on the MNIST dataset and saves the model as `mnist_h5.keras`.

### Step 2 — Run the Digit Recognizer

```bash
python digit_recognizer.py
```

- **Draw** a digit on the white canvas using your mouse
- Click **"Recognize"** to predict the digit
- Click **"Clear"** to reset the canvas

---

## 📊 Results

After training for 10 epochs, the model achieves:

| Metric        | Score   |
|---------------|---------|
| Test Accuracy | ~99%    |
| Test Loss     | ~0.03   |

---

## 🛠️ Tech Stack

- **Python** — Core programming language
- **TensorFlow / Keras** — Deep learning framework
- **NumPy** — Numerical computation
- **Pillow** — Image processing
- **Tkinter** — GUI framework
- **pywin32** — Windows screen capture

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

<p align="center">Made with ❤️ by <a href="https://github.com/neerajojha1855">Neeraj Ojha</a></p>
