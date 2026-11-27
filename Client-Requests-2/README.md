# 📊 Nova Mart – Retail Promotions & Campaign Performance Analysis

## 📌 Project Overview

This project focuses on analyzing retail promotional campaign performance using Python and Pandas.

The objective is to evaluate how promotional campaigns influence sales quantity and revenue across different cities and product categories.

The analysis addresses **7 business questions provided by the client**, covering store distribution, category-wise sales contribution, price-sales correlation, sales distribution, promotional effectiveness and revenue performance.

The findings help businesses identify successful promotional strategies, understand customer purchasing patterns and make better data-driven decisions.

---

## 🎯 Business Objectives

- Analyze store distribution across different cities.
- Identify top-performing product categories during promotions.
- Understand the relationship between promotional price and sales quantity.
- Examine pre-promotion sales distribution across product categories.
- Measure city-wise incremental sales growth.
- Evaluate promotion types based on incremental revenue and sales quantity.
- Compare revenue performance before and after promotions.

---

## 📂 Dataset Overview

The project uses four datasets:

| Dataset         | Description                                    |
| --------------- | ---------------------------------------------- |
| `dim_campaigns` | Campaign information and campaign dates        |
| `dim_products`  | Product details and categories                 |
| `dim_stores`    | Store information and city details             |
| `fact_events`   | Sales quantities, prices and promotion details |

---

## 🛠️ Tools & Technologies

- **Python** – Data analysis and calculations
- **Pandas** – Data manipulation and aggregation
- **NumPy** – Numerical operations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Jupyter Notebook** – Interactive analysis

---

# 📈 Business Analysis & Key Insights

## Q1. Store Distribution Across Cities

**Business Question:** Which city has the highest number of stores, and how does Bengaluru compare with Hyderabad and Chennai?

### Key Findings

| City          | Number of Stores |
| ------------- | ---------------: |
| Bengaluru     |               10 |
| Chennai       |                8 |
| Hyderabad     |                7 |
| Coimbatore    |                5 |
| Visakhapatnam |                5 |
| Madurai       |                4 |
| Mysuru        |                4 |
| Mangalore     |                3 |
| Trivandrum    |                2 |
| Vijayawada    |                2 |
| **Total**     |           **50** |

### Business Insights

- Bengaluru has the highest store presence, accounting for 20% of total stores.
- Chennai ranks second with 8 stores, followed by Hyderabad with 7.
- Bengaluru has 2 more stores than Chennai and 3 more than Hyderabad.
- Trivandrum and Vijayawada have the lowest store presence, with 2 stores each.

**Recommendation:** Evaluate expansion opportunities in cities with lower store coverage based on customer demand and market potential.

---

## Q2. Sankranti Campaign – Category-wise Sales Contribution

**Business Question:** Which product categories contributed the most to total quantity sold after the Sankranti promotion?

### Key Findings

| Product Category  | Quantity Sold | Contribution |
| ----------------- | ------------: | -----------: |
| Grocery & Staples |       177,724 |       70.51% |
| Home Appliances   |        35,610 |       14.13% |
| Home Care         |        16,894 |        6.70% |
| Combo1            |        12,411 |        4.92% |
| Personal Care     |         9,430 |        3.74% |
| **Total**         |   **252,069** |     **100%** |

### Business Insights

- Grocery & Staples dominated the campaign, contributing 70.51% of total sales volume.
- Home Appliances ranked second with a 14.13% contribution.
- The top two categories contributed 84.64% of total quantity sold.
- Personal Care recorded the lowest contribution at 3.74%.

**Recommendation:** Prioritize high-demand categories while introducing targeted promotional strategies to improve the contribution of lower-performing categories.

---

## Q3. Relationship Between Promotional Price and Sales Quantity

**Business Question:** What is the relationship between after-promotion price and after-promotion sales quantity?

### Key Finding

**Pearson Correlation: +0.27**

### Business Insights

- The correlation coefficient of +0.27 indicates a weak positive linear relationship.
- Higher after-promotion prices do not necessarily correspond to lower sales quantities in this dataset.
- Product demand, category, promotion type and customer preferences may also influence sales quantity.

**Recommendation:** Businesses should evaluate pricing alongside product demand and promotional strategies rather than relying on price alone.

*Note: Correlation does not establish causation.*

---

## Q4. Distribution of Quantity Sold Before Promotions

