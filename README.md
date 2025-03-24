# Credit Risk Prediction

## Overview
Credit risk assessment is crucial in the banking sector to minimize loan defaults and optimize lending strategies. This project develops a machine learning model to predict loan default probability based on applicant data.

## Business Objective
- Identify key factors influencing loan defaults.
- Develop a predictive model for credit risk assessment.
- Provide actionable insights for financial institutions.

## Dataset
The dataset consists of **45,000 loan applicants** with **14 features**, categorized as follows:
- **Personal Information:** Age, gender, education, income, employment experience, home ownership.
- **Loan Details:** Loan amount, intent, interest rate, loan-to-income ratio.
- **Credit History:** Credit score, credit history length, previous loan defaults.
- **Target Variable:** `loan_status` (1 = Default, 0 = Non-Default).

## Data Preprocessing
- **Missing Values:** Handled appropriately to maintain data integrity.
- **Categorical Encoding:** Applied label encoding for categorical variables.
- **Feature Scaling:** Standardized numerical variables using `StandardScaler`.

## Exploratory Data Analysis (EDA)
Key insights from data exploration:
- **Income Distribution:** Right-skewed, with a minority having high incomes.
- **Credit Score vs Default:** Higher credit scores correlate with lower default rates.
- **Loan Amount vs Default:** Larger loans increase default likelihood.
- **Loan Purpose:** Personal and business loans have higher default rates.

## Machine Learning Model Development
### Models Used
1. **Random Forest Classifier**
   - Accuracy: 85%, AUC-ROC: 0.78
   - Moderate performance, required recall improvement.
2. **XGBoost Classifier** (Best Model)
   - Accuracy: 89%, AUC-ROC: 0.84
   - Lower false positives, better classification of defaulters.

### Feature Importance
Top predictors of loan default:
1. **Credit Score** – Most influential factor.
2. **Loan Amount** – Higher amounts correlate with higher risk.
3. **Income-to-Loan Ratio** – Lower ratios increase default probability.
4. **Credit History Length** – Longer histories reduce default likelihood.
5. **Previous Defaults** – Strong indicator of future default risk.

## Business Recommendations
- **Stronger Credit Score Thresholds:** Enforce minimum credit score requirements.
- **Income-Based Loan Caps:** Limit loan amounts relative to income.
- **Enhanced Risk Monitoring:** Extra scrutiny for applicants with short credit histories.
- **Risk-Based Interest Rates:** Adjust rates for high-risk applicants to mitigate losses.
