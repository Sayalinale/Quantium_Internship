

# Retail Sales Trial Analysis

## Overview
This project compares the sales performance of trial stores (77, 86, and 88) with control stores during a trial period. By analyzing pre-trial data, control stores are selected based on similarity to trial stores. Sales performance during the trial period is then compared.

## Files
- `QVI_data.csv`: Transaction data.
- `Retail_Sales_Trial_Analysis.ipynb`: Jupyter notebook with the analysis code.

## Prerequisites
Required Python libraries:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`

Install them using:
```bash
pip install pandas numpy matplotlib seaborn
```

## Data Columns
- **DATE**: Transaction date.
- **STORE_NBR**: Store identifier.
- **TOT_SALES**: Sales amount.
- **LYLTY_CARD_NBR**: Loyalty card number (customer).
- **TXN_ID**: Transaction ID.

## Analysis Steps
1. **Load and preprocess data** (filter by pre-trial period).
2. **Calculate summary statistics** for each store (sales, customers, transactions).
3. **Identify trial stores** (77, 86, 88).
4. **Select control stores** based on similarity to trial stores.
5. **Filter trial period data** (Feb 1, 2019 – Apr 30, 2019).
6. **Compare sales** of trial vs. control stores.
7. **Visualize** results with a bar plot.

## How to Run
1. Place `QVI_data.csv` in the same directory as the notebook.
2. Run the notebook (`Retail_Sales_Trial_Analysis.ipynb`).
3. Review the printed results and bar plot for performance comparison.

## Conclusion
The analysis evaluates the effectiveness of trial interventions by comparing the sales performance of trial stores against control stores, offering insights into the impact of changes implemented during the trial period.
