# Customer Churn Prediction Using Logistic Regression

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Logistic%20Regression-orange)
![Status](https://img.shields.io/badge/Project-Completed-success)

## Project Overview

This project uses Machine Learning to predict customer churn in the telecommunications industry.

The objective is to identify customers who may discontinue their services and help businesses understand customer-retention risks.

## Dataset

**Dataset:** IBM Telco Customer Churn

**Source:** [Kaggle - Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

- Total records: 7,043
- Total columns: 21
- Target variable: `Churn`
- Classification type: Binary classification
- Target classes: Yes and No

## Technologies and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Google Colab

## Project Workflow

1. Dataset loading and inspection
2. Data cleaning and missing-value handling
3. Exploratory Data Analysis (EDA)
4. Feature selection
5. Train-test splitting (80:20)
6. One-Hot Encoding
7. Feature scaling using StandardScaler
8. Logistic Regression model training
9. Model evaluation
10. ROC Curve and AUC analysis
11. Classification threshold experiments
12. Class-weight balancing
13. Model saving and documentation

## Original Model Performance

The original Logistic Regression model achieved the following results:

| Evaluation Metric | Result |
|---|---:|
| Accuracy | 80.70% |
| Precision | 66.04% |
| Recall | 56.15% |
| F1-Score | 60.69% |
| ROC-AUC | 84.22% |

## Model Improvement Experiments

Two approaches were explored to improve churn identification.

### 1. Classification Threshold Adjustment

The classification threshold was reduced from 0.50 to 0.25.

Results:

- Accuracy: 73.31%
- Precision: 49.84%
- Recall: 81.02%
- F1-Score: 61.71%

### 2. Class Weight Balancing

A second Logistic Regression model was trained using `class_weight="balanced"`.

Results:

- Accuracy: 73.88%
- Precision: 50.52%
- Recall: 78.34%
- F1-Score: 61.43%

The threshold 0.25 experiment achieved the highest Recall and F1-Score among the approaches tested.

**Evaluation note:** Threshold experiments were conducted on the test dataset for learning and comparison. Independent validation and evaluation on an untouched test dataset are required before selecting a final deployment model.

## Key Business Insight

A lower classification threshold helped identify more customers who were likely to churn.

However, it also increased false-positive predictions.

The appropriate threshold depends on the business trade-off between missing potential churn customers and contacting customers who would have stayed.

## Repository Contents

- `Logistic_Regression_Customer_Churn.ipynb` — Complete Google Colab project notebook.
- `README.md` — Project overview, methodology and results.

## Future Improvements

- Perform threshold optimisation using validation data.
- Compare Logistic Regression with Random Forest and other algorithms.
- Improve model interpretability.
- Develop a customer churn prediction interface.
- Explore API-based model deployment.

## Author

**Vivek Sawant**

This project was developed as a practical Machine Learning learning project to strengthen skills in Python, data analysis and predictive modelling.
