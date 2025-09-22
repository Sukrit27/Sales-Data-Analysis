# Sales Data Analysis (SQL Project)

## About This Project
This is a project where I analyzed Walmart's sales data. My goal is to use SQL to explore sales patterns, identify high-performing branches and products, and understand customer behavior. The insights from this analysis could help in thinking about how to optimize sales strategies.

The dataset for this project comes from the Kaggle Walmart Sales Forecasting Competition. It covers sales transactions from three branches in Myanmar (Mandalay, Yangon, and Naypyitaw).

## About the Data
The dataset includes 1,000 rows of sales transactions with the following 17 columns:

| Column | Description | Data Type |
|---|---|---|
| invoice_id | Invoice ID for the sales transaction | VARCHAR(30) |
| branch | Branch where the sale occurred (A, B, or C) | VARCHAR(5) |
| city | The location of the branch | VARCHAR(30) |
| customer_type | Type of customer (e.g., Member, Normal) | VARCHAR(30) |
| gender | Gender of the customer | VARCHAR(10) |
| product_line | Category of the product sold | VARCHAR(100) |
| unit_price | The price of one unit of the product | DECIMAL(10, 2) |
| quantity | The number of units sold | INT |
| VAT | Tax on the purchase | FLOAT(6, 4) |
| total | The total cost of the purchase | DECIMAL(12, 4) |
| date | Date of the purchase | DATETIME |
| time | Time of the purchase | TIME |
| payment | Payment method used (e.g., Cash, Ewallet) | VARCHAR(15) |
| cogs | Cost Of Goods Sold | DECIMAL(10, 2) |
| gross_margin_pct | Gross margin percentage | FLOAT(11, 9) |
| gross_income | Gross income from the sale | DECIMAL(12, 4) |
| rating | Customer rating (1-10) | FLOAT(2, 1) |

## My Approach

### 1. Data Wrangling
I started by building a database and creating the `sales` table. When I created the table, I set all fields as `NOT NULL`, so no null value handling was required for this dataset.

### 2. Feature Engineering
To get more insights, I created new columns from the existing data:
* **`time_of_day`**: I added this column (Morning, Afternoon, Evening) to see which part of the day has the most sales.
* **`day_name`**: I added this column (e.g., Mon, Tue) to find out which days of the week are busiest.
* **`month_name`**: I added this column (e.g., Jan, Feb) to identify which months have the highest sales.

### 3. Exploratory Data Analysis (EDA)
With the data prepared, I performed the analysis by writing SQL queries to answer the questions listed below.

## Questions I Answered

### Generic Questions
1.  How many distinct cities are in the dataset?
2.  In which city is each branch located?

### Product Analysis
1.  How many distinct product lines are there?
2.  What is the most common payment method?
3.  What is the most-selling product line?
4.  What is the total revenue by month?
5.  Which month had the highest Cost of Goods Sold (COGS)?
6.  Which product line generated the highest revenue?
7.  Which city has the highest revenue?
8.  Which product line incurred the highest VAT?
9.  I added a `product_category` column ('Good'/'Bad') based on whether its sales were above the average.
10. Which branch sold more products than the average branch?
11. What is the most common product line broken down by gender?
12. What is the average rating for each product line?

### Sales Analysis
1.  What is the number of sales made in each time of day per weekday?
2.  Which customer type generates the highest revenue?
3.  Which city has the largest tax (VAT)?
4.  Which customer type pays the most in VAT?

### Customer Analysis
1.  How many unique customer types are there?
2.  How many unique payment methods are there?
3.  What is the most common customer type?
4.  Which customer type buys the most (by transaction count)?
5.  What is the gender of most of the customers?
6.  What is the gender distribution for each branch?
7.  During which time of day do customers give the most ratings?
8.  What is the average rating for each time of day, broken down by branch?
9.	Which day of the week has the best avg ratings?
10.	Which day of the week has the best average ratings per branch?

