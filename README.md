# Retail Sales & Profitability Analysis

Exploratory data analysis of retail order data in Python, focused on what drives profit: product categories, discounting, regions, customers and shipping.

## Overview

This project analyses a retail orders dataset of 9,994 order lines and 21 columns, covering orders from 2014 to 2017 across the United States. The data has no missing values and no duplicate rows, so the work goes straight into analysis.

The notebook answers a handful of business questions:

- Which categories and sub-categories actually make money, not just revenue?
- How much do discounts hurt profit, and at what level does it turn negative?
- Which states and regions lose money?
- Who are the most profitable customers and what do they buy?
- How are sales distributed over the year, and how fast do orders ship?

Reusable helper functions (`profit_by`, `discount_impact`, `state_profibility`, `top_customer`, `top_customer_purchase`) group the data and calculate total sales, total profit, order count, profit margin and average order value for any column.

Overall, the dataset totals roughly $2.30M in sales and $286K in profit, a margin of about 12.5%.

## Key Findings

1. **Furniture sells a lot but earns very little.** Technology (17.4% margin) and Office Supplies (17.0%) are healthy, while Furniture generates about $742K in sales with only a 2.5% margin ($18K profit).

2. **Some sub-categories lose money.** Tables (-$17.7K, -8.6% margin), Bookcases (-$3.5K) and Supplies (-$1.2K) are unprofitable. Machines bring in $189K in sales but only a 1.8% margin. The top earners are Copiers ($55.6K profit at 37.2% margin from just 68 order lines), Phones ($44.5K) and Accessories ($41.9K).

3. **Discounts above 20% destroy profit.** Margin is 29.5% with no discount, 16.6% at 10% off and 11.8% at 20% off. From 30% off it turns negative (-10.1%) and keeps falling, down to about -180% at an 80% discount. Furniture has the highest average discount (17.4%), and Tables average 26%, which explains their losses.

4. **Ten states are operating at a loss.** Texas (-$25.7K), Ohio (-$17.0K), Pennsylvania (-$15.6K) and Illinois (-$12.6K) are the biggest drags, followed by North Carolina, Colorado, Tennessee, Arizona, Florida and Oregon. California ($76.4K) and New York ($74.0K) lead in profit.

5. **A few customers are extremely profitable.** The top customer, Tamara Chand, produced about $9.0K profit at a 47% margin. Top customers typically have margins of 40% or more, often driven by a few large Copier or Phone orders.

6. **Sales are strongly seasonal.** September, November and December are the peak months, with the single best month being November 2017 (about $118K). January and February are consistently the weakest.

7. **Shipping times are consistent across regions.** Same Day ships in 0 days, First Class in 2, Second Class in 3 and Standard Class in 4 days (about 5 in the West).

## Tools & Tech Stack

- **Python 3:** core language
- **pandas:** data loading, cleaning, date handling and aggregation
- **seaborn:** statistical visualisations (bar, line and scatter plots)
- **matplotlib:** figure layout and customisation (dual-axis charts)
- **Jupyter Notebook:** interactive analysis environment