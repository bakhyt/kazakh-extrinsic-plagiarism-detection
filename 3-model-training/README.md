### 📁 `3-model-training/` Folder

# Model Training

We trained several state-of-the-art transformer-based models separately on both the **English** and **Kazakh** datasets. The selected models for our plagiarism detection task include:

**1. [Sentence Transformers (all-mpnet-base-v2)](https://huggingface.co/sentence-transformers/all-mpnet-base-v2)**  
- A powerful sentence embedding model based on MPNet architecture. Designed specifically for capturing semantic similarity between sentences, offering state-of-the-art performance in semantic textual similarity tasks.

**2. [XLM-RoBERTa Base](https://huggingface.co/xlm-roberta-base)**  
- A multilingual transformer-based language model trained on text data from 100 languages. It excels at understanding cross-lingual contexts and performs strongly in multilingual classification and similarity tasks.

**3. [XLM-RoBERTa Large](https://huggingface.co/xlm-roberta-large)**  
- A larger, more robust variant of XLM-RoBERTa Base, featuring more parameters and increased capacity, leading to significantly improved performance in multilingual NLP tasks, especially beneficial for nuanced semantic tasks like plagiarism detection.

**4. [KazakhBERTmulti (amandyk/KazakhBERTmulti)](https://huggingface.co/amandyk/KazakhBERTmulti)**  
- A transformer model specifically pre-trained on a large corpus of Kazakh text data. It is tailored to the Kazakh language, offering improved understanding of linguistic subtleties, making it ideal for NLP tasks focused on Kazakh texts.

**5. [DistilBERT](https://huggingface.co/distilbert-base-uncased)**  
- A lighter and faster variant of the popular BERT model, retaining nearly the same accuracy but with fewer parameters. Suitable for environments where computational efficiency and speed are essential.

**6. [MiniLM](https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)**  
- A compact yet powerful multilingual transformer model, optimized for producing effective sentence embeddings. It delivers a good balance between computational efficiency and strong performance in text similarity and paraphrasing tasks.

**7. [SBERT (Sentence-BERT)](https://huggingface.co/sentence-transformers)**  
- A modification of the standard BERT model specifically optimized for computing sentence embeddings. It greatly improves the efficiency of semantic similarity computations, making it a strong choice for plagiarism detection and text similarity tasks.

These models were selected based on their demonstrated effectiveness in NLP tasks, especially in semantic text similarity and classification tasks.

---

## Notebook:
- [`3-model-training.ipynb`](3-model-training.ipynb):
  - Complete training script, hyperparameters, and detailed explanations.

## Training Results:
- Training and validation losses
- Accuracy, Precision, Recall, and F1-score on validation set

