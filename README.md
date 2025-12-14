# Mini AI Pipeline Project: News Headline Classification

## 1. Task Description and Motivation
This project aims to classify news headlines into four categories:  
World, Sports, Business, and Sci/Tech.

The task is useful for automatically organizing news articles in large-scale
news platforms and serves as a clear example for comparing simple rule-based
methods with modern AI pipelines.

---

## 2. Dataset
We use a subset of the **AG News** dataset from Hugging Face. A total of
2,500 samples were used, with 2,000 for training and 500 for testing.

All text was lowercased and truncated to a maximum length of 128 tokens.
No additional preprocessing was applied.

---

## 3. Naïve Baseline
The baseline classifier uses keyword-based rules to detect Sports, Business,
and Sci/Tech headlines.

Headlines that do not match any predefined keywords are classified as
World by default. This approach is considered naïve because it relies on
surface-level word matching and cannot capture contextual meaning.

---

## 4. AI Pipeline
Our AI pipeline uses **DistilBERT** as a pre-trained encoder, followed by a
classification head.

The pipeline consists of tokenization, contextual representation using
the Transformer model, and a final decision stage that predicts one of
the four categories.

---

## 5. Evaluation and Results

| Method       | Accuracy | F1    |
|--------------|----------|-------|
| Baseline     | 0.380    | 0.403 |
| DistilBERT   | 0.878    | 0.879 |

The Transformer-based model significantly outperformed the naïve baseline
across both evaluation metrics.

---

## 6. Reflection and Limitations
The keyword-based baseline performed worse than expected on ambiguous
headlines, especially when words like “Apple” or “Amazon” appeared outside
their usual contexts. The Transformer-based model significantly improved
performance by capturing semantic meaning rather than relying on surface-level
keywords.

However, training required more computational resources and careful
tokenization. Accuracy and F1-score were useful metrics, but they did not fully
reflect model confidence or uncertainty. One limitation of this project is the
small dataset size, which may limit generalization. Given more time, I would
experiment with data augmentation or compare multiple pre-trained models.
