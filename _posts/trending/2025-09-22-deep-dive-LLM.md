---
layout: default
title: "What is LLM?"
date: 2025-09-22
categories: [Trending]
tags: [LLM, Tensor, Trending]
author: Rakesh Tyata
---

**LLM** Large Language Model is a type of neural network designed to understand and generate human-like text. It consists of many layers stacked together, each performing mathematical transformations on the data. LLMs learn patterns from vast text data during training and store that knowledge in their weights. Example: **GPT models, BERT, T5**

💡 Analogy: LLM = a giant brain that processes sequences of words to predict the next word or generate text.

A **layer** is a building block in a neural network. By **stacking many layers** together, you create the full model (like an LLM). This is why LLMs are often called deep learning models — **deep** just means "many layers stacked". A layer takes an **input tensor**, applies mathematical operations (like matrix multiplication + activation), and produces an **output tensor**.

💡 Analogy: A layer is like an organ in your body that transforms incoming energy or material and passes it on to the next organ for further processing.

A **tensor** is a multi-dimensional array (1D = vector, 2D = matrix, 3D+ = higher-order), used to represent all data inside a neural network (input, output, activations and weigths). Frameworks like **PyTorch** and **TensorFlow** treat everything (inputs, weights, and activations) as **tensors**. Examples:

- **Embedding Matrix:** 2D tensor: (vocab_size × embedding_dim)

  ````
  # Each row = a word in the vocab
  embedding_matrix = [
     [0.11, -0.23, 0.45, 0.67], # word 1
     [0.09, 0.88, -0.33, 0.12]  # word 2
  ]```

  ````

- **Attention Weights:** 3D tensor: (batch × sequence_length × attention_dim)

  ````
  # Each batch has a sequence of tokens, each token has attention weights
  attention_weights = [
     [
        [0.1, 0.2, 0.3, 0.4],  # token 1
        [0.5, 0.6, 0.7, 0.8],  # token 2
        [0.9, 1.0, 1.1, 1.2],  # token 3
     ]
  ]```

  ````

- **Transformer Feedforward:** 2D/3D tensor: (input_dim × hidden_dim)
  ````
     # 2D weight matrix: connects input to hidden neurons
     feedforward_weights = [
        [0.12, 0.34, 0.56, 0.78],  # input feature 1 → hidden 4
        [0.90, 0.11, 0.22, 0.33],  # input feature 2 → hidden 4
        [0.44, 0.55, 0.66, 0.77],  # input feature 3 → hidden 4
     ]```
  ````

💡 Analogy: A tensor is like blood flowing through your body and it carries oxygen, nutrients, and signals to different organs.

![LLM Diagrams]({{ '/assets/images/llm_diagrams.jpg' | relative_url }})

---

## 🧠 Memory in LLMs

LLM includes 2 types of memory. **Short-Term Memory (Context Window)** and **Long-Term Memory**.

### Short-Term Memory (Context Window)

The **context window** is a memory optimization technique and it stores the computed keys (K) and values (V) from the model's self attention layers for previoulsy generated tokens in a sequence. By **reusing these cached K-V pairs** for subsequent tokens, the LLM avoids redundant computation, making generation faster. For example, **GPT-3.5**: ~4K tokens in KV cache, **GPT-4**: ~128K tokens in KV cache

The LLMs like ChatGPT use multi tiered caching strategy.

- **GPU Memory (VRAM):** Stores active and frequently used data for minimal latency (expensive but fast).
- **CPU Memory (RAM or SSD):** Keeps less active, less frequently used data.
- **Distributed Cache (e.g., Redis):** Holds specific conversation history or session data.

### Long-Term Memory

The **long-term memory** (like remembering a user across sessions), that’s not in the LLM’s weights. Instead, the system (like ChatGPT) stores the information externally in (vector DB, key-value store) and feeds it back into the prompt for the next run.

This allows the LLM to behave as if it “remembers” things across sessions without bloating its internal weights.

---

## 🧠 How LLMs Work Internally (Without a Vector DB)

💡 **Pure LLM Setup** — All the knowledge is baked into the model’s weights.

### 🔹 Steps:

1. 📝 **Tokenization**  
   Break user input into tokens (IDs).

2. 🎨 **Embedding Lookup**  
   Convert Each token ID → learned vector (embedding).

3. ⚙️ **Pass Through Layers**

   - Attention mechanism is the key for "short term memory" and it decides how much of previous tokens to use.
   - At each layer, the vector embeddings are passed through along with attention.
   - Apply **Matrix multiplications** with weight tensors (Q, K, V, Feedforward).
   - Apply **Non-linear activations**.
   - Use **Attention mechanisms** to mix information across tokens.

4. 🎯 **Output Probabilities**  
   Final layer → **logit vector** (one score per vocabulary token).  
   Softmax → probability distribution.

5. 🚀 **Token Generation**
   - Pick or sample the highest-probability token.
   - Append it to input.
   - Repeat steps 3–5.

---

## 🧠 How LLMs Work With a Vector DB (RAG – Retrieval-Augmented Generation)

💡 **LLM + Search System** — Combines model weights with fresh/external info.

### 🔹 Steps:

1. 📝 **User Query → Embedding**  
   Convert query into a vector using an embedding model.

2. 🔍 **Search in Vector DB**

   - Store chunks of text/documents as vectors.
   - Compute **similarity (cosine)** between query vector & stored vectors.
   - Retrieve top-K relevant chunks.

3. 🧩 **Construct Augmented Prompt**  
   Combine user’s original query + retrieved chunks into one prompt.

   Example:

   - User question: “What’s the latest iPhone model?”
   - Retrieved data: “iPhone 16 launched in Sept 2025…”
   - Final prompt: “Answer based on this info: iPhone 16 launched in Sept 2025.”

4. ⚙️ **Pass Through LLM**  
   Feed augmented prompt to the LLM.  
   LLM uses internal reasoning + retrieved data to craft answer.

5. 🚀 **Generate Output**  
   Same as pure LLM flow, but now grounded in external data.

# 📌 Summary of LLM, Layers, and Tensors

- **Layers** = building blocks that transform input tensors into output tensors.
- **Tensors** = the core data structure for weights, inputs, and activations in neural networks.
- **Without a vector DB**: The LLM relies solely on its **internal weights**. Everything is just math → embeddings → transformer layers → next token.
- **With a vector DB**: The LLM **augments the prompt** by retrieving relevant external data (via embeddings + similarity search) before generating an answer.
