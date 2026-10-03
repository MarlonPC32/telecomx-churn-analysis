# Telecom X — Customer Churn: Exploratory Data Analysis

EDA of telecom customers to find what distinguishes customers who cancel from those who stay. This analysis feeds the [churn prediction pipeline](https://github.com/MarlonPC32/telecomx-churn-prediction).

## Data

- Nested JSON from the Telecom X source (`TelecomX_Data.json`), loaded with `pd.read_json` — 7,267 records.
- 4 nested columns (`customer`, `phone`, `internet`, `account`) flattened with `pd.json_normalize`.

## Cleaning

- Normalized the nested JSON columns into flat features.
- `Charges.Total`: coerced to numeric; nulls (all tenure-0 customers with no billing history yet) filled with 0.
- Stripped and lowercased inconsistent string categories (contract, payment method, internet service).
- **Target handling:** the raw data contains 224 records (3.1%) with a blank churn label. Blank is not "No" — those records were **excluded** from analysis, leaving 7,043 labeled records. Relabeling unknowns as retained would fabricate negative labels and corrupt every downstream result.
- Engineered `Cuentas_Diarias` = `Charges.Monthly` / 30 for exploration. It correlates 1.00 with the monthly column — a pure rescale — so it is excluded from modeling.

## Export

The notebook writes `telecomx_datos_tratados.csv` (7,043 × 22) as its final step, so the handoff to modeling is reproducible. The prediction repo commits a copy.

## Analysis

- Target distribution: 26.5% churn vs. 73.5% retained (labeled records only).
- **Segment rates** (within-segment churn share plus segment size — not raw counts) by contract type, payment method, and gender.
- Boxplots: tenure, total charges, and monthly charges split by churn status.
- Correlation heatmap over numeric features.

## Findings

- Contract length is the sharpest categorical split — month-to-month customers churn at far higher rates than one- and two-year customers.
- Electronic-check payers churn more than automatic or mailed-check payers.
- Tenure separates the classes clearly (correlation with churn: −0.35): churned customers concentrate at low tenure — the early months are the risk window.
- Monthly charges correlate positively (+0.19) and total charges negatively (−0.20) with churn in this snapshot.

## Reproduce

```bash
pip install pandas matplotlib seaborn
```

Open `TelecomX_Churn_Analysis.ipynb` and run all cells top to bottom.

## Context

Built for the Telecom X Data Science Challenge (Oracle Next Education).
