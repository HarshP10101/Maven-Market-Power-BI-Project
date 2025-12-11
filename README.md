# **Maven Market Power BI Project**

This project is a full Power BI solution built for a fictional retail company called Maven Market. I used their customer, product, store, region, transactions, and return data to create a complete analytics model and an interactive dashboard that answers real business questions.

The goal was simple: take raw CSV exports and turn them into a usable BI system that helps leaders understand performance, spot trends, and make decisions with confidence.

---

## **1. Business Scenario**

Maven Market operates grocery stores across the United States, Canada, and Mexico. Their reporting was scattered, inconsistent, and difficult to analyze. To fix that, I built a unified Power BI model that brings all their data together and highlights:

* Revenue and profit patterns
* Product and brand performance
* Store and regional trends
* Return rates and operational issues
* Weekly and monthly sales behavior
* Goal tracking for financial targets

This project follows the same steps a BI analyst or consultant would take in a real client engagement.

---

## **2. How I Built the Solution**

### **Step 1. Cleaning and Preparing the Data**

I started in Power Query and prepared all lookup tables and fact tables.
Some of the key steps include:

* Standardizing column names and data types
* Combining the 1997 and 1998 transaction files into one table
* Creating additional business logic fields like:

  * price tiers
  * weekend flags
  * customer segments
  * store remodel age
  * full address fields
* Cleaning nulls and fixing formatting issues
* Building a full calendar table with day, week, month, quarter, and year columns

This gave me a solid foundation before moving into modeling.

---

### **Step 2. Designing the Data Model**

I built a star schema with relationships that mirror how real retail systems are structured.

**Fact tables:**

* Transactions
* Returns

**Dimension tables:**

* Customers
* Products
* Stores
* Regions
* Calendar

The model includes one-to-many relationships, a snowflake connection from Stores to Regions, and an inactive relationship for stock date analysis.
All foreign keys are hidden to keep the report view clean and easy to navigate.

---

### **Step 3. Building the Analytical Layer with DAX**

I created a full set of DAX measures to track performance. These cover:

* Total quantity sold and returned
* Revenue, cost, profit, and margin
* Return rate
* Time intelligence calculations like:

  * Year-to-date revenue
  * Last month revenue
  * 60-day rolling revenue
* Weekend vs weekday comparisons
* A revenue target based on a 5 percent lift over the previous month
* Benchmark metrics using ALL to override filters when needed

Everything was validated with spot checks to make sure the numbers matched expectations.

---

### **Step 4. Building the Dashboard**

The final report is designed for leaders who want quick insights without digging into raw tables.

Some of the main visuals include:

* KPI cards for monthly performance
* A brand performance matrix with data bars and color cues
* A geographic view showing performance by country, state, and city
* A weekly revenue chart to highlight seasonality
* A gauge showing revenue vs target
* A slicer panel for country selection
* Bookmarks with specific insights, including Portland surpassing 1,000 sales in December

The layout makes it easy to scan, compare, and dig deeper when needed.

---

## **3. Key Insights**

Here are some of the findings uncovered by the dashboard:

* **Stronger visibility:** Performance across all three countries now shows up in one place.
* **Brand performance:** Brands can be ranked by transactions, profit, margin, and return rate.
* **Healthy operations:** Return rates are under 1 percent, and problem areas stand out immediately.
* **Financial indicators:** The revenue target shows if the company is pacing ahead or falling behind compared to the previous month.
* **Seasonality:** Weekly revenue reveals clear peaks and patterns.
* **City analysis:** Drill-downs help spot outliers, like Portland’s strong December performance.
* **Scalability:** The structured model is ready for future years and additional data sources.

---

## **4. Files in This Repo**

* `MavenMarket_Report.pbix`
* `data/` folder with all CSV files
* `DashboardPreview.pdf`
* `README.md`

---

## **5. How to Explore the Project**

1. Clone or download the repo
2. Open the PBIX file in Power BI Desktop
3. Update file paths if needed
4. Refresh the data
5. Explore each report page and bookmark
---

## **6. Final Note**

This project demonstrates my ability to own a BI solution from start to finish. I cleaned and modeled the data, built the analytical layer, and designed a dashboard that turns numbers into decisions. The final report mirrors the kind of work that helps business leaders move faster and make informed choices. It represents the standard of quality I bring to any data role.
