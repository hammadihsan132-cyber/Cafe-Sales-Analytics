**Cafe Sales Analytics Notebook README**

**Overview**

This Jupyter Notebook (Cafe_Sales_Analytics.ipynb) performs data cleaning, transformation, and exploratory data analysis (EDA) on a cafe sales dataset. The dataset starts as a "dirty" CSV file (dirty_cafe_sales.csv) containing inconsistencies, missing values, and incorrect data types. The notebook cleans the data, calculates key metrics like revenue, and generates insights such as total sales, top-selling items, trends over time, and busiest days. Finally, it exports a cleaned version of the dataset (clean_cafe_sales.csv).

**The analysis focuses on:**

Sales revenue and transaction patterns.
Item performance (e.g., top sellers by quantity and revenue).
Trends by month, day, location, and payment method.
Visualizations for monthly and daily sales trends.

This notebook is useful for data analysts or cafe owners looking to derive actionable insights from sales data.
Requirements

**Python Version: Python 3.x (tested on 3.12.3 in Google Colab).**

**Libraries:**

pandas (for data manipulation).
numpy (for numerical operations).
matplotlib (for plotting).
seaborn (for enhanced visualizations).

**Environment:** 

The notebook is designed for Google Colab but can run in any Jupyter environment. No additional installations are needed in Colab as the libraries are pre-installed.
Input Data: dirty_cafe_sales.csv (a CSV file with cafe sales records, including columns like Transaction ID, Item, Quantity, Price Per Unit, etc.).

**If running locally, install dependencies via:**

textpip install pandas numpy matplotlib seaborn
Usage

**Setup:**

Place dirty_cafe_sales.csv in the working directory (e.g., /content/ in Colab).
Open the notebook in Jupyter or Google Colab.

**Run the Notebook:**

Execute cells sequentially.
The notebook loads the data, cleans it, performs analysis, generates plots, and exports the cleaned CSV.
Key outputs include printed summaries (e.g., total revenue, top items) and visualizations (plots saved as PNG files).

**Key Sections:**

**Data Loading and Inspection:** 

Loads CSV, checks shape, info, description, and missing values.

**Data Type Conversion:**

Converts Quantity, Price Per Unit, Total Spent to numeric; Transaction Date to datetime.

**Handling Missing Values:** 

Fills non-critical missing values (e.g., Payment Method, Location) with "Not Specified"; drops rows missing 

**Quantity or Price Per Unit.**
Item	Price   Per Unit
0	    Cake	     3.0
1	    Coffee	  2.0
2	    Cookie	  1.0
3	    ERROR  	  1.5
4	    Juice	    3.0
5	    Salad	    5.0
6	    Sandwich	4.0
7	    Smoothie	4.0
8	    Tea	      1.5
9	    UNKNOWN	  3.0
10	   Unknown	3.0

**Data Cleaning:**

Calculates accurate Revenue (Quantity * Price Per Unit), removes duplicates.

**Feature Engineering:**

Extracts Year, Month, Day, and Day_Name from Transaction Date.

**Analysis and Insights:** 
From the analysis we get insights that which item sell more and what are the busy days in week and form wich product e get more revenew and which product have less sale so all these insights are very useful for business.

**Total revenue.  $80478.5**

**Top-selling items (by quantity and revenue).**
	     
**Item**	     **Revenue**
Salad	    15600.0
Sandwich	12296.0
Smoothie	12132.0
Juice	    9561.0
Cake	    9540.0
Coffee	  6424.0
Tea	      4431.0
Cookie	  2898.0
Unknown	  2651.0
UNKNOWN	  2550.0
ERROR	    2395.5


**Revenue distribution by location and payment method.** 
<img width="587" height="515" alt="image" src="https://github.com/user-attachments/assets/1b8f7d7c-6ed1-4136-8811-1824308e31c1" />

**REVENUE BY LOCATION**

**Location**	     **Revenue**
Not Specified	  26606.5
In-store	      24598.0
Takeaway	      23868.0
ERROR	          2906.0
UNKNOWN	        2500.0

**REVENUE BY PAYMENT MEMTHOD**

**Payment**        **Method**	
Not Specified	  2310
Digital Wallet	2068
Credit Card	    2047
Cash	          2044
ERROR          	271
UNKNOWN        	266


**Monthly sales trend (line plot).**

**Busiest day of the week** (e.g., Monday identified as busiest).

**Export:** 

Saves cleaned data to clean_cafe_sales.csv and prompts download (in Colab).
Reload and Verify: Loads the cleaned CSV for final info and description checks.

**Outputs:**

Cleaned CSV: clean_cafe_sales.csv (contains 9006 rows after cleaning, with added columns like Revenue, Year, Month, Day, Day_Name).
Visualizations:
Monthly Sales Trend (line plot, saved as monthly_sales_trend.png).
Daily Sales Trend (bar plot, saved as daily_sales_trend.png).

Printed Results: Summaries like total revenue (~80,478), top items (e.g., Coffee as top seller), average transaction (~8.94), etc.


**Data Description**

**Input File: dirty_cafe_sales.csv**

**Rows:** 10,000 (original, before cleaning).

**Columns:** 8 (Transaction ID, Item,Quantity, Price Per Unit, Total Spent, Payment Method, Location, Transaction Date).
Issues: Missing values, incorrect data types (e.g., strings instead of numerics), inconsistent totals, duplicates.

**Cleaned File: clean_cafe_sales.csv**

**Rows:** 9,006 (after dropping invalid rows and duplicates).

**Columns:** 13 (original + Revenue, Year, Month, Day, Day_Name).

All critical columns are numeric/datetime; missing non-critical values filled.

**Key Statistics from Cleaned Data:**

Total Revenue: 80,478.

Average Quantity per Transaction: ~3.02.

Average Price Per Unit: ~2.95.

Average Total Spent (Revenue): ~8.94.

Data covers the year 2023 only.

Top Item by Quantity: Cookie (total quantity: 5,496).

Top Item by Revenue: Salad (revenue: 15,025).

Busiest Day: Monday (1,328 transactions).
