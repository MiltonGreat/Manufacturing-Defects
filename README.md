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

#### 3. Project Workflow

- Data Loading and Cleaning
- Exploratory Data Analysis (EDA)
- Data Splitting and Resampling
- Model Training and Hyperparameter Tuning
- Evaluation: Use SHAP to interpret feature importance.
- Predictions and Insights

#### 4. Key Findings
      
- Cross-Validation Metrics: Accuracy (~30%) and Weighted F1 Score (~30%)
- Best Model: XGBoost with tuned hyperparameters.

#### 5. Future Work

- Improve Model Generalization: Explore other machine learning models such as Gradient Boosting and XGBoost, and tune hyperparameters using GridSearchCV.
- Feature Engineering: Create more features from the dataset, such as interaction terms or temporal patterns, to improve the model's predictive power.
- Data Augmentation: Introduce more data or simulate additional complex manufacturing defects to create a more challenging dataset.
- Hyperparameter Tuning: Further tune the hyperparameters of the models to avoid overfitting and improve performance on unseen data.

#### 6. Source

https://www.kaggle.com/datasets/fahmidachowdhury/manufacturing-defects
