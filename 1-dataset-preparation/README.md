### 📁 `1-dataset-preparation/` Folder

# Dataset Preparation

This folder contains detailed steps, scripts, and explanations on how the **Kazakh extrinsic plagiarism detection dataset** was created.

## Overview:
- The dataset is derived from the original [PAN Plagiarism Detection Corpus](https://pan.webis.de/).
- English plagiarism cases were identified using XML metadata provided by the PAN corpus.
- Identified English text pairs (suspicious and source texts) were then automatically translated into Kazakh using the **Google Translate API**.
- Text pairs (both original English and translated Kazakh versions) were carefully aligned, labeled (as plagiarized or non-plagiarized), cleaned, and shuffled.

## Preparation Workflow:
1. **Extracting plagiarized text pairs** from PAN XML files.
2. **Translating English texts** to Kazakh language automatically.
3. **Matching and organizing** translated Kazakh texts with their original English counterparts.
4. **Labelling text pairs**: each aligned pair is labeled (`1` for plagiarized, `0` for non-plagiarized).
5. **Data cleaning and deduplication**: ensuring uniqueness and quality of text pairs.
6. **Balancing and shuffling**: creating final training and testing datasets ready for model training and evaluation.

## Files:
- [`data-preparation.ipynb`](`1_extract_plagiarised_texts_and_translate_and_create_dataset.ipynb`):
  - Complete notebook detailing the entire dataset creation and preprocessing pipeline with explanatory comments.

## Outputs:
The processed, cleaned, and finalized datasets are available in the [`2-dataset`](../2-dataset) folder for immediate use in model training and evaluation.
