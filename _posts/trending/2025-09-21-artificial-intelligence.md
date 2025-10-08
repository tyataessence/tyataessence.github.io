---
layout: default
title: "What is Artificial Intelligence?"
date: 2025-09-21
categories: [Trending]
author: Rakesh Tyata
---

# <span style="color:#1f77b4;">Artificial Intelligence (AI)</span>

Artificial Intelligence is the science and technology of creating computer systems, that makes machines "intelligent" with ability to learn, understand and apply knowledge. When you see a cloudy sky, your brain predicts whether it might rain — that’s your natural intelligence at work. Similarly, Artificial Intelligence (AI) is about making machines act smart like the human brain: learning, reasoning, solving problems, understanding language, recognizing images, and making decisions.

💡 Let me further break down this concept, by comparing with Pet Dog.

- Dog learns to sit and fetch, through repeated commands and rewards. Likewise, AI learns from large amount of data with feedback on what's right and wrong. This refers AI **training**.
- Dog starts to recognize cues like hand signals, tone of voice. Similarly AI recognizes **patterns** in data (images, words, numbers)
- Trained Dog performs the command when asked. Likewise, AI gives an **answer, prediction or action** when prompted.

💡 Artificail Intelligence is a massive topic. To explore further, let me compare it with onion, that is commonly used as ingredients while cooking food.

- Assuming the entire onion as **Artifical Intelligence**, if you peel few layers then the remaining onion becomes **Machine Learning** (ML is subset of AI).
- Next peel few more layers, then it becomes **Neural Network** (NN is subset of ML).
- Peel few more layers again, then it becomes **Deep Learning** (DL is subset of NN).
- Each of these topics (ML, NN, DL) have different variant layers.

---

## <span style="color:#ff7f0e;">Machine Learning (ML)</span>

Machine Learning (ML) is a branch of Artificial Intelligence where machine (model) learn patterns from data and improve their performance on tasks without being explicitly programmed.

💡 Example: Instead of hard-coding rules to detect spam emails, you feed a model thousands of emails labeled “spam” or “not spam.” The model then learns the patterns and can classify new emails on its own.

Based on the training approach or strategy, here are some of the most common types of Machine Learning:

- **Supervised Learning:** Learn and trained from labeled data. For example, Image classification, speech recognition, spam detection, prediction house prices etc.
- **Unsupervised Learning:** Learn and trained from unlabeled data, finding hidden patterns or structures. For example, Autoencoders, clustering with embeddings, Customer Segmentation, Fraud Detection.
- **Semi Supervised Learning:** Learn and trained from small amount of labeled data + large amount of unlabeled data. For example, Medical Imaging, where labeled data is scarce.
- **Self Supervised Learning:** Learn and trained from labels, which are generated automatically from the data itself. For example, Language models (predicting the next word)
- **Reinforcement Learning:** Learn and trained by trial and error, guided by rewards or penalties. For example, robotics control. Types are - Value-Based, Policy-Based, Actor-Critic (Combined value-based and policy-based)

---

## <span style="color:#17becf;">Neural Networks (NN)</span>

Neural Network is a type of machine learning model inspired by the structure of the human brain. It consist of layers of interconnected “neurons” (mathematical units) that process data by applying weights and activations to detect patterns and make predictions.

💡 Example: A neural network can take an image of a cat, process it through several layers, and correctly identify it as a cat by recognizing patterns like shapes, edges, and textures.

Based on the Model Architecture, here are some of the most common types of Neural Networks:

- **Feedforward Nerual Networks (FNN):** The simplest type, layers of neurons with no loops and also known as Multi layer Perceptions (MLPs). The data flows only in one direction - from input layer -> hidden layers -> output layer.
- **Convolution Neural Networks (CNN):** Extract spatial features using filters and used in image data such as (images, video, medical scan).
- **Recurrent Neural Networks (RNN):** Each time it process an input, it maintain memory across time step known as hidden state, along with the output. Both output and hidden state is passed to next time. Good for sequence data such as (time series, text, speech). Variants are Long Short Term Memory (LSTM) - preserver memory for long periods of time using gates, Gated Recuurent Unit (GRU) - simplified LSTM with fewer gates, making it faster.
- **Transformers:** Handle sequential data with attention mechanisms (weighted importance of different inputs). Back bone of modern Natural Language Processing NLP (BERT, GTP).
- **Generative Models:** Learn patterns from data and can generate new, similar data. Instead of predicting a label, it create new samples like text, images, audio etc.Variants are Generative Adversarial Networks (GANs) - generate realistic images and videos, Variational Autoencoders (VAEs) - compress/reconstruct data, Diffusion Models - create data by reverse process, to denoise it into a realistic data.
- **Graph Neural Networks:** Work with graph-structured data (social, networks, molecules)
- **Hybrid Architectures:** Combinations (e.g. CNN + RNN, Transformer + GNN)

