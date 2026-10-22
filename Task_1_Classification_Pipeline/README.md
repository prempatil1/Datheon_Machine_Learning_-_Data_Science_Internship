# Task 1: Multi-Class Classification Pipeline

## Project Overview
This project uses the Iris flower dataset to build and evaluate
two supervised machine learning classification models:
Logistic Regression and Decision Tree Classifier.

The objective is to predict the species of an Iris flower using
its sepal and petal measurements.

## Dataset
- Source: Seaborn Iris dataset
- Total samples: 150
- Features: 4 numerical measurements
- Target: `species`
- Classes: Setosa, Versicolor, Virginica
- Missing values: None

## Technologies Used
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Methodology
1. Load and inspect the Iris dataset.
2. Perform exploratory data analysis (EDA).
3. Visualize feature relationships using a pairplot.
4. Split the data into 80% training and 20% testing sets.
5. Scale features using StandardScaler.
6. Train Logistic Regression and Decision Tree models.
7. Evaluate both models using classification metrics.
8. Visualize confusion matrices and decision boundaries.

## Model Performance

| Metric | Logistic Regression | Decision Tree |
|---|---:|---:|
| Accuracy | 93.33% | 93.33% |
| Macro Precision | 93.33% | 93.33% |
| Macro Recall | 93.33% | 93.33% |
| Macro F1-Score | 93.33% | 93.33% |

Both models correctly classified 28 out of 30 test samples.

## Visualizations
- Exploratory pairplot
- Confusion matrix heatmaps
- Decision boundary plots using petal length and petal width

Note: Decision boundary plots use two features for 2D visualization.
The main evaluation models use all four numerical features.

## How to Run
1. Install the dependencies listed in the repository's `requirements.txt`.
2. Open `Task_1_Classification_Pipeline.ipynb` in VS Code.
3. Select the appropriate Python environment.
4. Run the notebook cells in order.

## Project Status
Implemented and evaluated locally. Final verification and GitHub
submission remain pending.