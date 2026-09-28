# Customer-Shopping-Behaviour-Analysis
Customer behaviour analysis using Python, SQL and an interactive Power BI dashboard

# 🛍️ Customer Shopping Behaviour Analysis

## 📌 Project Overview
An end-to-end analysis of customer shopping behaviour, combining **Python** (data cleaning), **SQL** (business questions) and **Microsoft Power BI** (interactive dashboard) to understand who buys what, how much they spend, and how subscriptions, discounts and shipping relate to spending.

The project turns raw transactional data into clear insights on revenue, customer segments, product performance and spending patterns across demographics.

**Data source:** `customer_shopping_behavior.csv` — the original dataset of 3,900 customer purchase records with 18 columns covering demographics, products, purchase amounts, subscription status, shipping, discounts and purchase frequency. After cleaning and feature engineering in Python, the final dataset (`Post_Python_customer_behaviour.csv`) has 19 columns.

## 🎯 Business Objectives
The analysis focuses on:

- Tracking overall revenue and average spend
- Comparing revenue across gender and age groups
- Evaluating product category and product-level performance
- Understanding the impact of subscriptions, discounts and shipping types
- Segmenting customers by purchase history (New, Returning, Loyal)

## 🛠️ Tools & Technologies
- Python (pandas) in Google Colab
- SQL (PostgreSQL)
- Microsoft Power BI
- Data Cleaning & Feature Engineering
- Data Visualization

## 🧹 Data Preparation (Python)
- Filled 37 missing review ratings with the **median rating of each product category**
- Standardised column names to `snake_case` for use in both Python and SQL
- Created `age_group` (Young Adult, Adult, Middle-aged, Senior) using age quartiles
- Created `purchase_frequency_days` by mapping purchase frequency to number of days
- Verified `promo_code_used` was identical to `discount_applied`, then dropped the redundant column

## 📈 Key Metrics

| Metric | Result |
|---|---|
| Total Revenue | $233,081 |
| Total Customers | 3,900 |
| Average Purchase Amount | $59.76 |
| Average Review Rating | 3.75 |
| Subscribed Customers | 27% |
| Purchases With a Discount | 43% |

## 🔎 Key Findings

### Product Categories
| Category | Revenue | Share |
|---|---|---|
| Clothing | $104,264 | 44.7% |
| Accessories | $74,200 | 31.8% |
| Footwear | $36,093 | 15.5% |
| Outerwear | $18,524 | 7.9% |

### Gender
| Gender | Revenue | Share | Avg. Spend |
|---|---|---|---|
| Male | $157,890 | 67.7% | $59.54 |
| Female | $75,191 | 32.3% | $60.25 |

Male customers generate more revenue because there are more of them (2,652 vs 1,248), not because they spend more per order.

### Subscription Status
| Status | Customers | Revenue | Avg. Spend |
|---|---|---|---|
| Non-subscribers | 2,847 | $170,436 | $59.87 |
| Subscribers | 1,053 | $62,645 | $59.49 |

Subscribers do not spend more per order than non-subscribers.

### Age Groups
| Age Group | Revenue |
|---|---|
| Young Adult (18–31) | $62,143 |
| Middle-aged (45–57) | $59,197 |
| Adult (32–44) | $55,978 |
| Senior (58–70) | $55,763 |

### Customer Segments
| Segment | Previous Purchases | Customers |
|---|---|---|
| Loyal | 11+ | 3,116 |
| Returning | 2–10 | 701 |
| New | 1 | 83 |

### Other Highlights
- **Top rated products:** Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Handbag (3.78)
- **Shipping:** Express averages $60.48 vs $58.46 for Standard
- **Discounts:** about half of discounted purchases (839 of 1,677) were still above the average purchase amount
- **Repeat buyers and subscriptions:** about 27.6% of repeat buyers subscribe vs 27% overall, so there is no meaningful link
- **Most purchased items:** Jewelry (Accessories), Pants and Blouse (Clothing), Sandals (Footwear), Jacket (Outerwear)

Differences in spend are small across most groups, so these are descriptive patterns rather than statistically tested conclusions.

## 📊 Dashboard Preview
![Customer Dashboard](Customer-Dashboard.png)

## 📂 Files
- `Customer_Shopping_Behaviour_Analysis (1).ipynb` — data cleaning and feature engineering
- `Customer_Behaviour_Final_code.sql` — SQL queries answering 10 business questions
- `Customer_Behaviour_PBI.pbix` — Power BI project file
- `customer_shopping_behavior.csv` — original dataset
- `Post_Python_customer_behaviour.csv` — cleaned dataset (output of the Python notebook)
- `Customer-Dashboard.png` — dashboard preview

## 💡 Project Takeaway
This project demonstrates how Python, SQL and Power BI can be combined to take raw customer data from cleaning, to analysis, to an interactive dashboard.

Through this project, I gained hands-on experience with data cleaning, feature engineering, SQL analysis (CTEs, window functions, CASE segmentation), KPI development, dashboard design and communicating business insights.
