# LOAN APPLICATION ANALYSIS

## Dashboard 1: Loan Applicant Risk Analysis

![Loan Applicant Risk Analysis](./Screenshot%202026-10-30%20115543.png)

## Dashboard 2: Further Loan Approval Analysis

![Further Loan Approval Analysis](./Screenshot%202026-10-30%20115626.png)

A Power BI dashboard project exploring historical loan application outcomes and how approval rates vary across applicant characteristics and loan-related measures.

## Project overview

This project analyses **614 loan applications** and presents the findings across two dashboard pages:

1. **Loan Applicant Risk Analysis** — a high level view of application outcomes and approval rates across education, property area, marital status, and employment status.
2. **Further Loan Approval Analysis** — a deeper look at credit history, approved versus rejected applications, average applicant income, and average loan amount by loan status.

The purpose is to turn historical application data into clear, decision-supporting insights. The dashboards describe patterns in the available data; they do not predict future defaults or establish why a loan was approved or rejected.

## Dashboard previews

### 1. Loan Applicant Risk Analysis

![Loan Applicant Risk Analysis dashboard](images/loan-applicant-risk-analysis.png)

This page includes:
- Total applicants
- Approved applicants
- Rejected applicants
- Overall approval rate
- Approval rate by education
- Approval rate by property area
- Approval rate by marital status
- Approval rate by employment status
- Slicers for property area, education, and credit history

### 2. Further Loan Approval Analysis

![Further Loan Approval Analysis dashboard](images/further-loan-approval-analysis.png)

This page includes:
- Approval rate by credit history
- Number of approved and rejected applications
- Average applicant income by loan status
- Average loan amount by loan status

## Key findings

Based on the values displayed in the dashboards:

| Metric / comparison | Result |
|---|---:|
| Total applicants | 614 |
| Approved applicants | 422 |
| Rejected applicants | 192 |
| Overall approval rate | 68.73% |
| Approval rate — graduates | 70.83% |
| Approval rate — non-graduates | 61.19% |
| Approval rate — semiurban | 76.82% |
| Approval rate — urban | 65.84% |
| Approval rate — rural | 61.45% |
| Approval rate — credit history 1 | 79.58% |
| Approval rate — credit history 0 | 7.87% |
| Average applicant income — rejected | 5,446.08 |
| Average applicant income — approved | 5,384.07 |
| Average loan amount — rejected | 151.22 |
| Average loan amount — approved | 144.29 |

### Interpretation

- About 68.73% of applications were approved, while 31.27% were rejected.
- Applicants coded with credit history `1` have a much higher observed approval rate than those coded `0`. This is the largest visible difference among the approval-rate comparisons shown. 
- Semiurban applicants have a higher observed approval rate than urban and rural applicants.
- Graduates have a higher observed approval rate than non-graduates.
- Rejected applicants have slightly higher average applicant income and average loan amount than approved applicants. This indicates that income alone does not explain the historical approval outcomes.

These are descriptive findings and associations, not evidence of causation.

## Business recommendations

1. Investigate credit history patterns and confirm exactly what the `0` and `1` values represent.
2. Review differences in approval rates across applicant groups to understand whether other variables explain the observed patterns.
3. Check categories with missing or unknown information before making decisions based on their approval rates.
4. Where possible, compare approval decisions with actual repayment and default outcomes to assess lending risk more directly.

## Data quality and interpretation notes

- The marital status chart reports a **100% approval rate** for the `Unknown` category. The number of applicants in that category should be checked because small group can produce a misleadingly high percentage.
- The credit history chart displays categories `0` and `1`, while the dashboard slicer also includes `Unknown`. Confirm whether unknown credit history records are excluded from the chart, filtered out, or otherwise handled.
- Confirm the meaning and units of the income and loan amount fields before assigning a currency symbol or describing them as monthly or annual amounts.
- The labels `Yes` and `No` in the marital-status chart should be mapped to their exact meanings using the dataset's data dictionary.
- Approval rate measures historical approval decisions. It is **not** the same as repayment success, default probability, or model accuracy.

## Tools

- **Microsoft Power BI** — dashboard design, interactive slicers, KPI cards, and visual analysis.
- **Loan application dataset** — https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset?utm_source=chatgpt.com

## Future improvements

- Include the Power BI `.pbix` file, if it can be shared.
- Document data cleaning, missing-value treatment, and calculated measures.
- Add applicant counts alongside approval rates for each category.
- Investigate unknown and missing categories.
- Add affordability measures such as loan amount relative to income.
- If repayment outcome data is available, analyse defaults and repayment performance.

## Disclaimer

This project is for educational and analytical demonstration. The findings describe the dataset represented in the dashboards and should not be used as standalone criteria for approving or rejecting real loan applicants. Lending decisions require validated data, appropriate risk assessment, fairness checks, and consideration of applicable laws and regulations.
