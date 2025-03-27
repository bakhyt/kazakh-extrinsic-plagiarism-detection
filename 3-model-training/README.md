### 📁 `3-model-training/` Folder

# Model Training

We trained several state-of-the-art transformer-based models separately on both the **English** and **Kazakh** datasets. The selected models for our plagiarism detection task include:

1. **[Sentence Transformers (all-mpnet-base-v2)](https://huggingface.co/sentence-transformers/all-mpnet-base-v2)**  
2. **[XLM-RoBERTa Base](https://huggingface.co/xlm-roberta-base)**  
3. **[XLM-RoBERTa Large](https://huggingface.co/xlm-roberta-large)**  
4. **[KazakhBERTmulti (amandyk/KazakhBERTmulti)](https://huggingface.co/amandyk/KazakhBERTmulti)**  
5. **[DistilBERT](https://huggingface.co/distilbert-base-uncased)**  
6. **[MiniLM](https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)**  
7. **[SBERT](https://huggingface.co/sentence-transformers)**  

These models were selected based on their demonstrated effectiveness in NLP tasks, especially in semantic text similarity and classification tasks.

---

## Notebook:
- [`3-model-training.ipynb`](3-model-training.ipynb):
  - Complete training script, hyperparameters, and detailed explanations.

## Training Results:
- Training and validation losses
- Accuracy, Precision, Recall, and F1-score on validation set

