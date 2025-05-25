## 📁 `4-plagiarism-detection-pipeline-and-evaluation/` Folder

## 🧪 Plagiarism Detection Pipeline and Evaluation

This folder hosts the implementation of a **two-step plagiarism detection pipeline** tailored for the **Kazakh language**. The pipeline uses a **hybrid approach** that combines:

* **SimHash**: Efficiently detects candidate text regions likely to contain plagiarism by quickly narrowing down large search spaces.
* **Fine-tuned Transformer Model**: Performs precise semantic classification of suspicious–source text pairs as **plagiarized** or **non-plagiarized** using a Kazakh-trained transformer (e.g., XLM-RoBERTa or KazakhBERTmulti).

This design balances **speed** and **accuracy**, making it suitable for practical deployment on large-scale document collections.

---

### 📄 Evaluation Setup

To evaluate the effectiveness of the pipeline, we used a **realistic and rigorous test scenario** based on actual plagiarism cases from the PAN dataset.

* **Test Set**:
  1,000 suspicious–source document pairs randomly sampled from the PAN corpus, each with manually annotated plagiarized segments in the original XML metadata.

* **Kazakh Translation**:
  All document pairs were automatically translated into Kazakh. For each pair, a row was created in a CSV file containing:

  * The full **suspicious document** (in Kazakh)
  * The full **source document** (in Kazakh)
  * A list of **gold-standard plagiarized segments** (translated from PAN annotations)

---

### ⚙️ Evaluation Procedure

For each document pair (i.e., each row in the CSV file), the pipeline performs the following steps:

1. **Candidate Detection**:
   SimHash identifies potential plagiarized regions within the suspicious and source documents.

2. **Semantic Classification**:
   The fine-tuned transformer model evaluates each candidate region to determine if it represents plagiarism.

3. **Metrics Calculation**:
   The predicted plagiarized spans are compared against the gold-standard.
   Evaluation is conducted at the **word level**, and for each pair, the pipeline computes:

   * **Precision**
   * **Recall**
   * **F1-Score**

---

### 📊 Final Output

After processing all 1,000 document pairs, the pipeline reports the **average scores** across the full test set:

* **Average Precision**
* **Average Recall**
* **Average F1-Score**

---

This end-to-end evaluation framework provides a **realistic benchmark** of how well the system performs on full-length translated documents, simulating **practical use cases** such as academic integrity tools or automated manuscript screening in the Kazakh language.
