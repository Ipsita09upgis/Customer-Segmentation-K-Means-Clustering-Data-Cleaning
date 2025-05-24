# 🧼 K-Means Clustering: Data Cleaning

This repository contains the **data cleaning steps** performed as part of a customer segmentation project using K-Means Clustering on online retail transaction data.

## 📄 File Overview

- `K Means Clustering Data Cleaning_Ipsita.ipynb`: Jupyter Notebook containing data cleaning operations and saving the cleaned dataset.
- `Online Retail Cleaned.xlsx`: Cleaned version of the original dataset, saved for further analysis.

## 📊 Dataset

The dataset used is an Excel file containing online retail transactions with fields such as:
- `InvoiceNo`
- `StockCode`
- `Description`
- `Quantity`
- `InvoiceDate`
- `UnitPrice`
- `CustomerID`
- `Country`


---

## ✅ Data Cleaning Steps

### 1. Handle Missing Values
- Checked for null values using `isnull().sum()`.
- Dropped rows missing `CustomerID` or `Description`.

### 2. Remove Duplicates
- Removed duplicate records using `drop_duplicates()`.

### 3. Filter Invalid Transactions
- Removed rows where `Quantity <= 0` or `UnitPrice <= 0`.
- Excluded cancelled transactions (`InvoiceNo` starting with 'C').

### 4. Correct Data Types
- Converted `CustomerID` to integer for consistency.

---

## 💾 Save Cleaned Data

After cleaning, the data was saved back to an Excel file for reuse:

```python
df.to_excel("Online Retail Cleaned.xlsx", index=False)


🛠 Technologies Used
Python 3.x
Pandas
Jupyter Notebook
OpenPyXL (for Excel writing)
