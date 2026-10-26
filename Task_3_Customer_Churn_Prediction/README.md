# Task 3: Predictive Customer Churn Classifier

## Project Overview

This project predicts whether a telecommunications customer
will leave the service using the Telco Customer Churn dataset.

Two classification models are developed and compared:
- Random Forest Classifier
- XGBoost Classifier

## Objectives

- Clean the dataset and convert `TotalCharges` to numeric.
- Analyze customer churn and class imbalance.
- Split the data using stratified train-test splitting.
- Handle missing values and encode categorical features.
- Address class imbalance using class weighting.
- Evaluate models using five-fold cross-validation.
- Compare ROC-AUC, precision, recall, and F1-score.
- Plot ROC curves and confusion matrices.
- Identify the top 10 features using XGBoost feature importance.

## Dataset

- **Source:** [Telco Customer Churn Dataset](https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv)
- **Rows:** 7,043
- **Columns:** 21
- **Target:** `Churn`
- **Classes:** `Yes` and `No`
- **Missing values:** 11 blank values in `TotalCharges`

The dataset is loaded directly from a public CSV URL.

## Methodology

1. Load and inspect the dataset.
2. Convert `TotalCharges` to numeric and identify missing values.
3. Analyze churn class distribution.
4. Split the data into 80% training and 20% testing sets.
5. Build preprocessing pipelines for imputation and categorical encoding.
6. Apply class weighting to address class imbalance.
7. Train Random Forest and XGBoost using five-fold cross-validation.
8. Evaluate both models on the held-out test set.
9. Visualize ROC curves, confusion matrices, and feature importance.

## Cross-Validation Results

| Model | ROC-AUC | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| XGBoost | 0.8446 | 0.5356 | 0.7746 | 0.6332 |
| Random Forest | 0.8212 | 0.6309 | 0.4722 | 0.5399 |

## Test Set Results

| Model | ROC-AUC | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| XGBoost | 0.8405 | 0.5291 | 0.7781 | 0.6299 |
| Random Forest | 0.8224 | 0.6170 | 0.4652 | 0.5305 |

XGBoost achieved a test ROC-AUC above 0.80 and higher recall
than Random Forest. It was therefore selected as the preferred
model for identifying potential churners in this experiment.

## Feature Importance

The top features identified by the trained XGBoost model include:

1. Month-to-month contract
2. Fiber-optic internet service
3. No online security
4. No tech support
5. Two-year contract

Feature importance describes how the trained model uses
features; it does not establish causation.

## Visualizations

- Customer churn class distribution
- ROC curves for both models
- Confusion matrices
- Top 10 feature importance bar chart

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

## How to Run

1. Install Python and Jupyter Notebook.
2. Install the dependencies:

   `pip install pandas numpy matplotlib seaborn scikit-learn xgboost`

3. Open `Task_3_Customer_Churn_Prediction.ipynb`.
4. Select the appropriate Python environment.
5. Run the notebook cells in order.

An internet connection is required to load the dataset.

## Conclusion

The project demonstrates customer churn prediction,
class imbalance handling, model comparison, ROC-AUC
evaluation, confusion matrix analysis, and feature importance.

XGBoost achieved a test ROC-AUC of 0.8405 and recall of
0.7781, making it the preferred model for this experiment.
