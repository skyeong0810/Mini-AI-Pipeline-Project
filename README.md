# Mini-AI-Pipeline-Project

Task:
Classify news headlines into one of four categories-
World
Sports
Business
Sci/Tech

Input:
A single news headline (short text)

Output:
One category label

Motivation:
Automatic news categorization helps organize large volumes of online news and improves user experience in news aggregation systems.

Success Criteria:
Higher accuracy and F1-score than a naïve baseline
Consistent improvement across all categories

# Reflection
The keyword-based baseline performed worse than expected on ambiguous headlines, especially when words like “Apple” or “Amazon” appeared outside their usual contexts. The transformer-based model significantly improved performance by capturing semantic meaning rather than relying on surface-level keywords. However, training required more computational resources and careful tokenization. Accuracy and F1-score were useful metrics, but they did not fully reflect model confidence or uncertainty. One limitation of this project is the small dataset size, which may limit generalization. Given more time, I would experiment with data augmentation or compare multiple pre-trained models.
