# 📊 Financial Statements of Major Companies (2009–2023) Dashboard

## 📌 Project Overview

Proyek ini menganalisis data historis laporan keuangan dari **12 perusahaan** selama periode **2009–2023**, yang terdiri dari **161 records**, serta membangun dashboard keuangan interaktif menggunakan **Microsoft Excel**.

Analisis berfokus pada beberapa indikator keuangan utama, termasuk **Revenue, Gross Profit, Net Income, dan Net Profit Margin**. Dashboard digunakan untuk mengeksplorasi kinerja perusahaan, membandingkan kategori industri, serta melihat perubahan Revenue dan Net Income dari waktu ke waktu.

---

## 🗂️ Dataset

- **Dataset:** Financial Statements of Major Companies (2009–2023)
- **Source:** Kaggle
- **Publisher:** Rishabh Patil
- **Period:** 2009–2023
- **Records:** 161
- **Companies:** 12

📎 **Dataset Source:**  
[Financial Statements of Major Companies (2009–2023) – Kaggle](https://www.kaggle.com/datasets/rish59/financial-statements-of-major-companies2009-2023/data)

---

## 🛠️ Data Preparation & Analysis

The following steps were performed during this project:

### Data Preparation

- Parsed raw CSV data using **Text to Columns**
- Reviewed blank and missing values
- Applied median imputation where required
- Verified data types and measurement units
- Applied custom number formatting for financial values

### Analysis & Excel Features

- Created supporting financial metrics, including **COGS, OPEX/Other Expenses, and Net Profit Margin**
- Built supporting **PivotTables**
- Created interactive **Slicers** for Year, Company, and Category
- Developed KPI summaries
- Built a **Waterfall Chart** to visualize the profit breakdown
- Created company and industry performance comparisons
- Analyzed Revenue and Net Income trends from 2009 to 2023

---

# 📈 Dashboard Highlights & Key Insights

## 1️⃣ Profit Breakdown

The Profit Bridge Waterfall Chart visualizes the relationship between:

**Revenue → COGS → Gross Profit → OPEX/Other Expenses → Net Income**

### 🔍 Key Insight

Based on the aggregated data:

- **Total Revenue:** $12,213,879
- **COGS:** $6,195,141 (50.7%)
- **OPEX/Other Expenses:** $4,042,204 (33.1%)
- **Total Net Income:** $1,976,534
- **Net Profit Margin:** 13.7%

The visualization provides a summary of how the financial components are represented within the aggregated dataset.

---

## 2️⃣ Company & Industry Performance

The dashboard compares **Revenue and Net Income** across companies and industry categories.

### 🔍 Key Insight

Based on the available dataset:

- The **IT category** recorded the highest aggregated Revenue at **$6,189,902**
- The IT category also recorded the highest aggregated Net Income at **$1,514,327**
- **Apple (AAPL)** recorded the highest aggregated Revenue at **$2,965,609**
- Apple also recorded the highest aggregated Net Income at **$680,563**

Some companies in the dataset recorded negative aggregated Net Income during the analysis period, including:

- **PCG:** -$3,985
- **SHLDQ:** -$10,429

> **Note:** These findings are based on the companies and historical records available in the dataset and should not be interpreted as a representation of the current financial condition of the companies or industries.

---

## 3️⃣ Multi-Year Financial Trend (2009–2023)

A Combo Chart was used to compare changes in **Revenue and Net Income** over the available historical period.

### 🔍 Key Insight

Based on the data:

- The highest **Net Income** was recorded in **2021** at **$319,285**
- The highest **Revenue** was recorded in **2022** at **$1,639,071**

The results show that Revenue and Net Income did not reach their highest values in the same year.

---

# 🖼️ Dashboard Preview

![Financial Statements Analysis Dashboard Preview](Financial%20Dashboard%20Image.jpeg)

📄 **[View Full Dashboard in High-Resolution PDF](./Financial%20Dashboard%20PDF.pdf)**

---

# 📁 Workbook Structure

The Excel workbook is organized into the following sheets:

| Sheet | Description |
|---|---|
| **Financial Data** | Raw financial dataset used for the analysis |
| **Data Cleaning** | Data preparation, cleaning, and formatting process |
| **Staging KPI** | Supporting PivotTables and calculations used for the dashboard |
| **Dashboard** | Final interactive dashboard containing KPIs, charts, and slicers |

### 📄 Main File

`Financial_Statements_Analysis_Dashboard.xlsx`

---

# 🧰 Tools & Skills Demonstrated

**Tool:** Microsoft Excel

**Skills & Techniques:**

- Data Cleaning
- Missing Value Handling
- Data Preparation
- Data Transformation
- Financial Metric Calculation
- PivotTables
- PivotCharts
- Interactive Slicers
- Data Visualization
- Waterfall Charts
- Trend Analysis
- Dashboard Development

---

# 🎯 Project Takeaways

Through this project, I practiced transforming raw financial data into a structured analysis and interactive dashboard using Microsoft Excel.

This project helped me strengthen my understanding of:

**Raw Data → Data Preparation → Analysis → Visualization → Dashboard Development**

---

# 👤 Author

**Alena Mansika**

- 💻 **GitHub:** [@alenamansika](https://github.com/alenamansika)
- 💼 **LinkedIn:** [Alena Mansika](https://www.linkedin.com/in/alenamansika)
