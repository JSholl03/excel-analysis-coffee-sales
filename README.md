# Coffee Orders Dataset

## Overview

This dataset represents a fictional coffee sales business and is designed for **data analysis, visualization, and portfolio projects using Excel formulas only**. It combines **order-level transaction data** with **customer** and **product** reference tables and includes pre-built Excel dashboard sheets created entirely with native Excel functionality (no code, macros, or scripts).

The dataset is well-suited for projects involving:

* Sales and revenue analysis
* Customer segmentation
* Product performance analysis
* Excel-based dashboarding and reporting
* Advanced Excel formulas (XLOOKUP, INDEX/MATCH, SUMIFS, PivotTables)
* Business analysis without coding

---

## File Structure

The Excel file contains **multiple sheets**, which can be grouped into **data tables** and **analysis/dashboard views**.

### Data Tables

These sheets should be used as the primary data sources for analysis:

#### 1. `orders`

Transactional, line-item–level order data.

**Key columns:**

* `Order ID` – Unique identifier for each order
* `Order Date` – Date the order was placed
* `Customer ID` – Foreign key linking to the `customers` table
* `Product ID` – Foreign key linking to the `products` table
* `Quantity` – Units purchased
* `Unit Price` – Price per unit
* `Sales` – Total sales value (Quantity × Unit Price)
* `Coffee Type` – Short code for coffee type
* `Roast Type` – Short code for roast level
* `Size` – Product size (kg)
* `Customer Name`, `Email`, `Country` – Customer attributes included for convenience

Each row represents **one product within an order** (not one order total).

---

#### 2. `customers`

Customer-level reference data.

**Key columns:**

* `Customer ID` – Primary key
* `Customer Name`
* `Email`
* `Phone Number`
* `Address`, `City`, `Country`, `Postcode`
* `Loyalty Card` – Indicates loyalty program participation (`Yes` / `No`)

This table can be joined to `orders` using `Customer ID`.

---

#### 3. `products`

Product-level reference data.

**Key columns:**

* `Product ID` – Primary key
* `Coffee Type` – Arabica, Robusta, Excelsa, etc.
* `Roast Type` – Light, Medium, Dark
* `Size` – Product size (kg)
* `Unit Price`
* `Price per 100g`
* `Profit` – Profit per unit

This table can be joined to `orders` using `Product ID`.

---

### Analysis & Dashboard Sheets

These sheets are **derived from the core data** and are intended for visualization and insights:

* `Dashboard` – High-level KPI and summary view
* `TotalSales` – Aggregated sales metrics
* `CountryBarChart` – Sales by country visualization
* `Top5Customers` – Top customers by revenue

These sheets are optional for analysis and primarily serve as **examples of business reporting**.

---

## Data Model

The dataset follows a simple **star schema**:

* **Fact table:** `orders`
* **Dimension tables:** `customers`, `products`

**Relationships:**

* `orders.Customer ID` → `customers.Customer ID`
* `orders.Product ID` → `products.Product ID`

---

## Example Analysis Questions

* Which countries generate the highest revenue?
* Who are the top customers by lifetime value?
* How does roast type affect profitability?
* What product sizes have the best margin?
* Do loyalty card holders generate more revenue?

---

## Tools & Technologies

This dataset was built and analyzed using:

* **Microsoft Excel** (formulas, PivotTables, charts)

No programming languages, scripts, macros, or external tools were used.**

---

## Notes

* This is a **synthetic dataset** created for learning and portfolio purposes.
* Customer data is fictional and does not represent real individuals.
* Currency values are assumed to be consistent across the dataset.

---

## JS

Created and curated for data analytics practice and portfolio demonstration.

If you use this dataset in a project, feel free to reference it in your analysis or README.
