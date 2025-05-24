### 📁 `1-dataset-preparation/kazakh-expert-assessments/` Folder

# Expert Assessments of Translated Dataset

This folder contains the results and analysis of expert evaluations for the Google-translated PAN plagiarism dataset, translated from English into Kazakh. These evaluations assess both the **translation quality** and the **preservation of plagiarism signals** in the Kazakh version.

---

## 📚 Background

* **Dataset Origin**: Approximately 30,000 plagiarized text pairs were extracted from the PAN corpus and translated into Kazakh using Google Translate.
* **Evaluation Sample**: A subset of 2,000 pairs was selected for expert assessment.
* **Expert Panel**: Ten native Kazakh speakers participated. Each evaluated 200 pairs, with 200 pairs duplicated across annotators to assess consistency.

---

## 🧪 Assessment Methodology

Each Kazakh expert evaluated two aspects of the translated suspicious–source text pairs:

### 1. Translation Meaningfulness

* **Goal**: Assess whether the translated Kazakh text is understandable and faithful.
* **Scale**:

  * `0` – Not meaningful
  * `1` – Imperfect but understandable
  * `2` – Fully meaningful

### 2. Plagiarism Similarity

* **Goal**: Determine the degree of similarity between the Kazakh suspicious and source documents.
* **Scale**:

  * `0` – Dissimilar
  * `1` – Similar (same topic, but differing details)
  * `2` – Very similar (some differences, but nearly same meaning)
  * `3` – Identical (same meaning, minor stylistic differences allowed)

*Note: 200 of the 2,000 examples were intentionally duplicated to measure inter-rater consistency.*

---

## 🎥 Assessment Instructions

A 40-minute instructional video was created to guide experts through the evaluation process. It includes:

* An explanation of the two questions
* Step-by-step demonstrations with five example assessments

📺 **[Watch the video on YouTube](https://youtu.be/2219IXAgBr4?si=gqLNDYQZulwyFBeY)**

The video was shared with all ten experts before they began the evaluation task. Clarifications were provided as needed, and assessments were completed within three months.

---

### 📂 Folder Contents

* **Expert Ratings**:

  * Raw `.txt` files (`instruction.txt`, `info.txt`) containing expert scores are organized in subfolders.
  * Compressed archive of all submissions: [`kazakh-experts-evaluation.zip`](./kazakh-experts-evaluation.zip)

* **Processing Code**:

  * The notebook that parses expert files, computes agreement metrics, and summarizes results is located in the parent folder:
    [`../1-1-translation-assessments-summary.ipynb`](../1-1-translation-assessments-summary.ipynb)

* **Summary CSVs**:

  * Translation quality (Q1): [`first-question-2000-tasks-summary.csv`](./first-question-2000-tasks-summary.csv)
  * Plagiarism detection (Q2): [`second-question-2000-tasks-summary.csv`](./second-question-2000-tasks-summary.csv)
  * Duplicated task evaluations:

    * [`first-question-20-shared-tasks-summary.csv`](./first-question-20-shared-tasks-summary.csv)
    * [`second-question-20-shared-tasks-summary.csv`](./second-question-20-shared-tasks-summary.csv)

---

## 📈 Results Summary

### Translation Quality (Q1)

**Full Set (2,000 Pairs)**:

* Accepted (Score 1 or 2): **97.15%**
* Not meaningful (Score 0): **2.85%**

**On 200 Duplicated Tasks**:

* Identical scores: **48.5%**
* ±1-point differences: **49.0%**
* Major disagreements: **2.5%**

🔹 *Conclusion*: High translation reliability, with only 2.85% requiring revision and strong inter-annotator alignment.

---

### Plagiarism Detection (Q2)

**Full Set (2,000 Pairs)**:

* Plagiarized: **\~79.5%**
* Non-plagiarized: **\~20.5%**

**Breakdown of Plagiarism Severity**:

* Non-plagiarized: \~20.5%
* Partially plagiarized: \~22.5%
* Mostly plagiarized: \~28.0%
* Fully plagiarized: \~29.5%

**On 200 Duplicated Tasks**: Same distribution observed.

🔹 *Conclusion*: Label distribution closely matches the original PAN corpus (80% plagiarized), indicating strong preservation of the plagiarism signal during translation.

---

## 🔍 Inter-Annotator & Human–Gold Agreement

Agreement was evaluated using **Cohen’s kappa**\~\cite{cohen1960coefficient}:

| Comparison Type                   | Observed Agreement | Cohen’s Kappa |
| --------------------------------- | ------------------ | ------------- |
| Human–Human (Q1 - Meaningfulness) | 0.975              | 0.95          |
| Human–Human (Q2 - Plagiarism)     | 1.00               | 1.00          |
| Human–Original (Q2 - Plagiarism)  | \~0.99             | \~0.98        |

---

## ✅ Overall Conclusions

* **Translation Quality**: 97.15% of translated texts are acceptable.
* **Plagiarism Preservation**: Translations retain plagiarism structure almost exactly (79.5% vs. original 80%).
* **Expert Consistency**: Extremely high inter-rater agreement confirms the validity and consistency of human annotations.

These results affirm that the translated dataset is a high-quality resource for Kazakh extrinsic plagiarism detection research and model development.
