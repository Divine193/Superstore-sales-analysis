# Superstore-sales-analysis

## Description
This project involves analysing  sales data from a superstore using Excel, SQL and powerBI. I used Excel for data entry and initial cleanup, SQL for querying the sales database, and powerBI for creating visual reports

## Table of Contents
- [Requirements](#requirements)
- [Data Sources](#data-sources)
- [Excel Data Cleanup](#excel-data-cleanup)
- [SQL Queries](#sql-queries)
- [PowerBI Reports](#powerbi-reports)
- [Conclusion](#conclusion)
- [License](#license)
  
 ## Requirements 
- SQL Server or another SQL database system 
- Excel
- PowerBI Desktop

## Data Sources
We have three primary data sources: 
1. **Sales Data**: Entered and cleaned in Excel.
2. **Sales Database**: SQL database containing detailed sales records.

## Excel Data Cleanup
I used Excel for the initial data entry and to clean the raw sales data.
- [Superstore-data](Projects/Sample-Superstore.xlxs) : The sales dataset

## SQL Queries
After cleaning the data with Excel, we imported it into the SQL database and used various SQL queries to analyze it.

- Total Sales and Profit by Region
 ```code
select region, sum(sales) total_sales, sum(profit) total_profits 
from superstore 
group by 1;
```

- BEST SELLING AND MOST PROFITABLE PRODUCTS AND THEIR SUB CATEGORIES
```code
select product_name, Sub_Category,  sum(sales), sum(profit), (sum(profit) / sum(sales) * 100) profit_percent
from superstore
group by 1,2
order by 4 desc;
```
## PowerBI Reports
Using the data extracted with SQL, I created PowerBI reports to provide visual insights into the sales performance. The PowerBI dashboards include:

Overall Sales Performance: Displays total sales, sales by categories, and sales by region
Customer Analysis: Displays best selling customers, most profitable cusstomers

- Sample Dashboard
## [Sales Dashboard](Sales_project_images/Overall_Sales_dashboard.jpg)

## Insights:
- The Consumer segment emerged as the top perforing segment over the years.
- Top performing categories by sales were Technology followed by Furniture then Office Supplies while the top performing categories by profits were Technology followed by Office supplies then Furniture.
- Copiers, Phones, Accessories, Binders, Chairs, Storage, and Appliances were among the best selling and most profitable Sub-categories
- A lot of products from the Copiers, Binders, Machines, Chairs, and Supplies Sub-category emerged as the best selling products with Canon imageCLASS 2200 Advanced Copier being the top performer both in Sales and profits.
- The Top performing states by sales were California, New York, Texas, Washington and Pennsylvania, Despite being Top performers in sales, Texas and Pennsylvania were the least profitable states due to the large discounts awarded to those states.
- The best purchasing customers bought goods from the Copiers, Binders and Machines. Sean Miller was the best purchasing customer but he was the least profitable because he bought low end products that require a high cost of maintenance.
- Cisco TelePresence System EX90 Videoconferencing Unit was the least profitable product despite having high demand, This is due to the high cost of maintaining the machine, which reduces the profit that would have been made on the goods.
- Due to the growth of sales in the past years according to the data given, sales are expected to grow exponentially in the coming years while profits increase gradually.


## Conclusion
By utilizing Excel for initial data handling, SQL for data querying, and PowerBI for visual reporting, we effectively analyzed our sales data. This integrated approach provided actionable insights into our sales performance, customer behavior, and employee productivity, leading to informed business decisions.

## License
No licenses.

## Contact
Maintainer - Divinefavour 

```

This example incorporates Excel for initial data entry and cleanup, SQL for data extraction and transformation, and PowerBI for visualization, showcasing how these tools can work together in a comprehensive sales data analysis project. If you have any questions or need further details, feel free to ask!
