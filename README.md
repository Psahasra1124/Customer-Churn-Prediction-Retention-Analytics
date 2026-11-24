# Customer Churn Prediction & Retention Analytics

An end-to-end data analytics project focused on understanding customer churn in the telecommunications industry using SQL, Python, Machine Learning, and Power BI.

The project analyses customer behaviour, identifies factors associated with customer churn, evaluates machine learning models, and presents business insights through an interactive three-page Power BI dashboard.

## Business Problem

Customer churn occurs when customers stop using a company's services. High churn can negatively impact revenue, customer relationships, and business growth.

The objective of this project is to analyse customer data, identify important churn patterns, understand the factors influencing customer decisions, and provide actionable recommendations to improve customer retention.

## Dataset

- **Dataset:** IBM Telco Customer Churn
- **Source:** [Kaggle – Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Total Records:** 7,043 customers
- **Original Features:** 21

## Tools & Technologies

- **SQL (MySQL):** Data querying, business analysis, joins, subqueries, and customer segmentation.
- **Python:** Data cleaning, exploratory data analysis, feature engineering, and machine learning.
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.
- **Power BI:** Interactive dashboards, KPI cards, data visualisations, and customer churn analysis.

## Key Findings

- Overall customer churn rate: **26.54%**
- Month-to-month contract customers have a higher churn rate (**42.71%**) compared with one-year (**11.27%**) and two-year (**2.83%**) contract customers.
- New customers with 0–12 months of tenure have a higher churn rate (**47.44%**) than long-term customers with 49–72 months of tenure (**9.51%**).
- Fiber optic internet service and electronic check payments are associated with higher churn.
- Churned customers have higher average monthly charges than retained customers.

## Machine Learning Results

Three classification models were evaluated using 5-fold cross-validation.

| Model | Cross-Validation Mean F1 Score |
|---|---:|
| Logistic Regression (Tuned, C=100) | **0.595** |
| Random Forest | 0.528 |
| Decision Tree | 0.516 |

**Selected Model: Logistic Regression (C=100)**

| Evaluation Metric | Score |
|---|---:|
| Accuracy | 79.63% |
| Precision | 64.08% |
| Recall | 52.94% |
| F1 Score | 57.98% |
| ROC-AUC | 0.84 |

**Model Limitation:** The recall of approximately 53% indicates that the model misses a considerable proportion of actual churners at the default 50% classification threshold. In a real-world application, the classification threshold should be evaluated according to business priorities.

## Business Recommendations

1. Prioritise retention campaigns for customers in their first 12 months.
2. Investigate service quality and reliability concerns associated with fiber optic customers.
3. Review the electronic check payment experience.
4. Encourage month-to-month customers to consider longer-term contracts through suitable retention offers.
5. Monitor customer satisfaction and monthly charges to identify potential churn risks.

## Power BI Dashboard

The Power BI report contains three interactive pages designed to explore customer churn, its contributing factors, and customer charge patterns.

### 1. Churn Overview

- Total Customers
- Churned Customers
- Retained Customers
- Overall Churn Rate
- Customer distribution analysis
- Contract and tenure analysis

### 2. Churn Drivers

- Churn analysis by Payment Method
- Churn analysis by Internet Service
- Churn analysis by Technical Support
- Churn analysis by Online Security
- Churn analysis by Paperless Billing
- Churn analysis by Partner Status

### 3. Customer & Revenue Analysis

- Total Customer Charges
- Total Monthly Charges
- Average Monthly Charges
- Total Customer Charges by Contract Type
- Average Monthly Charges by Internet Service
- Customer Charges by Contract Type and Churn Status
- Churn Rate by Contract Type
- Customer Churn by Tenure Group
- Average Customer Charges by Churn Status
- Interactive Contract Slicer

**Note:** Total Customer Charges represents cumulative charges recorded for customers, not revenue recognised during a specific reporting period.

## Project Structure

```text
customer-churn-prediction/
│
├── dashboard/
│   └── Customer Churn Prediction & Retention Analytics.pbix
│
├── data/
│   └── Dataset files
│
├── images/
│   └── Dashboard screenshots
│
├── notebooks/
│   └── Jupyter notebooks
│
├── sql/
│   └── SQL analysis queries
│
├── README.md
├── LICENSE
└── requirements.txt
```

## How to Run the Project

1. Download or clone the project repository.
2. Install Python and the required dependencies.
3. Create a virtual environment.
4. Install the required libraries:

   ```bash
   pip install -r requirements.txt
   ```

5. Open the Jupyter notebooks in the `notebooks` folder to explore the data cleaning, analysis, and machine learning workflow.
6. Execute the SQL queries in the `sql` folder using MySQL.
7. Open the Power BI file in Power BI Desktop:

   `dashboard/Customer Churn Prediction & Retention Analytics.pbix`

8. Explore the three dashboard pages and interact with the available filters and visualisations.

## Project Highlights

- End-to-end customer churn analysis.
- SQL-based business analysis.
- Exploratory data analysis using Python.
- Machine learning model evaluation.
- Interactive three-page Power BI dashboard.
- Customer segmentation based on tenure.
- Business recommendations based on analytical findings.

## Dataset Acknowledgement

The IBM Telco Customer Churn dataset is sourced from Kaggle and is used for educational and analytical purposes.