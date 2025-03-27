### 📁 `4-model-evaluation/` Folder

# Model Evaluation
This section evaluates the trained models using test datasets.

## Evaluation Metrics:
- **Accuracy:** Overall correctness of model predictions.
- **Precision:** Accuracy of positive predictions.
- **Recall:** Ability of the model to detect actual plagiarized instances.
- **F1-score:** Harmonic mean of precision and recall.

## Evaluated Models:
- Kazakh XLM-RoBERTa Large (v2, v3)
- Kazakh XLM-RoBERTa Base
- English XLM-RoBERTa Base (for comparative purposes)

## Notebook:
- [`4-model-evaluation.ipynb`](4-model-evaluation.ipynb):
  - Complete evaluation script and results.

## Results:
| Model                         | Accuracy | Precision | Recall | F1-Score |
|-------------------------------|----------|-----------|--------|----------|
| Kazakh XLM-RoBERTa Large v3   | 95.1%    | 99.4%     | 90.7%  | 94.9%    |
| Kazakh XLM-RoBERTa Base       | 74.7%    | 66.8%     | 98.4%  | 79.6%    |
| English XLM-RoBERTa Base      | 96.4%    | 94.3%     | 98.8%  | 96.5%    |
