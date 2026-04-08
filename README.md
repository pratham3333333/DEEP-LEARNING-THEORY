Here are **Unit 1 — Elaborative Theory Answers (6 Marks Each)** 📘✍️
Written in **GitHub README format** so you can directly paste.

---

# 📘 Unit 1 – Linear Algebra (6 Marks Answers)

---

# 1. Mathematical Objects in Linear Algebra

## Definition

Linear algebra uses mathematical structures to represent data in deep learning and machine learning models.

## Types of Mathematical Objects

### 1. Scalar

A scalar is a single numerical value.
Example: 5, 3.14
Used for bias, learning rate.

### 2. Vector

A vector is a one-dimensional array of numbers.
Example:

```
v = [1, 2, 3]
```

Used to represent features.

### 3. Matrix

A matrix is a two-dimensional array of numbers.
Example:

```
A = [1 2
     3 4]
```

Used for weights.

### 4. Tensor

A tensor is a multi-dimensional array.
Example: Image data (height × width × channel)

## Applications

* Used in neural networks
* Used in feature representation
* Used in weight calculations

---

# 2. Matrix Multiplication and Properties

## Definition

Matrix multiplication is the process of multiplying rows of first matrix with columns of second matrix.

## Example

```
A = [1 2
     3 4]

B = [5 6
     7 8]

A × B = [19 22
         43 50]
```

## Types

* Matrix × Matrix
* Matrix × Vector
* Scalar × Matrix
* Element-wise multiplication

## Properties

1. Associative property → (AB)C = A(BC)
2. Distributive property → A(B+C) = AB + AC
3. Not commutative → AB ≠ BA
4. Identity matrix exists

## Applications

* Neural network forward pass
* Image transformations

---

# 3. Transpose Operation and Broadcasting

## Transpose Operation

Transpose converts rows into columns.

Example:

```
A =
1 2 3
4 5 6

Aᵀ =
1 4
2 5
3 6
```

## Broadcasting

Broadcasting allows operations on matrices of different sizes.

Example:

```
[1 2 3] + 2 = [3 4 5]
```

## Uses

* Matrix alignment
* Neural network calculations
* Adding bias values

---

# 4. Linear Combination, Dependence and Independence

## Linear Combination

A linear combination is formed by multiplying vectors with scalars and adding them.

```
v = a1v1 + a2v2
```

## Linear Dependence

Vectors are dependent if one vector can be expressed using others.

Example:

```
v2 = 2v1
```

## Linear Independence

Vectors are independent if none can be formed from others.

## Applications

* Feature selection
* Dimensionality reduction

---

# 5. Norm Operation and Properties

## Definition

Norm is used to measure magnitude or length of a vector.

## Types

### L1 Norm

```
||x||₁ = |x1| + |x2| + ... + |xn|
```

### L2 Norm

```
||x||₂ = √(x1² + x2² + ... + xn²)
```

### Infinity Norm

Maximum absolute value.

## Properties

1. Non-negative
2. Zero vector gives zero norm
3. Triangle inequality
4. Scaling property

## Applications

* Regularization
* Distance calculation

---

# 6. Eigen Decomposition

## Definition

Eigen decomposition expresses a matrix in terms of eigenvalues and eigenvectors.

```
Av = λv
```

Where
λ = eigenvalue
v = eigenvector

## Steps

1. Compute determinant
2. Solve characteristic equation
3. Find eigenvectors

## Applications

* PCA
* Dimensionality reduction
* Data compression

---

# 7. Problems Based on Eigen Decomposition

Example:

```
A = [2 0
     0 3]
```

Eigenvalues:

```
λ1 = 2
λ2 = 3
```

Eigenvectors:

```
[1 0]
[0 1]
```

## Steps

1. Solve det(A − λI) = 0
2. Find λ
3. Substitute and solve for vector

---

# 8. Problems Based on Norm

Example:

```
v = [1,2,3]
```

L1 Norm:

```
|1|+|2|+|3| = 6
```

L2 Norm:

```
√(1²+2²+3²) = √14
```

## Applications

* Feature scaling
* Regularization
* Similarity measurement

---

