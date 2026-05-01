# Week 1 — NLP Foundations

> Covers tokenization, embeddings, semantic similarity, and text classification from first principles.

## Prerequisites

- Basic Python programming knowledge
- Familiarity with Jupyter notebooks
- Understanding of machine learning concepts (helpful but not required)

## Overview

| Technology | Version |
|------------|---------|
| Python | 3.10+ |
| Jupyter Lab | Latest |
| HuggingFace Transformers | Latest |
| PyTorch | Latest |
| Pandas | Latest |
| Scikit-learn | Latest |

## Learning Objectives

By the end of this week, you'll understand:

- How tokenization works and its impact on costs and context
- What embeddings are and how to compute semantic similarity
- Text preprocessing techniques using Pandas
- Classical vs modern approaches to text classification

## Notebooks

| File | What it covers |
|------|----------------|
| [01_tokenization.ipynb](01_tokenization.ipynb) | WordPiece tokenization, token vs word, cost and context implications |
| [02_embeddings.ipynb](02_embeddings.ipynb) | Token embeddings, sentence embeddings via mean pooling, cosine similarity |
| [03_pandas_nlp.ipynb](03_pandas_nlp.ipynb) | Pandas for NLP data manipulation and text processing |
| [04_text_classification.ipynb](04_text_classification.ipynb) | TF-IDF vs embeddings, text classification with DistilBERT |
| [05_evaluation_metrics.ipynb](05_evaluation_metrics.ipynb) | Evaluation metrics for NLP models (accuracy, precision, recall, F1-score) |

## Project Structure

```
week1-nlp-foundations/
├── README.md                    # This file
├── .gitignore                   # Git ignore rules
├── 01_tokenization.ipynb        # Tokenization fundamentals
├── 02_embeddings.ipynb          # Embeddings and similarity
├── 03_pandas_nlp.ipynb          # Text processing with Pandas
├── 04_text_classification.ipynb # Text classification models
└── 05_evaluation_metrics.ipynb  # Model evaluation metrics
```

## Notebooks

| File | What it covers |
|------|----------------|
| [01_tokenization.ipynb](01_tokenization.ipynb) | WordPiece tokenization, token vs word, cost and context implications |
| [02_embeddings.ipynb](02_embeddings.ipynb) | Token embeddings, sentence embeddings via mean pooling, cosine similarity |
| [03_pandas_nlp.ipynb](03_pandas_nlp.ipynb) | Pandas for NLP data manipulation and text processing |
| [04_text_classification.ipynb](04_text_classification.ipynb) | TF-IDF vs embeddings, text classification with DistilBERT |

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate
pip install jupyterlab transformers torch pandas scikit-learn
jupyter lab
```

## Checkpoint

A **token** is a numerical ID representing a subword unit from a fixed vocabulary. A single word can map to multiple tokens depending on how common it is. API costs are billed per token, not per word — so technical text, names, and non-English content costs more than it looks. Context windows are also measured in tokens, meaning high token-per-word content fills the window faster.

## Key Concepts

| Concept | One-liner |
|---------|-----------|
| **WordPiece** | Unknown words split into subword pieces using `##` prefix |
| **Token embedding** | Each token ID → 768-dimensional float vector encoding meaning |
| **Mean pooling** | Average all token embeddings to get a single sentence vector |
| **Cosine similarity** | Measures angle between vectors — 1.0 = identical meaning, 0 = unrelated |