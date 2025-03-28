### 📁 `3-model-training/` Folder

# Model Training

This folder documents the training of several state-of-the-art transformer-based models on both **English** and **Kazakh** datasets for extrinsic plagiarism detection. The primary goal is to identify the model that best detects plagiarism in Kazakh texts.

## 🧠 Trained Models

1. **[SBERT (Sentence Transformers - all-mpnet-base-v2)](https://huggingface.co/sentence-transformers/all-mpnet-base-v2)**  
   A powerful sentence embedding model built on the MPNet architecture, optimized for semantic textual similarity and capturing nuanced sentence-level semantics.

2. **[XLM-RoBERTa Base](https://huggingface.co/xlm-roberta-base)**  
   A multilingual transformer trained on text from over 100 languages, proficient in cross-lingual tasks and delivering consistent performance across various NLP applications.

3. **[XLM-RoBERTa Large](https://huggingface.co/xlm-roberta-large)**  
   An enhanced version of XLM-RoBERTa Base with more parameters and a deeper architecture, offering improved accuracy in multilingual and complex semantic tasks such as plagiarism detection.

4. **[KazakhBERTmulti (amandyk/KazakhBERTmulti)](https://huggingface.co/amandyk/KazakhBERTmulti)**  
   A specialized transformer model pretrained on extensive Kazakh textual data, designed to capture the linguistic subtleties of the Kazakh language and excel in related NLP tasks.

5. **[DistilBERT](https://huggingface.co/distilbert-base-uncased)**  
   A lightweight, efficient version of BERT that maintains comparable accuracy with fewer parameters, making it ideal for scenarios prioritizing speed and computational efficiency.

6. **[MiniLM](https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)**  
   A compact multilingual transformer optimized for generating high-quality sentence embeddings, balancing computational efficiency with robust performance in text similarity tasks.

## 📌 Comparative Model Training

## 📌 Comparative Model Training

Models were systematically trained on both [**Kazakh**](../2-dataset/kz_dataset_120K_ready_for_training.csv) and [**English**](../2-dataset/en_dataset_120K_ready_for_training.csv) datasets. Since English is a high-resource language, its performance serves as a reliable benchmark. However, our primary focus is on enhancing model performance for **Kazakh**, a lower-resource language, to ensure effective plagiarism detection through accurate text similarity evaluation.

## 📒 Notebook

- **[`3-model-training.ipynb`](3-model-training.ipynb):**  
  This notebook includes the complete training script, detailed hyperparameter configurations, and thorough explanations of the training process.

## 📊 Training Results

- Detailed metrics on training and validation losses.
- Comprehensive evaluations based on accuracy, precision, recall, and F1-score on the validation datasets.
