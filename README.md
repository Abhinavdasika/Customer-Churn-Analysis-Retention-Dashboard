# Customer Churn Analysis & Retention Dashboard

## Project Overview

This project analyses telecom customer churn to understand customer behaviour, identify high-risk segments and highlight potential retention opportunities.

An interactive four-page Power BI dashboard was developed to present key business metrics, churn drivers, customer segmentation and recommended retention actions.

**Objective:** Turn customer data into actionable insights that can support customer retention decisions.

## Tools & Technologies

- **Power BI** – Interactive dashboard development and reporting
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and business metrics
- **Python (Pandas, NumPy)** – Data analysis and preparation, if used in the final workflow
- **SQL** – Data querying, if used in the final workflow

## Dataset

- Dataset: IBM Telco Customer Churn
- Original records: 7,043 customers
- Original columns: 33
- Target variable: `Churn Label`
- Customer information includes tenure, contract type, payment method, internet service, monthly charges, total charges and churn reasons.

## Data Preparation

The preparation process included:

- Reviewing missing values and duplicate records.
- Removing constant or non-informative columns.
- Standardising data types and categorical values.
- Converting `Total Charges` into a numeric field.
- Preserving missing total-charge values for zero-tenure customers instead of automatically replacing them with zero.
- Creating tenure segments for customer risk analysis.

## Dashboard Pages

### 1. Executive Overview

Provides a high-level view of customer churn and key business metrics.

Key metrics:
- Total customers: 7,043
- Churned customers: 1,869
- Overall churn rate: 26.54%
- Average tenure: 32.37 months
- Historical total charges associated with churned customers: approximately $2.86 million

Visuals include churn by contract type, tenure, payment method and internet service.

### 2. Churn Driver Analysis

Examines customer characteristics and reported reasons associated with churn.

Key findings:
- Electronic check customers: 45.29% churn rate.
- Fiber optic customers: 41.89% churn rate.
- Customers without online security: 41.77% churn rate.
- Customers without tech support: 41.64% churn rate.
- Average monthly charges: $74.44 for churned customers versus $61.27 for retained customers.

The leading reported churn reason was attitude of support person (192 customers), followed by competitors offering higher download speeds (189 customers).

### 3. Retention Strategy & Opportunities

Segments customers by tenure to identify groups that may require additional retention attention.

| Tenure segment | Customers | Churned | Churn rate |
|---|---:|---:|---:|
| 0–12 months | 2,186 | 1,037 | 47.44% |
| 13–24 months | 1,024 | 294 | 28.71% |
| 25–48 months | 1,594 | 325 | 20.39% |
| 49–72 months | 2,239 | 213 | 9.51% |

The first-year customer segment has the highest churn rate and represents an important area for further retention analysis.

### 4. Retention Action Plan

Presents proposed business actions based on the observed churn patterns:

1. **Early-tenure retention:** Evaluate onboarding, early satisfaction check-ins and issue resolution.
2. **Contract strategy:** Test suitable longer-term contract incentives.
3. **Customer support:** Review complaints, response times and support quality.
4. **Competitive positioning:** Investigate competitor pricing, internet speeds and service-quality gaps.

These are recommendations for testing, not proven interventions.

## Key Business Insights

- Overall churn is 26.54%.
- Month-to-month contract customers have a 42.71% churn rate, compared with 2.83% for two-year contract customers.
- Customers in their first 12 months have a 47.44% churn rate.
- Electronic check customers have a 45.29% churn rate.
- Fiber optic customers have a 41.89% churn rate.
- Customers without online security or tech support show higher churn rates than customers with those services.

## Business Value

The dashboard helps stakeholders:

- Identify customer segments with comparatively high churn.
- Understand the characteristics and reported reasons associated with churn.
- Prioritise customer groups for further investigation.
- Develop retention experiments and monitor their results.

## Project Limitations

- The analysis is descriptive and based on historical customer data.
- Observed relationships do not establish causation.
- The dashboard does not predict future churn.
- The recommended retention actions have not been experimentally validated.
- Historical charges associated with churned customers should not be interpreted as future revenue loss.

## Repository Contents

```text
customer-churn-retention-analysis/
│
├── dashboard/
│   └── Customer_Churn_Retention_Dashboard.pbix
│
├── data/
│   └── telco_churn_cleaned.csv
│
├── screenshots/
│   ├── executive-overview.png
│   ├── churn-driver-analysis.png
│   ├── retention-strategy.png
│   └── retention-action-plan.png
│
└── README.md
```

## How to Use

1. Clone or download this repository.
2. Open the `.pbix` file using Microsoft Power BI Desktop.
3. If Power BI requests the source data, update the file path to the CSV in the `data` folder.
4. Refresh the data to explore the dashboard.

## Dataset Attribution

Dataset: IBM Telco Customer Churn sample dataset, commonly distributed through Kaggle.

Include the original dataset source link and comply with its applicable usage and attribution terms.

---

**Project Type:** Data Analytics | Business Intelligence | Customer Retention  
**Dashboard Tool:** Microsoft Power BI
