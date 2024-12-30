
# Fraud Detection Analysis and Model Evaluation

## Project Overview

This project involves analyzing synthetic financial transaction data to identify fraudulent transactions. The dataset is processed, visualized, and analyzed to engineer features, uncover patterns, and train machine learning models for classification.

---

## Table of Contents

1. [Project Steps](#project-steps)
2. [Dataset Description](#dataset-description)
3. [Data Visualization](#data-visualization)
4. [Feature Engineering](#feature-engineering)
5. [Machine Learning Models](#machine-learning-models)
6. [Evaluation Metrics](#evaluation-metrics)
7. [Prerequisites](#prerequisites)
8. [How to Run](#how-to-run)


---

## Project Steps

1. **Data Loading:** Load the dataset (`Synthetic_Financial_datasets_log.csv`) and preview its structure.
2. **Variable Analysis:** Analyze the type and significance of variables.
3. **Exploratory Data Analysis (EDA):**
   - Distribution of transaction types.
   - Fraudulent transaction analysis by type.
   - Correlation heatmaps for fraud indicators.
4. **Feature Engineering:**
   - Add `balance_diff`, `relative_amount`, and `suspicious` columns.
   - Encode categorical variables for modeling.
5. **Machine Learning Modeling:**
   - Train various classifiers like Logistic Regression, Decision Tree, Random Forest, etc.
   - Evaluate models using Accuracy, Precision, Recall, and F1-Score.

---

## Dataset Description

The dataset contains the following columns:
- **step**: Discrete time units representing transaction order.
- **type**: Transaction type (e.g., CASH-IN, TRANSFER).
- **amount**: Monetary value of the transaction.
- **nameOrig**: Unique identifier for origin account.
- **oldbalanceOrg**: Account balance before the transaction (origin account).
- **newbalanceOrig**: Account balance after the transaction (origin account).
- **nameDest**: Unique identifier for destination account.
- **oldbalanceDest**: Account balance before the transaction (destination account).
- **newbalanceDest**: Account balance after the transaction (destination account).
- **isFraud**: Binary indicator (1 = Fraudulent transaction, 0 = Non-fraudulent).
- **isFlaggedFraud**: Binary indicator for flagged fraud (1 = Flagged, 0 = Not Flagged).

---

## Data Visualization

1. **Transaction Type Distribution:**
   - Bar chart showing the frequency of transaction types.
2. **Fraudulent Transactions by Type:**
   - Bar chart for fraudulent transaction counts by type.
3. **Correlation Heatmap:**
   - Visualize relationships between variables, including fraud indicators.
4. **Pie Chart for Transaction Distribution:**
   - Pie chart displaying the proportion of transaction types.

---

## Feature Engineering

New features added to enhance model performance:
1. **balance_diff:** Difference between `oldbalanceOrg` and `newbalanceOrig`.
2. **relative_amount:** Relative transaction amount as a ratio of `amount` to `oldbalanceOrg`.
3. **suspicious:** Flag for transactions where the balance remains unchanged despite a transaction.

---

## Machine Learning Models

The following classifiers are used to detect fraud:
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Naive Bayes
- AdaBoost

Each classifier is evaluated using a consistent training-test split (80-20).

---

## Evaluation Metrics

The models are assessed based on:
1. **Accuracy:** Proportion of correct predictions.
2. **Precision:** Proportion of correctly identified fraudulent transactions.
3. **Recall:** Ability to detect all fraudulent transactions.
4. **F1-Score:** Harmonic mean of Precision and Recall.

---

## Prerequisites

Ensure the following dependencies are installed:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly
```

---

## How to Run

1. Place the dataset (`Synthetic_Financial_datasets_log.csv`) in the project directory.
2. Execute the script in jupyter notebook (main_final.ipynb)
3. View the printed metrics and visualizations.


