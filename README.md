# Project: Investigate SuperStore Dataset

## Table of Contents
- [Introduction](#intro)
- [Data Inspection](#inspection)
- [Data Wrangling](#wrangling)
- [Exploratory Data Analysis](#exploratory)
- [Data Visualizations](#viz)
- [Conclusions](#conclusions)
- [Recommendations](#recommendations)

---

<a id="intro"></a>
## Introduction

### SuperStore Analysis Report

#### 1. Dataset Introduction
In this report, we analyze a comprehensive SuperStore sales dataset to understand the key factors influencing business performance, profitability, and customer purchasing behavior. The dataset records various transactional details, including customer segments, product categories, geographic locations (cities and states), discount levels, shipping modes, and financial metrics such as sales and profits. The primary goal is to uncover data-driven patterns and actionable insights that help stakeholders optimize discount strategies, improve regional profitability, and maximize overall revenue.

#### 2. Dependent and Independent Variables
To drive our analysis, the report is structured around core dependent and independent variables:
* **Dependent Variables:** 
  * `Sales` (Total revenue generated per transaction).
  * `Profit / Profit Margin` (Net financial gain or loss).
  * `Order Volume / Frequency` (Number of orders placed).
* **Independent Variables:**
  * `Segment` (Customer categories: Consumer, Corporate, Home Office).
  * `Discount` (Percentage of discount applied to orders).
  * `Category / Sub-Category` (Product classifications).
  * `State / City / Region` (Geographic locations of customers).
  * `Shipping Duration` (Time elapsed between order and ship dates).

#### 3. Research Questions
Throughout this report, we aim to answer the following analytical questions based on our data exploration and visualizations:
1. Which customer segment (Consumer, Corporate, Home Office) contributes the highest profit margin and total revenue?
2. Who are the top 10 high-value customers based on total sales & frequency of orders?
3. Which top 10 states generate the lowest or negative total profits?
4. Is there a relationship between shipping duration and the total number of orders or sales volume?
5. What are the monthly and yearly trendlines for total sales and profits?
6. How is total sales distributed across different product categories?
7. What is the total order volume and Sales contribution per city?
8. How do different discount levels impact profit margins across various product sub-categories?

---

<a id="inspection"></a>
## 1. Data Inspection
* **Libraries Imported:** Pandas, NumPy, Matplotlib, Seaborn.
* **Dataset Loading:** Loaded from `..\RawData\Superstore.xls` using `pd.read_excel`.
* **Data Overview:** The dataset contains **9,994 rows** and **21 columns** covering transactional information, geographic data, and financial indicators.
* **Missing Values:** Identified minor missing values in the `Postal Code` column (9,983 non-null out of 9,994).
* **Statistical Summary:** 
  * `Sales` average is around $229.86 with a maximum of $22,638.48, indicating potential high-value outliers.
  * `Profit` ranges from a minimum of -$6,599.98 to a maximum of $8,399.98, pointing towards loss-making transactions (often heavily discounted items).

---

<a id="wrangling"></a>
## 2. Data Wrangling
* **Data Types Optimization:** Identified opportunities to optimize memory usage by converting low-cardinality columns (`Ship Mode`, `Segment`, `Country/Region`, `State`, `Region`, `Category`, `Sub-Category`) to `category` data type and `Postal Code` to `str`.
* **Handling Missing Data:** Addressed missing postal codes and ensured date columns (`Order Date`, `Ship Date`) are properly parsed as datetime objects.

---

<a id="exploratory"></a>
## 3. Exploratory Data Analysis
* Examined distributions and unique counts across features (e.g., 793 unique customers, 531 cities, 1,862 product IDs).
* Investigated extreme values in sales and negative profits to understand the underlying causes (such as high discount rates applied to specific sub-categories like Tables and Binders).

---

<a id="viz"></a>
## 4. Data Visualizations
* Generated plots to analyze trends over time (monthly/yearly sales and profit trajectories).
* Visualized regional and state-level performance to pinpoint loss-making areas.
* Explored the correlation between discount levels and profitability across product categories.

*(ملاحظة: يمكنك إضافة صورك هنا بهذا الشكل لاحقاً)*
```markdown
![Sales Trend](images/sales_trend.png)
