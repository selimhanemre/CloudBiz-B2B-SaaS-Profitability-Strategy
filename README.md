# Profitability Analysis: Revamping Discount Strategy for CloudBiz

![Banner Image](https://img.shields.io/badge/Status-Complete-green) ![Tools](https://img.shields.io/badge/Tools-SQL%20%7C%20Tableau-blue)

## 📌 Project Overview
**Client:** CloudBiz (Fictional B2B SaaS Company)  
**Role:** Lead Data Analyst  
**Objective:** Diagnose the root cause of a 30% profit decline in 2025 despite record-breaking revenue growth.

**The Business Problem:**
Founded in 2022, CloudBiz has seen consistent growth. However, in 2025, the company experienced a troubling anomaly: while sales revenue hit an all-time high, profit margins plummeted. I was brought in to analyze the sales data, identify the leak, and propose data-driven solutions to the executive team.

## 🚀 Executive Summary
The analysis reveals that the profit decline is **not** due to a lack of demand or poor product fit, but rather an unoptimized **discounting strategy**.

* **The Win:** Q4 2025 Sales broke records at **$280k** (+20% YoY).
* **The Loss:** Q4 2025 Profit fell to **$27k** (-30% YoY).
* **The Cause:** High-tier discounts (>30%) eroded margins, resulting in a **$47k net loss**.
* **The Opportunity:** Capping discounts at 20% and restructuring the product portfolio can recover approximately **$50k in annual profit** without significantly impacting sales volume.

---

## 🔍 Key Insights & Analysis

### 1. The "Profitless Growth" Trap
The company is scaling revenue successfully, but efficiency is dropping. As shown below, Q4 is traditionally the strongest quarter. In 2025, while the blue line (Sales) reached a new peak, the green line (Profit) diverged sharply downward. This indicates we are spending too much to acquire each dollar of revenue.

![Sales vs Profit Trend](assets/image_f702da.png)
*Figure 1: Comparison of Sales vs. Profit over time. Note the divergence in Q4 2025.*

### 2. Identifying the Bleeding Regions
While the US market remained stable, the **APJ (Asia Pacific)** and **EMEA (Europe, Middle East, Africa)** regions were responsible for the bulk of the profit loss.
* **APJ:** Generated 18% of sales but only 3% of profit.
* **Specific Product Leaks:** The product "Contact Matcher" alone lost **$11.5k** in APJ, and "Big Ol Database" lost **$3.6k** in EMEA. These are otherwise profitable products in other regions, pointing to a regional pricing anomaly rather than a product defect.

![Regional Product Performance](assets/image_f702a1.png)
*Figure 2: Profit Breakdown by Region and Product. The negative bars highlight specific product failures in APJ and EMEA.*

### 3. The Impact of Aggressive Discounting
Deep diving into pricing revealed the root cause: unregulated discounts.
* **The Red Zone:** Transactions with discounts of 30% or higher resulted in a cumulative loss of **$47k**.
* **The Culprits:** The "Contact Matcher" and "Big Ol Database" products saw the heaviest discounting, driving them into negative profitability.

![Discount Heatmap](assets/image_f70284.png)
*Figure 3: Net Profit/Loss by Product and Discount Tier. Discounts >30% consistently yield negative returns.*

### 4. Product Portfolio Optimization
Not all products are performing equally.
* **Star Performer:** "Alchemy" (Top Left in chart) is the ideal case study. Despite lower discounts and a higher price point, sales quantity remained stable (69 to 73 units) while profits skyrocketed ($17k to $25k).
* **Underperformers:** "Contact Matcher" drove high volume but negative profit due to the discount issues identified above.
* **Redundancies:** We have several "Gold" variants (e.g., *SaaS Connector Pack - Gold*) that are not outperforming their standard counterparts, creating portfolio bloat.

![Product Scatter Plot](assets/image_f7027e.png)
*Figure 4: Profit vs. Quantity Sold. High volume does not equal high profit.*

### 5. The "Efficient Frontier" of Discounting
There is a positive correlation between discounts and revenue (discounts *do* drive sales), but there is a point of diminishing returns.
* **The 20% Threshold:** The data shows that we can generate significant revenue ($200k+) with a maximum discount of 20%.
* **Wasteful Spend:** To generate that same revenue using high discounts (>30%), we essentially "gave away" $55k in value compared to just $20k in value at the lower tier.

![Sales vs Discount Correlation](assets/image_f702da.png)
*Figure 5: Correlation between Sales and Discounts. The trend holds even when high discounts are removed, proving deep cuts are unnecessary.*

### 6. Discounting Does Not Buy Loyalty
A common justification for high discounts is "Customer Lifetime Value" (LTV)—the idea that a cheap entry price leads to a profitable long-term relationship. The data refutes this.
* **Negative Correlation:** Customers who received the highest average discounts actually generated the **lowest** total lifetime profit for the company.
* **Strategy Shift:** Buying loyalty with price cuts is a failed strategy.

![LTV Scatter Plot](assets/image_f70245.png)
*Figure 6: Lifetime Value (Profit-based) vs. Average Discount. Higher discounts correlate with lower long-term value.*

---

## 💡 Recommendations

Based on this analysis, I propose the following actions for the leadership team:

### 🟢 For Finance: Implementation of a "Discount Ceiling"
* **Action:** Cap sales discounts at **20%** immediately.
* **Impact:** This eliminates the "Red Zone" identified in Figure 3, potentially recovering ~$47k in annual margin.
* **Protocol:** Any discount >20% requires VP-level approval and a written justification.

### 🔵 For Product: Portfolio Consolidation
* **Action:** Simplify the SKU list.
    * Merge *SaaS Connector Pack - Gold* into *SaaS Connector Pack*.
    * Merge *Marketing Suite* into *Marketing Suite - Gold*.
* **Action:** Review the "Storage" product.
    * With only **$858 in total 2025 sales**, this product is a distraction. Unless it serves as a strategic lead magnet, I recommend sunsetting it to free up engineering and marketing resources for high-margin products like "Alchemy."

### 🟠 For Marketing: Value-Based Selling
* **Action:** Shift messaging away from price.
    * Use the "Alchemy" product as the internal case study: customers are willing to pay full price for perceived value.
* **Action:** Retargeting Adjustments.
    * Stop targeting customer segments that historically demand >30% discounts, as they have proven to have low Lifetime Value. Focus ad spend on lookalike audiences of our full-price customers.

---

## 🛠 Tools Used
* **Data Analysis:** SQL & Excel
* **Visualization:** Tableau
* **Reporting:** PowerPoint & GitHub

---
*Author: [Your Name]*
*Location: Little Rock, AR*
