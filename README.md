**SQL Project on Pizza Sales**

**Project Overview**

This project involves analyzing the sales data of a pizza restaurant to derive insights that can help improve business operations and profitability. The analysis covers basic metrics, intermediate evaluations, and advanced revenue analysis.

**Dataset**
The dataset consists of four main tables:

**pizza_types**

pizza_type_id (INT, PRIMARY KEY)
name (VARCHAR(100))
category (VARCHAR(50))
ingredients (TEXT)

**Pizzas**

pizza_id (INT, PRIMARY KEY)
pizza_type_id (INT, FOREIGN KEY references pizza_types(pizza_type_id))
size (VARCHAR(20))
price (DECIMAL(10, 2))

**Orders**

order_id (INT, PRIMARY KEY)
order_date (DATE)
order_time (TIME)

**order_details**

order_details_id (INT, PRIMARY KEY)
order_id (INT, FOREIGN KEY references Orders(order_id))
pizza_id (INT, FOREIGN KEY references Pizzas(pizza_id))
quantity (INT)

**Cardinality and Relationships**

pizza_types to Pizzas: 1
pizza_types is connected to Pizzas through pizza_type_id.
Pizzas to order_details: 1
Pizzas is connected to order_details through pizza_id.
Orders to order_details: 1
Orders is connected to order_details through order_id.
Analysis Objectives

**Basic Analysis:**
Retrieve the total number of orders placed.
Calculate the total revenue generated from pizza sales.
Identify the highest-priced pizza.
Identify the most common pizza size ordered.
List the top 5 most ordered pizza types along with their quantities.

**Intermediate Analysis:**
Join the necessary tables to find the total quantity of each pizza category ordered.
Determine the distribution of orders by hour of the day.
Join relevant tables to find the category-wise distribution of pizzas.
Group the orders by date and calculate the average number of pizzas ordered per day.
Determine the top 3 most ordered pizza types based on revenue.

**Advanced Analysis:**
Calculate the percentage contribution of each pizza type to total revenue.
Analyze the cumulative revenue generated over time.
Determine the top 3 most ordered pizza types based on revenue for each pizza category.
How to Use This Project
Setup the Database: Create the database and tables using the provided SQL schema.
Insert Data: Populate the tables with data relevant to the pizza sales.


**Run Queries:**

Execute the provided SQL queries to perform the analyses outlined in the objectives.
Analyze Results: Review the query results to gain insights into the pizza sales performance.

**Conclusion**
This project aims to provide a comprehensive analysis of pizza sales data to help the restaurant make informed, data-driven decisions. The detailed analysis covers basic order metrics, category-based evaluations, and advanced revenue analysis, offering valuable insights into customer preferences and sales trends.
