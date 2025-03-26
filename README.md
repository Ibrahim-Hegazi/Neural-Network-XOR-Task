# XOR Gate Implementation Using NumPy and TensorFlow

## Table of Contents
- [Introduction](#introduction)
- [Manual Implementation](#manual-implementation)
- [TensorFlow Implementation](#tensorflow-implementation)
- [How It Works](#how-it-works)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Why This Matters](#why-this-matters)

---

## 📝 Introduction

This repository demonstrates two ways to implement an **XOR gate** using **Neural Networks**:
1. **A handcrafted implementation using NumPy** that mimics logic gates.
2. **A trainable neural network using TensorFlow/Keras** that learns XOR through training.

The XOR function is a fundamental example of **non-linearly separable** problems, making it an ideal starting point for understanding neural networks.

---

## ⚙️ Manual Implementation

The first approach manually simulates an XOR gate using logic gates implemented with the **sigmoid activation function**. 

### 🏗 How It Works:
- **Logic Gates:** XOR can be created using **NAND, OR, and AND** gates.
- **Sigmoid Activation:** Used to approximate these logic gates.
- **Layered Computation:** The first layer computes OR and NAND, and the second layer applies an AND operation.

### 📌 Mathematical Representation:
Each gate follows the equation:
\[
f(x_1, x_2) = \sigma(w_1 \cdot x_1 + w_2 \cdot x_2 + b)
\]
where:
- \( \sigma(z) = \frac{1}{1 + e^{-z}} \) (Sigmoid function)
- \( w_1, w_2 \) are weights
- \( b \) is a bias term

### ✅ XOR Truth Table:
| x1 | x2 | XOR Output |
|----|----|-----------|
| 0  | 0  | 0         |
| 0  | 1  | 1         |
| 1  | 0  | 1         |
| 1  | 1  | 0         |

---

## 🤖 TensorFlow Implementation

The second approach uses **TensorFlow/Keras** to build a **feedforward neural network** that learns XOR through training.

### 🏗 Neural Network Architecture:
- **Input Layer:** Two neurons (for x1 and x2).
- **Hidden Layer:** Two neurons with **ReLU activation**.
- **Output Layer:** One neuron with **Sigmoid activation**.

### 🏋️ Training Details:
- **Loss Function:** Binary Crossentropy
- **Optimizer:** Adam
- **Epochs:** 1000

After training, the model learns to correctly predict the XOR function.

---

## 🔬 How It Works

### Manual XOR Logic:
1. Compute **OR** and **NAND** of inputs.
2. Use an **AND** gate to combine these results.
3. The final output follows the XOR pattern.

### TensorFlow XOR Learning:
1. The model initializes with **random weights**.
2. It **adjusts weights** using backpropagation and gradient descent.
3. Over **1000 training epochs**, it learns the XOR pattern.

---

## 🛠 Installation

Ensure you have the required dependencies installed:

```bash
pip install numpy tensorflow
