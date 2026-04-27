# Week 1 — NLP Foundations

> Covers tokenization, embeddings, and semantic similarity from first principles.

## Overview

| Technology | Version |
|------------|---------|
| Python | 3.10+ |
| Jupyter Lab | — |
| HuggingFace Transformers | Latest |

## Notebooks

| File | What it covers |
|------|----------------|
| [01_tokenization.ipynb](01_tokenization.ipynb) | WordPiece tokenization, token vs word, cost and context implications |
| [02_embeddings.ipynb](02_embeddings.ipynb) | Token embeddings, sentence embeddings via mean pooling, cosine similarity |
| [03_pandas_nlp.ipynb](03_pandas_nlp.ipynb) | Pandas for NLP data manipulation and text processing |

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate
pip install jupyterlab transformers torch pandas
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