### 📁 `kazakh-extrinsic-plagiarism-detection/` Folder

# Kazakh Extrinsic Plagiarism Detection

This repository presents a comprehensive, end-to-end solution for **extrinsic plagiarism detection in the Kazakh language**. It includes curated datasets, expert annotations, model training scripts, evaluation benchmarks, and a scalable detection pipeline—specifically designed to support low-resource NLP tasks using modern transformer-based architectures.

---

## 📂 Repository Structure

### [1. Dataset Preparation](1-dataset-preparation)

* Scripts and explanations for converting the PAN plagiarism corpus into a parallel Kazakh dataset.
* Automatic translation of English suspicious–source pairs into Kazakh using the Google Translate API.
* Precise alignment, cleaning, and binary labeling of suspicious–source text pairs.
* **Expert validation** by 10 native Kazakh speakers on 2,000 translated pairs to assess translation quality and preservation of plagiarism signals.

### [2. Dataset](2-dataset)

* Finalized and cleaned **Kazakh** datasets:

  * **20,000 training pairs**
  * **4,562 testing pairs**
* Balanced, labeled, and ready for use in model training and evaluation.

### [3. Model Training and Evaluation](3-model-training-and-evaluation)

* Training and benchmarking of multiple transformer-based models on the Kazakh dataset.
* Includes models such as XLM-RoBERTa (Large/Base), KazakhBERTmulti, SBERT, DistilBERT, and MiniLM.
* A single **English-trained XLM-RoBERTa Large model** is used as a benchmark to assess the performance gap between high-resource and low-resource settings.
* Contains a unified notebook for training, evaluation, and performance comparison.

### [4. Plagiarism Detection Pipeline and Evaluation](4-plagiarism-detection-pipeline-and-evaluation)

* Implementation of a scalable, two-stage plagiarism detection system.
* Integrates lexical similarity techniques (e.g., SimHash, TF-IDF) with transformer-based semantic models.
* **Evaluation Setup**:

  * A realistic test set of **1,000 suspicious–source document pairs** was randomly selected from the original PAN dataset.
  * Each pair contains true plagiarism cases and was translated into Kazakh.
  * A CSV file stores: (1) full suspicious document, (2) full source document, and (3) the gold-standard plagiarized segments from the PAN XML.
* **Evaluation Procedure**:

  * For each row, the pipeline detects plagiarized spans and compares them to the gold-standard.
  * Precision, recall, and F1-score are computed at the **word level**.
* **Final Output**:

  * The system calculates the **average precision**, **average recall**, and **average F1-score** over all 1,000 document pairs.
* This evaluation framework reflects the pipeline's ability to detect plagiarism in real-world Kazakh texts.

---

## 🎯 Objectives

* Develop a high-quality plagiarism detection framework tailored to the **Kazakh language**.
* Benchmark state-of-the-art transformer models for semantic similarity and detection accuracy.
* Contribute openly available resources to advance **Kazakh NLP** and low-resource language research.

---

## ✅ Conclusion and Future Work

This project successfully:

* **Prepared and validated a comprehensive Kazakh extrinsic plagiarism dataset**
* **Trained and benchmarked multiple transformer models**, identifying the most effective for Kazakh
* **Built and evaluated a scalable detection pipeline** suited for practical deployment

---

### 🚀 Future Directions

* Improve performance through advanced fine-tuning, longer sequence handling, and ensemble modeling
* Expand the system for **multilingual and cross-lingual plagiarism detection**
* Integrate the solution into real-world platforms used in education, research, and publishing

---

## 📬 Contact

For questions, feedback, or collaboration inquiries, please reach out via email or [open an issue](https://github.com/your-username/kazakh-extrinsic-plagiarism-detection/issues) on GitHub.
