# Customer Retention Modelling

A customer analytics project that predicts customer retention using RFM (Recency, Frequency, Monetary) analysis and logistic regression.

The project develops a customer response model from historical transaction data to identify customers most likely to make repeat purchases. Multiple evaluation techniques—including ROC analysis, decile analysis, lift charts, and gain charts—are used to assess model performance and customer targeting effectiveness.

---

## Project Overview

Customer retention is one of the most important drivers of long-term business profitability. Identifying customers who are likely to return allows companies to improve marketing efficiency, personalize promotions, and reduce customer churn.

This project analyzes transaction data from an online bookstore to predict whether customers will make repeat purchases during a future time period using historical purchasing behaviour.

The analysis combines RFM customer segmentation with logistic regression to develop an interpretable customer retention model.

---

## Business Problem

Marketing teams often face limited budgets and cannot target every customer equally.

The objective of this project is to answer several business questions:

- Which customers are most likely to return?
- Which customer characteristics best predict retention?
- How accurately can customer retention be predicted?
- Which customer segments should receive marketing campaigns?

The resulting model supports data-driven customer relationship management (CRM) and targeted marketing strategies.

---

## Dataset

Dataset included in this repository:

```
book_transaction.csv
```

The dataset contains transaction records for **23,570 customers** who made their first purchase during the first quarter of 2017, with **69,659 transaction records** in total. Each record includes:

- Customer ID
- Transaction Date
- Number of Books Purchased
- Transaction Value

The data was divided into a **calibration period** (transactions on or before September 30, 2017) and a **validation period** (transactions after September 30, 2017) to evaluate customer retention. :contentReference[oaicite:1]{index=1}

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Statsmodels
- Matplotlib
- Logistic Regression
- RFM Analysis

---

## Project Workflow

1. Data preprocessing
2. Customer-level data restructuring
3. RFM feature engineering
4. Customer retention labelling
5. Logistic regression model development
6. ROC and AUC evaluation
7. Decile analysis
8. Lift chart analysis
9. Gain chart analysis
10. Business interpretation

---

## Feature Engineering

Customer purchasing behaviour was summarized using the RFM framework.

### Recency

Number of days since the customer's most recent purchase.

### Frequency

Number of purchases made during the calibration period.

### Monetary

Average transaction value during the calibration period.

Customers were labelled as **retained** if they made at least one purchase during the validation period. :contentReference[oaicite:2]{index=2}

---

## Predictive Model

A logistic regression model was developed to estimate the probability of customer retention using the three RFM variables.

Model evaluation included:

- ROC Curve
- AUC
- Confusion Matrix

The final model achieved an **AUC of approximately 0.77**, indicating good discrimination between retained and non-retained customers. All three RFM variables were statistically significant predictors of retention. :contentReference[oaicite:3]{index=3}

---

## Customer Segmentation Analysis

Customers were ranked into deciles according to:

- Recency
- Frequency
- Monetary Value

Retention rates were then compared across customer groups.

The analysis showed:

- Customers with more recent purchases had substantially higher retention.
- Higher purchase frequency strongly increased retention.
- Customers with larger average transaction values were more likely to return.

Among the three variables, **frequency demonstrated the strongest relationship with customer retention**. :contentReference[oaicite:4]{index=4}

---

## Model Evaluation

To evaluate customer targeting effectiveness, the project includes:

### ROC Curve

Measures overall classification performance.

### Decile Analysis

Evaluates retention rates across customer segments.

### Lift Chart

Measures the model's ability to rank customers according to retention probability.

### Gain Chart

Evaluates cumulative customer response performance.

The logistic regression model consistently outperformed individual RFM variables in ranking customers, while **frequency showed the strongest predictive power among the three RFM metrics**. :contentReference[oaicite:5]{index=5}

---

## Key Findings

Major findings include:

- Recent purchasing behaviour strongly predicts future retention.
- Purchase frequency is the strongest indicator of repeat purchasing.
- Customers with higher spending levels are generally more likely to be retained.
- Logistic regression provides better customer ranking performance than using individual RFM metrics alone.
- Lift and gain analyses demonstrate the model's effectiveness for customer targeting.

---

## Business Recommendations

Based on the analysis:

- Prioritize marketing campaigns for high-frequency customers.
- Re-engage inactive customers before recency increases further.
- Allocate promotional budgets using predicted retention probabilities rather than treating all customers equally.
- Use the retention model to support personalized CRM campaigns and customer lifecycle management.

---

## Repository Structure

```
customer-retention-modeling/

│
├── Code.ipynb
├── Customer Retention Modelling Report.pdf
├── book_transaction.csv
└── README.md
```

---

## Repository Contents

| File | Description |
|------|-------------|
| Code.ipynb | Data preprocessing, RFM feature engineering, logistic regression modelling, and evaluation |
| Book Transaction Report.pdf | Project report including methodology, visualizations, and findings |
| book_transaction.csv | Transaction dataset used for customer retention modelling |
| README.md | Project documentation |

---

## Future Improvements

Potential future enhancements include:

- Comparing additional machine learning models such as Random Forest, XGBoost, and Gradient Boosting.
- Incorporating customer demographics and product categories.
- Developing customer lifetime value (CLV) prediction models.
- Automating customer scoring for real-time CRM applications.
- Deploying the model as an API for marketing campaign management.

---

## Skills Demonstrated

- Customer Analytics
- Customer Retention Modelling
- CRM Analytics
- RFM Analysis
- Logistic Regression
- Feature Engineering
- ROC Analysis
- AUC Evaluation
- Lift Chart
- Gain Chart
- Customer Segmentation
- Predictive Modelling
- Python
- Data Visualization
