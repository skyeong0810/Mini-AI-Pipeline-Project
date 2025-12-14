# Mini AI Pipeline Project: News Headline Classification

## 1. Task Description and Motivation
This project aims to classify news headlines into four categories:
World, Sports, Business, and Sci/Tech. The task is useful for
automatically organizing news articles in large-scale news platforms.

## 2. Dataset
We use a subset of the AG News dataset from Hugging Face. A total of
2,500 samples were used, with 2,000 for training and 500 for testing.
All text was lowercased and truncated to 128 tokens.

## 3. Naïve Baseline
The baseline classifier uses keyword-based rules to detect Sports,
Business, and Sci/Tech headlines. Headlines that do not match any
keywords are classified as World.

## 4. AI Pipeline
Our AI pipeline uses DistilBERT as a pre-trained encoder, followed by
a classification head. The pipeline consists of tokenization,
representation, and decision stages.

## 5. Evaluation and Results
| Method | Accuracy | F1 |
|--------|----------|----|
| Baseline | 0.380 | 0.403 |
| DistilBERT | 0.878 | 0.879 |

## 6. Reflection and Limitations
The keyword-based baseline struggled with ambiguous headlines. The
Transformer-based model performed significantly better by capturing
semantic context. However, the small dataset limits generalization.
