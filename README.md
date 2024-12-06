# SuperStore-Dataset-MSExcel
This is the project for analysis of SuperStore Dataset using MSExcel.
**If you're practicing with same dataset and found yourself confused solving these questions then my friend, I got you. I will try to explain as much in details as possible.**

## Problem Statement
This project contains data related to SuprerStore Orders list. The dataset consists order list Of various products with details like Order ID, Order Date, Shipping Date and so on. As a data analyst, your task in hand is to find suitable approach to solve the problems given in the attached file.

## Requirements
To solve questions of this dataset you need to know the working knowledge of the following:

**Softwares**

- MS Excel

**Functions/Formulas**

- SUMIF
- LEFT, RIGHT, MID and FIND
- CONDITIONAL FORMATTING
- XLOOKUP
- DATEDIF
- IFS
- FILTER and SORTING
- PIVOT TABLE and PIVOT CHARTS

## Solutions and Approachs
In this project we will try find the solutions of all 8 questions asked in this given dataset.

**Q1: Calculate the total profit for each Order ID given below by summoning profits across all rows with the same ID.**

**A1** ![Screenshot 2024-12-02 134554](https://github.com/user-attachments/assets/97581501-6a2d-4d68-99b2-a98c1a16e8ac)

- This is very simple, we need to apply **SUMIF** to find total sum of profits for a single Order ID.

**Q2: Find the number of days between the Order Date and Ship Date for first 50 orders. Highlight orders shipped in less than three days using conditional formatting.**

**A2** ![Screenshot 2024-12-02 134903](https://github.com/user-attachments/assets/c34b0fed-9340-47b3-b93c-fb6c6227c289)

- To find the number of days, we will use **DATEDIF**. Now DATEDIF function is hidden in Excel because its one of the Excel legacy functions, if you don't know the syntax then here it is =DATEDIF(start_date, end_date, unit) where unit is "D", "M", "Y".
- After we select the Shipping days column we created, click on Conditional Formatting under Home Tab.
- Then select Highlight cell rules > Less than > type 3 in the option > format as you need and hit ok.


**Q3: Extract the first two letters of each Manager name from the Managers sheet and create a new table with these abbreviations.**

**A3** ![Screenshot 2024-12-02 133935](https://github.com/user-attachments/assets/7716a07e-c67b-4137-955b-992483f64cee)

- Now this is an interesting one, here we will use combo of LEFT, MID and FIND functions.
**I've explained the formula in the SuperStore Dataset - Solved file, MAke sure to check it out.**

**Q4: Use the Returns sheet to identify which orders in the given list were returned. Add a Returned? column to the Orders sheet with "Yes" or "No" values.**

**A4** ![Screenshot 2024-12-02 135025](https://github.com/user-attachments/assets/54837c92-6246-4f69-9c35-9e90c8e0074a)

- To solve this we will use XLOOKUP, where 
- lookup value - Order IDs given
- lookup array - Order ID column from Returns sheet
- return array - Returned column from Returns sheet
- last fields  - 0 and 1.

**Q5: In the Orders sheet, take first 500 orders classify these orders as "High Profit", "Medium profit" and "Low Profit" based on the Profit column. If the profit is greater than $150 label it as High Profit, if the profit is between $150-$50 label it as Medium Profit and else Low Profit.**

**A5** ![Screenshot 2024-12-02 135553](https://github.com/user-attachments/assets/4ce45421-d56c-4245-928d-fc1986e7b0a8)

- Here we will use IFS with the logic of,
- If Profit > 150 then High Profit
- If Profit >= 50 then Medium Profit
- If Profit < 50 then Low Profit.

**Q6. Filter to display only orders with a Profit greater than $1000. Sort the Orders sheet by Order Date fron oldest to newest.**

**A6** ![Screenshot 2024-12-02 135650](https://github.com/user-attachments/assets/6476079a-614d-4e13-8b6c-a873a8344072)

- First copy paste Order ID, Region, Order Date and Profit regions from Orders sheet.
- Apply filters from Home Tab to the header cells of the columns.
- Click on the filter of Profit column, select Number Filters then click Greater than and enter 1000 in the field, Hit ok.
- Click on the filter of Order Date column and sort from Oldest to Newest.

**Q7: Create a pivot table showing total Sales by Region and Category from the Orders sheet. Use this data to identify the highest-grossing category in each region. Based on the pivot table, create a clustered bar chart to compare sales across categories for each region.**

**A7** ![Screenshot 2024-12-02 135724](https://github.com/user-attachments/assets/9cb73bc8-7636-492f-ad0a-3681afd67132)

- From Insert Tab click on Pivot Tables, add Orders table in Range field, select the cell where you want the Pivot table and hit ok.
- Add Regions to rows, Category to columns and Sales in values.
- From PivotTable Analyse click on Pivot Chart, select clustered column chart.
- Format the table and chart as you prefer.

**Q8: From the Orders sheet take first 2000 orders, highlight rows where the Profit is negative or where the Discount exceeds 0.5.**

**A8** ![Screenshot 2024-12-02 135844](https://github.com/user-attachments/assets/19595e2f-bc7f-4875-8347-bd938081210a)

This is very simple:
- Select the Profit column > Click on Conditional Formatting and select Less Than > Enter 0 in the field and choose the format as you prefer.
- Select the Discount column > Click on Conditional Formatting and select Grater Than > Enter 0.5 in the field and choose the format as you prefer.