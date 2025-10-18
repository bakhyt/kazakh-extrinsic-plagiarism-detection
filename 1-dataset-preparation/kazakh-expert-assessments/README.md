
### 📁 `1-dataset-preparation/kazakh-expert-assessments/`

# Expert Assessments of the Kazakh PAN-KK Dataset

This folder contains native-speaker evaluations of the Google-translated **PAN 2010** plagiarism dataset (English → Kazakh). The assessments verify **translation quality** and **preservation of plagiarism signals**.

---

## 📚 Background

* **Dataset origin:** more than 20k suspicious–source pairs from PAN 2010, translated to Kazakh (Google Translate) with manual alignment.
* **Evaluation sample:** 2,000 pairs.
* **Expert panel:** 10 native Kazakh speakers; each evaluated 200 pairs. **200 pairs were duplicated** to measure agreement.

---

## 🧪 Assessment Methodology

Each expert read both texts (suspicious and translated source) and answered two questions:

**Q1 — Translation Meaningfulness (Kazakh rendering of the source)**

* 10 = Not meaningful
* 11 = Imperfect but understandable
* 12 = Fully meaningful

**Q2 — Plagiarism Similarity (suspicious vs. translated source)**

* 20 = Dissimilar
* 21 = Similar (same topic, differing details)
* 22 = Very similar (nearly same meaning)
* 23 = Identical (stylistic edits only)

> 200 of the 2,000 examples were intentionally duplicated (re-IDed) to estimate inter-annotator reliability.

---

## 🎥 Assessment Instructions

A 40-minute video explained Q1/Q2 and walked through five examples.
📺 **YouTube:** [https://youtu.be/2219IXAgBr4?si=gqLNDYQZulwyFBeY](https://youtu.be/2219IXAgBr4?si=gqLNDYQZulwyFBeY)

---

## 📂 Folder Contents

* **Expert ratings (raw):** Per-rater text files (e.g., `instruction.txt`, `info.txt`) organized in subfolders.
  Zip archive: [`kazakh-experts-evaluation.zip`](./kazakh-experts-evaluation.zip)
* **Processing code:** Notebook to parse files, compute agreement, and summarize results:
  [`../1-1-translation-assessments-summary.ipynb`](../1-1-translation-assessments-summary.ipynb)
* **Summaries (CSVs):**

  * Q1: [`first-question-2000-tasks-summary.csv`](./first-question-2000-tasks-summary.csv)
  * Q2: [`second-question-2000-tasks-summary.csv`](./second-question-2000-tasks-summary.csv)
  * Duplicated subset:
    [`first-question-20-shared-tasks-summary.csv`](./first-question-20-shared-tasks-summary.csv),
    [`second-question-20-shared-tasks-summary.csv`](./second-question-20-shared-tasks-summary.csv)

---

## 📈 Results Summary (Per-item Annotator Agreement)

For each document pair, we report aggregated votes, the majority label, **CSI**, and the consensus margin **Δ**. Each row in the summary CSVs corresponds to one suspicious–source pair.

* **Q1 (Meaningfulness):** Average **CSI = 61.5%**. Disagreement concentrates between **11** and **12** (both “meaningful”), which lowers consensus despite otherwise consistent judgments.
* **Q2 (Plagiarism):** Average **CSI = 64.0%**. Annotators are **unanimous on 20** (*Dissimilar*) and show strong agreement on **23** (*Identical*); residual disagreement appears at the **21–22** boundary (*Similar* vs. *Very similar*).

Additional aggregates:

* All items (**100%**, 20/20) are judged **meaningful** (majority in `{11, 12}`); within this set, **12 = 70%**, **11 = 30%**.
* Applying a decisiveness filter (**Δ ≥ 0.2**) retains **80%** (16/20) as **high-confidence** items; among those, **12 = 62.5%**, **11 = 37.5%**.
* **Ties (Δ = 0)** account for **20%** (4/20), all adjacent (**12 vs. 11**).

**Takeaway:** Strong convergence on clear cases with localized ambiguity at adjacent label boundaries—supporting the reliability of the annotated dataset for subsequent analysis and modeling.

---

## 🔍 Agreement Metrics (as used in the paper)

* **Consensus Strength Index (per item):**
  (\mathrm{CSI}*i=\frac{\max*{c\in C} v_{i,c}}{M}); corpus average (\mathrm{CSI}=\frac{1}{N}\sum_i \mathrm{CSI}_i).
* **Consensus margin:**
  (\Delta=\frac{v^{(1)}-v^{(2)}}{M}) (largest minus second-largest vote counts, divided by annotators).
  Tie policy: if top labels tie (e.g., 5–5 with (M=10)), mark as tie and set (\Delta=0).

*(These are recomputed by the provided notebook for both the full set and the duplicated subset.)*

---

## 📥 Availability

Dataset splits and code will be provided to reviewers via an anonymized link; public release (versioned and licensed) will follow upon acceptance.
