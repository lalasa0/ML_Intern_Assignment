# ML Intern Assignment

## Overview
This repository contains the code for a machine learning task involving data preprocessing, dimensionality reduction, model training, and evaluation using Random Forest, XGBoost, and an ensemble approach.

## Installation
Ensure you have Python installed, then install the necessary dependencies using:
```bash
pip install -r requirements.txt
```

## Running the Code
To train and evaluate the models, run the Jupyter Notebook (`ML_Intern_Assignment.ipynb`) or the Python script:
```bash
python ml_model_training.py
```

## Repository Structure

| File/Folder                | Description                                       |
|----------------------------|---------------------------------------------------|
| `ML_Intern_Assignment.ipynb` | Jupyter Notebook containing all tasks.           |
| `README.md`                | Instructions for installation and usage.         |
| `requirements.txt`         | List of required dependencies.                   |
| `report.pdf` (or `report.md`) | Summary of the approach, findings, and improvements. |

## Report Summary

### Preprocessing Steps

- Removed unnecessary columns and handled missing values.
- Standardized features and target variable using `StandardScaler`.
- Selected important features using **Lasso/Ridge Regression**.
- Applied **PCA** to reduce dimensionality (top 5 components).

### Model Training & Evaluation

- Trained **Random Forest** and **XGBoost** with hyperparameter tuning via GridSearchCV.
- Combined predictions using an **Ensemble (weighted average)** approach.
- Evaluated models using **MAE, RMSE, and R² score**.

#### Performance Metrics (Regression Models)

| Model           | MAE      | RMSE     | R² Score |
|---------------|---------|---------|----------|
| Random Forest | 1688.66 | 3185.65 | 0.9637   |
| XGBoost      | 1735.37 | 3692.30 | 0.9512   |
| Ensemble      | 1591.27 | 3142.31 | 0.9647   |

### Visualizations

- **Scatter Plot**: Actual vs. Predicted values for regression.
- **Confusion Matrix** (if classification task).

### Limitations & Improvements

- Further hyperparameter tuning can enhance performance.
- Larger dataset and feature engineering could improve generalization.

