Retail Sales Trial Analysis
Overview
This project analyzes the sales performance of specific stores during a trial period. The goal is to compare the sales performance of trial stores with control stores, using pre-trial data for store selection and similarity calculation. The analysis includes summary statistics, control store selection, and visual comparisons of sales data during the trial period.

Files
QVI_data.csv: The dataset containing transaction data.
Retail_Sales_Trial_Analysis.ipynb: The Jupyter notebook containing the code for data processing, analysis, and visualization.
Prerequisites
Make sure the following Python libraries are installed:

pandas: For data manipulation and analysis.
numpy: For numerical operations.
matplotlib: For data visualization.
seaborn: For advanced visualizations.
You can install the necessary libraries using pip:

bash
Copy
Edit
pip install pandas numpy matplotlib seaborn
Data Structure
The dataset (QVI_data.csv) should include the following columns:

DATE: The date of the transaction.
STORE_NBR: The store number.
TOT_SALES: The total sales for each transaction.
LYLTY_CARD_NBR: The loyalty card number of the customer.
TXN_ID: The unique transaction identifier.
Steps in the Analysis
1. Load Transaction Data
The code begins by loading transaction data from a CSV file and converting the DATE column to a datetime type for easier manipulation.

2. Pre-Trial Data Filtering
The data is filtered to include only transactions before February 1, 2019, representing the pre-trial period.

3. Summary Statistics Calculation
Summary statistics are calculated for each store during the pre-trial period. These include:

total_sales: The total sales for the store.
num_customers: The number of unique customers (based on loyalty card numbers).
num_transactions: The total number of transactions.
Additionally, the code calculates transactions_per_customer for each store.

4. Trial Stores Identification
Three stores (77, 86, and 88) are identified as trial stores. These stores are selected for the intervention or change being tested.

5. Control Stores Selection
Control stores are selected based on their similarity to the trial stores. A custom function calculates the Euclidean distance between stores based on three metrics: total_sales, num_customers, and transactions_per_customer. The closest match is selected as a control store for each trial store.

6. Trial Period Filtering
The data is filtered to include transactions during the trial period (February 1, 2019, to April 30, 2019).

7. Sales Comparison
Sales data is aggregated for both trial and control stores during the trial period. The total sales are summed up for each store and compared to evaluate the impact of the trial.

8. Data Visualization
A bar plot is created to visually compare the sales performance of trial stores against their respective control stores.

How to Run the Analysis
Prepare the Data: Ensure the dataset (QVI_data.csv) is in the correct format and accessible by the script.
Run the Script: Execute the code in the provided Jupyter notebook (Retail_Sales_Trial_Analysis.ipynb).
View Results: The summary statistics and performance comparison will be printed in the notebook. A bar plot comparing the sales of trial and control stores will be displayed.
Key Findings
Sales Performance: The visualizations and aggregated data show how the trial stores performed in comparison to their control stores.
Control Store Selection: The similarity-based selection of control stores ensures a meaningful comparison.
Impact of the Trial: Any observed differences in sales performance during the trial period may be attributed to the changes introduced.
Conclusion
This analysis provides insights into the effectiveness of interventions or changes made at trial stores. By comparing these stores to control stores, businesses can evaluate the impact on sales and other key metrics.

