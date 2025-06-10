
# E-Commerce User Behavior Analysis

## Project Overview

As a Junior Analyst at an e-commerce company, I was tasked with analyzing raw user activity logs to gain actionable insights into user behavior. Each row in the dataset represents a user event (such as viewing a product, opening a cart, or completing a purchase) recorded on the company's website. The key objectives were to:

- Build a **conversion funnel** to understand user drop-offs from viewing a product to completing a purchase.
- Perform a **cohort analysis** to calculate and track **conversion** and **retention rates** based on the users' first purchase dates, broken down month by month.

These insights are crucial for optimizing marketing efforts, improving user engagement, and enhancing the overall shopping experience.

### Data Source

The dataset was sourced from a Google Spreadsheet and includes the following fields:

- `user_id`: Unique identifier for each user  
- `event_type`: Type of activity (`view`, `shopping_cart`, `purchase`)  
- `category_code`: Product category  
- `brand`: Product brand  
- `price`: Product price  
- `event_date`: Timestamp of the event (ranging from **2019-09-24 to 2021-02-28**)  

### Tools Used

- **Google Sheets**: For data inspection, cleaning, and transformation  
- **Pivot Tables**: For building the conversion funnel, performing cohort analysis, and calculating retention rates

 ## Analysis

### Data Cleaning and Preparation

### Part 1: Build a Conversion Funnel

1. Loaded and inspected the data.
2. Created a pivot table in a new sheet named **`conversion_funnel`**.
3. Counted unique users at each stage of the funnel: view, shopping_cart, purchase.
4. Added two calculated columns to the pivot table:
   - **Total Conversion Rate**: `=B2/$B$2`
   - **Step-by-Step Conversion Rate**: `=B3/B2`

---

### Part 2: Cohort Data Preparation

1. Created a new pivot sheet named **`purchase_activity`**.
2. Calculated each user's **first purchase date** using a minimum date aggregation.
3. Added a new column `first_purchase_date` using:
   ```excel
   =VLOOKUP(A2, first_Purchase!$A$2:$B$1082, 2)
   ```
Created a pivot table that looks like below:

<img src= "First purchase activity.png" />

---

### Part 3: Retention Rate Calculation

<img src="Retention Rates.png" />

---
 
## Conclusions

- **Overall Trend**: User activity and retention decrease over time. The user base is shrinking from month to month across different cohorts.
- **Conversion Funnel**:
  - View → Shopping Cart: **29%** conversion rate — a relatively low engagement at this step.
  - Shopping Cart → Purchase: **35.61%** — a relatively strong conversion at this point.
  - View → Purchase (total): **10%** — low overall conversion, indicating potential issues in engagement or site experience at the top of the funnel.
- **Retention Rates**:
  - Decrease steadily as **cohort age** increases.
  - Highest observed retention: **13%** for the **2020-09** cohort at age 1 month.
  - Lowest observed retention: **0%** for **cohort age 4** across all cohorts.
- **User Behavior**: Users show engagement early after their first purchase but tend to churn quickly in subsequent months.

---

## Recommendations

### 1. Boost Top-of-Funnel Engagement
- Since only 29% of users who view products add them to the cart, focus on improving product pages with better CTAs, reviews, urgency messages (e.g., low stock), or incentives like discounts for first-time cart additions.

### 2. Retain and Nurture Early Buyers
- The first month after purchase shows the highest retention. Implement loyalty programs, follow-up emails, and exclusive deals in the 30 days after the first purchase to extend user engagement.

### 3. Address Drop in Long-Term Retention
- With 0% retention at cohort age 4, design reactivation campaigns (e.g., “We Miss You” offers, win-back promotions) for users inactive beyond 3 months.

### 4. Monitor and Act on Monthly Cohorts
- Track month-over-month changes in both conversion and retention. Identify and replicate strategies used during successful months like **September 2020**.

### 5. Personalize Based on User Lifecycle
- Use cohort age to personalize messaging: offer first-purchase perks for newcomers, and loyalty rewards for recurring buyers within the first three months.

---

*Prepared by the Junior Data Analyst – E-Commerce Insights Team*