**Business Question:** How does the distribution of quantity sold before promotions vary across different product categories?

### Key Observations

| Product Category  | Observed Sales Distribution                          |
| ----------------- | ---------------------------------------------------- |
| Grocery & Staples | Most observations concentrated around 300–400 units  |
| Home Care         | Right-skewed distribution, mainly around 20–60 units |
| Combo1            | Wide distribution with distinct sales clusters       |
| Home Appliances   | Broad distribution, approximately 20–140 units       |
| Personal Care     | Right-skewed distribution, mainly around 20–80 units |

### Business Insights

- Grocery & Staples demonstrates relatively high baseline sales volume.
- Home Care and Personal Care have right-skewed distributions.
- Combo1 shows considerable variation in sales quantities.
- Home Appliances has a broader spread of sales observations.
- Different product categories demonstrate different baseline demand patterns.

**Recommendation:** Develop category-specific promotional strategies based on existing demand patterns and sales variability.

---

## Q5. City-wise Incremental Sold Units Percentage (ISU%)

**Business Question:** Which cities experienced the highest and lowest sales quantity growth after promotions?

### Formula

ISU% = ((Quantity After Promotion − Quantity Before Promotion) / Quantity Before Promotion) × 100

### Key Findings

| Rank | City          | Units Before | Units After |    ISU% |
| ---: | ------------- | -----------: | ----------: | ------: |
|    1 | Madurai       |       14,086 |      31,169 | 121.28% |
|    2 | Bengaluru     |       48,972 |     105,141 | 114.70% |
|    3 | Coimbatore    |       18,200 |      38,900 | 113.74% |
|    4 | Chennai       |       39,183 |      83,273 | 112.52% |
|    5 | Vijayawada    |        5,297 |      11,106 | 109.67% |
|    6 | Trivandrum    |        4,884 |      10,170 | 108.23% |
|    7 | Mysuru        |       18,202 |      37,470 | 105.86% |
|    8 | Hyderabad     |       34,335 |      69,399 | 102.12% |
|    9 | Mangalore     |        7,454 |      14,929 | 100.28% |
|   10 | Visakhapatnam |       17,037 |      33,916 |  99.07% |

### Business Insights

- Madurai achieved the highest ISU% at 121.28%.
- Visakhapatnam recorded the lowest ISU% at 99.07%.
- All 10 cities experienced positive sales quantity growth.
- Bengaluru generated the highest after-promotion sales volume, with 105,141 units.
- The difference between the highest and lowest city-wise growth was 22.21 percentage points.

**Recommendation:** Analyze the successful promotional strategies in Madurai and identify opportunities to improve campaign performance in Visakhapatnam.

---

## Q6. Promotion Type Performance in Hyderabad

**Business Question:** Which promotion types generated the highest incremental revenue and incremental sold units?

### Key Findings

| Promotion Type | Revenue Before | Revenue After |     IR% |    ISU% |
| -------------- | -------------: | ------------: | ------: | ------: |
| 25% OFF        |      1,547,135 |     1,009,192 | -34.77% | -12.90% |
| 33% OFF        |      6,015,872 |     5,836,633 |  -2.98% |  45.17% |
| 50% OFF        |        360,534 |       245,212 | -31.99% |  35.94% |
| 500 Cashback   |     10,476,000 |    23,342,500 | 122.82% | 167.38% |
| BOGOF          |      4,293,700 |     7,476,120 |  74.12% | 252.83% |

### Business Insights

- BOGOF generated the highest incremental sold units percentage at 252.83%.
- 500 Cashback generated the highest incremental revenue percentage at 122.82%.
- BOGOF increased units sold from 9,559 to 33,727.
- 500 Cashback increased revenue from 10.48 million to 23.34 million.
- 25% OFF recorded negative growth in both revenue and quantity.
- 50% OFF increased quantity but experienced a 31.99% revenue decline.
- 33% OFF increased sales quantity by 45.17%, while revenue declined slightly.

### Promotional Strategy Recommendations

| Business Objective      | Recommended Promotion |
| ----------------------- | --------------------- |
| Increase sales volume   | BOGOF                 |
| Increase revenue growth | 500 Cashback          |
| Re-evaluate performance | 25% OFF and 50% OFF   |

**Recommendation:** Select promotional strategies based on business objectives. Evaluate discount costs and profit margins before implementing them.

