# 📊 Monthly Performance Report - Power BI Report
![image](https://github.com/user-attachments/assets/ba8d8e08-d15c-493e-9cc2-89d3b1d41288)

## 🚀 Overview
This Power BI project presents a comprehensive **monthly performance report** for **Amazon Sponsored Ads**, using three categories of ad types:
- **Sponsored Product**
- **Sponsored Brand**
- **Sponsored Display**
The report helps stakeholders track and analyze key advertising KPIs like **Spend**, **Sales**, **Orders**, **CTR**, **CPC**, and **Conversion Rate** 
across various dimensions such as **Category**, **Ad Type**, **ASIN**, and **Time (Month/Year)**.

---
# 📂 Project Structure
## 🧾 Data Description

The dataset contains monthly performance metrics from **Jan 2024 and Feb 2024**, and ** Jan 2025 to March 2025** broken down by ASIN, Category, and Ad Type

### 🔑 Common Columns Used:
- `Date`
- `Category`
- `Ad Type`
- `ASIN`
- `Impressions`
- `Clicks`
- `Spend`
- `14 Day Total Sales ($)`
- `14 Day Total Orders (#)`

---

## 🛠️ Data Transformation (Power Query)

For each sheet (`Product`, `Brand`, `Display`), the following transformations were applied:
- Converted `Date` column to `Month-Year` format for trend analysis.
- Removed null or irrelevant rows (e.g., blank ASINs).
- Renamed columns for consistency and readability.
- Ensured numeric data types for all metric columns.
- Created a unified schema for all three ad types.

---
## 📈 Key Metrics and DAX Measures

| KPI                | DAX Formula |
|--------------------|-------------|
| **Total Spend**        | `Total Spend = SUM('TableName'[Spend])` |
| **Total Sales**        | `Total Sales = SUM('TableName'[14 Day Total Sales ($)])` |
| **Total Orders**       | `Total Orders = SUM('TableName'[14 Day Total Orders (#)])` |
| **CTR (%)**            | `CTR = DIVIDE(SUM('TableName'[Clicks]), SUM('TableName'[Impressions])) * 100` |
| **Avg CPC**            | `Avg CPC = DIVIDE(SUM('TableName'[Spend]), SUM('TableName'[Clicks]))` |
| **Conversion Rate (%)** | `Conversion Rate = DIVIDE(SUM('TableName'[14 Day Total Orders (#)]), SUM('TableName'[Clicks])) * 100` |

---
## 🖼️ Visualizations by Sheet
![image](https://github.com/user-attachments/assets/d831db55-3646-4154-9972-a2ad63e3ea7c)

### 📌 Sheet 1: Sponsored Product
**Slicers**: Month, Category, Ad Type  
**KPI Cards**: Total Spend, Total Sales, Total Orders, CTR (%), Avg CPC, Conversion Rate (%)  
**Charts**:
1. 📈 CTR and Conversion Rate Trend (Line and Clustered Chart - Month vs. CTR & Conversion Rate)
2. 📈 Sales and Spend Trend (Line and Clustered Chart)
3. 📊 Top 10 ASINs by Sales (Bar Chart)
4. 📉 Sales and Spend by Category (Clustered Column Chart)
5. 🎯 Overall Spend by Ad type (Donut chart)

![image](https://github.com/user-attachments/assets/11f57a7c-c8a4-4f17-b21a-c90c37c5a8f5)

### 📌 Sheet 2: Sponsored Brands
**Slicers**: Month, Category, Ad Type  
**KPI Cards**: Total Spend, Total Sales, Total Orders, CTR (%), Avg CPC, Conversion Rate (%)  
**Charts**:
1. 📈 CTR and Conversion Rate Trend (Line and Clustered Chart - Month vs. CTR & Conversion Rate)
2. 📈 Sales and Spend Trend (Line and Clustered Chart)
3. 📊 Top 10 ASINs by Sales (Bar Chart)
4. 📉 Sales and Spend by Category (Clustered Column Chart)
5. 🎯 Overall Spend by Ad type (Donut chart)

![image](https://github.com/user-attachments/assets/56ac696f-b44c-4b61-b412-d673d4ec16a0)

### 📌 Sheet 3: Sponsored Display
**Slicers**: Month, Category, Ad Type  
**KPI Cards**: Total Spend, Total Sales, Total Orders, CTR (%), Avg CPC, Conversion Rate (%)  
**Charts**:
1. 📈 CTR and Conversion Rate Trend (Line and Clustered Chart - Month vs. CTR & Conversion Rate)
2. 📈 Sales and Spend Trend (Line and Clustered Chart)
3. 📊 Top 10 ASINs by Sales (Bar Chart)
4. 📉 Sales and Spend by Category (Clustered Column Chart)
5. 🎯 Overall Spend by Ad type (Donut chart)

## 🔍 Filters and Slicers Used
- `Date (Month-Year)`
- `Ad Type`
- `Category`
- `ASIN`

## 📎 How to Use

1. Clone the repo and open the `.pbix` file in Power BI Desktop.
2. Replace data sources if needed under **Transform Data > Edit Queries**.
3. Explore interactive visuals with slicers and filters.

## 💡 Insights Gained

- **Top Performing ASINs**: Understand which products are driving the most revenue.
- **Cost Efficiency**: Compare CPC vs. CTR to optimize bidding strategy.
- **Conversion Performance**: Track how well ads convert clicks into orders.
- **Ad Type Comparison**: Analyze the effectiveness of Product vs Brand vs Display campaigns.

---

## 📞 Contact

For any feedback or contributions, feel free to connect:

**Shraddha S Kharvi**  
[LinkedIn](https://www.linkedin.com/in/shraddha-kharvi-42588b218/)  
📧 shraddhakharvi2024@gmail.com
