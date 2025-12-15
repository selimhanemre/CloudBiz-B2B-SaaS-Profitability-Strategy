# Profitability Analysis: Revamping Discount Strategy for CloudBiz

![Banner Image](https://img.shields.io/badge/Status-Complete-green) ![Tools](https://img.shields.io/badge/Tools-SQL%20%7C%20Tableau-blue)

## Project Overview
**Client:** CloudBiz (Fictional B2B SaaS Company)  
**Role:** Lead Data Analyst  
**Objective:** Diagnose the root cause of a 30% profit decline in 2025 despite record-breaking revenue growth.

**The Business Problem:**
Founded in 2022, CloudBiz has seen consistent growth. However, in 2025, the company experienced a troubling anomaly: while sales revenue hit an all-time high, profit margins plummeted. I was brought in to analyze the sales data, identify the leak, and propose data-driven solutions to the executive team.

## Executive Summary
The analysis reveals that the profit decline is **not** due to a lack of demand or poor product fit, but rather an unoptimized **discounting strategy**.

* **The Good:** Q4 2025 Sales broke records at **$280k** (+20% YoY).
* **The Bad:** Q4 2025 Profit fell to **$27k** (-30% YoY).
* **The Cause:** High-tier discounts (30%-80%) eroded margins, resulting in a **$47k net loss**.
* **The Solution:** Capping discounts at 20% and restructuring the product portfolio should approximately **increase annual profit by 50%** without significantly impacting sales volume.

---

## Key Insights & Analysis

### 1. Lower than Expected Profits
The company is scaling revenue successfully, but profits is failing to follow suit. As shown below, Q4 is traditionally the strongest quarter. In 2025, while the blue line (Sales) reached a new peak, the green line (Profit) diverged downward. This shows we are spending too much to acquire each sale or to deliver each product.

![Sales vs Profit Trend](images/Sales_Profit.png)
*Figure 1: Comparison of Sales vs. Profit over time.*

### 2. Products & Regions
While the US market remained stable, the **APJ (Asia Pacific)** and **EMEA (Europe, Middle East, Africa)** regions were responsible for the bulk of the profit loss.
* APJ generated 18% of sales but only 3% of profit.
* The product "Contact Matcher" alone lost **$11.5k** in APJ, and "Big Ol Database" lost **$3.6k** in EMEA. These are otherwise profitable products in other regions, pointing to a pricing anomaly rather than a product defect.

![Regional Product Performance](images/Product_Region.png)
*Figure 2: Profit Breakdown by Region and Product.*

### 3. The Impact of High Discounts
Deep diving into pricing revealed the root cause: unregulated discounts.
* Transactions with discounts of 30% or higher resulted in a cumulative loss of **$47k**.
* The "Contact Matcher" and "Big Ol Database" products saw the heaviest discounting, driving them into negative profitability.

![Discount Heatmap](images/Profit_Table.png)
*Figure 3: Net Profit/Loss by Product and Discount Tier. Discounts >20% consistently yield negative returns.*

### 4. Product Portfolio Optimization
Not all products are performing equally.
* **Star Performer:** "Alchemy" (Top Left in chart) is the ideal case study. Despite lower discounts and a higher price point, sales quantity remained stable (69 to 73 units) while profits skyrocketed ($17k to $25k).
* **Underperformers:** "Contact Matcher" drove high volume but negative profit due to the discount issues identified above.
* **Redundancies:** We have several "Gold" variants (e.g., *SaaS Connector Pack - Gold*) that are not outperforming their standard counterparts, creating portfolio bloat.

![Product Scatter Plot](images/Product_Performance.png)
*Figure 4: Product Performance - Profit & Quantity Sold. *

### 5. Do Discounts Drive Revenue?
There is a positive correlation between discounts and revenue (discounts *do* drive sales), but there is a point of diminishing returns.
* The data shows that we can generate significant revenue ($200k) even with a maximum discount of 20%.
* To generate that same revenue using high discounts (>30%), we essentially "gave away" $55k in value compared to just $20k if discounts were capped at 20%.

![Sales vs Discount Correlation](images/Discounts_Revenue.png)
*Figure 5: Correlation between Sales and Discounts. The trend holds even when sales with high discounts are removed, proving deep cuts are unnecessary.*

### 6. Discounting Does Not Buy Loyalty
A common justification for high discounts is "Customer Lifetime Value" (LTV)—the idea that a cheap entry price leads to a profitable long-term relationship. The data refutes this.
* **Negative Correlation:** Customers who received the highest average discounts actually generated the **lowest** total lifetime profit for the company.
* **Strategy Shift:** Buying loyalty with price cuts is a failed strategy. It is better to focus on making each sale profitable. 

![LTV Scatter Plot](images/Customer_Loyalty.png)
*Figure 6: Lifetime Value (Profit-based) vs. Average Discount. Higher discounts correlate with lower long-term value.*

---

## Actionable Recommendations

Based on this analysis, I propose the following actions for the leadership team:

### Finance Team
* **Implement a Discount Ceiling:** Enforce a strict policy capping sales discounts at 20%. Any discount above this threshold requires VP-level approval.
* **Protect Profit Margins:** Flag any quote that results in negative margin immediately in the CRM before the sale can be closed.

### Product Team
* **Consolidate the Lineup:**
    * Merge *SaaS Connector Pack - Gold* into *SaaS Connector Pack*.
    * Merge *Marketing Suite* into *Marketing Suite - Gold*.
* **Review the "Storage" product.**
    * With only **$858 in total 2025 sales**, this product is a distraction. Unless it serves as a strategic lead magnet, I recommend removing it to free up resources for high-profit products like "Alchemy."

### Marketing Team
* **Stop High-Discount Campaigns:** Shift marketing copy from discounts to value-based messaging. Use the Alchemy product as a case study for selling on value rather than price.
* **Retarget:** Stop targeting customer segments that tend to demand >30% discounts. Focus ad spend on similar audiences to our high-LTV, low-discount customers.
* **Collect Data:** Collect data on the marketing channel for each sale for future analysis and marketing optimization. 

---

## Tools Used:
* Excel, Python, Power Query, Power BI.

---
*Author: Selimhan Dagtas*
