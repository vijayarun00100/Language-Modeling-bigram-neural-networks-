# 🧠 Language Modeling – Bigram & Neural Network Approach

This repository demonstrates how to **build a character-level language model from scratch** using both a **Bigram Probability Model** and a **simple Neural Network**.  
The goal is to generate realistic names (or similar sequences) based on the statistical patterns in the dataset (`names.txt`).

---

## 📘 Overview

The project walks through:
- Constructing a **Bigram model** (rule-based frequency approach)
- Building a **Neural Network model** (learned parametric approach)
- Comparing the two in terms of performance and generative ability

---

## 🚀 Features

### 🔹 Bigram Probability Model
- Calculates probabilities of each character following another using bigram counts.  
- Applies **Add-One Smoothing** to handle unseen pairs.  
- Generates new names by sampling characters based on bigram probabilities.  
- Visualizes bigram frequency distribution.

### 🔹 Neural Network Model
- Encodes character pairs using **one-hot encoding**.  
- Trains a **single-layer neural network** using **PyTorch** to predict the next character given the current one.  
- Learns bigram statistics in a **parametric** manner.  
- Uses **gradient descent** to minimize cross-entropy loss.  
- Can generate names by **chaining predictions** from the trained model.  

### 🔹 Visualization
- Displays the **bigram frequency matrix**.  
- (Optional) Visualizes **one-hot encodings** and training progress.

---


---

## ⚙️ Usage

### 1️⃣ Load the Dataset
Reads all names from `names.txt` into a list.

### 2️⃣ Count Bigrams
- Enumerates all character pairs (including start/stop tokens).  
- Stores counts in a matrix and normalizes to derive probabilities.

### 3️⃣ Name Generation (Bigram Model)
- Samples next characters from the learned probabilities until the end token is reached.

### 4️⃣ Train Neural Network
- Converts bigram pairs into input-output training sets.  
- Trains a PyTorch model on one-hot encoded data.  
- Computes **cross-entropy loss** during training.

### 5️⃣ Generate Names (Neural Network)
- Uses trained weights to **probabilistically generate** new names character by character.

---

## 🧩 Getting Started

### 🖥 Requirements
- Python 3.x  
- PyTorch  
- Matplotlib  

### ▶️ How to Run
1. Open `makeover.ipynb` in **Google Colab** or **Jupyter Notebook**.  
2. Ensure `names.txt` is present in the working directory.  
3. Run all cells sequentially to:
   - Process data  
   - Train the model  
   - Visualize and generate outputs  

---

## 🧠 Notes

- This project illustrates the **evolution from rule-based frequency models** to **simple neural networks** for text generation.  
- Character-level modeling makes it adaptable for **any language or symbolic dataset**.  
- Perfect for educational use and understanding **language modeling fundamentals** and **PyTorch basics**.

---


---

## 🧑‍💻 Author
**Vijay Arunachalam**  
Computer Science and Engineering – VIT Chennai  
*Specialization: Cyber Physical Systems*  

---

## 🏷 License
This project is intended for **educational and research purposes**.  
Feel free to fork and experiment!



