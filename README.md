# Language-Modeling-bigram-neural-networks-
This repo is all about building language model from scratch using bigram model as well as neural network


makeover.ipynb
This project demonstrates a step-by-step approach to character-level language modeling using both a simple bigram counting method and a basic neural network. The primary dataset is a text file (names.txt) containing a list of names, and the goal is to generate new names (or similar sequences) that statistically resemble those in the dataset.

Features
Bigram Probability Model:

Calculates probabilities of every character following another character using bigram counts.

Smooths probabilities to avoid zero-likelihoods (add-one smoothing).

Generates new names by sampling according to bigram probabilities.

Neural Network Model:

Encodes character pairs using one-hot encoding.

Trains a single-layer neural network to predict the next character given the current one (essentially learning bigram statistics in a parametric way).

Uses gradient descent for training, tracks loss, and can generate names by chaining predictions.

Visualization:

Visualizes the bigram frequency matrix.

(Optional) Visualizes the one-hot encoded representations.

Usage
Load the Dataset:

Reads all names from names.txt into a list.

Count Bigrams:

Enumerates all character pairs (with start/stop tokens) across names and counts their occurrences.

Stores counts in a matrix and normalizes to get probabilities.

Name Generation with Bigram Model:

Samples the next character at each step using bigram probabilities until an end token is reached.

Neural Network Training:

Converts bigram pairs into input-output training pairs.

Uses PyTorch to train a weight matrix on one-hot encoded data to predict the next character for each position.

Calculates cross-entropy loss.

Name Generation with Neural Network:

Uses the trained parameters to probabilistically generate new names.

Getting Started
Requirements:

Python 3.x

PyTorch

Matplotlib

How to Run:

Open makeover.ipynb in Google Colab or Jupyter Notebook.

Make sure names.txt is present in the working directory.

Run all cells to process data, train the model, and visualize outputs.

File Structure
makeover.ipynb: Main Colab notebook.

names.txt: Plain text file with one name per line.

Notes
The project illustrates the transition from rule-based frequency models to simple neural networks for text generation.

All generation is character-wise, enabling flexible adaptation for any language or symbol-based dataset.

Suitable as an educational resource for understanding language modeling basics and PyTorch implementation.

