# H1N1 Vaccine Prediction using Machine Learning

## Overview
This project predicts whether an individual will receive the H1N1 vaccine using demographic, behavioral, and health-related survey data. The workflow includes data preprocessing, exploratory data analysis (EDA), model training, hyperparameter tuning, and Explainable AI (XAI).

## Dataset
- Training and testing datasets provided by the hackathon organizers.
- Target variable: `h1n1_vaccine` (0 = No, 1 = Yes).

## Methodology
1. Data loading and exploration
2. Missing value imputation
   - Numerical features: Median
   - Categorical features: Mode
3. One-Hot Encoding of categorical variables
4. Feature alignment between train and test datasets
5. Train-validation split (80:20)
6. Model training and evaluation using F1-score
7. Hyperparameter tuning using RandomizedSearchCV
8. Explainable AI using SHAP

## Models Evaluated
- Logistic Regression
- Random Forest
- Gradient Boosting
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

## Results

| Model | Best F1-Score | Rank |
|---------|---------|---------|
| Logistic Regression | 0.6905 | 1 |
| Support Vector Machine | 0.6801 | 2 |
| Gradient Boosting | 0.6799 | 3 |
| Random Forest | 0.6719 | 4 |
| K-Nearest Neighbors | 0.5907 | 5 |

**Best Model:** Logistic Regression

## Explainable AI (XAI)
SHAP (SHapley Additive exPlanations) was used to interpret the Logistic Regression model.

Key findings:
- Doctor recommendation was the strongest predictor of vaccination.
- Perceived H1N1 risk significantly influenced vaccination decisions.
- Belief in vaccine effectiveness was another major factor.
- Education level, healthcare worker status, and age also contributed to predictions.

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- SHAP
- Google Colab

## Author
Developed as part of the Data Science Challenge Hackathon.
