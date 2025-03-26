# XOR Gate Implementation Using NumPy and TensorFlow

This repository contains two different implementations of an XOR gate:  
1. **A handcrafted neural network using NumPy** (simulating logic gates with the sigmoid function).  
2. **A trainable neural network using TensorFlow/Keras** (learning XOR via a multi-layer perceptron).  

## 🚀 Under the Hood  

### 1️⃣ XOR Gate with NumPy (Manually Designed Neural Network)

This implementation simulates an XOR gate using a combination of logic gates (AND, OR, NAND). The core idea is to use a **sigmoid activation function** to approximate these gates.  

#### 🔢 **Mathematical Representation**  

Each gate is modeled using the function:  
\[
f(x_1, x_2) = \sigma(w_1 \cdot x_1 + w_2 \cdot x_2 + b)
\]
where:
- \( \sigma(z) = \frac{1}{1 + e^{-z}} \) is the sigmoid function.
- \( w_1, w_2 \) are weights.
- \( b \) is the bias.

#### 🏗 **Gate Combinations for XOR**
- **OR Gate:** Approximated with high positive weights.
- **NAND Gate:** Approximated with high negative weights.
- **AND Gate:** Used to combine results of OR and NAND to produce XOR.

##### **Truth Table Validation**
The implementation prints the XOR truth table:

| Input (x1, x2) | Output |
|---------------|--------|
| (0, 0)       | 0      |
| (0, 1)       | 1      |
| (1, 0)       | 1      |
| (1, 1)       | 0      |

### 2️⃣ XOR Gate with TensorFlow (Trainable Neural Network)

This implementation builds and trains a **2-layer feedforward neural network** using **TensorFlow/Keras**.

#### 📌 **Model Architecture**
- **Input Layer:** Takes 2 inputs (x1, x2).
- **Hidden Layer:** 2 neurons with **ReLU activation**.
- **Output Layer:** 1 neuron with **sigmoid activation** (binary classification).

#### 🎯 **Training**
- Loss function: **Binary Crossentropy**
- Optimizer: **Adam**
- Training for **1000 epochs**.

##### **Predictions**
After training, the model predicts the XOR output with high accuracy.

## 📦 Dependencies
Ensure you have the required dependencies installed:
```bash
pip install numpy tensorflow
