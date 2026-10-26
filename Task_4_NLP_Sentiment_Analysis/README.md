# Task 4: NLP Sentiment Classification on Customer Reviews

## Project Overview

This project demonstrates a Natural Language Processing (NLP)
pipeline for classifying customer reviews as positive or negative.

The provided `sentiment_reviews.csv` dataset is used to clean text,
extract TF-IDF features, train two classifiers, and test custom
review phrases using an interactive prediction function.

## Objectives

- Inspect the review dataset and sentiment distribution.
- Clean text using lowercasing, HTML tag and punctuation removal.
- Remove stopwords while preserving important negation words.
- Apply lemmatization.
- Convert text into numerical TF-IDF features.
- Train Multinomial Naive Bayes and Logistic Regression.
- Compare classification metrics.
- Visualize confusion matrices.
- Implement a `predict_sentiment()` function for custom reviews.

## Dataset

- **File:** `sentiment_reviews.csv`
- **Rows:** 10
- **Columns:** 3
- **Text column:** `review_text`
- **Target column:** `sentiment`
- **Sentiment distribution:** 5 positive, 4 negative, 1 neutral
- **Missing values:** None

The neutral review is excluded from binary model training because
the assignment focuses on positive and negative sentiment.

## Methodology

1. Load and inspect the provided dataset.
2. Clean and preprocess review text.
3. Exclude neutral reviews for binary classification.
4. Split the remaining reviews into training and testing sets.
5. Fit TF-IDF on training text and transform the test text.
6. Train Multinomial Naive Bayes and Logistic Regression.
7. Evaluate both models using accuracy, precision, recall, and F1-score.
8. Plot confusion matrices.
9. Test custom phrases with `predict_sentiment()`.

## Model Evaluation

The available binary dataset contains only 9 reviews:
7 training reviews and 2 testing reviews.

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Multinomial Naive Bayes | 0.50 | 0.50 | 1.00 | 0.667 |
| Logistic Regression | 0.50 | 0.50 | 1.00 | 0.667 |

Both models classified the two test reviews as positive,
including one negative review.

These metrics are included to document the completed workflow.
They are not reliable estimates of real-world model performance
because the dataset and test set are extremely small.

## Technologies Used

- Python
- Pandas and NumPy
- NLTK
- Scikit-learn
- TF-IDF Vectorizer
- Multinomial Naive Bayes
- Logistic Regression
- Matplotlib and Seaborn

## How to Run

1. Install Python and Jupyter Notebook.
2. Install the dependencies:

   `pip install pandas numpy matplotlib seaborn scikit-learn nltk`

3. Place `sentiment_reviews.csv` in the Task 4 project folder.
4. Open `Task_4_NLP_Sentiment_Analysis.ipynb`.
5. Select the appropriate Python kernel and run the cells in order.

Internet access may be required to download NLTK language resources
during the first run.

## Conclusion

The project implements the required sentiment classification
workflow, including text cleaning, TF-IDF vectorization, two
classification models, evaluation metrics, confusion matrices,
and custom sentiment prediction.

A larger labelled dataset is needed to produce meaningful
benchmark results and more reliable sentiment predictions.