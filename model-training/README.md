**Kazakh Model Training**  

In this stage, we train a **multilingual XLM-RoBERTa Large** model on our custom-prepared **Kazakh dataset** for the task of **text similarity and plagiarism detection**. The dataset consists of 120,000 labeled pairs of suspicious and source texts, balanced across positive (plagiarized) and negative (non-plagiarized) examples.

Given the low-resource nature of the **Kazakh language**, we leverage a **pretrained transformer model** capable of handling multilingual text to fine-tune it for our specific task. We use stratified splitting to ensure label balance across training and validation sets and apply several optimization techniques such as learning rate scheduling, mixed precision training, and regularization to improve performance.

The goal of this training is to produce a robust model that can accurately classify whether two given paragraphs are semantically similar or not.