---

## Q7. Revenue Performance Across Product Categories in Bengaluru

**Business Question:** How did promotions impact revenue across different product categories in Bengaluru?

### Key Findings

| Product Category  | Revenue Before |  Revenue After | Revenue Increase |     Growth |
| ----------------- | -------------: | -------------: | ---------------: | ---------: |
| Combo1            |     15,777,000 |     38,125,000 |       22,348,000 |    141.65% |
| Grocery & Staples |     12,262,460 |     13,861,259 |        1,598,799 |     13.04% |
| Home Appliances   |      2,188,810 |      4,122,680 |        1,933,870 |     88.35% |
| Home Care         |      2,104,460 |      3,180,020 |        1,075,560 |     51.11% |
| Personal Care     |        576,321 |        389,629 |         -186,692 |    -32.39% |
| **Total**         | **32,909,051** | **59,678,588** |   **26,769,537** | **81.34%** |

### Overall Revenue Performance

| Metric                   |      Value |
| ------------------------ | ---------: |
| Revenue Before Promotion | 32,909,051 |
| Revenue After Promotion  | 59,678,588 |
| Incremental Revenue      | 26,769,537 |
| Overall Revenue Growth   | **81.34%** |

### Business Insights

- Bengaluru recorded an overall revenue increase of 81.34%.
- Total incremental revenue was 26.77 million.
- Combo1 generated the highest incremental revenue of 22.35 million.
- Combo1 contributed approximately 83.49% of total incremental revenue.
- Home Appliances recorded 88.35% revenue growth.
- Personal Care was the only category with negative revenue growth, declining by 32.39%.
- Grocery & Staples generated 13.86 million in revenue after promotions.

**Recommendation:** Continue evaluating successful Combo1 and Home Appliances strategies while investigating the decline in Personal Care.

---

# 📌 9. Overall Executive Summary

The analysis highlights the following major findings:

| Business Metric                   | Key Result                 |
| --------------------------------- | -------------------------- |
| Total Stores                      | 50 across 10 cities        |
| Highest Store Presence            | Bengaluru – 10 stores      |
| Top Sankranti Category            | Grocery & Staples – 70.51% |
| Price–Quantity Correlation        | +0.27                      |
| Highest City-wise ISU%            | Madurai – 121.28%          |
| Lowest City-wise ISU%             | Visakhapatnam – 99.07%     |
| Highest Hyderabad ISU%            | BOGOF – 252.83%            |
| Highest Hyderabad IR%             | 500 Cashback – 122.82%     |
| Bengaluru Revenue Growth          | 81.34%                     |
| Highest Bengaluru Category Growth | Combo1 – 141.65%           |

---

## 💡 10. Final Business Recommendations

1. **Optimize Store Distribution:** Evaluate expansion opportunities in cities with lower store presence.
2. **Focus on High-Performing Categories:** Prioritize Grocery & Staples during Sankranti campaigns.
3. **Improve Promotional Strategies:** Use BOGOF for sales volume growth and 500 Cashback for revenue growth in Hyderabad.
4. **Replicate Successful Campaigns:** Investigate the factors behind Madurai's highest ISU%.
5. **Address Underperforming Categories:** Review Personal Care's negative revenue growth in Bengaluru.
6. **Adopt Data-Driven Pricing:** Consider product demand and promotion type when evaluating pricing strategies.
7. **Measure Profitability:** Include discount costs, margins and campaign expenses in future promotional evaluations.

---

## 🏁 11. Conclusion

This project demonstrates how data analytics can help businesses evaluate retail promotional performance and make informed decisions.

The analysis reveals that promotional effectiveness varies across cities, product categories and promotion types.

Key findings include:

- Grocery & Staples contributed 70.51% of Sankranti sales volume.
- Madurai achieved the highest city-wise sales quantity growth at 121.28%.
- BOGOF generated the highest incremental sold units percentage in Hyderabad at 252.83%.
- 500 Cashback generated the highest incremental revenue percentage in Hyderabad at 122.82%.
- Bengaluru achieved 81.34% overall revenue growth after promotions.

These insights can help businesses improve promotional planning, allocate resources effectively and develop more targeted retail strategies.

---

## 👨‍💻 Author

**Retail Promotions Analytics Project**

*Data Analysis | Python | Pandas | Business Insights | Data Visualization*


