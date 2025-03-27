### 📁 `3-model-training/` Folder

# Model Training
This section describes the training process of machine learning models, specifically fine-tuned for Kazakh text similarity detection.

## Model Details:
- **Architecture:** XLM-RoBERTa (Large variant)
- **Dataset:** Kazakh labeled dataset (120K paragraph pairs)
- **Training Parameters:**
  - Learning Rate: `1e-5`
  - Epochs: `3-5`
  - Batch Size: `4` (with gradient accumulation)
  - Optimizer: AdamW with Warmup Scheduler

## Notebook:
- [`3-model-training.ipynb`](3-model-training.ipynb):
  - Complete training script, hyperparameters, and detailed explanations.

## Training Results:
- Training and validation losses
- Accuracy, Precision, Recall, and F1-score on validation set

