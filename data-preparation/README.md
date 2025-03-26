### 📁 `data-preparation/` Folder

This folder contains the **code and scripts used for preparing the dataset** for the *Kazakh Text Similarity Detection* task.

#### 📄 `1_extract_plagiarised_texts_and_translate_and_create_dataset.ipynb`

This notebook includes the following steps:

1. **Extraction** of plagiarized text segments from the [PAN Plagiarism Detection Corpus](https://pan.webis.de/).
2. Using PAN XML files to locate suspicious and source texts via offset and length.
3. **Saving the extracted segments** as individual `.txt` files.
4. **Translating** the English segments into **Kazakh** using Google Translate API.
5. Organizing English–Kazakh pairs into folders by alignment.
6. **Creating a labeled CSV dataset** suitable for training text similarity detection models.

---

### 📌 Notes:
- Both **suspicious** and **source** texts are extracted.
- Each aligned pair is labeled (`1` for plagiarized, `0` for non-plagiarized).
- Translations are prefixed with `kz-` for distinction.
- The output is structured and ready for model training and evaluation.
