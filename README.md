# Bigram Language Model Training and Generation

This repository contains code for training and generating text using a Bigram Language Model. The model is trained on a given text dataset and can generate new text based on the learned patterns.

## Installation

You can install the required Python package using pip:

```bash
pip install wget
```

## Dataset

The dataset used for training the language model is sourced from the following URL:
[Dataset URL](https://raw.githubusercontent.com/karpathy/char-rnn/master/data/tinyshakespeare/input.txt)

The dataset is downloaded and saved as `input.txt` for further processing.

## Data Preprocessing

- The dataset is read from `input.txt`, and its length in characters is computed.
- All unique characters in the dataset are identified and sorted to create the vocabulary.
- The vocabulary size and the list of unique characters are printed.
- Character-to-integer and integer-to-character mappings are created.
- Encoder and decoder functions are defined to convert text to integers and vice versa.
- The text is encoded using the vocabulary, resulting in an encoded data tensor.
- The data is split into training and validation sets.

## Training Process

The training process involves the following steps:

### Sequence Extraction

- Sequences of characters are extracted from the training data with a specified block size.

### Model Architecture

- The Bigram Language Model is defined, which consists of:
  - Token embedding table
  - Position embedding table
  - Stacked transformer blocks
  - Layer normalization for the final output
  - Linear layer for language modeling prediction

### Loss Calculation

- The model computes logits and calculates the loss using cross-entropy.

### Training Loop

- The model is trained using backpropagation and gradient descent.
- An AdamW optimizer is used for parameter updates.
- The training loop runs for a specified number of steps.

## Text Generation

The trained model can generate text based on an initial context. The generation process involves:

- Iteratively predicting the next token based on the current context.
- Sampling from the predicted token probabilities.
- Appending the sampled token to the context for the next prediction.
- Continuing this process until the desired length of generated text is reached.

## Hyperparameters

Hyperparameters for training and model architecture are defined at the beginning of the code, allowing for easy customization.

## Usage

You can train the model by running the provided code. After training, you can generate text by providing an initial context to the model.

Please note that this is a simplified Bigram Language Model, and more advanced models like GPT-3 are available for more sophisticated natural language processing tasks.

For any questions or issues, please contact [Your Name/Email].

**Enjoy generating text with your Bigram Language Model!**
