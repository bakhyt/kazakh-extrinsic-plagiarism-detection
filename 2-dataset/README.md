### 📁 `2-dataset/` Folder

# Datasets for Training and Testing

This folder includes finalized datasets ready for training and evaluating text similarity and plagiarism detection models in Kazakh and English.

## Datasets Overview:

- **Training Dataset**:
  - 120K text pairs (Kazakh and English separately).
  - Labeled (plagiarized/non-plagiarized), balanced, shuffled, and cleaned.

- **Testing Dataset**:
  - Approximately 4000 sentence pairs.
  - Carefully balanced and cleaned for reliable benchmarking.

## File Structure:
| Filename                                      | Description                                     |
|-----------------------------------------------|------------------------------------------------|
| `kz_dataset_120K_ready_for_training.csv`      | Final preprocessed **Kazakh** training dataset (120,000 pairs, balanced, labeled, shuffled)    |
| `en_dataset_120K_ready_for_training.csv`      | Final preprocessed **English** training dataset (120,000 pairs, balanced, labeled, shuffled)    |
| `kz-3950-sentences-for-testing1.csv`          | Testing dataset (Kazakh), labeled and balanced |
| `en-4500-sentences-for-testing6.csv`          | Testing dataset (English), labeled and balanced|

---

### ⚠️ Note on Availability:

Some datasets may not be publicly shared in this repository due to copyright or research policy constraints. Please contact the repository maintainer if you require access.
