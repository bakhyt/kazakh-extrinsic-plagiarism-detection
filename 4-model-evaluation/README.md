### 📁 `4-model-evaluation/` Folder

# Model Evaluation
This section evaluates the trained models using on both Kazakh and English test datasets. The tested models include:

- **Kazakh**: XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT, KazakhBERTmulti
- **English**: XLM-RoBERTa (Large/Base), DistilBERT, MiniLM, SBERT

Each model receives suspicious and source text pairs, then predicts whether the pair is plagiarized (label=1) or not (label=0). We compute accuracy, precision, recall, and F1-score for a comprehensive performance view. These results guide the selection of the optimal model for implementation in the Kazakh extrinsic plagiarism detection pipeline.

## Notebook:
- [`4-model-evaluation.ipynb`](4-model-evaluation.ipynb):
  - Complete evaluation script and results.
