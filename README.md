## Building a Neural Network from Scratch for Fashion-MNIST

#### Pre-processing Steps:
- 1: Load Fashion MNIST Data
- 2: Normalize Data
- 3: Transpose and Reshape X data
- 4: One-hot encode the y-data 
- 5: Initialize Weights and Biases Matrices

#### Neural Network Steps:
- 1: Forward Propogation
- 2: Back Propogation
- 3: Update Parameters



## Math for Forward Propagation

$$
Z^{[1]} = W^{[1]}X + b^{[1]}
$$

$$
A^{[1]} = g_{\text{ReLU}}(Z^{[1]})
$$

$$
Z^{[2]} = W^{[2]}A^{[1]} + b^{[2]}
$$

$$
A^{[2]} = g_{\text{softmax}}(Z^{[2]})
$$

---

## Math for Backward Propagation

$$
dZ^{[2]} = A^{[2]} - Y
$$

$$
dW^{[2]} = \frac{1}{m} dZ^{[2]} A^{[1]T}
$$

$$
db^{[2]} = \frac{1}{m} \sum dZ^{[2]}
$$

$$
dZ^{[1]} = W^{[2]T} dZ^{[2]} \cdot g'^{[1]}(Z^{[1]})
$$

$$
dW^{[1]} = \frac{1}{m} dZ^{[1]} A^{[0]T}
$$

$$
db^{[1]} = \frac{1}{m} \sum dZ^{[1]}
$$

---

## Math for Parameter Updates

$$
W^{[2]} := W^{[2]} - \alpha dW^{[2]}
$$

$$
b^{[2]} := b^{[2]} - \alpha db^{[2]}
$$

$$
W^{[1]} := W^{[1]} - \alpha dW^{[1]}
$$

$$
b^{[1]} := b^{[1]} - \alpha db^{[1]}
$$

---
