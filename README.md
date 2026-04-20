# 📊 Sales Data Analysis Project

## 👤 About the Project

This project analyzes historical sales data to uncover business insights, identify trends, and support data-driven decision making.

The analysis focuses on:

* Sales performance over time
* Product line effectiveness
* Country-level demand
* Order status patterns

---

## 🛠️ Tech Stack

* 🐍 Python
* 📦 Pandas
* 📊 Matplotlib
* 📈 Jupyter Notebook



---

## 📊 Key Business Insights

* 🇺🇸 USA has the highest number of orders, indicating a strong primary market
* 🚗 Classic Cars is the top-performing product line
* 📅 Sales peaked around 2004, followed by fluctuations
* ⚠️ Cancelled orders suggest potential operational or customer issues
* 🌍 Some countries show low engagement → opportunity for expansion

---

## 📈 Example Analysis Performed

* Grouped sales by year and country
* Identified top 5 countries by order volume
* Analyzed product line performance
* Explored distribution of sales using histograms

---

## 📌 Key Skills Demonstrated

* Data Cleaning & Preprocessing
* Exploratory Data Analysis (EDA)
* Business Insight Generation
* Data Visualization
* Analytical Thinking

---

## 📎 Detailed Insights

# Sales Data Analysis — Business Insights Report

**Dataset:** `sales_data_sample.csv` | **Period:** 2003–2005

---

## 1. Dataset Overview — Basic Statistics

| **Metric** | **Value** |
|---|---|
| **Total rows** | 2,823 |
| **Number of columns** | 25 |
| **Time range** | 2003-01-06 — 2005-05-31 |
| **Number of countries** | 19 |
| **Product lines** | 7 (Classic Cars, Vintage Cars, Motorcycles, Planes, Trucks, Ships, Trains) |
| **SALES — Min** | $482.13 |
| **SALES — Max** | $14,082.80 |
| **SALES — Mean** | $3,553.89 |
| **SALES — Median** | $3,184.80 |
| **Q1 / Q3 / IQR** | $2,203 / $4,508 / $2,304 |
| **Duplicate rows** | 0 |
| **ORDERDATE type** | object → datetime64 (converted) |
| **Missing Values** | ADDRESSLINE2 (71%), STATE (29%), TERRITORY (38%), POSTALCODE (3%) — filled with "Unknown" |

> **Note:** The 2005 data covers only January–May (5 months). Care should be taken when making year-over-year comparisons.

---

## 2. Status, Year, and Product Analysis

| **STATUS** | **2003** | **2004** | **2005** |
|---|---|---|---|
| **Shipped** | 976 | 1,287 | 354 |
| **Cancelled** | 16 | 44 | -- |
| **Resolved** | 8 | 8 | 31 |
| **On Hold** | -- | 6 | 38 |
| **In Process** | -- | -- | 41 |
| **Disputed** | -- | -- | 14 |

---

## 3. Revenue by Country — Top 5

| **#** | **Country** | **Order Count** | **Revenue ($)** | **Revenue Share (%)** |
|---|---|---|---|---|
| **1** | USA | 1,004 | 3,627,982.83 | 36.6% |
| **2** | Spain | 342 | 1,215,686.92 | 12.3% |
| **3** | France | 314 | 1,110,916.52 | 11.2% |
| **4** | Australia | 185 | 630,623.10 | 6.4% |
| **5** | UK | 144 | 478,880.46 | 4.8% |

- **Total revenue (all countries):** $10,032,628.85
- **TOP 5 countries' share:** ~70.3%

---

## 4. Average Order Value (AOV) by Country

| **Country** | **Order Count** | **AOV ($)** | **Rank** |
|---|---|---|---|
| Denmark | 63 | **3,899.00** | 1 (1st) |
| Switzerland | 31 | **3,797.21** | 2 |
| Sweden | 57 | **3,684.46** | 3 |
| Austria | 55 | **3,673.86** | 4 |
| USA | 1,004 | **3,613.53** | 9 |
| Canada | 70 | **3,201.12** | 19 (lowest) |

---

## 5. Business Insights

### [1] INSIGHT #1: USA Is the Dominant Market Leader

