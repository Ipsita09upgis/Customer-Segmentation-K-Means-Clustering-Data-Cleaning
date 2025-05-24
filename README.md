# Customer-Segmentation-K-Means-Clustering-Data-Cleaning

# 🧼 K-Means Clustering: Data Cleaning

This repository contains the **data cleaning steps** carried out as part of a customer segmentation project using K-Means Clustering on online retail data. T
he goal is to clean, transform, and prepare the online retail dataset for clustering analysis.

## 📄 File Overview

- `K Means Clustering Data Cleaning_Ipsita.ipynb`: Jupyter Notebook dedicated to cleaning the dataset before applying clustering algorithms.

## 📊 Dataset

The dataset used is an online retail dataset with fields such as:
- `InvoiceNo`
- `StockCode`
- `Description`
- `Quantity`
- `InvoiceDate`
- `UnitPrice`
- `CustomerID`
- `Country`

> 📌 *Note: The dataset file (`Online Retail.xlsx`) is not included in this repo. Please ensure it is available locally for the notebook to run properly.*

---

## ✅ Data Cleaning Steps

### 1. Handle Missing Values
- Checked for null values using `isnull().sum()`.
- Dropped rows missing `CustomerID` or `Description`.

### 2. Remove Duplicates
- Identified and removed duplicate rows using `drop_duplicates()`.

### 3. Filter Invalid Transactions
- Removed transactions with `Quantity <= 0` or `UnitPrice <= 0`.
- Filtered out cancelled orders (`InvoiceNo` starting with 'C').

### 4. Correct Data Types
- Converted `CustomerID` to integer type for further analysis.

---

## 🛠 Technologies Used

- Python 3.x
- Pandas
- Jupyter Notebook


