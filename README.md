# Real-Time ASL Alphabet Interpreter

A deep learning application that translates American Sign Language (ASL) finger spelling into text in real-time. This project compares three distinct neural network architectures—a custom CNN, VGG16, and ResNet50—to find the optimal balance between accuracy and computational efficiency for live deployment.

## 📺 Project Demo

[![Live Demo Video](https://img.youtube.com/vi/L49sLVS_gpg/maxresdefault.jpg)](https://www.youtube.com/watch?v=L49sLVS_gpg)

[Watch my YouTube Video](https://www.youtube.com/watch?v=L49sLVS_gpg)

## 🚀 Key Features
* **Real-Time Translation:** Translates hand gestures to text instantly using OpenCV and TensorFlow.
* **Robust Accuracy:** Achieved **93.08% Test Accuracy** using Transfer Learning with ResNet50.
* **Ambiguity Resolution:** Specifically engineered to distinguish between visually similar signs (e.g., 'T' vs. 'N') using deep residual connections.
* **Comparative Study:** Includes code for three different architectures to demonstrate the progression from baseline to state-of-the-art.

## 🧠 Model Architectures
We implemented and evaluated three models to solve this problem:

1.  **Baseline CNN:** A custom convolutional network built from scratch. Served as a performance baseline (72.54% Accuracy).
2.  **VGG16 (Transfer Learning):** Leveraged pre-trained weights from ImageNet. Improved feature extraction but was computationally expensive.
3.  **ResNet50 (Final Solution):** The best-performing model. Uses residual connections (skip connections) to learn fine-grained spatial details, crucial for ASL nuances.

| Metric | Baseline CNN | VGG16 | ResNet50 |
| :--- | :---: | :---: | :---: |
| **Test Accuracy** | 72.54% | 79.76% | **93.08%** |
| **Training Time** | 30 mins | 123 mins | 94 mins |

## 📂 Project Structure

```bash
├── ai-baseline-cnn.ipynb       # Code for training the custom CNN from scratch
├── ai-vgg.ipynb                # Code for VGG16 implementation with Fine-Tuning
├── ai-resnet.ipynb             # Code for ResNet50 (Best Model)
├── app.ipynb                   # The live web application using OpenCV
└── README.md
