# DLassignment-2

## 📌 Overview

This repository contains two deep learning tasks implemented using PyTorch and HuggingFace's Transformers:

1. **Character-level Sequence-to-Sequence (seq2seq) Model** for Latin-to-Devanagari transliteration using RNNs.
2. **Fine-tuning GPT-2** to generate Justin Bieber-style song lyrics.

---

## 1. Latin to Devanagari Transliteration Model

### 🔍 Key Features

- Implements a seq2seq model using PyTorch
- Character-level tokenization and padding
- Configurable architecture: choose between RNN, LSTM, or GRU
- Model trained and evaluated on the Hindi subset of the [Dakshina dataset](https://github.com/google-research-datasets/dakshina)

### 🧠 Architecture

- Encoder-Decoder RNN-based framework
- Input Embedding Layer
- Hidden units and RNN cell type configurable
- Output layer with log-softmax over target vocabulary

### 📊 Results

- Performance varies based on RNN cell
- Validation accuracy and loss are plotted for each run
- Inference demonstrates transliteration of Latin script inputs to Devanagari outputs

### ▶️ How to Run

1. Open `RNNseq2seq.ipynb`
2. Run all cells sequentially
3. Sample predictions are displayed at the end of training

---

## 2. GPT-2 Fine-Tuning for Lyric Generation

### 🎵 Overview

Fine-tunes a pre-trained GPT-2 model to generate song lyrics in the style of Justin Bieber.

### 📚 Dataset

- `bieber.txt`: Contains approximately 3,700 lines of lyrics
- Used as input for GPT-2 fine-tuning

### 🛠️ Model Details

- Base Model: GPT-2 (124M parameters)
- Tokenizer: GPT2Tokenizer from HuggingFace
- Optimizer: AdamW
- Config:
  - Epochs: 5
  - Batch Size: 4
  - Learning Rate: 5e-5

### ✨ Text Generation Settings

- Temperature: 1.0
- Top-k sampling: 50–500
- Max Length: 256 tokens

### ▶️ How to Run

1. Open `FinetuneGPTtogeneratelyrics.ipynb`
2. Make sure to install dependencies using pip
3. Run the training cells
4. Use the final cell to generate lyrics

### 📝 Example Output

```text
Girl you're my angel, you're my darling
You're the sunshine in the morning
