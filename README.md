# Telecom X — Customer Churn: Exploratory Data Analysis

EDA of 7,267 telecom customers to find what drives cancellations. This analysis feeds the [churn prediction pipeline](https://github.com/MarlonPC32/telecomx-churn-prediction).

## Data

- Nested JSON from the Telecom X API (`TelecomX_Data.json`), loaded with `pd.read_json`.
- 4 nested columns (`customer`, `phone`, `internet`, `account`) flattened with `pd.json_normalize`.

## Cleaning

- Normalized the nested JSON columns into flat features.
- `Charges.Total`: coerced to numeric; nulls (customers with no billing history yet) filled with 0.
- Encoded `Churn` as 1/0.
- Stripped and lowercased inconsistent string categories (contract, payment method, internet service).
- Engineered `Cuentas_Diarias` = `Charges.Monthly` / 30 (estimated daily spend).

Output: `telecomx_datos_tratados.csv` — the cleaned dataset used for modeling.

## Analysis

- Target distribution: 25.7% churn vs. 74.3% retained.
- Crosstabs: churn rate by gender, contract type, and payment method.
- Boxplots: tenure, total charges, and monthly charges split by churn status.
- Correlation heatmap over numeric features.

## Findings

- Short-term (month-to-month) contracts churn far more than one- and two-year contracts.
- Electronic-check payers churn at higher rates than automatic or mailed-check payers.
- Churned customers skew toward low tenure — the first months are the risk window.
- Fiber-optic internet correlates positively with churn (r ≈ 0.30); tenure correlates negatively (r ≈ −0.34).

## Reproduce

```bash
pip install pandas matplotlib seaborn
```

Open `TelecomX_Churn_Analysis.ipynb` and run all cells top to bottom.

## Context

Built for the Telecom X Data Science Challenge (Oracle Next Education).
