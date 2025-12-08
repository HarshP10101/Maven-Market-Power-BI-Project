# Maven-Market-Power-BI-Project
Power BI project showcasing data cleaning, modeling, DAX, time intelligence, and dashboard design. Built using Maven Market retail data to analyze revenue, profit, product brands, returns, and regional store performance.

Below is your **final polished README.md** written in a **natural, industry-standard, recruiter-impressive style** with **no em dashes**.
This is ready to paste directly into GitHub.

---

## **1. Business Scenario**

Maven Market is a large grocery retailer operating across the United States, Canada, and Mexico. As the company expanded, leadership struggled to answer essential business questions because all reporting was scattered across disconnected CSV exports.

They needed a centralized BI solution that brings together customer data, product catalogs, store attributes, regional mapping, transactions, and return logs into one unified analytical model.

The goal of this project was to build a complete Power BI solution that supports:

* Revenue and profit tracking
* Product brand performance measurement
* Store and regional analysis
* Return rate and operational quality monitoring
* Weekly financial trending
* Goal tracking and insight-driven decision making

This project simulates a real consulting engagement where a data professional is brought in to deliver a complete BI workflow from raw data to executive dashboard.

---

## **2. Approach and Solution**

### **Step 1. Data Ingestion and Preparation**

Using Power Query, seven lookup tables and two fact tables were connected, cleaned, and enriched.

Key transformations included:

* Standardized data types and promoted headers for all tables
* Created a combined transactions table by ingesting 1997 and 1998 CSVs from a folder
* Added business logic columns such as price tiers, weekend flags, customer segmentation, remodel age, and full address fields
* Cleaned null values, formatted numeric fields, and prepared a complete Calendar dimension with month, quarter, and week attributes

This ensured consistency and accuracy before building the analytical model.

---

### **Step 2. Data Modeling**

A full enterprise star schema was created in Power BI Model View.

The model includes:

* Fact Tables: Transaction_Data and Return_Data
* Dimensions: Customers, Products, Stores, Regions, Calendar

Model highlights:

* One to many relationships with single directional filtering
* Proper snowflake relationship from Stores to Regions
* An inactive relationship for stock date analysis
* All foreign keys hidden to keep the reporting layer clean

This semantic model acts as a scalable foundation for all analytics and supports future data additions.

---

### **Step 3. Analytical Layer Using DAX**

A comprehensive DAX measure set was built to replicate how real organizations generate KPIs.

Core categories include:

* Quantity metrics for sold and returned products
* Revenue, cost, profit, and margin
* Return rate and operational indicators
* Time intelligence such as YTD revenue, last month revenue, and 60 day rolling revenue
* Weekend vs weekday behavioral analysis
* A revenue target measure that calculates a 5 percent lift over previous month revenue
* Global override measures (using ALL) to allow benchmark comparisons regardless of report filters

All measures were validated using spot checks to ensure accuracy.

---

### **Step 4. Interactive Dashboard Development**

A complete executive dashboard was designed in Power BI.

Key features:

* KPI cards showing current month transactions, profit, and returns with goal comparisons
* Product brand performance matrix with data bars and color based indicators
* Geographic insights using map and treemap visuals with drill down to country, state, and city
* Weekly revenue trending column chart for 1998
* Revenue vs Target gauge for financial goal alignment
* Slicer panel for country selection with clear interaction controls
* Bookmark based insights such as Portland crossing 1,000 sales in December

The layout was built for senior leaders to quickly scan, compare, and drill into business performance.

---

## **3. Business Impact and Results**

The final Power BI solution delivered several high value outcomes for Maven Market.

- **Unified Business Visibility**\
Leadership now has a single dashboard consolidating performance across three countries and more than fifty store locations.

- **Product Brand Insights**\
Brands can be ranked and compared based on total transactions, total profit, profit margin, and return rate. Average profit margin across all brands is roughly 60 percent.

- **Operational Efficiency Tracking**\
The overall return rate is under 1 percent. Problematic categories become visible immediately through color scaling.

- **Financial Performance Monitoring**\
The revenue target engine provides a forward looking view of whether the business is on track based on previous month performance.

- **Seasonality and Trend Identification**\
Weekly revenue patterns reveal strong seasonality and peak sales cycles.

- **City Level Deep Dives**\
Drill down interactions allow fast identification of outlier markets. One example insight is Portland crossing 1,000 sales in December, which is captured through a dedicated bookmark.

- **Scalable BI Foundation**\
The structured star schema, reusable DAX library, and organized model allow future enhancements with minimal effort.

This project mirrors the type of Power BI solution expected from a professional data analyst or BI consultant supporting retail operations.

---

## **4. Files Included**

* MavenMarket_Report.pbix
* Data folder containing all source CSV files
* Images folder containing dashboard screenshots and Maven Market branding
* README.md (this file)

---

## **5. How to Use This Project**

1. Download or clone the repository
2. Open the PBIX file in Power BI Desktop
3. Update file paths if necessary
4. Refresh the data model
5. Explore the report pages and bookmarks

This project is built to be easy for recruiters, hiring managers, and technical reviewers to review and run.

---

## **6. Final Remarks**

This Power BI solution demonstrates end to end BI capability including data transformation, relational modeling, analytical DAX design, interactive visualization, storytelling, and business-focused insight generation.

It is positioned as a real world consulting scenario that showcases your ability to deliver measurable business value through data.
