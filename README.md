# Zomato Customer Insights & Family Segment Analysis

**Goal:** Analyze Zomato customer behavior, sales trends, and purchasing patterns to identify high-value segments and opportunities for growth, with a special focus on **families**.

This project combines customer demographics with order data to uncover who drives revenue, when performance dips, and how Zomato can better target and retain its most valuable users.

---

## 📁 Project Overview

- **Tools:** Tableau (primary), CSV data
- **Data:**
  - `users.csv` – demographics and profile details  
    (age, gender, occupation, monthly income, family size, etc.)
  - `orders.csv` – transaction-level data  
    (order_date, sales_amount, sales_qty, user_id, restaurant id)

- **Focus Areas:**
  - Segmenting users (Families, Individuals, Students, etc.)
  - Understanding revenue contribution by segment
  - Weekend vs weekday performance
  - Seasonal trends across quarters

---

## 🔍 Key Business Questions

1. Which **customer segments** create the most revenue for Zomato?
2. How do **Families** behave compared to other segments (Individuals, Students, etc.)?
3. How do **weekend vs weekday** sales differ by segment?
4. Are there **seasonal patterns** (by quarter) that suggest opportunities for campaigns?
5. What **actionable steps** can Zomato take to improve engagement and smooth revenue dips?

---

## 🧠 Approach

### 1. Data Preparation

- Joined `users.csv` and `orders.csv` on `user_id`
- Cleaned and standardized:
  - Demographic fields (e.g., occupation, income categories)
  - Date fields for quarterly and weekday/weekend analysis
- Created derived fields:
  - **Customer segment** (e.g., Families vs non-Families)
  - **Weekend flag** (weekend vs weekday)
  - **Quarter** (Q1–Q4)

### 2. Segmentation & KPIs

- Defined **Families** based on user attributes (e.g., family size and other demographics)
- Calculated for each segment:
  - Total revenue
  - Order frequency
  - Average order value (AOV)
- Built views to compare:
  - Families vs Individuals vs Students
  - Income groups (including the prominent **"No Income"** category)

### 3. Weekend vs Weekday Analysis

- Aggregated sales by segment and by day type (weekend vs weekday)
- Calculated percentage change in sales volume on weekends:

  - **Families:** weekend sales drop by **32%**
  - **Individuals:** weekend sales drop by **22%**
  - **Students:** weekend sales drop by **39%**

- Analyzed how this pattern lines up with typical family routines and student behavior.

### 4. Seasonal (Quarterly) Trends

- Rolled up orders by quarter (Q1–Q4)
- Identified **softer performance in Q2 and Q4**, aligning with:
  - School breaks
  - Holiday season
- Used this to shape recommendations for **seasonal promotions**.

---

## 📊 Key Insights

1. **Families as the Core Driver**  
   - Families contribute the **highest revenue overall**.  
   - High-frequency family customers are the most **loyal and consistent**, making them a critical segment for retention.

2. **The “No Income” Segment Needs Clarification**  
   - A large share of customers are labeled as **“No Income”**, yet this group shows an **unexpectedly high Average Order Value (AOV)**.  
   - This suggests income is either misreported or not granular enough, limiting how useful it is for targeted campaigns.

3. **Weekend Performance Declines Across All Segments**  
   - Despite being high-value, Families see their sales fall **32% on weekends**.  
   - Individuals and Students show similar patterns, with weekend drops of **22%** and **39%** respectively.  
   - This points to a missed opportunity: weekends should be a prime time for food delivery.

4. **Seasonal Dips in Q2 and Q4**  
   - Sales soften in **Q2 and Q4**, which overlap with school breaks and major holidays.  
   - Without seasonal campaigns, Zomato leaves potential high-demand periods underutilized.

---

## 🎯 Recommendations

Based on the analysis, the following actions are recommended:

1. **Strengthen Family Engagement on Weekends**  
   - Launch a **“Weekend Family Feast”** campaign to position Zomato as a relaxing, affordable alternative to weekend cooking.  
   - Extend similar weekend-focused incentives to **Individuals and Students**, who also experience significant weekend drops.

2. **Refine Income Data Collection**  
   - Replace the broad “No Income” label with:
     - Income ranges, and/or  
     - Clarification of **household vs individual** income.  
   - Better granularity will enable more precise targeting and a clearer understanding of who Zomato’s high-value customers are.

3. **Leverage Seasonal Promotions in Q2 and Q4**  
   - Use **end-of-school** and **holiday-themed** campaigns to counteract dips in Q2 and Q4.  
   - Position Zomato as the go-to solution for convenient group meals during these busy times.

4. **Expand Incentives Beyond Peak Demand**  
   - Use targeted discounts and loyalty rewards during traditional **off-peak days and times**.  
   - This helps to **smooth demand**, stabilize revenue, and better utilize delivery capacity across the week.

---

## 📷 Dashboard & Report

## 📷 Dashboard & Report

- **Live Tableau Dashboard:**  
  [Zomato Customer Insights on Tableau Public](https://public.tableau.com/shared/F3BTK5BRB?:display_count=n&:origin=viz_share_link)

- **PDF Report:**  
  See `/docs/Zomato_Final_Rivera.pdf` for the full narrative and recommendations.

## 📂 Repository Structure

```text
data/
  users.csv                 # anonymized user data (demographics, income, family size)
  orders.csv                # order data (dates, revenue, user_id)
  README_data.md            # brief info about the dataset

dashboards/
  zomato_customer_insights.twbx   # Tableau workbook (if available)
  tableau_public_link.txt         # Tableau Public URL

docs/
  Zomato_Final_Rivera.pdf         # final written report

assets/
  dashboard_overview.png
  segment_performance.png
  weekend_vs_weekday.png

README.md
