# Northwind Data Visualizations
## Project Background

Northwind Traders is a fictional company specializing in the import and export of specialty food products. This project analyzes its sales data to uncover key insights and provide recommendations for enhancing profitability.

Insights and recommendations are provided on the following key areas:

+ **Sales Trend Analysis:** An evaluation of sales patterns and order profitability by region and product category.
+ **Employee Performance:** An assessment of individual employee sales performance.

A file holding the queries used to create the tables used and to perform other analysis can be found [here.](northwind_queries.sql) <br />
The interactive Tableau dashboards can be accessed [here.](https://public.tableau.com/app/profile/giovanni.pecorino/viz/NorthwindDashboards/SalesBreakdown?publish=yes)

## About the Dataset

The Northwind database contains 17 tables, of which only six were relevant for this analysis: *customers, categories, employees, orders, order_details,* and *products*. Together, these tables contain a total of 3,170 records.

![](images/erd.PNG)

## Executive Summary

### Overview of Findings

Month-to-month sales remain relatively stable, typically alternating between months of higher and lower sales—likely due to customers ordering less in the month following larger purchases. This pattern held consistently until the last four months, which saw a substantial 181% increase in sales. With 92.8% of all orders generating positive profits and this recent sales surge, the company is performing well and showing strong growth potential. The following sections will explore the factors driving recent performance and identify opportunities for further improvement. 

Below is a screenshot from the Tableau dashboard, with additional examples provided throughout the report. The complete interactive dashboard can be accessed and downloaded [here.](https://public.tableau.com/app/profile/giovanni.pecorino/viz/NorthwindDashboards/SalesBreakdown?publish=yes)
![](images/Northwind_sales.PNG)

## Insights

### Sales Trend Analysis

+ **Sales saw a dramatic 181.8% increase between November 1997 and April 1998.** Although there appears to be a sharp drop in May, this is due to April being the last month with complete data.
+ Sales follow a recurring peak-and-valley pattern, with an increase one month typically followed by a decrease the next. **Many customers alternate between high and low order volumes** rather than placing large orders consecutively.
+ The majority of sales come from **European customers, accounting for 61.1% of total sales.** The regional sales distribution has remained relatively consistent over the years.
+ Overall, **92.8% of orders are profitable, with an average profit of $116.49 per order.** However, only 1% of orders yield profits of $1,000 or more.
+ Quick-Stop, Ernst Handel, and Save-a-lot Markets are the top three customers in lifetime sales and profits, each with order volumes nearly double that of the fourth-highest customer. **Quick-Stop ranks as the top customer, with total spending of $110,277.31 and generating $23,695.71 in profit.**
+ **Beverages and dairy products are the top-performing categories, accounting for 21.2% and 18.6% of total sales, respectively.** In contrast, grains/cereals and produce are the lowest-performing categories, together contributing only 15.5% of total sales.
+ **Grains/cereals and produce are the lowest-selling categories in North and South America**, likely due to the robust agricultural industries in these regions, which allow for local sourcing of these products.
+ Côte de Blaye leads in both sales and profits, with lifetime sales of $141,396.73 and profits of $34,725.14. **Camembert Pierrot, Raclette Courdavault, and Gorgonzola Telino are the most frequently ordered products, with Camembert Pierrot selling 1,577 units compared to Côte de Blaye's 623 units.** At the other end, Chocolade is the least profitable product, generating only $160.25 in profits, while Mishi Kobe Niku is the least ordered, with just 95 units sold.
+ **Raclette Courdavault has the highest profit margin per unit at 66.07%,** followed closely by Singaporean Hokkien Fried Mee at 63.56%.
+ **The top countries by order volume and profit are the USA, Germany, Austria, Brazil, and France**, with the USA leading in both categories. Brazil represents the largest customer base in the South American market. In contrast, Norway and Poland rank lowest in both order volume and profit.

![](images/Northwind1.PNG)

### Employee Performance

+ Margaret Peacock is the top-performing sales representative overall. Although she currently ranks third in sales for 1998, **she held the #1 spot for the previous two years and has the highest cumulative sales.** So far in 1998, Janet Levering leads in total sales.
+ Steve Buchanan, Michael Suyama, and Anne Dodsworth consistently rank as the lowest-performing employees across all years. In 1998, Steve Buchanan and Michael Suyama were the lowest earners, bringing in just $20,000 and $14,000, respectively. Anne Dodsworth, however, shows signs of improvement, generating $41,000 in sales within the first four months—**a 57.7% increase over her total sales from the previous year.**
+ **Nancy Davolio has the highest sales with South American customers, with 71.8% of these sales occurring in 1998.** However, this figure may be skewed by a particularly large order placed in March. Additional time and data are needed to determine if this represents a lasting trend.

![](images/Northwind2.PNG)

## Recommendations

Based on the insights and findings above, the following recommendations have been provided:

+ Consider implementing promotions and discounts in the months following periods of high order volume to boost sales during dips. Additionally, offering discounts to customers in regions with lower sales could incentivize purchases. **Products with a profit margin of 50% or greater, such as Raclette Courdavault and Singaporean Hokkien Fried Mee, would be ideal candidates for discounts, as this strategy could stimulate sales without significantly affecting overall profitability.**
+ **Assign Margaret Peacock to oversee sales in low-performing regions such as Norway and Poland.** As the top sales representative, she has the potential to drive greater value in these areas compared to other representatives.
+ There was a significant increase in South American sales at the beginning of 1998, driven by Nancy Davolio. **If this trend continues, consider appointing her as the primary sales representative for South American clients.**
+ Steve Buchanan and Michael Suyama are the lowest-performing employees. **If the company needs to downsize, they may be the most expendable sales representatives.**


## Assumptions and Caveats

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:

+ There was a significant drop in sales from April to May 1998. For this analysis, it is assumed that the data ends in early May, and sales figures for the entire month of May are not included.
+ The profit and profit margin data for products was generated specifically for this analysis, as the original Northwind database did not include profit information for each order. To facilitate this level of analysis, I made two key assumptions. First, I assumed that the prices listed in the dataset reflect the selling price that Northwind Traders charges consumers. Second, I estimated that the profit margins for each product range from 10% to 40%. These margins were based on available information regarding average profit margins for real import/export companies. I then randomly assigned values within this range to each product to determine the cost incurred by Northwind Traders for each unit purchased from suppliers.

## Technologies

+ PostgreSQL: Used to create queries for the database
+ Tableau: Used to create visualizations and dashboards

