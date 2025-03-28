### 📁 `4-model-evaluation/` Folder

# Model Evaluation
This section evaluates the trained models using test datasets. The tested models include:

Kazakh: XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT, KazakhBERTmulti
English: XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT
Each model receives suspicious and source text pairs, then predicts whether the pair is plagiarized (label=1) or not (label=0). We compute accuracy, precision, recall, and F1-score for a comprehensive performance view.

## Notebook:
- [`4-model-evaluation.ipynb`](4-model-evaluation.ipynb):
  - Complete evaluation script and results.
