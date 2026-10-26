# Datheon Machine Learning & Data Science Internship

A collection of four machine learning and data science projects completed as part of the Datheon Machine Learning & Data Science Internship.

The repository covers supervised classification, regression, customer churn prediction, and NLP sentiment analysis using Python and Scikit-learn.

## Projects

| Task | Project | Techniques | Status |
|---|---|---|---|
| 1 | [Multi-Class Iris Classification](Task_1_Classification_Pipeline/) | Logistic Regression, Decision Tree, StandardScaler | Implemented |
| 2 | [Housing Price Prediction](Task_2_House_Price_Prediction/) | OLS, Ridge, Lasso, GridSearchCV | Implemented |
| 3 | [Customer Churn Prediction](Task_3_Customer_Churn_Prediction/) | Random Forest, XGBoost, class weighting, ROC-AUC | Implemented |
| 4 | [NLP Sentiment Classification](Task_4_NLP_Sentiment_Analysis/) | Text preprocessing, TF-IDF, Naive Bayes, Logistic Regression | Implemented as a small-data demonstration |

Each project folder contains its own Jupyter Notebook and README with methodology, results, and instructions.

## Project Highlights

### Task 1 — Multi-Class Classification

- Dataset: Iris flower measurements
- Models: Logistic Regression and Decision Tree
- Test accuracy: 93.33% for both models
- Includes exploratory data analysis, classification reports, confusion matrices, and decision-boundary visualizations.

### Task 2 — Housing Price Prediction

- Dataset: California Housing
- Models: Ordinary Least Squares, Ridge Regression, and Lasso Regression
- Best test RMSE: approximately $69,048
- Test R²: approximately 0.636
- Includes feature engineering, correlation and VIF analysis, GridSearchCV tuning, and residual visualizations.

### Task 3 — Customer Churn Prediction

- Dataset: Telco Customer Churn
- Models: Random Forest and XGBoost
- XGBoost test ROC-AUC: 0.8405
- XGBoost test recall: 0.7781
- Includes class-imbalance handling, cross-validation, ROC curves, confusion matrices, and feature importance.

### Task 4 — NLP Sentiment Classification

- Dataset: `sentiment_reviews.csv`
- Models: Multinomial Naive Bayes and Logistic Regression
- Techniques: Text cleaning, stopword removal, lemmatization, and TF-IDF vectorization
- Includes model comparison, confusion matrices, and a `predict_sentiment()` function.

**Dataset limitation:** The provided dataset contains only 10 reviews. After excluding the neutral review for binary classification, 9 reviews remain, with 7 used for training and 2 for testing. The resulting metrics are for demonstration only and are not reliable estimates of real-world performance.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- XGBoost
- NLTK
- Jupyter Notebook

## Getting Started

1. Clone the repository:

   `git clone https://github.com/prempatil1/Datheon_Machine_Learning_-_Data_Science_Internship.git`

2. Move into the project directory:

   `cd Datheon_Machine_Learning_-_Data_Science_Internship`

3. Install the required packages:

   `pip install -r requirements.txt`

4. Open the required task folder and launch its Jupyter Notebook in VS Code or Jupyter.

5. Follow the instructions in that task's README and run the notebook cells in order.

Some datasets are loaded from public URLs, so an internet connection may be required. Task 4 uses the local `sentiment_reviews.csv` file provided in its project folder.

## Repository Structure

```text
Datheon_Machine_Learning_-_Data_Science_Internship/
├── Task_1_Classification_Pipeline/
│   ├── Task_1_Classification_Pipeline.ipynb
│   └── README.md
├── Task_2_House_Price_Prediction/
│   ├── Task_2_House_Price_Prediction.ipynb
│   └── README.md
├── Task_3_Customer_Churn_Prediction/
│   ├── Task_3_Customer_Churn_Prediction.ipynb
│   └── README.md
├── Task_4_NLP_Sentiment_Analysis/
│   ├── Task_4_NLP_Sentiment_Analysis.ipynb
│   ├── sentiment_reviews.csv
│   └── README.md
├── requirements.txt
└── README.md
```

## Notes

These projects demonstrate practical machine learning workflows, from data exploration and preprocessing to model evaluation and visualization. Results should be interpreted in the context of each dataset's size and limitations.

