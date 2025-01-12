# Manufacturing Defect Analysis and Severity Prediction

## Overview

This project explores patterns in manufacturing defects and predicts defect severity to enhance quality control processes. By analyzing historical defect records and leveraging machine learning models, this project provides actionable insights to optimize manufacturing operations, reduce costs, and improve product quality.

This project explores patterns in defect data and uses machine learning to predict the severity of defects. Key objectives include:

1. Identifying trends and patterns in manufacturing defects.
2. Visualizing relationships between factors such as defect type, location, and severity.
3. Building and evaluating predictive models to classify defect severity.

### Problem Statement

Manufacturing defects lead to significant production losses, customer dissatisfaction, and increased costs. Predicting defect severity enables manufacturers to prioritize repairs and optimize production lines.

Using machine learning techniques, this project enhances defect analysis by identifying critical factors contributing to defects and predicting severity, aiding in informed decision-making and efficient resource allocation.

### Data

The dataset contains detailed records of manufacturing defects with the following features:

- defect_id: Unique identifier for each defect.
- product_id: Identifier for the product associated with the defect.
- defect_type: Type of defect (e.g., cosmetic, functional, structural).
- defect_date: Date when the defect was detected.
- defect_location: Where the defect occurred in the product (e.g., surface, internal).
- severity: Severity level of the defect (e.g., minor, moderate, critical).
- inspection_method: How the defect was detected (e.g., manual inspection, automated testing).
- repair_cost: The cost of repairing the defect.

Dataset Size: 1,000 records with no missing values after cleaning.

### Solution Approach

1. Data Preprocessing
- Missing Values: Imputed numerical features using median and categorical features using mode.
- Outlier Handling: Applied the IQR method to remove extreme outliers in repair_cost.
- Feature Engineering:
   - Extracted temporal features (defect_year, defect_month, defect_day) from defect_date.
   - Applied label encoding to categorical columns.

2. Exploratory Data Analysis (EDA)
- Visualized Key Insights:
   - Distribution of defect types and severity levels.
   - Repair costs by defect type and location.
   - Monthly defect occurrences to identify seasonal trends.

- Correlation Analysis: Explored relationships between features to understand their influence on severity.

3. Model Training
- Class Imbalance Handling:
- Used SMOTE (Synthetic Minority Over-sampling Technique) to balance severity levels.
     - Before SMOTE: Severity class distribution was imbalanced (0: 267, 1: 286, 2: 247).
     - After SMOTE: Severity levels were balanced (0: 286, 1: 286, 2: 286).

- Model Development: Trained an XGBoost classifier with hyperparameter tuning via GridSearchCV.

4. Model Evaluation
- Evaluated using metrics:
     - Precision: Measures the accuracy of positive predictions.
     - Recall: Measures the model's ability to identify all positive cases.
     - F1-Score: Harmonic mean of precision and recall for balanced evaluation.

### Results:

Model Performance: Precision, Recall, and F1-Scores were moderate (~0.30), indicating the need for further feature enrichment or advanced modeling.

Feature Importance: Key predictors of defect severity included defect_type, repair_cost, and defect_location.

Insights from EDA:
- High-cost defects were linked to specific defect types and locations.
- Critical defects were more frequently detected via automated testing methods.

### Challenges

1. Imbalanced Data: Severity levels were imbalanced, requiring oversampling with SMOTE.

2. Feature Limitations: The dataset lacked additional context (e.g., environmental factors, operator expertise), which may improve predictions.

3. Model Performance: The XGBoost model achieved only 30% accuracy on the test set, indicating the need for more feature-rich data and advanced algorithms.

### Future Directions

1. Feature Engineering:
- Incorporate additional data, such as material properties, production line settings, and environmental conditions.
- Add historical defect patterns for specific products or lines.

2. Advanced Models:
- Explore ensemble methods (e.g., Random Forest, Gradient Boosting) or deep learning models for improved accuracy.

3. Real-Time Monitoring:
- Integrate real-time data from IoT sensors to detect defects during production.

4. Dashboard Development:
- Build interactive dashboards for visualizing defect trends and severity predictions.

#### Source

https://www.kaggle.com/datasets/fahmidachowdhury/manufacturing-defects
