
# Superstore Profitability Analysis

## 📌 Project Overview

This project was undertaken as a consultant tasked with reviewing Superstore's sales operations and helping the company increase profitability and avoid bankruptcy. Using transactional data from the "superstore.xls" dataset—including information on products, orders, shipping, and returns—this analysis identifies key profit drivers, areas of loss, advertising opportunities, and risk factors due to product returns. Visualizations and metrics are used to support data-driven decisions and strategic recommendations.

#### Data Source
 - Tableau superstore dataset

 
 #### Tools used 
 - Excel- data source 
 - Tableau for data visualization.

---

## 📊 Analysis

<a href="https://public.tableau.com/views/Superstore_17435126136000/Productssellingandproductstostop?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link">Dashboard Link</a><br/>
<a href="https://github.com/Bhagya-laks/Triple-Ten-Projects/blob/main/Superstore%20Analysis/Superstore%20Analysis.pdf" >Analysis Report</a>

### Part 1: Profits & Losses
- Identified **top 2 most profitable dimension pairs**, such as *Sub-Category + Region* and *Product ID + Shipping Mode*.
- Detected **top 2 loss-making combinations**, highlighting areas for review or discontinuation.
- Highlighted **specific loss-generating products** (e.g., certain office supply items) that consistently underperform.
- Selected **3 profitable subcategories** (e.g., Copiers, Phones, Accessories) to focus on.
- Recommended **3 subcategories to avoid** (e.g., Binders, Tables, Bookcases) based on repeated losses.







<img src= "Profit and loss.png" />
  

### Part 2: Advertising Strategy
- Analyzed **average profit by state and month** to identify seasonality.
- Recommended **top 3 combinations of state + month** (e.g., Indiana in October, Vermont in November) for advertising investment.
- Calculated **advertising budget** using Return on Ad Spend (ROAS) model—1/5 of monthly profit as ad spend.
- Visualized **monthly trends** in profit across key states.

  <img src= "Three best states.png"/>
  

### Part 3: Returned Items
- **LEFT JOIN** performed between Orders and Returns tables to assess return rates.
- Created a calculated field for return status (`Returned = 1` for Yes, `0` for Null).
- Identified **high-return products** and **frequent-return customers**.
- Compared **average return rate vs. profit** across dimensions like product category and shipping mode.
- Visuals reveal that some products with high returns may still be profitable, warranting case-by-case evaluation.

---

## 🧠 Conclusions

1. **Profits are highly concentrated** in a few key combinations of product category and region.
2. **Losses are persistent** in certain subcategories and products that should be reviewed or discontinued.
3. **Advertising in Q4** (especially October and November) across a few high-performing states yields better returns.
4. **Customer returns** vary significantly by product and shipping mode, and not all high-return items are unprofitable.
5. **Subcategory-level performance** shows clear winners and underperformers, enabling sharper inventory decisions.

---

## ✅ Recommendations

### Profitability Actions
- Discontinue or re-evaluate products and subcategories showing consistent losses.
- Focus resources on high-margin, high-profit areas like Copiers and Phones.

### Advertising Strategy
- Launch targeted advertising in **Indiana**, **Vermont**, and **Rhode Island** during Q4.
- Use a **20% of profit** threshold to set ad budgets based on average monthly profit.

### Return Rate Management
- Reduce returns by improving shipping processes (e.g., evaluating "Same Day" shipping mode).
- Investigate and improve or eliminate high-return products with low profitability.

### Business Strategy
- Encourage **positive reviews** and improved service to boost product ratings.
- Promote **high-rated items** more aggressively, as ratings have a positive correlation with sales.
- Tailor promotions for demographic groups like **students** who show higher engagement.

---


