# Customer Profitability Sample

This repository contains a Power BI report that explores **customer profitability** across industries, products, regions and executives.  
It is inspired by the classic *Customer Profitability* sample and is designed to help business users quickly understand **where profit is created (or destroyed)** and which levers they can act on.

---

## 1. Objectives

The report answers questions such as:

- Which **industries, products and customers** generate the highest revenue and gross margin?
- How does **actual performance compare to budget** over time?
- Which **regions and executives** are driving results?
- Where do we see **margin erosion** that might require action (discounts, costs, mix, etc.)?

---

## 2. Data & Metrics
![Data & Metrics]()
### Main Business Concepts

- **Customer** – end client or account buying our products.
- **Product** – items sold (e.g. Primus, Gladius, MI-72, Sova).
- **Industry** – industry segment of the customer (CPG, Services, Retail, Utilities, etc.).
- **Region / State** – geographic allocation of revenue (North, South, East, Central; US states).
- **Executive** – account owner / salesperson responsible for the customer.

### Key Measures

- **RevenueTY** – Total revenue for the current year.
- **Gross Margin %** – Profitability ratio based on revenue and cost.
- **Revenue % Variance to Budget** – % difference between actual revenue and budget.
- **Number of Customers**
- **Number of Products**

---

## 3. Report Pages

### 3.1 Industry Margin Analysis
![Industry Margin Analysis]()
This page focuses on **profitability by industry and product**.

Main visuals:

- **KPI tiles**
  - Number of Customers  
  - Number of Products  
  - Gross Margin %

- **RevenueTY and Gross Margin % by Business Unit**  
  Column & line combo chart comparing revenue and gross margin % across business units.

- **Revenue Var % to Budget, GM% and RevenueTY by Industry**  
  Bubble plot showing:
  - X-axis: Revenue % Variance to Budget  
  - Y-axis: Gross Margin %  
  - Bubble size: RevenueTY  
  Used to quickly spot over-/under-performing industries.

- **Total Revenue by Product**  
  Treemap highlighting revenue contribution of each product (Primus, Gladius, Sova, etc.).

- **Gross Margin % by Month and Executive**  
  Area/line chart showing gross margin trends over the year split by executive (Andrew Ma, Annelie Zubar, Carlos Grilo, Tina Lassila, Valery Ushakov).

- **Slicers**  
  - Industry  
  - Product  

Use this page to **identify profitable / unprofitable industries and products**, and to compare margin performance across executives.

---

### 3.2 Team Scorecard
![Team Scorecard]()
This page is a **performance dashboard for the sales / account team**.

Main visuals:

- **KPI tiles**
  - Number of Customers  
  - Number of Products  
  - Gross Margin %

- **Revenue % Variance to Budget by Month and Executive**  
  Line chart showing how each executive performs vs. budget throughout the year.

- **Total Revenue by Region**  
  Treemap of revenue split across regions (North, South, East, etc.).

- **RevenueTY and Revenue % Variance to Budget by Month**  
  Combo chart (columns for RevenueTY, line for variance to budget) to track seasonality and performance vs plan.

- **RevenueTY by State (Map)**  
  Filled map displaying revenue distribution across US states.

- **Slicer**
  - Executive  

Use this page to **monitor team performance**, track **budget adherence**, and identify **regional opportunities or issues**.

---

## 4. How to Use the Report

1. **Open the `.pbix` file** in **Power BI Desktop** (or publish to Power BI Service).
2. Use the **Industry** and **Product** slicers on the *Industry Margin Analysis* page to drill into specific segments.
3. Switch to the **Team Scorecard** page to evaluate performance by **Executive** and **Region**.
4. Hover over data points to see **tooltips** with exact values for revenue, variance and margin.
5. Use cross-filtering:
   - Clicking an industry, product, region or executive will filter the other visuals on the page.

---

## 5. Technical Notes

- **Tool:** Power BI Desktop  
- **Data Model (typical structure):**
  - Fact table: `FactSales` (revenue, cost, budget, dates, customer, product, region, executive keys)
  - Dimension tables: `DimCustomer`, `DimProduct`, `DimIndustry`, `DimRegion`, `DimDate`, `DimExecutive`
- **DAX Measures (examples):**
  - `RevenueTY`
  - `CostTY`
  - `Gross Margin = [RevenueTY] - [CostTY]`
  - `Gross Margin % = DIVIDE([Gross Margin], [RevenueTY])`
  - `Revenue Var % to Budget = DIVIDE([RevenueTY] - [Budget Revenue], [Budget Revenue])`

(Names and formulas can be adjusted to match your actual model.)

---

## 6. Repository Structure (suggested)

```text
Customer-Profitability-Sample/
│
├─ Customer Profitability Sample.pbix
├─ data/               # Optional: source CSV/Excel files
├─ images/
│   ├─ industry-margin-analysis.png
│   └─ team-scorecard.png
└─ README.md

