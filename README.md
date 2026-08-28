[README_Sales_Performance_Dashboard.md](https://github.com/user-attachments/files/31537011/README_Sales_Performance_Dashboard.md)
# Sales Performance Dashboard

## About the Project

This project builds an executive-style **Sales Performance Dashboard** using Python, Pandas, NumPy, and Matplotlib.

The dashboard transforms order-level sales data into a management view of:

- total revenue,
- total profit,
- profit margin,
- units sold,
- monthly trends,
- regional performance,
- category revenue and profit,
- and top / bottom products.

The project goes beyond simply showing where sales are highest.

It asks a more important management question:

> **Is the revenue being generated profitably?**

---

## Dashboard Preview

![Sales Performance Dashboard](sales_performance_dashboard.png)

---

## Executive Summary

The dataset contains **200 sales records** covering **2023-01-01 through 2023-07-19**.

| KPI | Result |
|---|---:|
| Revenue | **$1,074,116** |
| Profit | **$93,264** |
| Profit Margin | **8.7%** |
| Units Sold | **18,153** |

The business generated more than **$1.07M in revenue**, but the overall margin was only **8.7%**.

That means sales volume is meaningful, but profitability is uneven.

---

## Key Business Insights

### 1. East Leads Revenue, but West Sold More Units

The **East region** generated approximately **$313,513** in revenue.

The **West region sold 4,865 units**, slightly more units than East.

This suggests differences in selling price, discounting, or product mix across regions.

---

### 2. South Is Generating Sales but Destroying Profit

South generated:

- **$194,632 revenue**
- **$-16,219 profit**
- **-8.3% margin**

This is more important than simply ranking South last in revenue.

Management should investigate:

- discounting,
- product mix,
- COGS,
- pricing,
- and loss-making products sold in the region.

---

### 3. Sports Is the Strongest Category

Sports generated:

- **$292,087 revenue**
- **$113,045 profit**
- **38.7% profit margin**

Sports is therefore both the top revenue category and the strongest profit contributor.

---

### 4. Several High-Revenue Categories Are Loss-Making

The data shows that:

- Home Appliances is loss-making
- Furniture is loss-making
- Clothing is loss-making
- Electronics is only modestly profitable

This demonstrates why revenue alone is not enough to judge category health.

---

### 5. April Had the Highest Revenue—but Lost Money

April generated the highest monthly revenue:

**$199,424**

Yet April profit was:

**$-5,567**

This is one of the strongest findings in the project.

> **High revenue does not automatically mean strong financial performance.**

Possible causes worth investigating include discounting, COGS, product mix, and regional mix.

---

### 6. June Was the Largest Profitability Warning

June generated:

- **$135,511 revenue**
- **$-27,851 profit**
- **-20.6% margin**

June therefore deserves deeper investigation.

---

### 7. July's Revenue Dip Needs Context

The dashboard shows July revenue of approximately:

**$76,685**

However, the dataset ends on **2023-07-19**.

July is therefore a **partial month** and should not be interpreted as a confirmed month-over-month collapse without adjusting for missing days.

A dashboard can be mathematically correct and still create a misleading business interpretation if time coverage is ignored.

---

### 8. Product_66 Is the Revenue Leader

The highest-revenue product is:

**Product_66 — $20,948**

The lowest-revenue product is:

**Product_118 — $56**

Product revenue should also be reviewed alongside product profit.

---

## Business Questions Answered

The dashboard helps answer:

- What is total revenue?
- What is total profit?
- What is the profit margin?
- How many units were sold?
- Which region leads revenue?
- Which category leads revenue?
- Which category contributes the most profit?
- What month had the highest revenue?
- Which months generated losses?
- Which products generate the highest and lowest revenue?
- Where is revenue failing to translate into profit?

---

## My Role

For this project, I completed the full sales-analysis workflow, including:

- loading the dataset,
- reviewing data quality,
- cleaning duplicates and dates,
- calculating KPIs,
- aggregating monthly performance,
- analyzing regional performance,
- comparing category revenue and profit,
- ranking products,
- identifying profitability risks,
- generating dashboard visuals,
- and developing executive business insights.

---

## Key Skills & Tools

### Programming

- Python
- Pandas
- NumPy
- Jupyter Notebook

### Visualization

- Matplotlib
- GridSpec
- KPI Cards
- Line Charts
- Bar Charts
- Horizontal Bar Charts
- Dashboard Layout Design

### Business Analytics

- Sales Analytics
- Revenue Analysis
- Profitability Analysis
- Profit Margin
- Regional Performance
- Product Performance
- Category Performance
- Executive KPI Reporting

---

## Dataset Overview

The dataset contains **14 columns**:

- Order ID
- Order Date
- Region
- Channel
- Product Category
- Product
- Units Sold
- Unit Price
- Discount Percentage
- COGS
- Customer Segment
- Revenue
- Profit
- Month

The uploaded dataset has **200 rows**, with no missing values and no exact duplicate records.

---

## Methodology

### 1. Data Loading

The source CSV is loaded with Pandas.

### 2. Data Quality Review

The notebook checks:

- row and column count,
- duplicate rows,
- missing values,
- and invalid dates.

### 3. Date Preparation

`order_date` is converted to datetime and a `YYYY-MM` month field is created.

### 4. Optional Region Filter

The notebook can analyze all regions or one region at a time.

### 5. KPI Calculation

The dashboard calculates:

- Revenue
- Profit
- Profit Margin
- Units Sold

### 6. Monthly Analysis

Revenue and profit are summarized by month.

### 7. Regional Analysis

Revenue, profit, units sold, and margin are calculated by region.

### 8. Category Analysis

Revenue and profit are compared across product categories.

### 9. Product Ranking

Products are ranked by revenue.

### 10. Profitability Diagnostics

The improved notebook also identifies:

- loss-making regions,
- loss-making categories,
- most profitable products,
- and largest product losses.

---

## Repository Structure

```text
sales-performance-dashboard/
│
├── Sales_Performance_Dashboard_GitHub.ipynb
│   └── Complete step-by-step analysis
│
├── sales_performance_dashboard.png
│   └── Dashboard preview
│
├── data/
│   └── sales_data.csv
│
├── sales_dashboard_outputs/
│   ├── monthly_performance.csv
│   ├── regional_performance.csv
│   ├── category_performance.csv
│   ├── product_performance.csv
│   └── sales_performance_dashboard.png
│
└── README.md
```

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/sales-performance-dashboard.git
cd sales-performance-dashboard
```

### 2. Install Required Packages

```bash
pip install pandas numpy matplotlib jupyter
```

### 3. Add the Dataset

Place the sales CSV in the project root or `data/` folder.

### 4. Start Jupyter

```bash
jupyter notebook
```

### 5. Open

```text
Sales_Performance_Dashboard_GitHub.ipynb
```

Run the cells from top to bottom.

---

## Limitations

### Partial July Data

The dataset ends on **2023-07-19**, so July is incomplete.

### Revenue and Profit Are Source Measures

The dashboard uses the provided `revenue` and `profit` fields as the authoritative business metrics.

### Small Dataset

The analysis contains only 200 orders.

A production dashboard would normally use a longer history and larger transaction base.

### Static Dashboard

The Matplotlib dashboard is static.

A future Power BI, Tableau, Streamlit, or Plotly version could add interactive filtering and drill-down.

---

## Future Improvements

Potential extensions include:

- monthly profit trend,
- profit margin by region,
- channel performance,
- customer-segment performance,
- discount vs. profit analysis,
- product profitability matrix,
- average selling price,
- month-over-month growth,
- target-vs.-actual performance,
- sales forecasting,
- and an interactive Power BI dashboard.

---

## Conclusion

This project demonstrates how a sales dashboard can move beyond topline reporting.

The business generated **$1,074,116 in revenue**, but deeper analysis reveals important profitability risks:

- South is loss-making.
- Several categories are loss-making.
- April produced record revenue but negative profit.
- June generated a significant loss.
- July is a partial month and requires cautious interpretation.

The strongest dashboard question is not simply:

**Where are sales highest?**

It is:

> **Which sales are creating sustainable profit, and which sales are creating hidden financial risk?**
