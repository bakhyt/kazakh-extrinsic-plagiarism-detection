### 📁 `1-dataset-preparation/` Folder

# Dataset Preparation

This folder contains the complete pipeline, scripts, and explanations for creating the **Kazakh Extrinsic Plagiarism Detection Dataset**.

## Overview

* **Source Data**
  The dataset is derived from the official [PAN Plagiarism Detection Corpus](https://pan.webis.de/), which provides annotated plagiarism cases in English.

* **English Plagiarism Identification**
  Plagiarized text segments were extracted from the PAN XML metadata, which contains detailed alignment information between suspicious and source documents.

* **Kazakh Translation**
  The extracted English suspicious–source text pairs were automatically translated into Kazakh using the **Google Translate API**, preserving structural alignment.

* **Data Alignment**
  Each translated Kazakh pair was aligned with its English counterpart. All pairs were labeled as either plagiarized (`1`) or non-plagiarized (`0`), then cleaned and shuffled for robustness.

## Preparation Workflow

1. **Extract Plagiarized Pairs**
   Parse PAN XML files to collect aligned English text segments for plagiarism cases.

2. **Automatic Translation**
   Translate both suspicious and source segments into Kazakh using the Google Translate API, preserving the pair structure.

3. **Match and Organize**
   Pair the translated Kazakh texts with their original English counterparts while keeping alignment intact.

4. **Labeling**
   Assign binary labels to each pair: `1` for plagiarized, `0` for non-plagiarized.

5. **Cleaning and Deduplication**
   Filter out duplicates, normalize spacing, and clean formatting artifacts.

6. **Balancing and Shuffling**
   Balance the number of plagiarized and non-plagiarized pairs and shuffle the dataset to prepare for model training and evaluation.

## Expert Assessments

To evaluate translation quality and annotation reliability, we conducted a human validation study involving ten native Kazakh speakers:

* **Sample Size**: 2,000 Kazakh text pairs (including 200 intentionally duplicated examples to measure consistency).
* **Annotation Criteria**:

  1. **Translation Meaningfulness** (scale: 0 = not meaningful, 2 = fully meaningful)
  2. **Plagiarism Similarity** (scale: 0 = not similar, 3 = highly similar)
* **Results**:
  Inter-annotator agreement was computed using **Cohen’s kappa**, with full implementation provided in the notebook
  [`1-1-calculating-expert-assessments.ipynb`](./1-1-calculating-expert-assessments.ipynb).
  Raw annotations, agreement metrics, and result summaries are available in the [`kazakh-expert-assessments`](./kazakh-expert-assessments) folder.

## Key Files

* **[`1-dataset-preparation.ipynb`](1-dataset-preparation.ipynb)**
  Main notebook containing the end-to-end dataset creation process, including parsing, translation, alignment, and cleaning.

## Outputs

The finalized and labeled datasets are saved in the [`2-dataset`](../2-dataset) folder. These datasets are ready for downstream model training, validation, and benchmarking tasks.
