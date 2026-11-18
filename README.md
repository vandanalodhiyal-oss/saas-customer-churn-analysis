# SaaS / Telecom Customer Churn Analysis

## Business Problem
A subscription business loses revenue every time a customer cancels. This project finds out **which customers churn, why they churn, and what the company can do to keep them.**

## Dataset
- **Source:** IBM Telco Customer Churn dataset (Kaggle)
- **Size:** 7,043 customers, 21 columns
- **Key columns:** tenure, Contract, InternetService, TechSupport, PaymentMethod, MonthlyCharges, TotalCharges, Churn

## Tools Used
Python (pandas, numpy, matplotlib, seaborn), Jupyter Notebook in VS Code

## Data Cleaning
- `TotalCharges` was stored as text. It had 11 blank values, all for customers with tenure 0 (brand new customers), so they were set to 0 and the column was converted to numeric.
- Checked for duplicate rows and customer IDs: none found.
- Converted `SeniorCitizen` from 0/1 to No/Yes.
- Created a `tenure_group` column (0-12, 13-24, 25-48, 49-72 months).
- Saved the cleaned data as `telco_churn_clean.csv`.

## Key Insights
**Overall churn rate: 26.5%** (about 1 in 4 customers).

1. **New customers leave first.** Churn is 47.4% in the first 12 months and falls to 9.5% after 4 years.
2. **Contract type is the strongest signal.** Month-to-month 42.7%, one-year 11.3%, two-year 2.8%.
3. **Fiber optic customers churn more.** 41.9% vs 19.0% for DSL.
4. **Tech support helps.** 41.6% churn without TechSupport vs 15.2% with it.
5. **Electronic check users are the riskiest.** 45.3% churn vs 15.2% for credit card payers.
6. **Higher bills, higher churn.** Churned customers paid 74.44 on average vs 61.27 for retained customers.

## Charts
![Churn by Contract](images/churn_by_contract.png)
![Tenure by Churn](images/tenure_by_churn.png)
![Monthly Charges by Churn](images/monthly_charges_by_churn.png)

## Recommendations
1. Improve **onboarding in the first 12 months** (welcome calls, early check-ins, support).
2. Offer **discounts to move month-to-month users to annual plans.**
3. Bundle **tech support** for new and Fiber optic customers.
4. Encourage **automatic payments** instead of electronic check.
5. Review **Fiber optic pricing and service quality.**

## Limitations
- The analysis shows patterns, not proof of cause.
- This is a sample dataset, so results may differ for other companies.
- No usage or support-ticket data was available.

## Files
- `churn_analysis.ipynb`: full analysis
- `WA_Fn-UseC_-Telco-Customer-Churn.csv`: raw data
- `telco_churn_clean.csv`: cleaned data
- `images/`: chart images

## Author
Vandana Lodhiyal
