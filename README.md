Plant Co. - Financial Performance Report

• Project Overview

This Power BI project provides a comprehensive financial performance analysis for Plant Co., a global supplier. The dashboard compares Key Performance Indicators (KPIs) between the selected year and the previous year (PY), enabling stakeholders to track growth or decline across regions and product categories.

The primary goal of this report is to transform raw financial data into actionable insights regarding profitability and market expansion.

• Tech Stack & Skills

Data Transformation: Power Query (ETL) for data cleaning, unpivoting, and attribute formatting.

DAX (Data Analysis Expressions): Developed advanced measures for Time Intelligence, including YTD, PYTD and YoY Growth percentages, Date time table

Data Visualization: Applied data storytelling principles using conditional formatting, dynamic slicers, waterfall chart, treemap, scatter chart, line and stacked column chart.

• Key Features & Business Insights
Year-over-Year (YoY) Analysis: Automated comparison of Sales, Quantity, and Gross Profit against the previous period.

Dynamic Filtering: Interactive slicing by year and KPIs.

Performance Scorecards: High-level KPI cards that provide an instant snapshot of corporate health.

Trend Identification: Visual representation of monthly performance to spot seasonal patterns in the global supply chain.

• Data Modeling & DAX Showcase

The project relies on a robust data model centered around a Date Dimension to ensure accurate time-based calculations.

Example: Create Date table with DAX:

Inpast = 
VAR lastsalesdate = MAX(Fact_Sales[Date_Time])
VAR lastsalesdatePY = EDATE(lastsalesdate,-12)
RETURN
Dim_Date[Date]<= lastsalesdatePY

Dim_Date = 
CALENDAR(
    DATE(2022, 1, 1),
    DATE(2024, 12, 31)
)
<img width="1774" height="800" alt="Screenshot 2026-01-30 103322" src="https://github.com/user-attachments/assets/8b0ceab5-39b4-4f6c-b7ce-92d53695f7f0" />

• How to Access

Clone this repository or download the .pbix file.

Open the file using Power BI Desktop.

The underlying dataset is located in the /Data folder for reference.

