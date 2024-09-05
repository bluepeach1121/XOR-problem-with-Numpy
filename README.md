# XOR-problem
 Training a neural network to approximate the XOR function,  demonstrating a neural network's ability to learn non-linear patterns.

 
<p>A dataset is said to be linearly separable if there exists a straight line (in 2D), a plane (in 3D), or a hyperplane (in higher dimensions) that can perfectly separate the classes.</p>

### Problem with Single-Layer Perceptron and XOR

#### 1. Understanding the Single-Layer Perceptron

A single-layer perceptron is a type of linear classifier that makes its predictions based on a linear combination of its input features. It has the following structure:

- **Input Layer**: Takes input features (in the case of XOR, two binary inputs).
- **Output Layer**: Produces a single output, which is a weighted sum of the inputs followed by an activation function (usually a step function or sigmoid for binary classification).

The perceptron updates its weights based on the error in its predictions during training, attempting to find a hyperplane (a line in 2D, a plane in 3D, etc.) that separates the data points into their respective classes.

#### 2. XOR Problem Recap

The XOR (exclusive OR) function outputs 1 if the inputs are different and 0 if they are the same. Here’s the XOR truth table:

| Input 1 | Input 2 | XOR Output |
|---------|---------|------------|
| 0       | 0       | 0          |
| 0       | 1       | 1          |
| 1       | 0       | 1          |
| 1       | 1       | 0          |

If we plot these points on a 2D plane, we observe:

- Points \((0, 0)\) and \((1, 1)\) correspond to output 0.
- Points \((0, 1)\) and \((1, 0)\) correspond to output 1.

#### 3. Linear Separability and the XOR Problem

A dataset is said to be **linearly separable** if there exists a straight line (in 2D), a plane (in 3D), or a hyperplane (in higher dimensions) that can perfectly separate the classes.

- **Linear Separability**: Points that can be separated into two groups using a straight line.
- **Non-linear Separability**: Points that cannot be separated into two groups using a straight line.

**For XOR**, there is no single straight line that can separate the points \((0, 0)\) and \((1, 1)\) from \((0, 1)\) and \((1, 0)\).

#### 4. Why the Single-Layer Perceptron Fails with XOR

- **Linear Classification**: A single-layer perceptron is essentially a linear classifier. It can only learn decision boundaries that are linear.
- **Non-Linear Decision Boundary Required**: The XOR function requires a non-linear decision boundary. To separate the XOR outputs correctly, you need at least two linear boundaries (or a single non-linear curve).
- **Inability to Learn XOR**: A single-layer perceptron will fail to converge on a solution for the XOR problem because it cannot find a linear hyperplane that correctly separates the outputs (0 and 1).

- 
There is no way to draw a single straight line that separates the two classes without misclassifying at least one point.

### 5. Solution: Use a Multi-Layer Perceptron (MLP)

A **multi-layer perceptron (MLP)**, also known as a neural network with at least one hidden layer, can solve the XOR problem because:

- **Non-Linear Activation Functions**: Hidden layers with non-linear activation functions (such as Sigmoid, ReLU, or Tanh) enable the network to learn non-linear decision boundaries.
- **Multiple Layers**: By combining multiple layers, the network can transform the input space in such a way that the problem becomes linearly separable in a higher-dimensional space.

For the XOR problem, a neural network with:

- **Input Layer**: 2 neurons (for two inputs).
- **Hidden Layer**: At least 2 neurons with a non-linear activation function.
- **Output Layer**: 1 neuron with a Sigmoid activation function.

This setup allows the network to learn a function that correctly maps all XOR inputs to their respective outputs by forming a non-linear decision boundary.
