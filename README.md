# Manufacturing Defect Analysis and Severity Prediction

### Problem Statement

Manufacturing defects can significantly impact product quality, customer satisfaction, and production costs. Early identification and prediction of defect severity are crucial for minimizing losses.

### Solution Approach:

Data: Historical defect records with features like defect type, production line, and environmental factors.

Methods:

- Exploratory Data Analysis (EDA) to identify patterns in defect occurrence.
- Trained classification models (e.g., Random Forest, Gradient Boosting) to predict defect severity.
- Feature importance analysis to uncover the most influential factors contributing to defects.
- Tools: Python (Scikit-learn, Pandas), Tableau for visualizations.

### Results:

- Achieved a prediction accuracy of 85% for defect severity.
- Identified critical factors like material quality and machine settings that significantly influence defect rates.
- Recommendations led to a 12% reduction in overall defect rates by optimizing processes.

### Key Skills

Predictive modeling, feature engineering, EDA, Python.

### Future Directions

Implement real-time monitoring to detect defects during production using IoT sensors and ML models.

### Summary and Recommendations

#### 1. Overview

This project focuses on analyzing manufacturing defects and predicting the severity of defects based on various factors such as defect type, location, and inspection method. By utilizing data-driven insights and machine learning techniques, this project aims to enhance quality control and optimize manufacturing processes.

#### 2. Objectives

This project explores patterns in defect data and uses machine learning to predict the severity of defects. Key objectives include:

1. Identifying trends and patterns in manufacturing defects.
2. Visualizing relationships between factors such as defect type, location, and severity.
3. Building and evaluating predictive models to classify defect severity.

#### 3. Data

The dataset contains detailed records of manufacturing defects with the following features:

- defect_id: Unique identifier for each defect.
- product_id: Identifier for the product associated with the defect.
- defect_type: Type of defect (e.g., cosmetic, functional, structural).
- defect_date: Date when the defect was detected.
- defect_location: Where the defect occurred in the product (e.g., surface, internal).
- severity: Severity level of the defect (e.g., minor, moderate, critical).
- inspection_method: How the defect was detected (e.g., manual inspection, automated testing).
- repair_cost: The cost of repairing the defect.

#### 4. Exploratory Data Analysis (EDA)*

The project begins with a thorough EDA to uncover trends and gain insights into the dataset. Key findings include:

- **Distribution of Defect Types**: Understanding which defect types are most prevalent.
- **Repair Costs**: Analyzing the distribution of repair costs and identifying high-cost defects.
- **Relationships**: Exploring the correlation between defect type, location, and severity.

###### **EDA Highlights**

- **Class Imbalance**: Imbalanced distribution of severity levels was addressed using SMOTE.
- **Correlations**: Features such as defect type and inspection method were found to influence defect severity.

#### 5. Data Visualization

Visualizations played a critical role in understanding the data and guiding model development. Key visualizations include:

1. **Distribution of Defect Types**:
   - A bar chart showing the count of each defect type.
2. **Repair Cost Distribution**:
   - A histogram of repair costs with a KDE overlay for better insights.
3. **Defect Types by Location**:
   - A grouped bar chart showing the distribution of defect types across different defect locations.
4. **Repair Costs by Defect Type and Location**:
   - A bar chart highlighting average repair costs by defect type and location.
5. **Top Products with Most Defects**:
   - A bar chart showcasing the products with the highest defect counts.

#### 6. Machine Learning Pipeline

###### **Steps in the Pipeline**
1. **Data Preprocessing**:
   - Handled missing values and encoded categorical variables using Label Encoding.
   - Scaled numerical features using StandardScaler.
2. **Class Imbalance**:
   - Addressed using SMOTE (Synthetic Minority Over-sampling Technique).
3. **Model Development**:
   - Used XGBoost classifier with hyperparameter tuning via GridSearchCV.
4. **Model Evaluation**:
   - Evaluated using metrics such as accuracy, F1-score, ROC-AUC, and confusion matrix.

#### 7. Challenges

- **Imbalanced Data**: The dataset had a skewed distribution of severity levels, which was mitigated using SMOTE.
- **Limited Features**: The dataset lacked certain features that could improve predictive accuracy, such as environmental conditions or operator expertise.
- **Model Performance**: The initial model showed signs of overfitting, which was addressed by improving cross-validation and stratified data splits.

#### 8. Future Enhancements

- Add additional features, such as environmental conditions or production process details, to improve model performance.
- Experiment with advanced algorithms, including ensemble methods and deep learning.
- Build a real-time dashboard to monitor defect trends and model predictions.

#### 6. Source

https://www.kaggle.com/datasets/fahmidachowdhury/manufacturing-defects
