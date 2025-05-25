## 📁 `3-model-training-and-evaluation/` Folder

# Model Training and Evaluation

This folder documents the full workflow for training and evaluating state-of-the-art transformer-based models on the **Kazakh extrinsic plagiarism detection dataset** from the [2-dataset](../2-dataset) folder. All models were trained specifically on Kazakh data, with one English model (XLM-RoBERTa Large) trained separately on English data and included for performance comparison. The primary objective is to identify the best-performing model for plagiarism detection in a **low-resource language** context.

---

## 🧠 Trained Models

We trained and benchmarked the following transformer-based models on Kazakh data:

1. **[XLM-RoBERTa Large](https://huggingface.co/xlm-roberta-large)**
   A powerful multilingual model. Trained both on Kazakh and English datasets to allow performance comparison.

2. **[XLM-RoBERTa Base](https://huggingface.co/xlm-roberta-base)**
   A lighter version of XLM-R, effective for multilingual tasks.

3. **[KazakhBERTmulti (amandyk/KazakhBERTmulti)](https://huggingface.co/amandyk/KazakhBERTmulti)**
   A Kazakh-specific model pretrained on native data.

4. **[SBERT (all-mpnet-base-v2)](https://huggingface.co/sentence-transformers/all-mpnet-base-v2)**
   A strong sentence embedding model fine-tuned on Kazakh pairs for plagiarism detection.

5. **[DistilBERT](https://huggingface.co/distilbert-base-uncased)**
   A smaller, faster variant of BERT evaluated for Kazakh performance.

6. **[MiniLM](https://huggingface.co/sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2)**
   A compact multilingual model tested for Kazakh text similarity.

---

## 📌 Training Procedure

All models were trained using the dataset:

* [`train-balanced-20000.csv`](../2-dataset/train-balanced-20000.csv)

Each model was trained to classify suspicious–source paragraph pairs as either plagiarized (`1`) or non-plagiarized (`0`). The dataset contains 20,000 balanced and labeled Kazakh examples. The English version of XLM-RoBERTa Large was trained separately to serve as a performance reference.

---

## 📊 Evaluation and Benchmarking

All trained Kazakh models were benchmarked on the [Kazakh test dataset](../2-dataset/test-balanced-4562.csv), which contains 4,562 labeled pairs. Evaluation was conducted using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**

This benchmarking provides a quantitative comparison of model performance on real Kazakh data and helps determine which architecture is most effective for downstream plagiarism detection. The English-trained model's results serve as a reference point for gauging the gap between high-resource and low-resource performance.

---

## 📒 Notebook

* **[`3-model-training-and-evaluation.ipynb`](3-model-training-and-evaluation.ipynb)**
  This notebook includes the full code for training, validation, evaluation, and performance comparison across all models.

---

## 📈 Results Summary

* Benchmark results for all Kazakh-trained models on the Kazakh test set
* Comparative performance metrics (Precision, Recall, F1) summarized in tables
* English-trained XLM-RoBERTa Large used as a benchmark reference

