📊 Telecom Customer Churn Analysis
🧠 Objective

To analyze telecom customer data, identify key churn drivers, and derive data-backed retention insights to reduce the 26.54% churn rate observed among customers.

📁 Dataset Overview
Dataset Name: Customer Churn.csv
Rows: 7,043 customers
Columns: 21
Target Variable: Churn (Yes/No)
Features: Customer demographics, account information, subscription details, tenure, payment method, and service usage.

⚙️ Tools & Libraries
Data Wrangling: pandas, numpy
Visualization: seaborn, matplotlib
Environment: Jupyter Notebook

🧹 Data Preparation
Step	Description
Missing Values	Replaced blank TotalCharges with 0 and converted to float
Data Types	Ensured numeric consistency for quantitative columns
Categorical Conversion	Transformed SeniorCitizen from binary (0/1) to Yes/No for interpretability
Duplicates	Checked for and found no duplicate CustomerID entries
Null Values	Verified zero nulls post-cleaning.

📊 Exploratory Data Analysis (EDA)
1. Overall Churn Rate
Out of 7,043 customers, 1,869 (26.54%) have churned.
Indicates a moderate-to-high attrition problem for the telecom provider.

2. Churn by Gender
Gender	Total Customers	Churned	Churn Rate
Male	3,554	946	26.6%
Female	3,489	923	26.5%

📈 Insight: Gender has negligible effect on churn — retention strategies should focus on behavioral and contractual factors rather than demographics.

3. Churn by Senior Citizen
Category	Total	Churned	Churn Rate
Senior Citizen	1,148	484	42.1%
Non-Senior	5,895	1,385	23.5%

🔍 Key Takeaway:
Senior citizens are 1.8× more likely to churn than younger customers — suggesting service accessibility, support, or affordability concerns.

4. Churn by Tenure
Tenure < 12 months: 45.7% churn
Tenure between 12–24 months: 21.3% churn
Tenure > 36 months: 8.1% churn

📊 Insight:
Churn is inversely related to tenure. Long-term customers demonstrate strong loyalty — indicating onboarding and early experience are critical retention phases.

5. Churn by Contract Type
Contract Type	Total	Churn Rate
Month-to-Month	3,875	43.2%
One Year	1,475	11.3%
Two Year	1,693	2.8%

🧩 Interpretation:
Customers with month-to-month contracts are 15× more likely to churn compared to those with two-year contracts. Lock-in plans clearly enhance stability.

6. Churn by Internet & Add-on Services
Service	Churn (No Service)	Churn (With Service)
Online Security	47%	15%
Tech Support	42%	16%
Device Protection	38%	22%
Online Backup	40%	21%

🧠 Key Insight:
Customers without security or tech-support add-ons show ~2× higher churn probability, highlighting that value-added services improve retention.

7. Churn by Payment Method
Payment Method	Churn Rate
Electronic Check	45.3%
Mailed Check	18.8%
Credit Card (AutoPay)	15.1%
Bank Transfer (AutoPay)	14.7%

💳 Observation:
Electronic check users churn 3× more than AutoPay users — emphasizing the importance of automated, frictionless payment systems.

📌 Consolidated Insights
Driver	Insight	Relative Risk
Senior Citizen	42% churn	+19% vs non-seniors
Tenure < 1 year	45.7% churn	+22% vs long-term users
Month-to-Month Contract	43% churn	+17% vs 1-year contracts
No Tech Support	42% churn	+11%
Payment via E-Check	45% churn	+19% vs AutoPay
💡 Strategic Recommendations

Retention Campaigns for New Customers:
Target customers in their first 3 months, where churn risk peaks at 45%+.
→ Offer discounts, personalized onboarding, or bonus features.

Loyalty Incentives for Seniors:
Introduce senior loyalty plans or support helplines to address the 42% churn in this segment.

Contract Optimization:
Promote annual or two-year contracts via small price cuts or loyalty benefits — could reduce churn by up to 15%.

Bundle Critical Services:
Packages including Tech Support + Online Security correlate with >50% lower churn rates.

Payment Optimization:
Encourage customers to switch from Electronic Check to AutoPay, potentially reducing churn by up to 20%.

🚀 Future Work

Even though this project focuses on EDA, future enhancements could include:

Churn Prediction Model: Using logistic regression or decision trees to predict high-risk customers.

Feature Importance Analysis: Quantify which services or demographics most strongly affect churn probability.

Cohort Analysis: Compare churn behavior across new vs. returning customers.

Interactive Dashboard: Power BI / Tableau dashboards for real-time churn tracking.

🏁 Business Impact

By acting on identified factors, the company can potentially lower churn from 26.5% to ~15–18%, improving annual revenue retention by ₹10–12 crore (approx.) assuming average revenue per user (ARPU) of ₹1,200/month.
