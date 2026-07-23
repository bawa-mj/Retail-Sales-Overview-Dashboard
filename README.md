# 📊 Retail Sales Overview Dashboard
An interactive, data-driven Power BI solution designed to track, analyze, and optimize retail sales performance across regions, categories, and customer segments. This dashboard processes transactional order data to surface key retail performance indicators, helping stakeholders understand revenue trends, customer behavior, and regional demand.

## 🚀 Key Business Metrics Tracked
*   **Revenue & Order Performance:** Real-time analysis of total revenue, total orders, average order value (AOV), and month-over-month growth %.
*   **Product Category Insights:** Deep-dive into top-performing product categories and their revenue contribution.
*   **Regional Breakdown:** Visual mapping of sales distribution across West, South, North, and East regions.
*   **Payment & Customer Analysis:** Payment method preferences and top revenue-generating customers.

## 📁 Repository Structure
The repository contains the core components of the Power BI solution:
*   **`retail_sales_dashboard.pbix`** — The production-ready Power BI desktop file containing pre-built DAX measures, a star-schema data model (Date Table + Fact Table), and visualization canvases.
*   **`Dataset/retail_sales_raw.xlsx`** — Raw source dataset used to build and test the dashboard.
*   **`DataModel/`** — Schema definitions including the DateTable, relationships, and calculated columns (Region, Month, Quarter).
*   **`Measures/`** — Documented DAX measures (Total Revenue, MoM Growth %, Average Order Value, etc.).

## 🛠️ Setup & Local Deployment
### Prerequisites
*   Windows OS (or a compatible VM environment).
*   Latest version of [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed.

### Steps
1. Clone this repository
2. Open `retail_sales_dashboard.pbix` in Power BI Desktop
3. Go to **Home → Transform Data → Data Source Settings** and point it to your local copy of `retail_sales_raw.xlsx`
4. Click **Refresh** to load the latest data

## 📸 Dashboard Screenshot & Preview
### 🎛️ Retail Sales Overview
![Retail Sales Overview Dashboard](https://raw.githubusercontent.com/bawa-mj/Retail-Sales-Overview-Dashboard/main/Retail%20Sale%20Overview-Dashboard.png)

## 📊 Data Cleaning Highlights (Power Query)
*   Fixed inconsistent category casing and payment method naming
*   Parsed mixed date formats (`YYYY-MM-DD` and `DD-MM-YYYY`) into a single clean Date type
*   Derived missing `State`/`Region` values from known `City` mappings where possible
*   Filled remaining gaps with `"Unknown"` rather than dropping valid revenue rows
