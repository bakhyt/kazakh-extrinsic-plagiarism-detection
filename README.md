### 📁 `kazakh-extrinsic-plagiarism-detection/` Folder

# Kazakh Extrinsic Plagiarism Detection

This repository provides a comprehensive framework, including datasets, models, and a robust pipeline for **extrinsic plagiarism detection specifically tailored for the Kazakh language**. The primary objective is to detect plagiarism by comparing suspicious documents against source documents, leveraging state-of-the-art Natural Language Processing (NLP) techniques, particularly transformer-based models.

## 📂 Repository Structure

### 1. [Dataset Preparation](1-dataset-preparation)
- Detailed methods, scripts, and notebooks to create and preprocess the Kazakh plagiarism detection dataset from the PAN Plagiarism Detection Corpus.
- Extraction and alignment of plagiarized English text pairs and their translation into Kazakh.

### 2. [Dataset](2-dataset)
- Prepared, cleaned, labeled, balanced, and shuffled training and testing datasets suitable for NLP model training and evaluation.

### 3. [Model Training](3-model-training)
- Training scripts and Jupyter notebooks demonstrating the fine-tuning of transformer models, particularly **XLM-RoBERTa Large**, optimized for detecting plagiarism in Kazakh texts.

### 4. [Model Evaluation](4-model-evaluation)
- Evaluation scripts, benchmarking results, and metrics (accuracy, precision, recall, F1-score) showcasing model effectiveness.

### 5. [Plagiarism Detection Pipeline](5-plagiarism-detection-pipeline)
- An efficient hybrid detection system combining **SimHash** for rapid candidate retrieval and the trained **XLM-RoBERTa** model for accurate plagiarism classification.

### 6. [Pipeline Evaluation](6-pipeline-evaluation)
- Comprehensive evaluation of the developed pipeline on a large-scale dataset (~1000 documents), emphasizing real-world applicability, efficiency, and accuracy.

## 🚀 Quick Start
Explore each folder step-by-step to:
- Understand the complete dataset creation process.
- Access and utilize ready-to-use datasets.
- Reproduce training of advanced NLP models.
- Evaluate and benchmark model performance and pipelines.

## 🎯 Project Objectives
- Develop and share robust methods for plagiarism detection specifically for Kazakh texts.
- Create and provide high-quality, labeled datasets to support NLP research in low-resource languages.
- Benchmark modern transformer-based NLP models in real-world scenarios.

## 📌 Highlights
- Leveraged the [PAN Plagiarism Detection Corpus](https://pan.webis.de/) as a foundational resource.
- Employed automatic translation and meticulous alignment of datasets.
- Utilized advanced NLP architectures (**XLM-RoBERTa Large**).
- Clearly documented and reproducible results provided through detailed Jupyter notebooks.

## 📚 References
- [PAN Plagiarism Detection Corpus](https://pan.webis.de/)
- [XLM-RoBERTa: Cross-lingual Language Model](https://huggingface.co/docs/transformers/model_doc/xlm-roberta)

---

Feel free to explore, contribute, or contact the authors for collaboration opportunities or additional details regarding the datasets, methods, and findings presented.
