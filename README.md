Telecom Customer Churn Analysis

# Overview
This project analyzes customer churn patterns for a telecom company by combining Power BI dashboards and Python for data preparation and statistical analysis. The objective is to uncover key drivers of churn, understand customer behavior patterns, and provide actionable recommendations for improving customer retention.

# Business Problem
Through analysis, the dataset revealed a churn rate of approximately 27% — a significant figure impacting revenue and customer lifetime value.

The project aimed to answer:

- What proportion of customers are churning?

- Which customer segments show higher churn risk?

- How does churn affect overall revenue?

- What are the primary factors influencing customer churn?

# Tools Used
- Power BI — for visual storytelling and interactive dashboards

- Python (Pandas, Matplotlib, NumPy, SciPy) — for data cleaning and statistical analysis

- Jupyter Notebook — for documenting the analysis process

- CSV Dataset — telecom customer records (IBM)

# Data Preparation
Before visualization, the dataset was cleaned and pre-processed in Python:

- Checked for missing values and duplicates

- Converted SeniorCitizen from binary numeric (0/1) to descriptive labels (No / Yes).

- Standardized No internet service entries as No internet for clarity.

- Harmonized contract terminology by renaming Month-to-month to Monthly.

- Imputed missing TotalCharges as 0 for customers with zero tenure (new customers).

- Created six tenure groups for cohort analysis: 0-12, 13-24, 25-36, 37-48, 49-60, and 61-72 months.


# Power BI Insights

Churn Rate (Insight): Approximately 27% of customers (1,869 of 7,043) were identified as having churned.

Churn by Contract Type:

Monthly contracts: 1,655 churned customers

One year contracts: 166 churned customers

Two year contracts: 48 churned customers

Churn by Payment Method:

Electronic check leads with 1,071 churned customers

Mailed check: 308 churned

Bank transfer (automatic): 258 churned

Credit card (automatic): 232 churned

Churn Rate by Internet Service:

Fiber optic: 42% churn rate

DSL: 19% churn rate

No internet: 7% churn rate

Revenue Impact:

Churned customers contributed approximately $2.86M (18%) of total revenue

Retained customers contributed approximately $13.19M (82%) of total revenue

Tenure Distribution:

Highest churn is concentrated in the first 12 months, with 1,149 churned customers out of 2,298 in this tenure group (50%).


Highest churn is concentrated in the first 12 months, with 1,149 churned customers out of 2,298 in this tenure group (50%).

# Python Analysis

Python was used to complement Power BI by providing in-depth data processing and correlations:

Data Cleaning: Filling missing values, standardizing categories, and tenure grouping.

Correlation Analysis:

Pearson correlation for numeric variables against churn

Cramér’s V for categorical variables against churn

Major Churn Drivers Identified:

Contract Type

Tenure Length

Payment Method

Internet Service Type

The full Jupyter notebook is available for detailed methodology: telecom_churn_analysis.ipynb

# Key Insights
Customers on monthly contracts have a much higher likelihood to churn.

Electronic check payment method correlates strongly with churn.

Fiber optic subscribers churn notably more than DSL or no internet users.

Customer churn is most prevalent within the first 12 months of service.

Churn equates to significant revenue loss, constituting 18% of total revenue.

# Recommendations

1. Incentivize customers to switch from monthly to yearly contracts through discounts or loyalty rewards.

2. Focus on onboarding and retention initiatives during the critical initial 12 months.

3. Address service quality or support issues related to fiber optic customers.

4. Encourage more secure automated payment methods like bank transfers and credit cards.
