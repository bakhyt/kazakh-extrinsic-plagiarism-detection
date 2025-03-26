**Model Evaluation on Test Set**  

In this stage, we evaluate the performance of our trained models using the **dedicated Kazakh and English test datasets** prepared earlier. These datasets are labeled, balanced, and unique, consisting of real-world examples that were not seen during training. Each model is evaluated on its respective language dataset to assess its ability to detect semantic similarity and potential plagiarism.

We benchmarked multiple models, including:
- **Kazakh XLM-RoBERTa (base and large)** trained on the Kazakh dataset
- **English XLM-RoBERTa (base)** trained on the English dataset

For each model, we compute standard classification metrics such as:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**

These metrics provide insight into the model’s ability to correctly identify both plagiarized (positive) and non-plagiarized (negative) text pairs. The evaluation results are then compared and visualized to determine which model performs best under the given conditions, especially in the low-resource Kazakh setting.
