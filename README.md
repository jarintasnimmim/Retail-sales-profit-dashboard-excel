# Retail Sales & Profit Performance Dashboard (Excel)
 
An interactive Excel dashboard analyzing retail sales and profit performance, built from a real-world transactional dataset (9,994 orders, 2014–2017). The project covers the full analytics workflow: data cleaning, PivotTable analysis, chart design, and dashboard assembly.
 
![Dashboard Preview](dashboard-preview.png)
 
## Business Problem
 
A retail superstore needed a clear, at-a-glance view of its sales and profit performance across regions, product categories, customer segments, and time — to identify which parts of the business are driving revenue, which are underperforming on margin, and where opportunities exist to improve profitability.
 
## Dataset
 
- **Source:** Sample Superstore Dataset (Kaggle)
- **Size:** 9,994 rows × 21 columns
- **Time period:** 2014–2017
- **Key fields:** Order Date, Region, Category, Segment, Product Name, Sales, Profit, Quantity
![Raw Data](raw-data-preview.png)
 
## Data Cleaning
 
Before analysis, the raw dataset was checked and cleaned in Excel:
- Checked for duplicate rows (none found)
- Checked for blank/missing values (none found)
- Converted Order Date and Ship Date from text to proper date format
- Verified numeric fields (Sales, Profit, Quantity, Discount) were correctly typed
- Verified category fields (Segment, Region, Category) had no spelling inconsistencies
## Analysis (PivotTables)
 
Five PivotTables were built to summarize the cleaned data from different angles:
 
![PivotTable Summary](pivottable-summary.png)
 
| PivotTable | Purpose |
|---|---|
| Region | Sales, Profit, and Order count by Region |
| Category | Sales, Profit, and Order count by Product Category |
| Order Date (Year/Month) | Monthly Sales & Profit trend, 2014–2017 |
| Segment | Sales, Profit, and Order count by Customer Segment |
| Top 10 Products | Top 10 products ranked by Profit |
 
## Dashboard
 
The final dashboard combines five KPI summary cards with five charts, all built using PivotCharts linked to the underlying PivotTables — plus interactive Slicers for filtering.
 
**KPIs:**
![KPI Summary](kpi-summary.png)
- Total Revenue: $2,297,201
- Total Profit: $286,397
- Total Quantity Sold: 37,873
- Total Orders: 5,009 (unique orders, calculated using `UNIQUE()`/`COUNTA()`)
- Profit Margin: 12.5%
  
**Charts:**
1. Sales by Category (Column)
2. Sales by Region (Bar)
3. Sales & Profit Trend, 2014–2017 (Line, dual-axis)
4. Sales by Segment (Doughnut)
5. Top 10 Products by Profit (Horizontal Bar)
   
**Interactivity:**
- 3 Slicers — Category, Region, and Segment — connected across all PivotCharts via Report Connections, so filtering by any one of them updates every chart on the dashboard simultaneously

*Demo: filtering the dashboard using Slicers*


https://github.com/user-attachments/assets/03464633-daeb-4913-8635-c94008e6da9e


## Key Insights
 
- **Category Performance:** Technology generated the highest sales ($836,154), followed by Furniture ($742,000) and Office Supplies ($719,047). Profit tells a different story: Technology also had the highest profit ($145,455), while Furniture had the lowest ($18,451) despite its near-top sales — the smallest profit-to-sales ratio of the three categories.
- **Regional Performance:** The West region recorded the highest Sales ($725,458) and highest Profit ($108,418) of any region. South had the fewest orders (822) of any region, yet outperformed Central on profit ($46,749 vs $39,706) despite lower sales — suggesting a smaller but comparatively more profitable customer base in the South.
- **Profitability:** Overall profit margin sits at approximately 12.5% ($286,397 profit on $2,297,201 in sales), providing a baseline to compare category-, region-, and segment-level performance against.
- **Product Performance:** The Canon imageCLASS 2200 Advanced Copier was the single highest-profit product ($25,200 alone — more than triple the next-highest product). Most of the top 10 products by profit are Technology items, reinforcing that Technology's strong performance is driven by a small number of high-value products.
- **Customer Segment:** Consumer generated the largest share of both Sales ($1,161,401) and Profit ($134,119) of the three segments, along with the highest order count (2,586) — this segment drives volume as well as revenue.
- **Sales & Profit Trend (2014–2017):** Sales showed a general upward trend, with higher peaks in later years, particularly toward the end of 2017. Profit did not grow at the same pace and stayed comparatively flat — revenue growth did not consistently translate into proportional profit growth.
## Business Recommendations
 
- **Investigate Furniture's low profit margin.** It has the second-highest sales but the lowest profit of any category — worth a closer look at discount levels, shipping costs, or pricing within this category.
- **Prioritize Technology and high-value products.** A small number of high-value Technology products (like the Canon imageCLASS copier) drive a disproportionate share of profit — consider expanding focus around similar high-margin items.
- **Study what makes the South region more profitable per order.** South has fewer orders than Central but generates more profit — understanding what's different about this region's customer base or product mix could reveal a replicable pattern.
- **Monitor the growing gap between Sales and Profit growth.** Sales has grown faster than Profit since 2014 — worth investigating further (e.g. rising costs, heavier discounting, a shift toward lower-margin products) before it becomes a larger issue.
- **Consider Consumer segment retention efforts.** Since Consumer drives the most orders and profit, retention or loyalty-focused initiatives here could have an outsized impact on overall performance.
## Tools & Techniques Used
 
- Excel Tables & structured references
- PivotTables & PivotCharts (Data Model)
- Distinct Order Count via `UNIQUE()` / `COUNTA()`
- Text-to-Columns for date cleaning
- Dynamic KPI cards linked to calculated cells
- Slicers connected across multiple PivotTables via Report Connections
- Custom color theming, data labels, and chart formatting
## Files
 
- `Sales superstore dataset.xlsx` — full workbook (raw data, cleaned data, calculations, PivotTables, dashboard)
- `dashboard-preview.png` — full dashboard screenshot
- `kpi-summary.png` — KPI summary card
- `raw-data-preview.png` — raw dataset preview
- `pivottable-summary.png` — PivotTable summary preview
## Next Steps / Limitations
 
- KPI cards currently show overall totals and are not yet linked to the Slicers (charts update with filters; KPI cards do not) — a planned future improvement
- Add Average Order Value as an additional KPI
 
