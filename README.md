# Power_BI_in_Financial_Analysis

![Financial Analysis](Cover.jpeg)

## Introduction
This project is to display Financial Analysis using POWER BI. The problem satatement is an imaginary case scenario I thought about after seeing the dataset.

## Problem Statement
A financial manager in an international company in the United States wishes to automate financial income statement and have a dynamic report clarify the revenue and gross margin up to date.

After discussion with him he approved to apply Six dashboards:
1. Revenue& Gross Margin using drill through to go to order details dashboard.
2. Income Statement with applying:
   - Vertical Analysis: clearing the percentage of each account vs gross margin called.
   - Horizontal Analysis: clearing the percentage of variance Month over Month .
3. Financial Simulation: applying What If? analysis to measure and evaluate the change in QTY, Unit Price, Cost and Expenses and the effect on Operating Income.
4. Revenue Analysis
5. Gross Margin key Influencers

## Data Sourcing
 the information was categorically seperated into differnt sheets or tables resulting into 5 tables:
- Account Headers
- Accounts
- Expenses
- Product
- Revenue




Data was then locally extracted from Excel Workbook into Power BI for transformation, analysis and visualization.

## Data Transformation

Data cleaning was performed per table.
The table appeared to be clean.
The quality of each column is 100% with no error or nulls.
Below is a preview of the tables:

Account Header Table             |           Account Table
:--------------------------:|:------------------------:
![](AccountHeaderTB.png)          |         ![](AccountTB.png)

Products Table              |         Expenses Table
:---------------------------:|:----------------------
![](ProductTB.png)             |     ![](ExpensesTB.png)


**Revenue Table**
![](RevenueTB.png)

For the Revenue and Expenses Tables, first rows were not headers and so resolved that by applying the "Use First row as header" action.
column datatypes were validated appropriately , also removed unnecessary columns.
For Product table we cleaned Product ID to validate Product ID in Revenue Table 

## Data Model Design
The data required for this analysis are located in various tables.
Therfore, appropriate modelling is required.
A star Schema is designed with the Revenue and Expenses Table representing the fact table containing all redundant data, and to which other dimension tables are modelled or connected to, using the column that is common. Date Table was created using CALENDARAUTO() Dax Function 
Revenue & Expenses Table has been modelled with:
- Revenue Table using the "Revenue Account ID"
- Expenses Table using the "Account ID"
- Date Table using the "Date"
- Product Table using "Product ID"
- Account Tables via "Account ID"
- AccountHeader Tables via "Header ID"

![model](Data Modelling.png)


## Data Aanalysis/ Visualization
Analysis was done using simple visuals since the tables have been perfectly modelled together.
Applied some Dax Function to get the required information

## Revenue and Margin

![](Revenue_Margin.png)

#### Company had Operational revenue over than 9M dollars with Gross margin over than 4M dollars represent 42% of Operational revenue.
While the highest revenue and Gross margin achieved on November, January had the highest % gross margin with 42%.
#### Retail Team had the highest Revenue with over than 4M dollars. Can easily notice that Food Category contributed over than 3M dollars.
#### Although Two Brother Mill Supplier had the highest revenue and gross margin with over than 5M and 1M dollars respectively , Kappa Drinks had the 
highest % of gross Margin 56% due to imported wine with gross margin of 70%.

I then had to drill down the Supplier to know the exact Group with the highest % gross margin in Kappa Drinks.

![](Revenue_Margin_2.png)

With further visual analysis, It is interesting to create dynamic income statement in Power BI adding Vertical and Horizontal Analysis.

## Income Statement

![](salesorganic.PNG)

Hmmm! Now we can notice that January has the minimum cost of sales which cause the increasing in gross margin % in January than November
We should be careful while checking Month over Month Horizontal analysis "% MOM HA" in Cost of sales & Operating Expenses that the decresing ⬇️ (-) sign means
increasing in Cost of sales & Operating Expenses as they are in negative sign and they cause decreasing gross revenue and gross margin.
For example Cost of sales had increased in February by about 121% than January its goes up from (148,107) to (327,834) 

![]()

Morris Garcia has the highest sales.

## Financial Simulation

![]()

.

## Conclusions/Recommendations
- ** ** 
- ** ** 
- ** ** 
------



###### My goal is to provide value to the stakeholders and not just to build reports and dashboard. 

Thank you.

