# Credit Card Fraud Detection using Machine Learning

## Project Overview

This project focuses on detecting fraudulent credit card transactions using supervised machine learning techniques. Due to the highly imbalanced nature of fraud datasets, Synthetic Minority Oversampling Technique (SMOTE) was applied to balance the training data before model training.

The project follows a complete machine learning workflow including Exploratory Data Analysis (EDA), data preprocessing, class balancing, model training, evaluation, and hyperparameter tuning.

---

## Objectives

- Perform Exploratory Data Analysis (EDA)
- Handle missing values and duplicate records
- Analyze class imbalance
- Balance the dataset using SMOTE
- Train Logistic Regression and Random Forest models
- Evaluate models using Precision, Recall, F1-Score, and ROC-AUC
- Identify important features contributing to fraud detection

---

## Dataset

**Dataset Name:** Credit Card Fraud Detection

This project uses the **Credit Card Fraud Detection** dataset containing anonymized transactions made by European cardholders.

Due to GitHub's file size limitations, the original dataset is **not included** in this repository. Instead, a **stratified sample** of the dataset is provided (`creditcard_sample.csv`) to keep the repository lightweight while preserving the original class distribution.

The complete dataset can be downloaded from Kaggle:

https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

After downloading, place the dataset in the project directory before running the notebook if you wish to reproduce the results on the full dataset.

### Dataset Information

- Original Dataset Size: **226,980 Transactions**
- Features: **30**
- Target Variable: **Class**
  - **0** → Legitimate Transaction
  - **1** → Fraudulent Transaction

### Repository Dataset

- File: `creditcard_sample.csv`
- Purpose: Demonstration and reproducibility
- Sampling Method: Stratified Sampling
- Preserves the original fraud-to-normal transaction ratio.

### Features

| Feature | Description |
|----------|-------------|
| Time | Seconds elapsed between transactions |
| V1 - V28 | PCA-transformed confidential features |
| Amount | Transaction Amount |
| Class | Target Variable |

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

---

## Exploratory Data Analysis

The following analyses were performed:

- Dataset Overview
- Missing Value Analysis
- Duplicate Record Detection
- Class Distribution Analysis
- Transaction Amount Distribution
- Correlation Heatmap
- Fraud vs Normal Transaction Visualization

---

## Data Preprocessing

### Missing Values

- Missing values were identified and removed.
- Dataset integrity was verified after preprocessing.

### Duplicate Records

Duplicate transactions were removed to improve model quality.

### Feature Scaling

The following numerical features were standardized using StandardScaler:

- Time
- Amount

---

## Handling Class Imbalance

The dataset was highly imbalanced.

Before SMOTE:

- Legitimate Transactions: 226,602
- Fraudulent Transactions: 378 (or according to processed dataset)

SMOTE was applied only on the training dataset to generate synthetic minority class samples and prevent data leakage.

---

## Machine Learning Models

### Logistic Regression

Used as the baseline classification model.

### Random Forest Classifier

Used as the primary classification model due to its ability to capture complex relationships and handle non-linear decision boundaries.

---

## Model Evaluation Metrics

The following evaluation metrics were used:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix

---

## Random Forest Performance

| Metric | Score |
|---------|-------|
| Accuracy | **99.85%** |
| Precision | **54.17%** |
| Recall | **82.11%** |
| F1 Score | **65.27%** |
| ROC-AUC | **97.36%** |

---

##  Workflow

1. Import Libraries
2. Load Dataset
3. Perform Exploratory Data Analysis
4. Handle Missing Values
5. Remove Duplicate Records
6. Feature Scaling
7. Train-Test Split
8. Apply SMOTE
9. Train Logistic Regression
10. Train Random Forest
11. Hyperparameter Tuning
12. Model Evaluation
13. Performance Comparison
14. Conclusion

---

##  Key Findings

- The dataset was highly imbalanced, making SMOTE essential.
- Random Forest significantly outperformed Logistic Regression.
- The model achieved a high Recall, successfully identifying most fraudulent transactions.
- ROC-AUC above 0.97 indicates excellent discrimination between fraudulent and legitimate transactions.
- Precision and Recall together provide a more meaningful evaluation than Accuracy alone for fraud detection.

---

##  Learning Outcomes

Through this project, the following concepts were implemented:

- Exploratory Data Analysis
- Data Cleaning
- Feature Scaling
- Handling Imbalanced Data
- SMOTE
- Logistic Regression
- Random Forest
- Hyperparameter Tuning
- Model Evaluation
- Fraud Detection

---

##  Future Improvements

- XGBoost Classifier
- LightGBM
- CatBoost
- Ensemble Learning
- Threshold Optimization
- Explainable AI (SHAP & LIME)
- Real-Time Fraud Detection API

---

## Author

**Lavanya Saxena**

B.Tech Artificial Intelligence & Data Science

---
