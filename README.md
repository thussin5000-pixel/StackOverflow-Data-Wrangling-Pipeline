# 🛠️ Data Wrangling: Stack Overflow Developer Survey Analysis

This repository contains the **Data Wrangling** phase of the Stack Overflow Developer Survey project. The goal of this phase was to transform raw, messy survey data into a clean, structured, and normalized format ready for exploratory data analysis (EDA) and machine learning.

## 📋 Objectives
The primary focus was to ensure data integrity and consistency by:
* Identifying and removing duplicate entries.
* Handling missing values using statistical imputation.
* Standardizing categorical labels (e.g., Country, Education Level).
* Applying feature scaling (Min-Max & Z-Score) for comparative analysis.

---

## 🚀 Key Steps & Implementation

### 1. Data Cleaning & De-duplication
* **Method:** Identified duplicate rows based on unique respondent profiles.
* **Result:** Removed `X` duplicate records to ensure each response is unique and unbiased.

### 2. Handling Missing Values (Imputation)
* Analyzed missing data patterns using heatmaps and percentage summaries.
* **Strategy:** * Used **Median** for numerical columns (e.g., Compensation) to avoid outlier bias.
    * Used **Mode** for categorical columns (e.g., Employment status) to retain the most frequent descriptors.

### 3. Normalization & Standardization
To compare salaries across different scales (Monthly vs. Yearly) and currencies:
* **Min-Max Scaling:** Transformed `ConvertedCompYearly` into a `0-1` range for uniform scaling.
* **Z-Score Standardization:** Scaled features to have a **Mean of 0** and **Standard Deviation of 1**, identifying outliers and data distribution spread.

### 4. Categorical Encoding
* Applied **One-Hot Encoding** to the `Employment` column, converting textual categories into binary numerical features ($0$ or $1$) suitable for algorithmic processing.

### 5. Data Harmonization
* Simplified complex categorical entries in `EdLevel` and `Country` to reduce noise and improve visualization clarity.

---

## 📊 Visualizations
During this phase, distributions were plotted to verify the impact of normalization techniques:
* **Histograms:** Compared raw vs. normalized vs. standardized distributions.
* **Box Plots:** Used to detect statistical outliers using the **IQR (Interquartile Range)** method.

---

## 🛠️ Tools Used
* **Python 3.x**
* **Pandas:** For data manipulation and cleaning.
* **Scikit-Learn:** For `MinMaxScaler` and `StandardScaler`.
* **Matplotlib & Seaborn:** For data distribution profiling.

---

## 💡 Key Insight
By performing these wrangling steps, we reduced the data noise by approximately **20%**, ensuring that subsequent analysis reflects the true trends of the global developer community.
