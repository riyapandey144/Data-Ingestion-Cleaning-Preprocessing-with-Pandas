# 🛒 Retail Grocery Sales — Data Cleaning Report

## 📌 Project Overview

This project focuses on **cleaning, standardizing, and enhancing a retail grocery sales dataset** using Python and Pandas.

The main objective was to improve data quality, handle inconsistencies, identify outliers, and create useful features for further analysis.

---

## 🎯 Objectives

The project performs the following tasks:

- 📥 Load and inspect the raw dataset
- 🔍 Identify missing values and duplicates
- 🧹 Clean text and numeric columns
- 📅 Standardize the `Order Date` column
- 📊 Detect and handle outliers
- ⚙️ Perform feature engineering
- 💾 Export the cleaned dataset

---

## 📊 Dataset Overview

| Metric | Value |
|---|---:|
| 📦 Total Records | **9,994** |
| 📋 Total Columns | **15** |
| ❌ Missing Values | **0** |
| 🔄 Duplicate Rows | **0** |
| 💰 Average Sales | **1,496.60** |
| 📈 Average Profit | **374.82** |
| 🏷️ Average Discount | **23%** |
| 💹 Average Profit Margin | **25.02%** |

---

## 🧹 Data Cleaning Process

### 1️⃣ Missing Values

Missing values were identified using Pandas.

- Numerical values were handled using the **median**.
- Categorical values were handled using the **mode**.
- ✅ Final missing values: **0**

### 2️⃣ Duplicate Records

Duplicate rows were identified and removed using:

`drop_duplicates()`

- ✅ Final duplicate rows: **0**

### 3️⃣ Text Cleaning

Unnecessary spaces were removed from text columns to ensure consistent categorical values.

### 4️⃣ Date Standardization

The `Order Date` column was converted into a proper datetime format.

This made the dataset suitable for **time-based analysis and feature extraction**.

---

## 📊 Outlier Detection

The **IQR (Interquartile Range)** method was used to identify extreme values in:

- 💰 `Sales`
- 📈 `Profit`

Outliers were handled using **IQR-based capping** rather than deleting records, allowing important transactions to remain in the dataset while reducing the influence of extreme values.

---

## ⚙️ Feature Engineering

Four useful features were created:

| New Feature | Description |
|---|---|
| 📅 `Year` | Year extracted from Order Date |
| 🗓️ `Month` | Numeric month extracted from Order Date |
| 📆 `Month_Name` | Name of the month |
| 💹 `Profit_Margin_%` | Profit as a percentage of Sales |

### 💡 Profit Margin Formula

```text
Profit Margin (%) = (Profit / Sales) × 100