# 9. Derivatives in Eigen Decomposition

## Definition

Derivative of eigenvalues is used in optimization problems.

Formula:

```
dλ/dx = vᵀ (dA/dx) v
```

## Uses

* Backpropagation
* Optimization
* Deep learning training

## Applications

* Neural networks
* Computer vision
* Signal processing

---
Here is **📘 Unit 2 — Elaborative Answers with Examples (6 Marks, GitHub README Format)** ✍️💻
Structured for **theory exam writing**.

---

# 📘 Unit 2 – Optimization and Activation Functions

---

# 1. Loss Function and Loss Functions Used in Regression

## Definition

A loss function measures the difference between actual output and predicted output. It helps in evaluating model accuracy.

## Types of Regression Loss Functions

### Mean Squared Error (MSE)

Formula:

```
MSE = (1/n) Σ (yi − ŷi)²
```

### Example

Actual Price = [100, 200]
Predicted Price = [110, 190]

```
MSE = ((100-110)² + (200-190)²)/2
    = (100 + 100)/2
    = 100
```

### Mean Absolute Error (MAE)

```
MAE = (1/n) Σ |yi − ŷi|
```

Example:

```
MAE = (10 + 10)/2 = 10
```

### Applications

* House price prediction
* Temperature prediction

---

# 2. Loss Functions Used in Classification

## Binary Cross Entropy

Used for binary classification.

```
L = -(y log(p) + (1-y) log(1-p))
```

### Example

Actual = 1
Predicted = 0.8

```
L = -(1 log(0.8)) = 0.22
```

## Categorical Cross Entropy

Used in multi-class classification.

Example:

```
Actual = [1,0,0]
Predicted = [0.7,0.2,0.1]

Loss = -log(0.7)
```

### Applications

* Spam detection
* Sentiment analysis

---

# 3. Activation Function and Linear Activation Function

## Definition

Activation function decides whether neuron should be activated.

## Linear Activation Function

```
f(x) = x
```

### Example

Input = 5
Output = 5

### Limitation

Multiple layers behave like single layer.

### Use Case

* Regression output layer

---

# 4. ReLU and Sigmoid Activation Function

## ReLU

```
f(x) = max(0, x)
```

### Example

Input: [-2, 3, 5]

Output:

```
[0, 3, 5]
```

### Advantages

* Fast computation
* Avoids vanishing gradient

---

## Sigmoid Function

```
f(x) = 1/(1 + e^-x)
```

### Example

Input = 0

```
Output = 0.5
```

### Applications

* Binary classification
* Probability output

---

# 5. Steps of Gradient Descent Algorithm

## Definition

Gradient descent minimizes loss by updating weights.

## Steps

1. Initialize weights
2. Forward pass
3. Calculate loss
4. Backpropagation
5. Update weights
6. Repeat

Weight Update:

```
W = W - α ∂L/∂W
```

### Example

Initial weight = 5
Gradient = 0.2
Learning rate = 0.1

```
W = 5 - (0.1 × 0.2)
W = 4.98
```

---

# 6. Types of Gradient Descent

## Batch Gradient Descent

Uses full dataset.

Example:
1000 samples → update once.

## Stochastic Gradient Descent

Uses one sample.

Example:
Update after each sample.

## Mini Batch Gradient Descent

Uses small batch.

Example:
Batch size = 32

Most commonly used in deep learning.

---

# 7. L1 and L2 Regularization

## L1 Regularization

```
Loss = Loss + λ Σ |w|
```

Example:
Weights = [2, -3]

```
L1 = |2| + |3| = 5
```

## L2 Regularization

```
Loss = Loss + λ Σ w²
```

Example:

```
L2 = 4 + 9 = 13
```

### Use

* Prevents overfitting
* Controls model complexity

---

# 8. Early Stopping

## Definition

Training stops when validation loss increases.

### Example

Epoch 1 → Loss 0.5
Epoch 2 → Loss 0.4
Epoch 3 → Loss 0.35
Epoch 4 → Loss 0.37 (Stop here)

Best model = Epoch 3

### Advantages

* Saves time
* Prevents overfitting

---

