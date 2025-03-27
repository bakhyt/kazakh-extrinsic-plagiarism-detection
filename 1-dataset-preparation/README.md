### 📁 `1-dataset-preparation/` Folder

# Dataset Preparation

This folder contains detailed steps, scripts, and explanations for creating the **Kazakh Extrinsic Plagiarism Detection Dataset**.

## Overview:
- The dataset is derived from the original [PAN Plagiarism Detection Corpus](https://pan.webis.de/).
- English plagiarism cases were identified using XML metadata provided by the PAN corpus.
- Identified English text pairs (suspicious and source texts) were automatically translated into Kazakh using the **Google Translate API**.
- Both original English and translated Kazakh text pairs were carefully aligned, labeled (as plagiarized or non-plagiarized), cleaned, and shuffled.

## Preparation Workflow:
1. **Extract plagiarized text pairs** from PAN XML files.
2. **Translate English texts** automatically into the Kazakh language.
3. **Match and organize** the translated Kazakh texts with their original English counterparts.
4. **Label text pairs**: each aligned pair is labeled (`1` for plagiarized, `0` for non-plagiarized).
5. **Clean and deduplicate** text pairs to ensure uniqueness and quality.
6. **Balance and shuffle** the dataset to create robust final training and testing sets.

## Files:
- [`1_extract_plagiarised_texts_and_translate_and_create_dataset.ipynb`](1_extract_plagiarised_texts_and_translate_and_create_dataset.ipynb):
  - Jupyter notebook detailing the dataset creation and preprocessing pipeline, with step-by-step explanations.

## Outputs:
The cleaned, labeled, and finalized datasets are available in the [`2-dataset`](../2-dataset) folder and ready for use in model training and evaluation.
