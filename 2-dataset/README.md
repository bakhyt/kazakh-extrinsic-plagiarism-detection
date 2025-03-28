### 📁 `2-dataset/` Folder

# Datasets

This folder contains the finalized datasets for training and evaluating text similarity and plagiarism detection models in both Kazakh and English.

## Datasets Overview

- **Training Dataset:**
  - Contains 120K text pairs for each language (Kazakh and English).
  - Each dataset is labeled (plagiarized/non-plagiarized), balanced, shuffled, and thoroughly cleaned.

- **Testing Dataset:**
  - Comprises approximately 4000 sentence pairs.
  - Meticulously balanced and cleaned to ensure reliable benchmarking.

## File Structure

| Filename                                     | Description                                                                 |
|----------------------------------------------|-----------------------------------------------------------------------------|
| `kz_dataset_120K_ready_for_training.csv`     | Final preprocessed **Kazakh** training dataset (120K pairs; balanced, labeled, shuffled) |
| `en_dataset_120K_ready_for_training.csv`     | Final preprocessed **English** training dataset (120K pairs; balanced, labeled, shuffled) |
| `kz-3950-sentences-for-testing1.csv`         | Testing dataset for Kazakh (labeled and balanced)                           |
| `en-4500-sentences-for-testing6.csv`         | Testing dataset for English (labeled and balanced)                          |

---

### ⚠️ Note on Availability

Due to copyright or research policy constraints, some datasets may not be publicly shared in this repository. Please contact the repository maintainer if you require access.
