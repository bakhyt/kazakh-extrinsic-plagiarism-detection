### 📁 `3-model-training/` Folder

# Model Training

In this stage, we trained several state-of-the-art transformer-based models separately on both **English** and **Kazakh** datasets to evaluate their effectiveness in extrinsic plagiarism detection. Our aim was to determine the most suitable model capable of accurately identifying plagiarism in Kazakh texts.

## 🧠 Models Trained:

**1. [Sentence Transformers (all-mpnet-base-v2)](https://huggingface.co/sentence-transformers/all-mpnet-base-v2)**  
A powerful sentence embedding model based on the MPNet architecture, specifically optimized for semantic textual similarity, yielding strong performance in capturing sentence-level semantics.

**2. [XLM-RoBERTa Base](https://huggingface.co/xlm-roberta-base)**  
A multilingual transformer-based model trained on text data from 100 languages, proficient in handling cross-lingual contexts and delivering consistent performance in multilingual NLP tasks.

**3. [XLM-RoBERTa Large](https://huggingface.co/xlm-roberta-large)**  
An enhanced variant of XLM-RoBERTa Base with a greater number of parameters and deeper architecture, resulting in significantly improved accuracy in multilingual and nuanced semantic tasks such as plagiarism detection.

**4. [KazakhBERTmulti (amandyk/KazakhBERTmulti)](https://huggingface.co/amandyk/KazakhBERTmulti)**  
A specialized transformer model pretrained extensively on Kazakh textual data. Tailored explicitly for the Kazakh language, this model provides superior handling of linguistic subtleties, making it highly effective for NLP tasks focused on Kazakh.

**5. [DistilBERT](https://huggingface.co/distilbert-base-uncased)**  
A lightweight and computationally efficient version of BERT. It achieves comparable accuracy with fewer parameters, making it ideal for environments where speed and efficiency are prioritized.

**6. [MiniLM](https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)**  
A compact multilingual transformer optimized for generating high-quality sentence embeddings, offering a good balance between computational efficiency and strong performance in text similarity tasks.

**7. [SBERT (Sentence-BERT)](https://huggingface.co/sentence-transformers)**  
An adaptation of the original BERT model optimized specifically for semantic similarity tasks, significantly enhancing efficiency when computing semantic relationships between text pairs.

## 📌 Comparative Model Training

We systematically trained these models on both **Kazakh** and **English** datasets. Due to English being a high-resource language, models generally perform strongly on it, providing a useful performance benchmark. However, given that **Kazakh** is a lower-resource language, our primary focus was to evaluate and enhance models specifically suited to accurately detect text similarity in Kazakh.

## 📒 Notebook:

- [`3-model-training.ipynb`](3-model-training.ipynb):  
    - Complete training script, hyperparameters, and detailed explanations.

## 📊 Training Results:
- Comprehensive metrics including training/validation losses
- Performance evaluations using accuracy, precision, recall, and F1-score on validation datasets

These results guide the selection of the optimal model for implementation in the Kazakh extrinsic plagiarism detection pipeline.

