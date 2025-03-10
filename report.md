# ML Intern Assignment - Report

## 1. Introduction
This report summarizes the approach taken to preprocess the dataset, apply dimensionality reduction, train machine learning models, evaluate performance, and propose potential improvements.

## 2. Data Preprocessing
- **Handling Missing Values:** Forward fill method was used.
- **Feature Scaling:** StandardScaler was applied to normalize features and target values.
- **Feature Selection:** Lasso Regression was used to select important features. Ridge Regression was an alternative approach if Lasso failed.

## 3. Dimensionality Reduction
- **PCA (Principal Component Analysis):** Applied with 5 components, retaining key variance in data.
- **Explained Variance Ratio:**
  - First Component: 86.2%
  - Second Component: 6.9%
  - Remaining Components: Less than 4% each

## 4. Model Training & Evaluation
Three models were trained and evaluated:

| Model          | MAE     | RMSE    | R^2    |
|---------------|---------|---------|--------|
| Random Forest | 1688.66 | 3185.65 | 0.9637 |
| XGBoost      | 1735.37 | 3692.31 | 0.9512 |
| Ensemble     | 1591.28 | 3142.31 | 0.9647 |

- **Best Model:** The ensemble approach performed the best in terms of RMSE and R^2 score.

## 5. Visualization
- **Regression:** A scatter plot was generated to visualize actual vs. predicted values.
- **Classification (If applicable):** A confusion matrix can be plotted for classification problems.

## 6. Limitations & Improvements
### **Limitations:**
- PCA might have caused some loss of important features.
- Further hyperparameter tuning could improve results.
- Data imbalance, if present, might affect predictions.

### **Potential Improvements:**
- Explore other feature selection techniques.
- Try ensemble techniques with different weight distributions.
- Increase dataset size to improve model generalization.

## 7. Conclusion
The ensemble model showed the best performance with an R^2 score of 0.9647. Further fine-tuning, feature engineering, and dataset expansion could enhance the results further.

