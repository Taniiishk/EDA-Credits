# 📊 Credit EDA Dashboard

## Exploratory Data Analysis on Credit Application Data (< 25MB)

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![Pandas](https://img.shields.io/badge/Pandas-DataAnalysis-red.svg)](https://pandas.pydata.org)
[![Seaborn](https://img.shields.io/badge/Seaborn-Statistics-brightgreen.svg)](https://seaborn.pydata.org)

</div>

---

## 📖 Project Overview

This repository contains **reduced-size** credit application data for EDA, with both files under 25MB. Perfect for quick analysis, prototyping, and learning without dealing with the full large datasets.

🎯 **Key Objectives:**
- Understand the structure and quality of credit dataset
- Analyze the distribution of the target variable (credit default risk)
- Identify key features that correlate with credit approval/denial
- Visualize relationships between applicant demographics and credit outcomes
- Provide insights for further modeling or business decision-making

---

## 📁 Project Structure

```text
EDA Credits/
├── 📄 application_data_reduced.csv    # 30,000 rows, 122 features (23.5MB) ✅ Under 25MB
├── 📄 previous_application_reduced.csv # 15,000 rows, 130 features (4.8MB) ✅ Under 25MB
├── 📓 EDA Credits.ipynb               # Jupyter Notebook with full analysis
```

---

## 🗂️ Dataset Description

### `application_data_reduced.csv`

| Metric | Value |
|--------|-------|
| **Rows** | 30,000 credit applications (reduced from 307,511) |
| **Features** | 122 columns (same as original) |
| **Target** | `TARGET` (1 = good credit, 0 = default) |
| **Size** | 23.5MB ✅ Under 25MB |

**Key Columns:** `SK_ID_CURR`, `TARGET`, `AMT_INCOME_TOTAL`, `AMT_CREDIT`, `AMT_ANNUITY`, `FLAG_OWN_CAR`, `FLAG_OWN_REALTY`, `CODE_GENDER`, `NAME_EDUCATION_TYPE`, `NAME_FAMILY_STATUS`, `EXT_SOURCE_1`, `EXT_SOURCE_2`, `EXT_SOURCE_3`

### `previous_application_reduced.csv`

| Metric | Value |
|--------|-------|
| **Rows** | 15,000 previous applications (reduced from ~395,000) |
| **Features** | 130 columns (key loan contract features) |
| **Size** | 4.8MB ✅ Under 25MB |

- Previous credit application records linked to main applications
- Contains loan amounts, contract types, decision data, and payment history
- Compressed size negligible compared to original 386MB

---

## 🔍 Analysis Performed (in EDA Credits.ipynb)

The notebook includes thorough EDA covering:

| Section | Description |
|---------|-------------|
| **📦 Imports** | pandas, numpy, matplotlib, seaborn |
| **📥 Data Loading** | Reading `application_data.csv` with pandas |
| **🔎 Data Inspection** | Shape, info, and first rows analysis |
| **📊 Univariate Analysis** | Distribution plots for key numerical features |
| **📈 Categorical Analysis** | Value counts and bar charts for categorical features |
| **🎯 Target Analysis** | TARGET variable distribution and class imbalance assessment |
| **🔗 Correlation Matrix** | Pearson/Spearman correlations between numerical features |
| **📌 Feature Insights** | Identifying top predictors of creditworthiness |
| **🎨 Visualizations** | Multiple charts and graphs for pattern discovery |

---

## ▶️ How to Run

All data files are now under 25MB for easy sharing and quick EDA.

### 📊 Data Files - Ready to Use

| File | Rows | Features | Size | ✅ |
|------|------|----------|------|-----|
| `application_data_reduced.csv` | 30,000 | 122 | 23.5MB | ✅ |
| `previous_application_reduced.csv` | 15,000 | 130 | 4.8MB | ✅ |

### 🛠️ No Extraction Needed!

These CSV files are ready-to-use immediately:

```bash
# Quick start with pandas
pip install pandas numpy matplotlib seaborn jupyter

# Launch the notebook
jupyter notebook EDA Credits.ipynb
# or
jupyter lab EDA Credits.ipynb
```

### 📊 Load the Reduced Data in Notebook

```python
import pandas as pd

# Load reduced application data (30K rows - already under 25MB!)
df = pd.read_csv('application_data_reduced.csv')

# Load reduced previous application data
prev = pd.read_csv('previous_application_reduced.csv')

print(f"Application data shape: {df.shape}")
print(f"Previous application shape: {prev.shape}")
```

### 🎯 What You Can Do with 30K rows

- ✅ Quick exploratory analysis in minutes
- ✅ Visualize feature distributions
- ✅ Check target variable balance
- ✅ Calculate correlations
- ✅ Build simple predictive models
- ✅ Perfect for learning and prototyping

### 📈 Comparison: Full vs Reduced

| Metric | Full Data | Reduced Data | Improvement |
|--------|-----------|--------------|-------------|
| **Application rows** | 307,511 | 30,000 | 90% smaller |
| **Application size** | 166MB | 23.5MB | 86% smaller |
| **Previous rows** | ~395,000 | 15,000 | 96% smaller |
| **Previous size** | 386MB | 4.8MB | 99% smaller |
| **Analysis time** | Hours | Minutes | Instant |

### 💡 Recommended Workflow

1. **Start with reduced data** - Get insights in minutes
2. **Validate findings** on a subset
3. **Use full data** only when needed for final modeling
4. **Share easily** - Under 25MB files work via email, git, etc.

---

## 💡 Key Insights (Preliminary)

Based on initial exploration:

- ⚖️ **Class Balance**: The TARGET variable shows noticeable imbalance between good and bad credit applicants
- 💸 **Skewed Distributions**: Income and credit amount features are right-skewed — log transformation recommended
- 🧩 **Missing Values**: Several features have significant missing data requiring imputation or removal
- 📊 **Categorical Patterns**: Certain demographics (employment type, housing situation) show distinct creditworthiness patterns
- 🔗 **Correlations**: Strong correlations observed between income, credit amount, and loan default risk

---

## 🛠️ Tech Stack

- **Language**: Python 3.9+
- **Data Analysis**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Environment**: Jupyter Notebook / JupyterLab
- **Data Format**: CSV files

---

## 📜 License

This project is for **educational and analytical purposes**. Based on open credit dataset for learning exploratory data analysis techniques.

---

<div align="center">

**Happy Analyzing!** 🚀

*Feel free to fork, explore, and enhance the analysis.*

</div>