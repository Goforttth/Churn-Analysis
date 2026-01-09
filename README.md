# Customer Churn Analysis Project

## Project Overview

Customer churn refers to customers who stop using a company’s services. Reducing churn is critical for business growth because retaining existing customers is often cheaper than acquiring new ones.

This project builds a **machine learning model** to predict customer churn using historical customer data. The goal is to:
- Identify customers at high risk of churning
- Understand the factors that influence churn
- Provide actionable business recommendations



## Dataset Description

The dataset contains customer-level information, including:

- Demographic details (e.g. SeniorCitizen, Partner, Dependents)
- Account information (e.g. tenure, Contract type, Payment method)
- Service usage (e.g. PhoneService, Internet services, Streaming)
- Billing information (MonthlyCharges, TotalCharges)
- Target variable: **Churn** (1 = churned, 0 = stayed)



## Data Preprocessing

The following preprocessing steps were applied:

- Converted categorical variables using **one-hot encoding**
- Standardised numerical features such as:
  - tenure
  - MonthlyCharges
  - TotalCharges
- Removed non-informative identifiers
- Ensured the target variable (Churn) was binary



## Feature Engineering

Additional features were created to improve model performance:

- **num_services**: counts how many services a customer uses
- Scaled tenure to reflect customer loyalty
- Encoded contract length to capture commitment level

These features help the model better understand customer behaviour patterns.



## Model Building

### Logistic Regression

Logistic Regression was used as a baseline model because:
- It is simple and interpretable
- It works well for binary classification
- It provides probability scores for churn risk

The dataset was split into training and testing sets using stratification to preserve class balance.



## Model Evaluation

The model was evaluated using multiple metrics:

- **Confusion Matrix**
- **Precision, Recall, and F1-score**
- **ROC AUC Score**

### Performance Summary

- Accuracy: ~81%
- ROC AUC: ~0.84
- Strong performance in identifying non-churners
- Moderate performance in identifying churners



## Postdictive Analysis

Postdictive analysis compares predicted churn with actual churn outcomes.

### Where the Model Performed Well
- Correctly identified most customers who did not churn
- Effectively ranked customers by churn risk
- Strong overall discrimination between churners and non-churners

### Where the Model Failed
- Missed some customers who actually churned (false negatives)
- Churn class imbalance affected recall
- Logistic Regression may not capture complex customer behaviour patterns



## Why Use Multiple Models?

Both **Logistic Regression** and **Random Forest** were explored because:

- Logistic Regression provides interpretability
- Random Forest captures non-linear relationships
- Comparing models helps balance accuracy and explainability

Random Forest typically performs better but is harder to interpret, while Logistic Regression is easier to explain to stakeholders.



## Business Recommendations

Based on the analysis, the company should:

### Reduce Churn By:
- Offering incentives to customers with short tenure
- Encouraging longer-term contracts
- Improving support services for high-risk users
- Addressing high monthly charges with flexible plans

### Customer Prioritisation
Focus retention efforts on:
- Customers with high predicted churn probability
- Month-to-month contract customers
- Customers using few services
- Customers with rising monthly charges



## Conclusion

This project demonstrates how machine learning can be applied to predict customer churn and generate actionable business insights. While the model performs well overall, future improvements could include:
- Handling class imbalance
- Adding customer satisfaction data
- Using advanced models with explainability tools



## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook



## Author

Rachael  
Customer Churn Analysis Project
