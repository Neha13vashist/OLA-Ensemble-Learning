# Ola Driver Churn Analysis

## Business Problem

Ola, a ride-sharing platform, is facing challenges with driver churn, impacting operational efficiency and incurring high recruitment costs. Retaining drivers is crucial for sustained growth and cost-effectiveness. The Analytics Department at Ola aims to predict driver churn based on various attributes, including demographics, tenure, and performance data, to proactively implement retention strategies.

## Approach

### Exploratory Data Analysis (EDA)

1. **Loading and Inspecting the Dataset:**
   - Checked the dataset's structure and characteristics.
2. **Data Processing and Feature Engineering:**
   - Converted date-like features to their respective data types.
   - Checked for missing values and prepared data for KNN Imputation using numerical features.
   - Aggregated data to remove multiple occurrences of the same driver data.

### Feature Engineering Steps

1. **Create Columns:**
   - Created a column indicating whether the quarterly rating has increased for each driver.
   - Created a target variable column indicating whether the driver has left the company.
   - Created a column indicating whether the monthly income has increased for each driver.

2. **Statistical Summary:**
   - Checked the statistical summary of the derived dataset.

3. **Correlation Analysis:**
   - Checked correlation among independent variables.

4. **One-Hot Encoding:**
   - Applied one-hot encoding to categorical variables.

5. **Class Imbalance Treatment:**
   - Explored the impact of class imbalance on model performance.
   - Treated class imbalance using various techniques.

6. **Standardization:**
   - Standardized the training data.

### Machine Learning Model

1. **Ensemble Learning:**
   - Utilized Bagging (Random Forest Classifier) and Boosting (Gradient Boosting) methods.
   - Explored Random Forest and XGBoosting classifiers.

2. **Results Evaluation:**
   - Evaluated models using Classification Report and ROC AUC curve.

## Observations from Results

### Exploratory Data Analysis

- July received the maximum number of drivers in 8 years.
- Joining of drivers increased by about 500% after 2017.
- City C20 was used by the most drivers.
- Grade 2 was received by most drivers.
- Quarterly Rating 1 was predominant among drivers.

### Machine Learning Model

- Precision and recall showed trade-offs, influencing the choice of the model.
- Class imbalance treatment impacted precision, recall, and F1-score differently.
- Gradient Boosting showed improved recall, while Random Forest showed improved precision after class imbalance treatment.

## Recommendations

1. **Retention Strategies:**
   - Prioritize retention strategies based on precision or recall, considering cost implications and effectiveness.

2. **Employee Engagement:**
   - Focus on improving quarterly ratings and income stability to enhance driver satisfaction.

3. **Continuous Monitoring:**
   - Implement a continuous monitoring system to track driver attributes influencing churn.

## Conclusion

The analysis provides insights into factors contributing to driver churn and predicts potential churn based on various attributes. Implementation of retention strategies and continuous monitoring can help Ola reduce driver churn, enhance driver satisfaction, and optimize recruitment costs. Continuous evaluation and adaptation of strategies will be crucial for sustained success.
