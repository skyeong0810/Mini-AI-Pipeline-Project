# Mini AI Pipeline Project: News Headline Classification

## 1. Task Description and Motivation
This project aims to classify news headlines into four categories:\n
World, Sports, Business, and Sci/Tech. The task is useful for automatically organizing news articles in large-scale news platforms.

## 2. Dataset
We use a subset of the AG News dataset from Hugging Face. A total of 2,500 samples were used, with 2,000 for training and 500 for testing.\n
All text was lowercased and truncated to 128 tokens.

## 3. Naïve Baseline
The baseline classifier uses keyword-based rules to detect Sports, Business, and Sci/Tech headlines.\n
Headlines that do not match any keywords are classified as World.

## 4. AI Pipeline
Our AI pipeline uses DistilBERT as a pre-trained encoder, followed by a classification head.\n
The pipeline consists of tokenization, representation, and decision stages.

## 5. Evaluation and Results
| Method | Accuracy | F1 |
|--------|----------|----|
| Baseline | 0.380 | 0.403 |
| DistilBERT | 0.878 | 0.879 |

## 6. Reflection and Limitations
The keyword-based baseline performed worse than expected on ambiguous headlines, especially when words like “Apple” or “Amazon” appeared outside their usual contexts. The transformer-based model significantly improved performance by capturing semantic meaning rather than relying on surface-level keywords. However, training required more computational resources and careful tokenization. Accuracy and F1-score were useful metrics, but they did not fully reflect model confidence or uncertainty. One limitation of this project is the small dataset size, which may limit generalization. Given more time, I would experiment with data augmentation or compare multiple pre-trained models.
