### 📁 `5-plagiarism-detection-pipeline/` Folder

# Plagiarism Detection Pipeline

This folder contains the implementation of a **two-step plagiarism detection pipeline** specifically developed for the Kazakh language. The pipeline leverages a hybrid approach combining:

- **SimHash**: For efficiently identifying candidate plagiarism cases among large document collections.
- **Fine-tuned Kazakh RoBERTa Model**: For precise classification of suspicious text pairs as plagiarised or non-plagiarised.

## Pipeline Workflow:

1. **Candidate Selection (SimHash)**:
   - Use SimHash to efficiently scan and retrieve text pairs that are likely to be plagiarised based on hashing similarity.

2. **Fine-grained Classification (Kazakh RoBERTa)**:
   - Classify candidate pairs precisely using our transformer-based model trained specifically on Kazakh texts.

## Notebook:

- [`5-plagiarism-detection-pipeline.ipynb`](5-plagiarism-detection-pipeline.ipynb):
  - Step-by-step code demonstrating the pipeline implementation, explanations of each stage, and practical usage examples.
