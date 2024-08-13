# Text Classification of BBC News Articles

## Overview
This project involves the classification of BBC News Articles into five categories: Business, Entertainment, Politics, Sport, and Tech. Various machine learning classifiers were used in conjunction with unigram, bigram, and trigram models to achieve this task. The classifiers used in this project include Naive Bayes, Logistic Regression, Support Vector Machine (SVM), Random Forest, and K-Nearest Neighbors (KNN).

## Dataset
The dataset used in this project consists of BBC News articles, each labeled with one of the five categories. The data was preprocessed to clean and tokenize the text, and then different n-gram models were applied.

## Preprocessing Steps
The following preprocessing steps were performed on the dataset:

1. Lowercasing Text
2. Removing HTML Tags
3. Removing URLs
4. Removing Punctuations
5. Handling ChatWords
6. Handling StopWords
7. Tokenization
8. Lemmatization

## Models Used
- **Naive Bayes**
- **Logistic Regression**
- **Support Vector Machine (SVM)**
- **Random Forest**
- **K-Nearest Neighbors (KNN)**

## N-Gram Models
Three n-gram models were applied to the dataset:

1. **Unigram Model**: Each word is treated as a separate feature.
2. **Bigram Model**: Pairs of consecutive words are treated as features.
3. **Trigram Model**: Triplets of consecutive words are treated as features.

## Results
The following table summarizes the accuracy of each classifier with different n-gram models:

| Classifier       | Unigram Accuracy | Bigram Accuracy | Trigram Accuracy |
|------------------|------------------|-----------------|------------------|
| Naive Bayes      | 98%              | 96%             | 71%              |
| Logistic Regression | 96%           | 90%             | 52%              |
| SVM              | 96%              | 64%             | 39%              |
| Random Forest    | 97%              | 87%             | 41%              |
| KNN              | 63%              | 24%             | 28%              |

## Analysis
1. **Naive Bayes**: The Naive Bayes classifier achieved the highest accuracy with the unigram model (98%). This suggests that it is well-suited for handling text classification with simpler feature representations. The performance drops with bigrams and trigrams, likely due to increased sparsity and complexity.

2. **Logistic Regression**: This model also performed well with the unigram model (96%) but showed a significant drop with bigrams (90%) and trigrams (52%). The decline indicates that the model might struggle with higher-dimensional feature spaces.

3. **SVM**: The SVM classifier performed best with the unigram model (96%) but struggled with bigrams and trigrams. The performance degradation with more complex n-gram models suggests that SVM may not handle the increased feature space as effectively.

4. **Random Forest**: Random Forest achieved high accuracy with the unigram model (97%) but experienced a notable decrease with bigrams (87%) and trigrams (41%). The drop might be due to the model's tendency to overfit on complex features.

5. **KNN**: The KNN classifier showed the lowest performance across all n-gram models, with the highest accuracy being 63% for unigrams. The performance decline with bigrams and trigrams further suggests that KNN struggles with high-dimensional and sparse feature spaces.

## How to Run the Project

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Akiffazal/bbc-news-classification.git
   ```
   
2. **Install the Required Libraries**
   ```bash
   pip install -r requirements.txt
   ```
   
3. **Run the Jupyter Notebook**
   ```bash
   jupyter notebook
   ```
   
   Open the `BBC_News_Classification.ipynb` file and run the cells to preprocess the data, train the models, and evaluate their performance.

## Conclusion
Naive Bayes and Random Forest classifiers performed well with the unigram model, achieving the highest accuracy. However, as the complexity of the n-gram models increased, the performance of all classifiers declined, with the trigram model showing the least accuracy across all classifiers.

---
