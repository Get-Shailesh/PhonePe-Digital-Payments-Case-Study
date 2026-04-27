<div align="center">

# 📱 PhonePe Digital Payments Analysis
### A Comprehensive Data Analysis Case Study on India's Digital Payment Ecosystem
#### Q1 2018 — Q2 2021

![PhonePe](https://img.shields.io/badge/PhonePe-Digital%20Payments-5f259f?style=for-the-badge&logo=phonepe)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Analysis-150458?style=for-the-badge&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-11557c?style=for-the-badge)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

</div>

---

## 📌 Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Tools & Libraries](#tools--libraries)
- [Analysis Tasks](#analysis-tasks)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [How to Run](#how-to-run)
- [Author](#author)

---

## 🔍 Overview

This case study provides an in-depth analysis of **PhonePe's digital payment transactions** across all Indian states and districts from **Q1 2018 to Q2 2021**. The analysis covers transaction trends, user behavior, device usage patterns, and demographic correlations to uncover meaningful insights about India's rapidly growing digital payments landscape.

> PhonePe is one of India's largest digital payments platforms, processing billions of transactions annually across 36 states and union territories.

---

## 📂 Dataset

The dataset spans **14 quarters** (Q1 2018 → Q2 2021) and covers:
- **36** States & Union Territories
- **736** Unique Districts
- **5** Transaction Types

| Sheet | Rows | Description |
|---|---|---|
| `State_Txn and Users` | 504 | State-level transactions, amount, ATV, registered users, app opens |
| `State_TxnSplit` | 2,514 | Transaction breakdown by type per state |
| `State_DeviceData` | 5,544 | Device brand usage statistics per state |
| `District_Txn and Users` | 10,248 | District-level transaction and user data |
| `District Demographics` | 742 | Population, area, density per district |

### Data Dictionary

| Column | Description |
|---|---|
| `State` | Name of the state |
| `Year` / `Quarter` | Time period |
| `Transactions` | Number of transactions |
| `Amount (INR)` | Total transaction amount |
| `ATV (INR)` | Average Transaction Value |
| `Registered Users` | Number of registered PhonePe users |
| `App Opens` | Number of times app was opened |
| `Transaction Type` | Category of transaction |
| `Brand` | Device brand used |
| `Population` / `Density` | Demographic indicators |

---

## 📁 Project Structure
PhonePe-Digital-Payments-Case-Study/
│
├── 📓 PhonePe_Digital_Payments_Analysis.ipynb   # Main analysis notebook
├── 📊 phonepe-pulse_raw-data_...xlsx            # Raw dataset (5 sheets)
├── 📄 district_code_mapping.csv                 # District → Code mapping
└── 📝 README.md                                 # Project documentation

---

## 🛠️ Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning, analysis |
| Matplotlib | Data visualization |
| Jupyter Notebook | Interactive development environment |

---

## 📊 Analysis Tasks

### ✅ Task 1 — Data Loading & Understanding
- Loaded and explored all 5 datasets
- Analyzed data types and summary statistics
- **Missing Values Found:**
  - `State_Txn and Users` → `Amount (INR)`: 1 missing (0.2%)
  - `District_Txn and Users` → `Code`: 28 missing (0.27%)
- Total unique states: **36** | Total unique districts: **736**
- State with most districts: **Uttar Pradesh (75 districts)**

### ✅ Task 2 — Exploratory Data Analysis
- Calculated total transactions and amounts per state
- Identified most common transaction types per state and quarter
- Analyzed device brand penetration across states
- Computed ATV trends and app usage patterns
- Exported unique district-to-code mapping as CSV

### ✅ Task 3 — Data Quality Checks
- Compared district-level vs state-level aggregations
- Found **1 discrepancy** in Andhra Pradesh (Amount field)
- Root cause: 1 missing `Amount (INR)` value causing ₹672 Billion difference

### ✅ Task 4 — Data Merging & Advanced Analysis
- Merged State and Demographics datasets for population ratio analysis
- Correlated population density with transaction volume
- Calculated average transaction amount per registered user
- Analyzed device brand usage ratios across all states

### ✅ Task 5 — Data Visualization
- Line plots for transaction and amount trends over time
- Pie charts for transaction type distribution by quarter
- Bar charts for population density across districts

### ✅ Task 6 — Insights & Conclusions
- Identified macro trends in India's digital payment growth
- Correlated demographic indicators with payment behavior
- Developed actionable recommendations for business growth

---

## 🔑 Key Insights

### 📈 Transaction Trends
| Metric | Finding |
|---|---|
| Overall Growth | Consistent upward trend from Q1 2018 to Q2 2021 |
| Peak Periods | Q4 quarters show spikes due to festive season (Diwali) |
| COVID Impact | Slight dip in Q1-Q2 2020, strong recovery by Q3-Q4 2020 |
| Growth Rate | Significantly accelerated post-2019 |

### 🏆 Top & Bottom States by Transaction Volume
| Rank | Top States | Bottom States |
|---|---|---|
| 1 | Karnataka — 2.98 Billion | Lakshadweep — 71,610 |
| 2 | Maharashtra — 2.83 Billion | Andaman & Nicobar — 1.2 Million |
| 3 | Telangana — 2.35 Billion | Ladakh — 1.88 Million |
| 4 | Andhra Pradesh — 1.78 Billion | Mizoram — 2.16 Million |
| 5 | Rajasthan — 1.38 Billion | Meghalaya — 5.64 Million |

### 💳 Transaction Types
| Finding | Detail |
|---|---|
| Most Dominant | **Peer-to-peer (P2P) payments** across almost all states |
| Second Most Common | **Recharge & Bill Payments** |
| Least Common | **Financial Services** |
| Interesting Pattern | Smaller UTs like Andaman occasionally prefer Recharge over P2P |

### 📱 Device Usage
| Finding | Detail |
|---|---|
| Top Brands | **Xiaomi & Samsung** dominate across all states |
| Premium Segment | **Apple** has very low share — budget Android leads |
| Emerging Brands | **Realme & Vivo** growing rapidly in market share |
| Insight | PhonePe's user base is primarily budget Android users |

### 👥 Demographics & Transactions
| Metric | Correlation | Interpretation |
|---|---|---|
| Population vs Transactions | Strong Positive | Bigger population = more transactions |
| Density vs Transactions | Moderate Positive | Urban areas transact more |
| Population vs Amount | Strong Positive | More people = higher total amount |
| Density vs Amount | Moderate Positive | Dense areas have higher spend |

### 🏙️ Most Populous Districts per State
| State | Most Populous District |
|---|---|
| Uttar Pradesh | Allahabad |
| Maharashtra | Pune |
| West Bengal | North 24 Parganas |
| Tamil Nadu | Chennai |

### ⚠️ Data Quality Findings
| Issue | Detail |
|---|---|
| Missing Amount | 1 missing value in Andhra Pradesh |
| Missing District Codes | 28 districts have no code assigned |
| Amount Discrepancy | ₹672 Billion gap in Andhra Pradesh between state and district aggregation |

---

## 💡 Recommendations

### 1. 🎯 Target Low-Adoption Regions
Focus marketing and incentive programs on Lakshadweep, Mizoram, Meghalaya and other northeastern states to drive digital payment adoption in underserved areas.

### 2. 📱 Optimize for Budget Android
Since Xiaomi and Samsung dominate the user base, prioritize app performance optimization for mid-range Android devices to improve user experience.

### 3. 🏪 Boost Merchant Payments
Peer-to-peer payments dominate but Merchant Payments remain underutilized. Launch merchant onboarding campaigns especially in Tier 2 and Tier 3 cities.

### 4. 🏙️ Urban Premium Services
High-density urban districts show higher transaction volumes and amounts. Target these areas for premium financial services like investments and insurance.

### 5. 📊 Fix Data Integrity Issues
Address the 28 missing district codes and the missing Amount value in Andhra Pradesh to ensure accurate reporting and decision-making.

### 6. 🎉 Leverage Festive Seasons
Q4 consistently shows transaction spikes. Plan targeted cashback campaigns and promotions around Diwali and year-end to maximize transaction volumes.

### 7. 💼 Financial Services Push
Financial Services is the least used transaction type. Introduce incentives for mutual funds, insurance, and gold investments through the PhonePe platform.

## ▶️ How to Run

1. **Clone the repository**
```bash
git clone https://github.com/ShaileshKhosare/PhonePe-Digital-Payments-Case-Study.git
cd PhonePe-Digital-Payments-Case-Study
```

2. **Install required libraries**
```bash
pip install pandas matplotlib openpyxl jupyter
```

3. **Launch Jupyter Notebook**
```bash
jupyter notebook
```

4. **Open the notebook**
PhonePe_Digital_Payments_Analysis.ipynb

5. **Update the file path** in Cell 1 to point to the Excel file on your system:
```python
FILE = r"C:\Your\Path\phonepe-pulse_raw-data_...xlsx"
```

6. **Run All Cells** → Kernel → Restart & Run All

---

## 👤 Author

<div align="center">

**Shailesh Khosare**

[![GitHub](https://img.shields.io/badge/GitHub-ShaileshKhosare-181717?style=for-the-badge&logo=github)](https://github.com/ShaileshKhosare)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Shailesh%20Khosare-0077B5?style=for-the-badge&logo=linkedin)](https://linkedin.com/in/ShaileshKhosare)

*If you found this analysis helpful, please ⭐ star the repository!*

</div>

---

<div align="center">
Made with ❤️ using Python & Pandas | © 2026 Shailesh Khosare
</div>
