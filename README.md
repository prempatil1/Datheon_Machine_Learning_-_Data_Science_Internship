# Datheon Machine Learning & Data Science Internship

A collection of four machine learning and data science projects covering classification, regression, customer churn prediction, and Natural Language Processing (NLP).

The projects use Python and popular data science libraries to demonstrate data exploration, preprocessing, model training, evaluation, and visualization.

## Projects Overview

| Task | Project | Models and Techniques | Key Result |
|---|---|---|---|
| 1 | [Multi-Class Iris Classification](Task_1_Classification_Pipeline/) | Logistic Regression, Decision Tree, StandardScaler | 93.33% test accuracy for both models |
| 2 | [Housing Price Prediction](Task_2_House_Price_Prediction/) | OLS, Ridge, Lasso, GridSearchCV | OLS test RMSE: approximately $69,048 |
| 3 | [Customer Churn Prediction](Task_3_Customer_Churn_Prediction/) | Random Forest, XGBoost, class weighting | XGBoost test ROC-AUC: 0.8405 |
| 4 | [NLP Sentiment Classification](Task_4_NLP_Sentiment_Analysis/) | Text preprocessing, TF-IDF, Naive Bayes, Logistic Regression | Small-data demonstration |

Each project folder contains a Jupyter Notebook and a dedicated README describing its methodology, results, and instructions.

## Project Roadmap

### Task 1 — Multi-Class Classification Pipeline

**Goal:** Predict Iris flower species using supervised machine learning.

- Load and explore the Iris dataset.
- Perform exploratory data analysis (EDA) and visualize feature relationships.
- Split the data into training and testing sets using an 80:20 split.
- Scale numerical features using `StandardScaler`.
- Train Logistic Regression and Decision Tree classifiers.
- Evaluate accuracy, precision, recall, and F1-score.
- Visualize confusion matrices and decision boundaries.

**Key Result:** Both models achieved 93.33% test accuracy, correctly classifying 28 of 30 test samples.

[View Task 1 Notebook and README](Task_1_Classification_Pipeline/)

### Task 2 — Housing Price Prediction

**Goal:** Predict median house values using the California Housing dataset.

- Load and inspect the dataset.
- Perform EDA and examine the house-value distribution.
- Split the data into training and testing sets.
- Create engineered features and an interaction feature.
- Configure preprocessing for missing values, scaling, and categorical encoding.
- Analyze correlations and multicollinearity using VIF.
- Train Ordinary Least Squares (OLS), Ridge, and Lasso regression models.
- Tune Ridge and Lasso using five-fold `GridSearchCV`.
- Compare RMSE, MAE, and R².
- Visualize actual versus predicted values and residual distributions.

**Key Result:** OLS achieved a test RMSE of approximately $69,048 and an R² of approximately 0.636.

[View Task 2 Notebook and README](Task_2_House_Price_Prediction/)

### Task 3 — Predictive Customer Churn Classifier

**Goal:** Predict which telecommunications customers are likely to leave the service.

- Load and inspect the Telco Customer Churn dataset.
- Convert `TotalCharges` to numeric and identify missing values.
- Analyze customer churn distribution and class imbalance.
- Split data using stratified sampling.
- Configure preprocessing for missing values and categorical encoding.
- Address class imbalance using class weighting.
- Train Random Forest and XGBoost classifiers.
- Evaluate models using five-fold cross-validation.
- Compare ROC-AUC, precision, recall, and F1-score.
- Plot ROC curves and confusion matrices.
- Visualize the top 10 features using XGBoost feature importance.

**Key Result:** XGBoost achieved a test ROC-AUC of 0.8405 and a recall of 0.7781.

[View Task 3 Notebook and README](Task_3_Customer_Churn_Prediction/)

### Task 4 — NLP Sentiment Classification

**Goal:** Classify customer reviews as positive or negative.

- Load and inspect the provided review dataset.
- Clean text by converting it to lowercase and removing HTML tags and punctuation.
- Remove stopwords while preserving important negation words.
- Apply lemmatization.
- Split the data into training and testing sets.
- Convert text into numerical features using TF-IDF with `max_features=5000`.
- Train Multinomial Naive Bayes and Logistic Regression.
- Compare classification metrics and visualize confusion matrices.
- Implement a `predict_sentiment()` function for custom reviews.

**Dataset Limitation:** The provided `sentiment_reviews.csv` contains only 10 reviews: 5 positive, 4 negative, and 1 neutral. After excluding the neutral review, only 9 reviews remain for binary classification, with 7 used for training and 2 for testing. The resulting metrics are for demonstration only and are not reliable estimates of real-world model performance.

[View Task 4 Notebook, Dataset, and README](Task_4_NLP_Sentiment_Analysis/)

## Technologies Used

- **Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Gradient Boosting:** XGBoost
- **Natural Language Processing:** NLTK, TF-IDF
- **Development Environment:** Jupyter Notebook, VS Code
- **Version Control:** Git and GitHub

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/prempatil1/Datheon_Machine_Learning_-_Data_Science_Internship.git
```

### 2. Navigate to the Project Directory

```bash
cd Datheon_Machine_Learning_-_Data_Science_Internship
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Open a Project Notebook

Open the required task folder in VS Code or Jupyter Notebook, select a compatible Python environment, and run the notebook cells in order.

**Note:** An internet connection is required for tasks that load datasets from public URLs and for downloading NLTK language resources when needed. Task 4 uses the local `sentiment_reviews.csv` file included in its project folder.

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

## Project Notes

These projects demonstrate practical workflows spanning exploratory data analysis, feature engineering, data preprocessing, model training, hyperparameter tuning, evaluation, and visualization.

Performance results should be interpreted in the context of the dataset, evaluation method, and any limitations. In particular, Task 4 is a small-data demonstration rather than a reliable benchmark for real-world sentiment classification.
