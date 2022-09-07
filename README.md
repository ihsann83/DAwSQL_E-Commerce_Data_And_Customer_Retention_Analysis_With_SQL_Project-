# DAwSQL_E-Commerce_Data_And_Customer_Retention_Analysis_With_SQL_Project-

An e-commerce organization demands some analysis of sales and delivery processes. 
Thus, the organization hopes to be able to predict more easily the opportunities and 
threats for the future.
You are asked to make the following analyzes for this scenario by following the 
instructions given

# Introduction


- You can benefit from the ERD diagram given to you during your work.

- You have to create a database and import into the given csv files. 
(https://www.youtube.com/watch?v=14FpoXKTEJw)

- During the import process, you will need to adjust the date columns. You need 
to carefully observe the data types and how they should be.In our database, a 
star model will be created with one fact table and four dimention tables.

- The data are not very clean and fully normalized. However, they don't prevent 
you from performing the given tasks. In some cases you may need to use the 
string, window, system or date functions.

- There may be situations where you need to update the tables.

- Manually verify the accuracy of your analysis.

OPTIONAL: You can clean and normalize the data, change the data types of some 
columns, clear the id columns, and assign them as keys. Then you can create the data 
model.

# Analyze the data by finding the answers to the questions below:


1. Join all the tables and create a new table with all of the columns, called 
combined_table. (market_fact, cust_dimen, orders_dimen, prod_dimen, 
shipping_dimen)

2. Find the top 3 customers who have the maximum count of orders.

3. Create a new column at combined_table as DaysTakenForDelivery that 
contains the date difference of Order_Date and Ship_Date.

4. Find the customer whose order took the maximum time to get delivered.

5. Count the total number of unique customers in January and how many of them 
came back every month over the entire year in 2011

6. Write a query to return for each user the time elapsed between the first 
purchasing and the third purchasing, in ascending order by Customer ID.

7. Write a query that returns customers who purchased both product 11 and 
product 14 as well as the ratio of these products to the total number of products 
purchased by the customer.


# Customer Segmentation


Categorize customers based on their frequency of visits. The following steps will 
guide you.

1. Create a view that keeps visit logs of customers on a monthly basis. (For each 
log, three field is kept: Cust_id, Year, Month)

2. Create a view that keeps the number of monthly visits by users. (Separately for 
all months from the business beginning)

3. For each visit of customers, create the next month of the visit as a separate 
column.

4. Calculate the monthly time gap between two consecutive visits by each 
customer.

5. Categorise customers using average time gaps. Choose the most fitted labeling 
model for you.

For example: 

o Labeled as churn if the customer hasn't made another purchase in the 
months since they made their first purchase.

o Labeled as regular if the customer has made a purchase every month.

# Month-Wise Retention Rate

Find month-by-month customer retention ratei since the start of the business.

There are many different variations in the calculation of Retention Rate. But we will 
try to calculate the month-wise retention rate in this project.

So, we will be interested in how many of the customers in the previous month could 
be retained in the next month.

Proceed step by step by creating views. You can use the view you got at the end of 
the Customer Segmentation section as a source.

1. Find the number of customers retained month-wise. (You can use time gaps)

2. Calculate the month-wise retention rate.

o Month-Wise Retention Rate = 1.0 * Total Number of Customers in The Previous 
Month / Number of Customers Retained in The Next Nonth

