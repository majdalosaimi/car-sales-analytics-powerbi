# Car Sales Analysis Dashboard (Power BI)

## 📌 Project Overview
An interactive and dynamic **Power BI Dashboard** designed to track and analyze car sales performance. The project focuses on key performance indicators (KPIs) such as Year-to-Date (YTD) sales, Month-to-Date (MTD) sales, average pricing, and quantity sold, with breakdowns by car model, dealer region, body style, and color.

The goal of this dashboard is to empower decision-makers with actionable insights into sales trends, regional performance, and customer preferences.

---
## 📊 Dashboard Preview
![Dashboard Overview](screenshots/overview_dashboard.png)
![Dashboard Overview](screenshots/details_dashboard.png)

**Key Dashboard Features:**

* **Overview Page:** High-level executive KPIs, weekly sales trends, geographic performance, body style/color distribution, and top-selling manufacturers.
* **Details Page:** A transactional-level grid view with custom formatting and visual data bars for a quick, deep-dive analysis of specific sales records.
* **Interactive Filters:** Global slicers for Body Style, Dealer Name, Transmission, Engine Type, and Date.

---

## 🛠️ Data Journey (ETL & Modeling)

1. **Data Cleaning & Transformation (Power Query):**
   * Imported the raw single-table CSV dataset.
   * Cleaned data formats, handled missing values, and validated column data types.
   * Standardized text fields (e.g., Company, Color, and Body Style).

2. **Data Modeling:**
   * Created a dedicated, custom **Calendar Table (Date Dimension)** using DAX to enable time-intelligence calculations.
   * Established a **1-to-many relationship** between the Calendar Table and the Sales Fact Table to ensure accurate filtering across YTD and MTD metrics.

---

## 💡 Key Business Insights

Based on the dashboard analysis, here are the most critical business takeaways:

### 1. Overall Sales Performance (YTD vs. MTD)
* **Robust YTD Growth:** Total Year-to-Date sales reached **$371.2M**, representing a strong **23.59% YoY increase** (+$70.8M growth).
* **High Transaction Volume:** Total cars sold YTD is **13.3K units** (up **24.57%**).
* **Stable Pricing:** The average price per car stayed highly stable at **$28.0K** (only a minor drop of -0.79%). 
* *Note on Historical Context:* The overall historical sales in the dataset stand at **$671.5M** (as seen in the details tab), showing that the YTD performance contributes to more than half of the lifetime business value.

### 2. Seasonality & Weekly Trends
* Sales exhibit fluctuations throughout the year, with a massive peak occurring around **Week 35**, reaching a record weekly sales high of **$14.9M**. This indicates potential seasonal promotions or high-demand periods that should be capitalized on in future marketing campaigns.

### 3. Top Performing Brands & Regions
* **Brand Dominance:** **Chevrolet** leads the market share, accounting for **$27.1M (7.30% of total sales)** with **1,043 cars sold**, closely followed by **Dodge** at **$25.0M (6.74%)**.
* **High-End Segment:** **Cadillac** represents the premium segment with a high YTD Average Price of **$42.2K**, contributing **$15.3M (4.13%)** to total revenue.
* **Regional Hubs:** The Southern region (centered around **Austin**) and the North-Central region (**Janesville**) show the highest density of car sales based on dealer map bubble sizes.

### 4. Consumer Preferences
* **Color Preference:** **Pale White** is by far the most preferred car color, dominating the sales share over Black and Red.
* **Body Style:** **SUVs**, **Sedans**, and **Hatchbacks** make up the vast majority of the sales volume compared to hardtops or passenger vans.
