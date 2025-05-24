### 📁 `2-dataset/` Folder

# Dataset

This folder contains the finalized datasets for training and evaluating **text similarity** and **plagiarism detection** models in both **Kazakh** and **English**.

---

## 📊 Datasets Overview

* **Training Dataset**
  * Contains **20,000 text pairs** for each language (Kazakh and English).
  * Each dataset is labeled (`1` = plagiarized, `0` = non-plagiarized), balanced, shuffled, and thoroughly cleaned.

* **Testing Dataset**
  * Consists of **4,562 labeled text pairs**.
  * Carefully balanced and cleaned to ensure reliable and fair benchmarking.

---

## 📂 File Structure

| Filename                                                                 | Description                                                                                         |
| ------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| [`train-balanced-20000.csv`](./2-dataset/train-balanced-20000.csv)       | Final preprocessed **Kazakh and English** training dataset (20K pairs; balanced, labeled, shuffled) |
| [`test-balanced-4562.csv`](./2-dataset/test-balanced-4562.csv)           | Final **testing dataset** for Kazakh and English (balanced, labeled, and cleaned)                   |

---

### ⚠️ Note on Availability

Due to copyright or research policy constraints, some datasets may not be publicly available in this repository.  
Please contact the repository maintainer if you require access.
