# Sales Analysis Dashboard | Microsoft Power BI

An interactive retail sales analytics dashboard built in Microsoft Power BI to track revenue KPIs, analyze customer segments, and evaluate multi-channel sales performance across 300,000+ transaction records.

---

## Project Overview

In retail sales, large volumes of transactional data often obscure high-level trends, customer behavior, and operational bottlenecks. The objective of this project was to transform raw, multi-attribute retail data into a dynamic, decision-ready analytics dashboard.

By cleaning, modeling, and structuring over 300,000 records, I built an interactive executive dashboard in Microsoft Power BI that allows business stakeholders to monitor financial KPIs, examine monthly revenue trends, evaluate product category and brand performance, and inspect customer purchasing patterns across geographic regions.

---

## Dataset

- **Total Records:** 302,010 rows
- **Total Attributes:** 30 columns
- **Key Fields:**
  - **Transaction & Customer:** `Transaction_ID`, `Customer_ID`, `Name`, `Email`, `Phone`, `Address`, `City`, `State`, `Zipcode`, `Country`, `Age`, `Gender`, `Income`, `Customer_Segment`
  - **Order Details:** `Date`, `Year`, `Month`, `Time`, `Shipping_Method`, `Payment_Method`, `Order_Status`
  - **Product & Financials:** `Product_Category`, `Product_Brand`, `Product_Type`, `products`, `Total_Purchases`, `Amount`, `Total_Amount`, `Ratings`, `Feedback`

---

## Tools & Skills Used

- **Microsoft Power BI**
  - **Data Modeling & DAX:** Created explicit measures (`Total Revenue`, `Avg Order Value`, `Total Orders`, `Avg Rating`), custom aggregations, and dynamic filter contexts.
  - **Power Query (ETL):** Data type normalization, standardization of missing entries, date/time dimension parsing, and schema preparation.
  - **Data Visualization & KPI Reporting:** Built an executive layout featuring KPI cards, Area-filled Line charts, Clustered Bar and Column charts, and Donut charts.
  - **UI/UX & Canvas Design:** Structured a widescreen canvas (1900 × 1100 px) with a modern dark-navy (`#1F2A44`) header banner and sidebar control panel for visual hierarchy.
  - **Interactivity & Cross-Filtering:** Configured multi-criteria slicers (`Country`, `Year`, `Gender`) and enabled bidirectional visual cross-filtering across all report components.

---

## Data Cleaning & Preparation Steps

1. **Handling Missing & Inconsistent Values:** Standardized blank or unrecorded entries across demographic and geographic attributes by categorizing them as `"Unknown"` to maintain complete reporting consistency without sacrificing transaction volume.
2. **Date & Time Formatting:** Parsed raw timestamp data into dedicated `Date`, `Year`, and `Month` fields to support chronological sorting and seasonal time-series analysis.
3. **Data Type Normalization:** Formatted financial fields (`Amount`, `Total_Amount`), quantities (`Total_Purchases`), and ratings into consistent numerical and currency data types to ensure accurate DAX aggregations.
4. **DAX Measure Engineering:** Engineered explicit measures to ensure scalable, dynamic calculation across any applied slicer selection:
   - `Total Revenue = SUM(Sales[Total_Amount])`
   - `Avg Order Value = AVERAGE(Sales[Total_Amount])`
   - `Total Orders = COUNTROWS(Sales)`
   - `Avg Rating = AVERAGE(Sales[Ratings])`
5. **Deduplication & Quality Control:** Audited all 302,010 records to eliminate duplicates, validate transactional integrity, and ensure clean categorical relationships before report development.

---

## Dashboard Preview

### Executive Sales Analysis Dashboard

![Sales Analysis Dashboard](./assets/dashboard_overview.png)

> *Place a screenshot of your Power BI dashboard in `./assets/dashboard_overview.png` to display the preview directly on GitHub.*

- **What It Shows:** An executive overview of retail sales performance consolidating high-level business metrics, temporal patterns, product categories, brand contributions, regional sales, payment preferences, and customer segments in a single interface.
- **KPIs Displayed:**
  - **Total Revenue:** $402.5M
  - **Total Orders:** 294,462
  - **Avg Rating:** 3.2 / 5.0
  - **Avg Order Value:** $1,367
- **Charts & Visualizations:**
  - **Monthly Revenue Trend (Line Chart):** Tracks monthly sales performance throughout the year with straight data labels and area shading, highlighting revenue peaks in April ($55.1M) and January ($49.6M).
  - **Revenue by Product Category (Clustered Bar Chart):** Compares total revenue across product lines: Electronics ($95.0M), Grocery ($89.0M), Clothing ($73.0M), Books ($72.7M), and Home Decor ($72.4M).
  - **Top 10 Revenue by Product Brand (Clustered Column Chart):** Identifies leading brands, led by Pepsi ($40.5M), Samsung ($24.8M), Sony ($24.5M), Nike ($24.4M), Zara ($24.4M), and Coca-Cola ($24.4M).
  - **Top 10 Revenue by State (Clustered Column Chart):** Displays top-performing regions, led by England (61,694), Berlin (51,451), New South Wales (43,959), and Ontario (43,946).
  - **Revenue by Customer Segment (Clustered Column Chart):** Evaluates revenue contribution across Regular (49%), New (30%), and Premium (21%) customer tiers.
  - **Order Status Analysis (Donut Chart):** Analyzes fulfillment progress: Delivered (43%), Shipped (22%), Processing (19%), and Pending (16%).
  - **Payment Method Analysis (Donut Chart):** Breaks down revenue share across payment methods: Credit Card (30%), Debit Card (26%), Cash (24%), and PayPal (20%).
- **Interactive Slicers & Filtering:**
  - Three interactive slicers in the dedicated dark-navy left sidebar allow filtering across all charts and KPI cards simultaneously:
    - **Country:** `Australia`, `Canada`, `Germany`, `UK`, `USA`, `Unknown`
    - **Year:** `2023`, `2024`, `Unknown`
    - **Gender:** `Female`, `Male`, `Unknown`
  - Dynamic cross-filtering enables selecting any data point (such as a brand, segment, or status slice) to instantly filter all other visuals across the dashboard.

---

## Key Insights

- **Top Product Category:** **Electronics** generated the highest total revenue at **$95.0M**, followed closely by **Grocery** at **$89.0M**.
- **Preferred Payment Method:** **Credit Card** is the most popular payment method, driving **30%** of total sales, followed by Debit Card (**26%**) and Cash (**24%**).
- **Leading Regional Markets:** **England** (61,694) and **Berlin** (51,451) generated the highest regional volume.
- **Primary Customer Segment:** **Regular** customers accounted for the largest revenue share at **49%**, followed by New (**30%**) and Premium (**21%**).
- **Fulfillment Performance:** **43%** of orders have been successfully delivered, with the rest distributed across shipped, processing, and pending stages.

---


