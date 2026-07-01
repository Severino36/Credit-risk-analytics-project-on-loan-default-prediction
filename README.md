# Credit-risk-analytics-project-on-loan-default-prediction


## Project Overview

This project develops machine learning models to predict loan default risk using borrower demographic, financial, and loan-related information. The objective is to help financial institutions identify high-risk borrowers and support more informed lending decisions.

The project follows a complete data science workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, model development, hyperparameter tuning, and model evaluation.

---

## Business Problem

Loan defaults can lead to significant financial losses for lenders. Accurately identifying borrowers who are likely to default allows financial institutions to:

- Reduce credit risk
- Improve loan approval decisions
- Minimise financial losses
- Enhance portfolio management

This project aims to build predictive models that classify borrowers as either likely to default or not default.

---

## Dataset

The dataset contains borrower demographic, financial, and loan-related information.

### Features

| Feature | Description |
|----------|-------------|
| Age | Borrower's age |
| Income | Annual income |
| LoanAmount | Amount borrowed |
| CreditScore | Borrower's credit score |
| MonthsEmployed | Employment duration |
| NumCreditLines | Number of active credit lines |
| InterestRate | Loan interest rate |
| LoanTerm | Loan duration |
| DTIRatio | Debt-to-income ratio |
| Education | Education level |
| EmploymentType | Employment status |
| MaritalStatus | Marital status |
| HasMortgage | Mortgage ownership |
| HasDependents | Dependents indicator |
| LoanPurpose | Purpose of the loan |
| HasCoSigner | Presence of a co-signer |
| Default | Target variable |

---

## Project Workflow

### 1. Data Cleaning

- Checked for missing values
- Imputed missing numerical values using median imputation
- Examined categorical variables
- Removed duplicates
- Treated outliers where necessary
- Verified data quality and consistency

### 2. Exploratory Data Analysis (EDA)

Performed:

- Univariate analysis
- Bivariate analysis
- Correlation analysis
- Default rate analysis across borrower groups

Visualisations included:

- Histograms
- Boxplots
- Countplots
- Heatmaps
- Default distribution plots

### 3. Feature Engineering

- Label encoding
- One-hot encoding
- Train-test split
- Feature preparation for machine learning models

### 4. Machine Learning Models

The following models were developed and evaluated:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. XGBoost Classifier

Hyperparameter tuning was performed to improve model performance.

---

## Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- Cross-Validation

Since the dataset is imbalanced, particular emphasis was placed on Recall and F1-Score for the default class.

---

## Model Results

### Decision Tree

| Metric | Value |
|----------|---------|
| Training Accuracy | 100.0% |
| Test Accuracy | 80.1% |
| Default Precision | 20% |
| Default Recall | 24% |
| Default F1-Score | 22% |

The Decision Tree achieved perfect training accuracy but significantly lower test accuracy, indicating overfitting. While it identified some default cases, overall performance on the minority class remained weak.

---

### Random Forest

| Metric | Value |
|----------|---------|
| Training Accuracy | 89.6% |
| Test Accuracy | 84.7% |
| Default Precision | 26% |
| Default Recall | 18% |
| Default F1-Score | 21% |

The Random Forest improved generalisation compared to the Decision Tree and achieved higher overall accuracy. However, its ability to identify default cases remained limited.

---

### XGBoost

| Metric | Value |
|----------|---------|
| Training Accuracy | 93.1% |
| Test Accuracy | 88.5% |
| Default Precision | 54% |
| Default Recall | 6% |
| Default F1-Score | 12% |

XGBoost achieved the highest overall accuracy and precision for default predictions. However, it detected very few actual defaulters, limiting its usefulness for credit risk prediction.

---

## Key Findings

- Credit Score was one of the strongest predictors of loan default.
- Debt-to-Income Ratio (DTI) showed a strong relationship with default risk.
- Income and employment duration influenced borrower repayment behaviour.
- Class imbalance significantly affected model performance.
- Models achieved high overall accuracy but struggled to identify default cases effectively.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- Jupyter Notebook

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/credit-risk-analytics.git
cd credit-risk-analytics
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

---

## Future Improvements

Potential improvements include:

- SMOTE and advanced oversampling techniques
- Cost-sensitive learning
- Threshold optimisation
- Ensemble stacking
- Additional borrower behavioural features
- Deep learning approaches

---

## Business Recommendations

- Prioritise Credit Score and DTI Ratio during loan assessments.
- Use predictive models as decision-support tools rather than standalone approval systems.
- Implement class imbalance handling techniques to improve default detection.
- Continuously retrain models using updated borrower data.
- Consider risk-based pricing strategies for high-risk borrowers.

---

## Author

**Your Name**

Credit Risk Analytics – Loan Default Prediction

Machine Learning | Credit Risk Modelling | Financial Analytics
