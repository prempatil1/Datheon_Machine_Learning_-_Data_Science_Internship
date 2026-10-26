# Task 2: Real Estate Housing Price Prediction

## Project Overview

This project predicts median house values using the California Housing dataset. Three regression models—Ordinary Least Squares (OLS), Ridge Regression, and Lasso Regression—are trained and evaluated.

## Objectives

- Explore the California Housing dataset.
- Identify and handle missing values.
- Perform feature engineering and create an interaction feature.
- Analyze feature correlations and multicollinearity using VIF.
- Build preprocessing pipelines for imputation, scaling, and categorical encoding.
- Tune Ridge and Lasso using GridSearchCV with five-fold cross-validation.
- Evaluate models using RMSE, MAE, and R².
- Visualize actual versus predicted values and residual distributions.

## Dataset

- **Source:** [California Housing Dataset](https://raw.githubusercontent.com/ageron/handson-ml2/master/datasets/housing/housing.csv)
- **Rows:** 20,640
- **Columns:** 10
- **Target:** `median_house_value`
- **Categorical feature:** `ocean_proximity`
- **Missing data:** 207 values in `total_bedrooms`

The dataset is loaded directly from its public URL, so a separate local CSV file is not required.

## Feature Engineering

The project creates the following features:

- `rooms_per_household`
- `bedrooms_per_room`
- `population_per_household`
- `income_x_house_age` — an interaction between median income and housing median age.

## Methodology

1. Inspect the data and perform exploratory analysis.
2. Split the data into 80% training and 20% testing sets.
3. Engineer additional features.
4. Configure preprocessing for missing values, scaling, and categorical encoding.
5. Examine correlations and VIF values.
6. Train OLS and tune Ridge and Lasso using GridSearchCV.
7. Compare test-set performance and inspect residual plots.

## Model Performance

| Model | RMSE ($) | MAE ($) | R² |
|---|---:|---:|---:|
| OLS | 69,048.192 | 49,376.489 | 0.636 |
| Lasso | 69,049.248 | 49,377.343 | 0.636 |
| Ridge | 69,056.220 | 49,382.628 | 0.636 |

The best alpha selected by cross-validation was 1.0 for both Ridge and Lasso. The three models achieved very similar results on the held-out test set, with OLS recording the lowest RMSE by a small margin.

## Visualizations

- Median house value distribution
- Numerical feature correlation heatmap
- Variance Inflation Factor (VIF) analysis
- Feature correlations with median house value
- Actual versus predicted plots
- Residual distribution plots for all three models

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## How to Run

1. Install Python and Jupyter Notebook.
2. Install the required libraries:

   `pip install pandas numpy matplotlib seaborn scikit-learn jupyter`

3. Open `Task_2_House_Price_Prediction.ipynb` in VS Code or Jupyter.
4. Select a compatible Python kernel.
5. Run the notebook cells in order.

An internet connection is required to load the dataset from its public URL.

## Conclusion

The project demonstrates regression modelling, feature engineering, preprocessing, hyperparameter tuning, model evaluation, and residual analysis using the California Housing dataset. All three models achieved an R² of approximately 0.636, with only minor differences in prediction errors.

