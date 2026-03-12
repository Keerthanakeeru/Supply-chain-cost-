## Supply Chain Cost Overview – Tableau Dashboard
### Project Overview
This project builds an interactive Supply Chain Cost Overview dashboard in Tableau to analyze total logistics cost, regional performance, supplier costs, and product‑level spending.
​
It is designed as a portfolio project to practice end‑to‑end BI skills, from data preparation to KPI design and visual storytelling, similar in spirit to my SQL‑based Domino’s Pizza Sales and Zepto Inventory Analysis projects.

The dashboard helps business stakeholders quickly understand where money is being spent in the supply chain and which regions, suppliers, and product types are driving overall costs.
​

#### Dataset Information
Domain: Supply Chain / Logistics

Source format: CSV (supply_chain_data.csv) imported into Tableau.
​

Grain: Each row represents a transaction combining product, supplier, location, and cost.

### Core Fields
Location – City/region where the order is fulfilled (Bangalore, Chennai, Delhi, Kolkata, Mumbai).
​

Supplier name – Supplier providing the goods or services.
​

Product type – Category such as skincare, haircare, cosmetics.
​

Costs – Numeric field representing supply chain cost for that record (transportation, procurement, etc.).
​

These fields are used to aggregate cost at different levels and to build KPIs and bar charts in the dashboard.
​

### Objectives
Calculate and visualize overall supply chain cost.

Compute average cost per region and average cost per supplier as high‑level KPIs.
​

Analyze cost distribution by region, supplier, and product type using clear bar charts.
​

Practice Tableau skills: calculated fields, KPI tiles, dashboard layout, borders, and titles.

### Skills and Tools Used
Tableau Desktop Public Edition for data visualization and dashboarding.
​

Data modeling in Tableau: using dimensions (Location, Supplier name, Product type) and measures (Costs).

Calculated fields for KPI metrics (Avg Cost per Region, Avg Cost per Supplier).
​

Dashboard design: tiled layout, containers, borders, legends, titles, and number formatting.
​

### Key Calculated Fields
Total Supply Chain Cost

Implemented as a simple aggregation in Tableau:

Measure used in KPI: SUM([Costs]).
​

Avg Cost per Supplier

Captures the average cost incurred per distinct supplier across the dataset.

Calculated field:

text
Avg Cost per Supplier = SUM([Costs]) / COUNTD([Supplier name])
This value is displayed as a KPI tile at the top of the dashboard.
​

Avg Cost per Region

Captures the average cost per distinct region/location.

Calculated field:


Avg Cost per Region = SUM([Costs]) / COUNTD([Location])
Also shown as a KPI tile for quick comparison with supplier‑level costs.
​

### Dashboard Design
The Supply Chain Cost Overview dashboard is divided into three main sections:
​

Top KPI Row

Avg Cost per Region

Total Supply Chain Cost

Avg Cost per Supplier
Each KPI is formatted as a centered text tile with borders for separation.
​

Middle Charts – Cost by Region and Supplier

Cost by Region: Horizontal bar chart showing total cost for each city (Chennai, Kolkata, Bangalore, Mumbai, Delhi) with data labels.
​

Cost by Suppliers: Horizontal bar chart showing cost by each supplier, allowing comparison of high‑cost vs low‑cost suppliers.
​

Bottom Chart – Cost by Product Type

Vertical bar chart displaying total cost for each product type (skincare, haircare, cosmetics) with labels on top of bars.
​

Helps identify which category consumes the most supply chain budget.

Formatting choices:

Consistent blue color palette across charts.

Light gray borders around KPI tiles and chart containers to visually segment the layout.
​

Clean white background with minimal gridlines for a presentation‑ready look.
​

### Example Business Questions Answered
What is the total supply chain cost across all locations and suppliers?

On average, how much cost is incurred per region and per supplier?

Which regions contribute the most to overall cost?

Which suppliers are the most expensive, and which are relatively efficient?

Which product types (skincare, haircare, cosmetics) drive the highest supply chain costs?

These insights can help operations teams prioritize cost optimization efforts—e.g., renegotiating with high‑cost suppliers or reviewing logistics in the most expensive regions.

### Learning Outcomes
Through this project I:

Practiced building KPI tiles and using calculated fields in Tableau.

Learned how to structure a single‑page executive dashboard for supply chain stakeholders.

Improved skills in visual hierarchy, borders, titles, and layout using tiled containers.

Strengthened understanding of how simple aggregations like average cost per region/supplier can translate into actionable supply chain insights.
​

### Future Improvements
Add time dimensions (month, quarter) to analyze how costs change over time.

Connect Tableau directly to a SQL database instead of a static CSV for automatic refresh.

Add filter controls (by region, supplier, or product type) to make the dashboard fully interactive.

Extend the data model with lead time, quantity, and on‑time delivery fields to analyze efficiency as well as cost.

Build a companion SQL analysis notebook to mirror the Domino’s and Zepto projects in terms of analytical depth.

