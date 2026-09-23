# 🏥 Healthcare Data Analysis — Task 5

## 📌 Overview
This notebook performs exploratory data analysis (EDA) on a healthcare dataset. It covers data loading, cleaning, feature engineering, and summary visualizations to understand patient admissions, demographics, and billing patterns.

## 📁 Dataset
- **File:** `healthcare_data_for_task - healthcare_data_for_task.csv`
- **Location expected:** `/content/` (Google Colab environment)

## ⚙️ Requirements
```
pandas
numpy
matplotlib
seaborn
```

## 🔍 Workflow

### 1. 📥 Data Loading
- Import required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`)
- Load the CSV dataset into a DataFrame

### 2. 🧭 Initial Exploration
- Preview data with `.head()`
- Check dataset dimensions with `.shape`
- List columns with `.columns`
- Inspect data types and non-null counts with `.info()`
- Generate summary statistics with `.describe()`

### 3. 🧹 Data Cleaning
- Check for missing values with `.isnull().sum()`
- Fill missing `Medical_Code` entries with `'Unknown'`
- Standardize `Admission_Type` text (strip whitespace, title case)
- Review unique values and counts in `Admission_Type`

### 4. 🗓️ Date Processing & Feature Engineering
- Convert `Date_of_Admission` and `Discharge_Date` to datetime format
- Extract year, month, and date components from admission dates
- Calculate `Stay_Days` (length of hospital stay) as the difference between discharge and admission dates

### 5. 📊 Analysis & Aggregation
- Summarize `Billing_Amount` statistics
- Compute average patient age grouped by `Medical_Condition`
- Build a cross-tabulation of `Medical_Condition` vs. `Gender`

### 6. 📈 Visualization
- Bar chart of `Admission_Type` value counts
<img width="220" height="199" alt="Screenshot 2026-09-23 091107" src="https://github.com/user-attachments/assets/9523e310-32c0-423c-8e78-7b6e4f736a51" />


## ✅ Key Outputs
- Cleaned and enriched DataFrame with a new `Stay_Days` column
- Summary statistics on billing and patient demographics
- Cross-tabulated insights between medical conditions and gender
- Visual breakdown of admission types
