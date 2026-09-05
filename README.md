# Investigate SuperStore Dataset

A data analysis project built using **Python (Jupyter Notebook)** and core data science libraries (**Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**) to investigate sales performance, profitability, and customer behavior.

---

## Project Overview
* **Goal:** Uncover data-driven insights to optimize business strategies, reduce financial losses, and maximize profitability.
* **Key Focus Areas:** Identifying top customer segments, analyzing geographic performance, and evaluating the direct impact of discount rates on product profitability.

---

## Workflow & Steps

### 1. Data Inspection
* Loaded and inspected the transactional dataset (consisting of **9,994 rows** and **21 columns**) from `RawData/Superstore.xls`.
* Checked for missing values (noted minor missing entries in the `Postal Code` column) and analyzed statistical distributions.
* Discovered extreme outliers in sales (up to ~$22,638) and significant negative profits (losses down to -$6,599), indicating underlying pricing or discounting issues.

### 2. Data Wrangling
* **Memory Optimization:** Converted low-cardinality string columns (`Segment`, `Region`, `Category`, `Sub-Category`, `Ship Mode`) to categorical data types to improve notebook performance.
* **Data Cleaning:** Handled missing postal codes and properly parsed datetime objects for `Order Date` and `Ship Date` to enable time-series analysis.

### 3. Exploratory Data Analysis (EDA)
* Analyzed patterns across **793 unique customers** and multiple product categories (`Furniture`, `Office Supplies`, `Technology`).
* Investigated loss-making transactions to isolate root causes, revealing that heavy discounts applied to specific sub-categories (such as *Tables* and *Binders*) were wiping out profit margins.

### 4. Data Visualizations & Insights
* Generated plots to track sales and profit trajectories over time, regional performances, and the correlation between discount levels and profitability.

*(ملاحظة: يمكنك إضافة صور الجرافات والداشبورد هنا)*
```markdown
![Sales Trend](images/sales_trend.png)
![Profit by Region](images/profit_by_region.png)