**Finding:** The USA leads in both metrics with 1,004 orders (35.5% of total) and $3,627,982.83 in revenue (36.6% of total). The gap between the USA and Spain in second place is nearly 3x.

**Recommendation:** Strengthen existing channel partnerships in the US market. Implement customer retention programs. Explore differential pricing strategies to drive growth in other markets.

---

### [2] INSIGHT #2: Denmark Leads in AOV — Small but High-Value Market

**Finding:** Denmark ranks 11th in order count with only 63 orders, yet leads in AOV ($3,899). This means each Danish customer spends more than customers in any other market.

**Recommendation:** Develop premium customer programs for Denmark, Switzerland, Sweden, and Austria. Assign dedicated account managers to these markets.

---

### [3] INSIGHT #3: No Cancelled Orders in 2005

**Finding:** There were 16 cancelled orders in 2003 and 44 in 2004. However, in 2005 (covering 5 months), there are zero Cancelled orders. This may be a positive operational signal.

**Recommendation:** Investigate the reason behind the reduction in cancellations in 2005. If this trend has been sustained since the end of 2004, it is likely the result of a successful operational change.

---

### [4] INSIGHT #4: Disputed and In Process Orders Appear Only in 2005

**Finding:** All orders with Disputed (14) and In Process (41) statuses were recorded only in 2005. Since the data covers the period up to May 31, these orders may still be open.

**Recommendation:** Check the current status of the 41 "In Process" orders — a large portion may still be convertible into revenue. Contact customers for "Disputed" orders and expedite resolution.

---

### [5] INSIGHT #5: Shipped Orders Dominate — On Hold Has Increased in 2005

**Finding:** 92.6% of all orders have a Shipped status. However, On Hold orders grew from 6 in 2004 to 38 in 2005 — this increase warrants attention.

**Recommendation:** Investigate the reason for the On Hold increase (credit limit, inventory, customer request?). Identify which countries and product lines are most affected.

---

### [6] INSIGHT #6: Sales Distribution Is Not Normal — Right-Skewed

**Finding:** The SALES histogram shows a right-skewed distribution: the mean ($3,553) is higher than the median ($3,184). Q1=$2,203, Q3=$4,508, IQR=$2,304. Orders above $10,000 (16 in total) are pulling the average upward.

**Recommendation:** Base segment analyses on the median. Track outlier orders ($10K+) in a separate VIP category. Apply differentiated strategies across Small/Medium/Large deal size categories.

---

### [7] INSIGHT #7: Classic Cars Holds a Dominant Position

**Finding:** Classic Cars is the top-selling product line with 967 orders (34.3%). Second: Vintage Cars (607, 21.5%), third: Motorcycles (331, 11.7%). Lowest: Trains (77, 2.7%).

**Recommendation:** Strengthen inventory management for Classic Cars. Apply bundling or upsell strategies for underperforming lines (Trains, Ships).

---

### [8] INSIGHT #8: EMEA Is the Primary Territory — US Territory Data Is Unclear

**Finding:** By territory: EMEA (1,407), APAC (221), Japan (121). The territory for the USA's 1,004 orders is marked as "Unknown", and the same applies to Canada's 70 orders.

**Recommendation:** Complete the territory labeling for US and Canadian orders. This data is essential for sales managers to set more precise regional targets.

---

## 6. Annual Revenue Comparison (Note: 2005 Is Incomplete)

| **Metric** | **2003 (full year)** | **2004 (full year)** | **2005 (5 months)** |
|---|---|---|---|
| **Order count** | 1,000 | 1,345 | 478 |
| **Total revenue ($)** | 3,516,979.54 | 4,724,162.60 | 1,791,486.71 * |
| **Top orders** | USA (976 Shipped) | USA (1,287 Shipped) | USA (354 Shipped) |

> \* The 2005 revenue covers only a 5-month period. **Comparisons with previous years may be misleading.** For this reason, the dataset will be re-analyzed by splitting it into 6-month periods.

## 📝 License

This project is licensed under the MIT License.

---

## 💡 Final Note

This project is part of my journey in becoming a Data Analyst.
Feedback and suggestions are welcome.
