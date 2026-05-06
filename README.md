Enterprise Sales Insights & Data Analytics

📌 Project Overview
This project involves a comprehensive data analysis and a Business Intelligence (BI) solution developed to track, visualize, and analyze enterprise sales data. By implementing an end-to-end ETL pipeline using **MySQL** and **Power BI**, this dashboard provides stakeholders with real-time, actionable insights into revenue trends, market performance, and customer purchasing behaviors.

 🛠 Tech Stack
* **Database & Data Processing:** MySQL, SQL
* **Business Intelligence & Visualization: Power BI
* **Data Transformation:** Power Query, DAX (Data Analysis Expressions)

## 🗄️ Data Pipeline & ETL Process
The raw data consisted of unorganized transactional records, customer details, and market information. The following steps were taken to ensure data integrity:
1. **Data Extraction & Exploration (SQL):** 
   * Queried the database to identify anomalies, such as negative/zero sales amounts and inconsistent currency codes (e.g., mixing USD and INR).
2. **Data Cleaning & Transformation (Power Query):**
   * Filtered out invalid transactional data (`sales_amount <= 0`).
   * Engineered a conditional column to normalize all revenue into a single base currency (converted USD to INR based on an exchange rate multiplier) to ensure accurate aggregations.
3. **Data Modeling:**
   * Built a **Star Schema** data model connecting the central `transactions` Fact table with `customers`, `markets`, `products`, and `date` Dimension tables.

## 📊 Key Dashboards & Insights
*(Replace the line below with a screenshot of your dashboard!)*
`![Dashboard Screenshot](link_to_your_image.png)`

The Power BI dashboard enables data-driven decision-making through several key features:
* **Revenue Tracking:** Dynamic tracking of Total Revenue and Sales Quantity.
* **Market Analysis:** Breakdown of revenue performance across different regional markets to identify high-growth areas.
* **Customer Insights:** Identification of top-performing customers driving the highest sales volumes.
* **Temporal Trends:** Interactive year and month slicers to analyze historical sales trajectories and seasonal fluctuations.

## 💻 SQL Analysis Snippets
Foundation data exploration was conducted using SQL before importing into Power BI. Key queries include:

*Checking for invalid transactions:*
```sql
SELECT * FROM transactions WHERE sales_amount <= 0;