# 9. Terms Explanation

## Regularization

Adds penalty to reduce overfitting.

Example:
Large weights reduced.

## Underfitting

Model too simple.

Example:
Linear model for complex data.

## Overfitting

Model memorizes training data.

Example:
100% training accuracy, poor test accuracy.

## Dataset Augmentation

Increasing data artificially.

Examples:

* Rotate image
* Flip image
* Add noise

---

# 10. Multi-task Learning

## Definition

Single model performs multiple tasks.

## Example

Face detection model predicts:

* Age
* Gender
* Emotion

Architecture:

```
Input → Shared Layers → Age
                     → Gender
                     → Emotion
```

## Advantages

* Shared learning
* Better accuracy
* Reduced training time

---
Here is **📘 Unit 3 — Elaborative Answers with Examples (6 Marks, GitHub README Format)** ✍️💻
Focused for **theory exam writing**.

---

# 📘 Unit 3 – CNN, RNN and Transfer Learning

---

# 1. Convolutional Neural Network (CNN)

## Definition

A Convolutional Neural Network (CNN) is a deep learning model used for processing image data. It automatically extracts features using convolution filters.

## Architecture

Input → Convolution → ReLU → Pooling → Fully Connected → Output

## Example

Image classification (Cat vs Dog)

* Input image: 64×64
* CNN extracts edges, shapes, textures
* Final output: Cat

## Applications

* Image recognition
* Face detection
* Medical imaging

---

# 2. Types of Pooling

## Max Pooling

Selects maximum value.

Example:

```
[1 3
 2 4] → 4
```

## Average Pooling

Takes average value.

Example:

```
(1+3+2+4)/4 = 2.5
```

## Min Pooling

Selects minimum value.

Example:

```
→ 1
```

## Use

* Reduce image size
* Reduce computation

---

# 3. Pre-trained Model and Fine-Tuning

## Definition

A pre-trained model is a model trained on large dataset and reused.

Examples:

* ResNet
* VGG
* MobileNet

## Fine-Tuning Steps

1. Load pre-trained model
2. Freeze initial layers
3. Train last layers
4. Adjust weights

## Example

Use pre-trained model for:

* Dog vs Cat classification
* Instead of training from scratch

## Advantages

* Less data required
* Faster training

---

# 4. Transfer Learning

## Definition

Transfer learning uses knowledge from one task to solve another.

## Example

Model trained on ImageNet → used for medical image classification.

## Steps

1. Load trained model
2. Replace output layer
3. Train new dataset

## Benefits

* Reduced training time
* Better accuracy

---

# 5. Architecture of CNN

## Layers

1. Input Layer
2. Convolution Layer
3. Activation (ReLU)
4. Pooling Layer
5. Fully Connected Layer
6. Output Layer

## Example

Image → Edge detection → Feature extraction → Classification

## Uses

* Object detection
* Handwriting recognition

---

# 6. Architectures of RNN

## Architecture 1 — One to One

Example: Image classification

Input → Output

## Architecture 2 — One to Many

Example: Image captioning

Image → "A dog running"

## Architecture 3 — Many to One

Example: Sentiment analysis

Words → Positive

---

# 7. FNN vs RNN

| FNN               | RNN              |
| ----------------- | ---------------- |
| No memory         | Has memory       |
| Independent input | Sequential input |
| Used for images   | Used for text    |
| Fast              | Slower           |

## Applications of RNN

* Speech recognition
* Language translation
* Chatbots

Example:
Input: "I love AI" → Positive sentiment

---

# 8. Architecture of LSTM

## Definition

LSTM is special RNN that solves vanishing gradient problem.

## Components

* Forget Gate
* Input Gate
* Output Gate
* Cell State

## Example

Sentence prediction:
"I am going to" → "school"

LSTM remembers long-term dependency.

## Applications

* Text generation
* Speech recognition

---

# 9. Teacher Forcing Architecture

## Definition

Teacher forcing uses actual output as next input during training.

## Example

Sequence:
Input: "I am"
Actual: "happy"

Model uses "happy" instead of predicted word.

## Advantage

* Faster convergence
* Better training

---

