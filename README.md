# Manufacturing-Defects

### Summary and Recommendations

#### 1. Overview

This project uses machine learning to analyze manufacturing defects and predict the severity of defects based on various factors such as defect type, location, and inspection method. The dataset contains simulated data related to defects observed during the quality control process in a manufacturing environment. The project aims to improve the quality control process by analyzing defect patterns and predicting severity, helping to prioritize repairs and optimize production costs.

#### 2. Data

The dataset is entirely synthetic and includes the following columns:

- defect_id: Unique identifier for each defect.
- product_id: Identifier for the product associated with the defect.
- defect_type: Type of defect (e.g., cosmetic, functional, structural).
- defect_date: Date when the defect was detected.
- defect_location: Where the defect occurred in the product (e.g., surface, internal).
- severity: Severity level of the defect (e.g., minor, moderate, critical).
- inspection_method: How the defect was detected (e.g., manual inspection, automated testing).
- repair_cost: The cost of repairing the defect.

#### 3. Data Analysis Steps

- Data Preprocessing: Cleaning and encoding categorical variables, scaling numerical variables, and handling missing data.
Feature Engineering: Creating new features such as defect frequency over time and mapping severity levels to numerical values.

- Modeling: Training machine learning models such as Random Forest and Logistic Regression to predict the severity of manufacturing defects.

- Cross-Validation: Using K-Fold cross-validation to validate the performance of the models and address overfitting concerns.
SHAP Analysis: Using SHAP (SHapley Additive exPlanations) to explain the contribution of each feature to the model’s predictions.

#### 4. Key Findings
      
Overfitting: 

- Perfect accuracy during training may indicate that the model has memorized the training data, meaning it performs well on known data but fails to generalize to unseen data.

Addressing Overfitting:
- Use cross-validation to ensure the model is evaluated on different subsets of data.
- Apply regularization techniques (like L1 or L2 regularization) to simplify the model and reduce overfitting.
- Evaluate simpler models first, such as Logistic Regression, to check for overfitting.

Data Leakage: 

- If information from the target variable leaks into the feature set (directly or indirectly), the model may achieve artificially high accuracy.

Preventing Data Leakage: 

- Carefully review the data to ensure no features are directly derived from the target variable.

Too Simple of a Problem: 
- The dataset may be simple or well-structured, making it easier for the model to achieve perfect accuracy.
- Next Steps: If the problem is simple, consider adding more complexity to the dataset or introducing more difficult classification tasks.

#### 5. Future Work

- Improve Model Generalization: Explore other machine learning models such as Gradient Boosting and XGBoost, and tune hyperparameters using GridSearchCV.
- Feature Engineering: Create more features from the dataset, such as interaction terms or temporal patterns, to improve the model's predictive power.
- Data Augmentation: Introduce more data or simulate additional complex manufacturing defects to create a more challenging dataset.
- Hyperparameter Tuning: Further tune the hyperparameters of the models to avoid overfitting and improve performance on unseen data.

#### 6. Source

https://www.kaggle.com/datasets/fahmidachowdhury/manufacturing-defects
