### 📁 `1-dataset-preparation/kazakh-expert-assessments/` Folder

# Expert Assessments of Translated Datasets

This folder contains the results and analysis of expert assessments for the Google-translated PAN plagiarism dataset from English to Kazakh. These evaluations verify both the translation quality and the preservation of plagiarism signals in the Kazakh version of the dataset.

---

## Background

- **Dataset Origin:** Over 22,000 plagiarized text pairs from the PAN corpus were translated into Kazakh using Google Translate.
- **Evaluation Sample:** 2,000 text pairs were selected for detailed expert assessment.
- **Expert Panel:** Ten Kazakh experts each evaluated 200 pairs, with 200 pairs intentionally duplicated across assessments to ensure consistency and fairness.

---

## Assessment Methodology

Kazakh experts evaluated the translated text pairs based on two key questions:

### 1. Meaningfulness of the Kazakh Version

- **Objective:** Determine whether the translated text is meaningful.
- **Scoring:**
  - **0:** Not meaningful.
  - **1:** Meaningful but with mistakes or sounding unnatural.
  - **2:** Fully meaningful.

### 2. Similarity Between the Kazakh Suspicious-Document and Kazakh Source-Document

- **Objective:** Assess the degree of similarity between the paired documents.
- **Scoring:**
  - **0:** Dissimilar – Unrelated texts or only slight context overlap.
  - **1:** Similar – Texts share the same general topic but have significant differences (e.g., one text may include details that the other omits).
  - **2:** Very Similar – Texts convey nearly the same meaning, though some important differences exist.
  - **3:** Identical – Texts are essentially identical in meaning (minor stylistic differences are acceptable).

*Note:*  
Each expert evaluated 200 text pairs, totaling 2,000 pairs. To check for inter-rater reliability, 200 pairs were duplicated across assessments.

---

## Contents

- **Assessment Data Files:**  
  Raw CSV/Excel files containing experts' ratings.
- **Assessment Script:**  
  A Python script that processes the assessments, calculates summary statistics, and generates detailed reports.

---

## Results Summary

### 1. Translation Quality Assessment (Question 1)

**Overall Results (2,000 Texts):**

- **Accepted Translations (Scores 1 or 2):** 97.15% (1,943 texts)  
  *Nearly all translations met quality standards.*
- **Disputed Translations (Score 0):** 2.85% (57 texts)  
  *A small portion were flagged as problematic.*

**Detailed Assessment on 200 Duplicated Tasks:**

- **Full Agreement (Identical Scores):** 48.5%
- **Partial Agreement (Minor Differences, ±1 point):** 49.0%
- **Disagreement (Significant Differences):** 2.5%

*Key Findings:*  
Over 97% of the translations were deemed acceptable, demonstrating high reliability in the Google-translated Kazakh texts. The duplicated tasks confirm strong inter-rater consistency, with only 2.5% showing significant discrepancies.

---

### 2. Plagiarism Detection Assessment (Question 2)

**Overall Results (2,000 Texts):**

- **Plagiarized Texts (Combined Rating):** Approximately 79.5%  
  *This aligns closely with the expected 80% from the English PAN corpus.*
- **Non-Plagiarized Texts:**  
  - Experts: 20.5%  
  - Expected (English PAN): 20%

**Granular Breakdown of Plagiarism Levels:**

- **Non-Plagiarized:** ~20.5%
- **Partially Plagiarized:** ~22.5%
- **Mostly Plagiarized:** ~28.0%
- **Fully Plagiarized:** ~29.5%

**Detailed Evaluation on 200 Duplicated Tasks:**

- **Non-Plagiarized:** 20.0%
- **Partially Plagiarized:** 22.5%
- **Mostly Plagiarized:** 28.0%
- **Fully Plagiarized:** 29.5%

*Key Insights:*  
The expert assessments demonstrate nearly perfect consensus (99.75% agreement) on the non-plagiarized texts. A small 0.5% increase in non-plagiarized texts (20% vs. 20.5%) indicates that in a few cases, partial plagiarism signals were weakened during translation. The clear gradation in plagiarism severity confirms that experts reliably distinguish between partial, mostly, and fully plagiarized content.

---

## Overall Conclusions

- **Translation Quality:**  
  With 97.15% of the translations deemed acceptable, the Google-translated Kazakh texts maintain their intended meaning with minimal discrepancies.

- **Plagiarism Signal Preservation:**  
  The translated texts retain expected plagiarism patterns—with approximately 80% of text pairs being plagiarized—demonstrating that translation has little adverse impact on the detection signal.

- **Expert Consistency:**  
  The high inter-rater reliability (as evidenced by the 200 duplicated tasks) reinforces the robustness of the assessments, confirming the overall quality and suitability of the translated dataset for further use in the extrinsic plagiarism detection pipeline.

---

These expert assessments provide valuable validation for the translated dataset, ensuring its quality for training and evaluation in our Kazakh extrinsic plagiarism detection project.
