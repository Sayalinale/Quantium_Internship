Sales Performance Analysis for Trial Store Layout

## Overview

This project analyzes the impact of lat changes in retail stores by comparing sales performance between trial stores and control stores. The analysis covers data from a pre-trial and trial period, identifying stores with similar characteristics and comparing their sales performance. The goal is to determine whether the lat changes lead to significant differences in sales.

## Objective

The primary objective of this analysis is to identify control stores that are similar to the trial stores and then compare their sales performance during the trial period to evaluate the impact of lat changes.

## Steps Taken

### 1. **Data Loading and Preprocessing**
   - **Transaction Data:** Loaded from the CSV file (`QVI_purchase_behavior.csv`, `QVI_transaction_data.csv`), which contains transaction information such as sales, store numbers, and customer details.
   - **Date Conversion:** The `DATE` column is converted into `datetime` format to filter data accurately.
   - **Pre-trial Data:** Filtered the data to include transactions before the trial period (before February 1, 2019).

### 2. **Store-Level Metrics Calculation (Pre-trial Period)**
   - **Total Sales:** Aggregated total sales (`TOT_SALES`) for each store.
   - **Number of Customers:** Counted the number of unique loyalty card numbers as a proxy for the number of customers.
   - **Number of Transactions:** Counted the total number of transactions (`TXN_ID`) for each store.
   - **Transactions per Customer:** Calculated the average number of transactions per customer (`transactions_per_customer`).

### 3. **Control Store Selection**
   - **Trial Stores:** Selected stores with trial lat changes (Store 77, Store 86, and Store 88).
   - **Similarity Score Calculation:** Used Euclidean distance to calculate the similarity between trial stores and all other stores based on total sales, number of customers, and transactions per customer. 
   - **Control Stores:** Identified the closest stores based on the similarity score as control stores:
     - **Store 77's Control Store:** Store 188
     - **Store 86's Control Store:** Store 13
     - **Store 88's Control Store:** Store 237

### 4. **Sales Data Aggregation for Trial Period**
   - **Trial Period Data:** Filtered the data to include transactions from February 1, 2019, to April 30, 2019 (trial period).
   - **Aggregated Sales Data:** Calculated total sales for trial and control stores during the trial period.
   - **Results:**
     - **Store 77 (Trial):** $777.0 in sales vs. **Control Store 188**: $2928.0
     - **Store 86 (Trial):** $2788.2 in sales vs. **Control Store 13**: $905.0
     - **Store 88 (Trial):** $4286.8 in sales vs. **Control Store 237**: $3817.6

### 5. **Sales Performance Comparison**
   - **Merged Data:** Combined trial and control sales data for performance comparison.
   - **Visualization:** Used a bar plot to visualize sales performance for each trial store vs. its control store during the trial period.

### 6. **Analysis and Interpretation**
   - **Store 77 (Trial):** Experienced a decline in sales compared to its control store.
   - **Store 86 (Trial):** Showed an increase in sales compared to its control store.
   - **Store 88 (Trial):** Also showed an increase in sales compared to its control store.
   - **Conclusion:** The lat changes may have had different impacts on sales across stores, with Store 77 showing a decrease and Stores 86 and 88 showing increases.

## Files in the Repository

- **`QVI_purchase_behavior.csv`, `QVI_transaction_data.csv`:** The raw transaction data used for analysis.
- **`Quantium-Internship.ipynb`,`Quantium-internshipT2.ipynb`:** Jupyter Notebook containing the complete analysis, including data preprocessing, control store selection, sales comparison, and visualization.


## Required Libraries

- `pandas` – for data manipulation and aggregation
- `numpy` – for numerical operations and distance calculations
- `seaborn` – for data visualization
- `matplotlib` – for plotting the sales comparison


## How to Run

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/rusername/sales-performance-analysis.git
   cd sales-performance-analysis
   ```

2. **Install Dependencies:**
   Make sure  have Python 3.x installed. Then, install the required libraries by running:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Analysis:**
   Open the Jupyter notebook (`sales_analysis.ipynb`) and run the cells to perform the analysis and visualize the results.

4. **Visualization:**
   The final step will generate a bar plot comparing the sales of trial stores to their respective control stores. Ensure that  have `matplotlib` and `seaborn` installed to visualize the plot.

## Example Output

- **Trial Stores vs Control Stores Sales Comparison:**
   - Trial Store 77: $777.0 vs Control Store 188: $2928.0
   - Trial Store 86: $2788.2 vs Control Store 13: $905.0
   - Trial Store 88: $4286.8 vs Control Store 237: $3817.6

A **bar plot** will be displayed to show these sales comparisons.

## Conclusion and Further Analysis

This analysis provides an initial comparison of trial stores against control stores. Based on the results, further statistical tests (e.g., t-tests, regression analysis) can be conducted to evaluate whether the observed differences in sales are statistically significant. Additionally, considering factors such as customer feedback, operational improvements, and long-term performance could provide a more comprehensive understanding of the lat changes' effectiveness.
