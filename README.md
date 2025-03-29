# Insurance-Claim-Severity-Prediction-Model

## Overview
This project aims to predict insurance claim severity using machine learning models. The dataset consists of various features, including policyholder demographics, vehicle details, and claim history. By leveraging statistical analysis and machine learning techniques, we aim to improve risk assessment and enhance underwriting decisions.

## Dataset
The dataset contains 5000 entries with 12 columns, categorized into:
- **Numerical Variables**: `age`, `car_age`, `engine_power`, `num_past_claims`, `total_past_claim_amount`, `deductible_amount`, `claim_amount` (target variable)
- **Categorical Variables**: `gender`, `location`, `car_type`, `coverage_type`, `accident_severity`

## Methodology

### 1. Data Exploration & Preprocessing
- **Data Quality Check**: No missing or duplicate values were found.
- **Outlier Detection**: Used box plots and z-score analysis to identify potential outliers.
- **Feature Scaling**: Applied StandardScaler to normalize numerical features.
- **Categorical Encoding**: One-hot encoding was used for categorical variables.

### 2. Exploratory Data Analysis (EDA)
- **Visualizations**:
  - Histograms, scatter plots, and box plots to understand data distribution.
  - KDE plots to analyze skewness in numerical variables.
  - Correlation heatmap to identify relationships between features and claim amount.
- **Key Insights**:
  - Right-skewed distribution in `claim_amount` required log transformation.
  - Weak linear correlations suggest the need for non-linear models.
  - `accident_severity`, `num_past_claims`, `car_age`, and `engine_power` show the strongest positive correlation with `claim_amount`.

### 3. Model Building
- **Feature Engineering**: Removed multicollinearity using VIF analysis.
- **Machine Learning Models**:
  - Tested multiple models including Linear Regression, Random Forest, and Gradient Boosting.
  - Used cross-validation to evaluate model performance.
- **Evaluation Metrics**: RMSE, MAE, and R-squared were used to assess model accuracy.

## Results & Recommendations
- The best-performing model effectively predicts claim severity with reasonable accuracy.
- Further improvements can be achieved using ensemble models and additional feature engineering.

## License
This project is licensed under the MIT License.
