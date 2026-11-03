Online Retail Dataset
Overview
This repository contains the Online Retail dataset in Excel format. It records transactions from a UK-based online retail business and can be used for data analysis, customer behaviour analysis, and customer segmentation.
Dataset File
- online+retail.zip — compressed archive containing Online Retail.xlsx.
- Worksheet: Online Retail
- Records: 541,909 transactions (excluding the header row).
- Columns: 8
- Date range: 1 December 2010 to 9 December 2011
- Countries represented: 38
Dataset Columns
Column	Description
InvoiceNo	Invoice number identifying a transaction.
StockCode	Product/item code.
Description	Product description.
Quantity	Quantity of the item in the transaction.
InvoiceDate	Date and time when the transaction was generated.
UnitPrice	Price per unit.
CustomerID	Customer identifier.
Country	Customer's country.


How to Use
1. Download online+retail.zip.
2. Extract the archive to get Online Retail.xlsx.
3. Open the Excel file or load it in Python.
Example using Pandas:
import pandas as pd

df = pd.read_excel("Online Retail.xlsx")

print(df.head())
print(df.info())
Use in Customer Segmentation
This dataset can be used to build an RFM (Recency, Frequency, Monetary) analysis:
- Recency: How recently a customer made a purchase.
- Frequency: How often a customer made purchases.
- Monetary: How much a customer spent.
These features can then be used with clustering algorithms such as K-Means and DBSCAN to explore customer groups.
Requirements
For Python usage:
pip install pandas openpyxl
Data Notes
The dataset contains transaction-level records. Before analysis, inspect missing customer IDs, cancelled invoices, duplicate rows, and non-positive quantities or prices. Apply cleaning rules according to the objective of your analysis.