---

## <span style="color:#1f77b4;">Deep Learning (DL)</span>

Deep Learning is subset of Machine Learning, that uses neural networks with many layers (hence deep) to model complex patterns in data. Each layer transforms its input into a more abstract representation, allowing the network to learn hierarchical features.

Base on the purpose, here are some of the most common types of Deep Learning:

- **Discriminative Models:** Focus on classificiation or regression.
- **Generative Models:** Create new data, from input data like (images, text, autio)
- **Representation Learning:** Learn useful features (embeddings or representations) from raw data.
- **Deep Reinforement Learning:** Combination of deep learning and reinforcement learning.

---

### <span style="color:#2ca02c;">Key Notes</span>

- **Training:** Learning patterns from data.
- **Inference:** Applying learned patterns to make predictions.
- **Neuron:** Takes input values, applies weights, adds bias and passes through an activation fuction, to predict the output.
- **Activation Function:** Decides if a neuron should fire or pass its signal forward.
- **Loss Function:** The difference between the expected (true) output and the model’s predicted output.
- **Epoch:** One full pass of training data through the model.
- **Overfitting:** When a model memorizes training data and fails on new data.
- **Underfitting:** When a model is too simple and cannot capture the underlying patterns.
- **Bias:** A parameter that allows the model to shift the activation function.
- **Dropout:** Randomly turning off neurons during training to improve generalization.
- **Gradient:** The derivative of the loss function w.r.t model parameters, used to update weights.
- **Optimizer:** Algorithm that adjusts the model’s weights to minimize the loss (e.g., SGD, Adam).

```
Artificial Intelligence (AI) - Make machines "intelligent" (simulate human decision-making)
 └── Machine Learning (ML) - Machines learn patterns from data without explicit programming
      ├── Supervised Learning - Learn from labeled examples to predict outcomes
      │     ├── Types:
      │     │     ├── Regression (Linear, Logistic) - Predict continuous or categorical outcomes
      │     │     ├── Decision Trees - Split data for predictions
      │     │     ├── SVM - Classify with hyperplanes
      │     │     └── kNN - Classify based on nearest neighbors
      │     └── Examples: Predicting house prices, spam detection
      │
      ├── Unsupervised Learning - Discover hidden patterns in unlabeled data
      │     ├── Types:
      │     │     ├── Clustering (K-Means, Hierarchical) - Group similar data
      │     │     ├── Dimensionality Reduction (PCA, t-SNE) - Reduce features
      │     │     └── Anomaly Detection - Detect unusual data points
      │     └── Examples: Customer segmentation, fraud detection
      │
      ├── Neural Networks (NN) - Models inspired by the brain for pattern recognition
      │     ├── Types:
      │     │     ├── Feedforward NN - Basic layered network
      │     │     ├── CNN - Processes images
      │     │     └── RNN (LSTM, GRU) - Processes sequences
      │     └── Examples: Handwriting recognition, image classification
      │
      │     └── Deep Learning (DL) - Neural networks with many layers for complex patterns
      │           ├── Types / Approaches:
      │           │     ├── Discriminative Models - Classification or regression
      │           │     ├── Generative Models - Create new data
      │           │     └── Representation Learning - Automatically learn useful features
      │           └── Examples: Face recognition, voice assistants, GPT models
      │
      └── Reinforcement Learning (RL) - Learn by trial and error with rewards
            ├── Types:
            │     ├── Value-based (Q-Learning, SARSA) - Learn state values
            │     ├── Policy-based (Policy Gradient) - Learn action policies
            │     └── Actor-Critic - Combines both approaches
            └── Examples: AlphaGo, robot navigation, Deep RL using neural networks

```
