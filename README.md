# 📱 PhonePe Digital Payments — Case Study

![PhonePe](https://img.shields.io/badge/PhonePe-Digital%20Payments-purple)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Overview
This case study analyzes transaction data from the PhonePe digital payments 
platform along with demographic data across various states and districts in India. 
The objective is to provide insights into transaction trends, device usage, 
and demographic correlations from Q1 2018 to Q2 2021.

---

## 📂 Dataset
The data is spread across 5 sheets in an Excel file:

| Sheet | Description |
|---|---|
| State_Txn and Users | State-level transactions, amount, ATV, registered users, app opens |
| State_TxnSplit | Breakdown by transaction type per state |
| State_DeviceData | Device brand usage per state |
| District_Txn and Users | District-level transaction and user data |
| District Demographics | Population, area, density per district |

**Time Period:** Q1 2018 → Q2 2021 (14 quarters)  
**Coverage:** 36 States/UTs | 736 Districts

---

## 🛠️ Tools & Libraries
- Python 3.x
- Pandas
- Matplotlib
- Jupyter Notebook

---

## 📊 Tasks Covered

### Task 1 — Data Loading & Understanding
- Loaded all 5 datasets and explored structure
- Displayed summary statistics and data types
- Identified missing values across all datasets
- Found total states (36), districts (736)
- Uttar Pradesh has the most districts (75)

### Task 2 — Exploratory Data Analysis
- Analyzed transaction trends by state over the years
- Identified top 5 and bottom 5 states by transaction volume
- Found most common transaction type per state and quarter
- Identified top device brand per state
- Calculated Average Transaction Value (ATV) per state
- Analyzed app usage trends over time
- Mapped unique district name to district code

### Task 3 — Data Quality Checks
- Compared district-level vs state-level aggregations
- Found 1 discrepancy in Andhra Pradesh (Amount field)
- Traced discrepancy to 1 missing value in Amount (INR)

### Task 4 — Data Merging & Advanced Analysis
- Calculated ratio of registered users to population per state
- Correlated population density with transaction volume
- Calculated average transaction amount per user
- Analyzed device brand usage ratio per state

### Task 5 — Data Visualization
- Line plots for transaction trends over time
- Pie chart for transaction type distribution
- Bar chart for population density by district

### Task 6 — Insights & Conclusions
- Identified key trends and patterns in transaction data
- Correlated demographic data with transaction behavior
- Summarized findings with actionable recommendations

---

## 🔑 Key Findings

| Finding | Detail |
|---|---|
| 🏆 Top State by Transactions | Karnataka (2.98 Billion) |
| 📉 Lowest State by Transactions | Lakshadweep (71,610) |
| 📱 Most Used Device | Xiaomi & Samsung |
| 💳 Most Common Transaction Type | Peer-to-peer Payments |
| 🏙️ Most Districts | Uttar Pradesh (75) |
| ⚠️ Data Discrepancy | Andhra Pradesh — Amount (INR) |

---

## 💡 Recommendations
1. Focus marketing efforts on low-adoption states like Lakshadweep, Mizoram & Meghalaya
2. Optimize the app experience for Xiaomi & Samsung devices
3. Promote Merchant Payments which is currently underutilized
4. Target high-density urban districts for premium financial services
5. Fix missing data issues in Andhra Pradesh for better data integrity

---

## 📁 Repository Structure
