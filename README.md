# PowerBi_DashBoard
Created Dashboard using Power BI with Maven Market dataset.<br>
Maven Market Dashboard:

![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/abd684e4-e670-4418-8486-1b0242635e40)

Maven Market Has the Following Dataset:
1) Customers
2) Products
3) Regions
4) Return Data
5) Stores
6) Transaction Data<br>

# Cleaning and Preparing Data:
In this phase, to confirm all data types are accurate, we have created new columns based on existing data, such as in the Customer Table, where we have added a new column named "full_name" merging first_name and last_name, separated by space; added a new column named "birth_year" extracting the year from the birthdate column and formatting it as text, created a conditional column named "has_children"  which equals "N" if total children are 0, otherwise "Y". 
In Products table we used statistical tool to return the number of distinct product brands, followed by distinct product names. Added calculated column to get discounted price which equals to 90% of original retail price (formated as fixed decimal number and rounded to 2 digits), Replaced the null values with zeros.
In Stores Table, we made sure that headers have been promoted. added a calculated column named full_address by merging store city, state and country comma and space separated. I also added a calculated column named "area_code" by extracting the characters before the dash in phone.
In the calendar table, added the following columns: start of week, start of month, name of day, quarter of year, name of month, year.
For transaction Data, we added a new folder on desktop  containing both files and in powerbi we combined the files and removed the source column.<br>

![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/2e46a052-42fd-4bf3-a867-e7c8ed1561b0)<br>

# Building Relationships:
 Created one-to-many relationship between Data(Fact) and Dimensions(Lookup) tables, Data going through only "Downstream"
 
![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/f7a2769b-1837-4f74-a9bc-7e91b3157f1d)<br>

# DAX Measures:
In Data view, we have added the following calculated columns:<br>

![image](https://github.com/Pradnya1111/PowerBi_DashBoard/assets/87003134/3c456af3-8e19-42f7-bb04-aec353c05fd6)<br>

# Visualizing Data:
Inserted the Matrix visual to show Total Transactions, Total Profit, Total Margin and Return Rate by Product Brand(Top N filter to show top 30 product brands by total transcations sorting  descending). Added KPI cards to show Total Transactions with start of month as trend axis and last month transaction as target goal, created two more copies for Total Profit and Total Returns(low is good).<br>
Added Map visual to show Total Transaction by store city, added selection controls menu in formatting pane to show Select All, also added Slicer.<br>
Added Treemap visual to break down Total Transactions by store country.
Added Gauge Chart to show Total Revenue against Revenue Target(Added visual level Top N filter to show latest start of month).








