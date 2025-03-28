### 📁 `4-model-evaluation/` Folder

# Model Evaluation

This folder assesses the performance of trained models on both Kazakh and English test datasets. The evaluation covers the following models:

- **Kazakh Models:**  
  XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT, KazakhBERTmulti
- **English Models:**  
  XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT

For each model, suspicious and source text pairs are evaluated to determine if they are plagiarized (label=1) or not (label=0). We measure performance using Accuracy, Precision, Recall, and F1-score, providing a comprehensive overview of each model's effectiveness. These metrics guide the selection of the optimal model for integration into the Kazakh extrinsic plagiarism detection pipeline.

## Notebook

- **[`4-model-evaluation.ipynb`](4-model-evaluation.ipynb):**  
  Contains the complete evaluation script along with detailed results analysis.