# 10. Bidirectional RNN and Deep RNN

## Bidirectional RNN

Processes sequence in both directions.

Example:
Sentence:
"I am happy today"

Uses past + future context.

## Deep RNN

Multiple RNN layers stacked.

Example:
Layer1 → word features
Layer2 → sentence meaning

## Applications

* Language translation
* Speech recognition

---

Here is **📘 Unit 4 — Elaborative Answers with Examples (6 Marks, GitHub README Format)** ✍️💻
Useful for **theory exam writing**.

---

# 📘 Unit 4 – Autoencoders, GANs, Transformers

---

# 1. Autoencoder and Architecture

## Definition

An Autoencoder is a neural network used to learn compressed representation of input data.

## Architecture

Input → Encoder → Bottleneck → Decoder → Output

## Example

Input Image: 28×28
Compressed to: 64 features
Reconstructed output: same image

## Working

1. Encoder reduces dimension
2. Bottleneck stores features
3. Decoder reconstructs data

## Applications

* Image compression
* Noise removal
* Feature learning

---

# 2. Sparse Autoencoder and Denoising Autoencoder

## Sparse Autoencoder

* Uses fewer active neurons
* Encourages feature learning

### Example

Only few neurons active for digit recognition.

## Denoising Autoencoder

* Removes noise from data

### Example

Input: noisy image
Output: clean image

```
Noisy → Encoder → Decoder → Clean
```

## Applications

* Image denoising
* Feature extraction

---

# 3. Boltzmann Machine and Energy-Based Model

## Boltzmann Machine

A stochastic neural network used for learning probability distribution.

## Components

* Visible units
* Hidden units

## Example

Recommendation system:
Input → user preferences
Output → recommended movie

## Energy-Based Model

Assigns energy to each configuration.

Lower energy = better prediction

## Applications

* Collaborative filtering
* Feature learning

---

# 4. GAN Architecture

## Definition

GAN consists of two networks:

* Generator
* Discriminator

## Architecture

Generator → Fake Data → Discriminator
Real Data → Discriminator

## Example

Generator creates fake faces
Discriminator detects real vs fake

## Working

1. Generator produces fake data
2. Discriminator evaluates
3. Both networks improve

## Applications

* Image generation
* Deepfake creation
* Data augmentation

---

# 5. Types of GAN

## Vanilla GAN

Basic GAN structure.

## DCGAN

Uses convolution layers.

## Conditional GAN

Generates output based on condition.

Example:
Input: label "dog" → output dog image

## CycleGAN

Image-to-image translation.

Example:
Horse → Zebra

---

# 6. Diffusion Model Architecture

## Definition

Diffusion models generate data by gradually removing noise.

## Steps

1. Add noise to data
2. Train model
3. Remove noise step-by-step
4. Generate image

## Example

Random noise → realistic image generation

## Applications

* AI art generation
* Image synthesis

---

# 7. Word Embedding

## Definition

Word embedding converts words into vectors.

## Example

```
King → [0.25, 0.61, 0.12]
Queen → [0.27, 0.59, 0.11]
```

Similar words have similar vectors.

## Popular Methods

* Word2Vec
* GloVe

## Applications

* NLP tasks
* Chatbots
* Text classification

---

# 8. Working of Transformers

## Definition

Transformer is deep learning model based on self-attention.

## Architecture

Input → Embedding → Attention → Feed Forward → Output

## Example

Sentence translation:
"I love AI" → "मैं AI से प्यार करता हूँ"

## Advantages

* Parallel processing
* Long sequence handling

## Applications

* Language translation
* Chatbots
* Text generation

---

# 9. Vanilla Autoencoder and Multi-layer Autoencoder

## Vanilla Autoencoder

Single hidden layer.

Example:
Input → Hidden → Output

## Multi-layer Autoencoder

Multiple hidden layers.

Example:
Input → Layer1 → Layer2 → Output

## Difference

| Vanilla       | Multi-layer   |
| ------------- | ------------- |
| Simple        | Complex       |
| Less features | Deep features |
| Fast          | Accurate      |

## Applications

* Feature extraction
* Dimensionality reduction

---
