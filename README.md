# Online Retail II: Sales Dashboard

An interactive dashboard that shows how a UK online gift-ware shop sold over two years, and when and where its customers buy.

**Live dashboard:** [paste your GitHub Pages link here]

## Business question
When does the shop earn most of its revenue, which products and countries matter most, and when do customers place orders?

## Data
- Source: UCI Online Retail II (real transactions of a UK-based online shop, many customers are wholesalers)
- Period: 1 December 2009 to 9 December 2011
- Size: 1,067,371 rows and 8 columns (Invoice, StockCode, Description, Quantity, InvoiceDate, Price, Customer ID, Country)
- Licence: CC BY 4.0

## Data cleaning
Starting from 1,067,371 rows:
- Removed cancelled orders (invoice numbers starting with "C"): 1,047,877 rows left
- Removed rows with quantity or price of 0 or less: 1,041,670 rows left
- Removed exact duplicate rows: 1,007,913 rows left
- Kept rows with no Customer ID (about 15% of revenue), because they are real sales. They are left out only when counting customers.
- Left out 4,699 non-product rows (such as postage and manual entries) from the top products chart
- Added new columns: Revenue (quantity x price), Month, Day of week and Hour

## Key findings
- Total revenue is about £20.5 million from 40,077 orders and 5,878 customers with an ID. The average order is about £511.
- Sales rise every autumn. September to November are the strongest months, and November 2011 was the best month (about £1.50 million).
- The United Kingdom brings about 85% of revenue.
- The top 20% of customers bring about 77% of the revenue from customers with an ID.
- The best-selling product is the Regency Cakestand 3 Tier (about £331,000).
- Thursday is the busiest day, and the busiest hour is 12:00. Saturday has almost no orders (30 in two years).

## Dashboard pages
1. Overview: KPI cards and monthly revenue with the autumn season shaded
2. Products and countries: top 10 products and top countries outside the UK
3. When customers buy: heatmap of orders by day and hour

## What I would suggest to the business
- Plan stock and staff before September, because the busiest months follow.
- Look after the top customers, because a small group brings most of the revenue.
- Keep the customer ID filled in at checkout, so more sales can be linked to customers.

## Limits of this analysis
- December 2011 is a partial month (data ends on 9 December), so its drop is not a real fall in sales.
- Revenue is in pounds (£) and is not adjusted for returns beyond removing cancelled orders.

## Tools
Python (pandas) in a Jupyter notebook in VS Code for cleaning, then HTML, CSS and JavaScript with Chart.js for the dashboard, hosted on GitHub Pages.

## Files
- index.html: the dashboard
- 01_load_and_clean.ipynb: loading, cleaning and summary tables

## Author
Built by Sandun Lakshan Ranathunga, undergraduate in Business Analytics. [add your LinkedIn link here]
