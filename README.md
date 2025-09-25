# Research Paper Text Summarization using T5

## 📌 Overview
This project implements an **abstractive text summarization system** for research articles using a fine-tuned **T5-small transformer model**.  
The model was trained on the **arXiv subset of the scientific_papers dataset** and evaluated with multiple NLP metrics (ROUGE, BLEU, METEOR, BERTScore).  
The goal is to assist researchers by generating concise, coherent summaries of lengthy scientific texts.  

---

## ✨ Features
- Preprocessing & tokenization of research papers  
- Fine-tuned **T5-small model** with Hugging Face  
- Evaluation with **ROUGE, BLEU, METEOR, BERTScore**  
- Beam search decoding for fluent summaries  
- Reproducible training pipeline  

---

## 📊 Dataset
- **Source:** Hugging Face `scientific_papers` dataset (arXiv subset)  
- **Description:** Contains pairs of research articles and their abstracts for supervised summarization tasks.  

---

## 🔧 Methodology
- Preprocessing with `T5Tokenizer` (inputs limited to 512 tokens, summaries capped at 150 tokens)  
- Model training using Hugging Face’s `Trainer` API  
- **Hyperparameters:**  
  - Learning rate: `3e-4`  
  - Batch size: `4`  
  - Epochs: `3`  
  - Optimizer: `AdamW`  
- Evaluation metrics: ROUGE, BLEU, METEOR, BERTScore  

---

## 📈 Results
- **Best Model Scores:**  
  - ROUGE-1: `0.412`  
  - ROUGE-2: `0.198`  
  - ROUGE-L: `0.375`  

The summaries are **concise and semantically meaningful**, but performance is limited by token truncation in long documents.  

---

