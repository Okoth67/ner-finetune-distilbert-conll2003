# Named Entity Recognition (NER) Fine-Tuning with DistilBERT on CoNLL-2003

This repository contains code and training setup for fine-tuning `distilbert-base-uncased` on the [CoNLL-2003](https://huggingface.co/datasets/conll2003) Named Entity Recognition dataset using Hugging Face Transformers.

---

## 📌 Task Overview

The goal is to train a lightweight NER model that can recognize entities like:
- PER (person)
- ORG (organization)
- LOC (location)
- MISC (miscellaneous)

---

## 🧠 Model

- **Base model**: [`distilbert-base-uncased`](https://huggingface.co/distilbert-base-uncased)
- **Architecture**: AutoModelForTokenClassification
- **Training epochs**: 3
- **Batch size**: 16
- **Optimizer**: AdamW
- **Learning rate**: 2e-5

---

## 🗂 Dataset

- **Source**: `conll2003` (from Hugging Face Datasets)
- **Split**: Train / Validation / Test
- **Entities**: `PER`, `LOC`, `ORG`, `MISC`, `O` (non-entity)

---

## 🚀 How to Run

```bash
# Create and activate virtual environment
conda create -n llm-env python=3.9 -y
conda activate llm-env

# Install requirements
pip install transformers datasets accelerate

# Run training notebook
jupyter notebook fine_tune_distilbert_ner.ipynb
