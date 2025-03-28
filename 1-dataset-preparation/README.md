### 📁 `1-dataset-preparation/` Folder

# Dataset Preparation

This folder contains detailed steps, scripts, and explanations for creating the **Kazakh Extrinsic Plagiarism Detection Dataset**.

## Overview

- **Source Data:**  
  Derived from the original [PAN Plagiarism Detection Corpus](https://pan.webis.de/).

- **English Plagiarism Identification:**  
  English plagiarism cases were identified using XML metadata provided by the PAN corpus.

- **Kazakh Translation:**  
  Identified English text pairs (suspicious and source texts) were automatically translated into Kazakh using the **Google Translate API**.

- **Data Alignment:**  
  Both the original English and translated Kazakh text pairs were carefully aligned, labeled (plagiarized or non-plagiarized), cleaned, and shuffled.

## Preparation Workflow

1. **Extract Plagiarized Pairs:**  
   Parse the PAN XML files to extract potential plagiarized text pairs.
2. **Automatic Translation:**  
   Translate the English texts into Kazakh using the Google Translate API.
3. **Match and Organize:**  
   Align the translated Kazakh texts with their original English counterparts.
4. **Labeling:**  
   Assign labels to each aligned pair (`1` for plagiarized, `0` for non-plagiarized).
5. **Cleaning & Deduplication:**  
   Remove duplicates and clean the text pairs to ensure data quality.
6. **Balancing & Shuffling:**  
   Balance the dataset and shuffle the pairs to create robust training and testing sets.

## Files

- **[`1-dataset-preparation.ipynb`](1-dataset-preparation.ipynb):**  
  A Jupyter notebook detailing the dataset creation and preprocessing pipeline, complete with step-by-step explanations.

## Outputs

The cleaned, labeled, and finalized datasets are available in the [`2-dataset`](../2-dataset) folder and are ready for use in model training and evaluation.
