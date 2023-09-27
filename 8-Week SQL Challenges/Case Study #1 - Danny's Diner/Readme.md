![image](https://github.com/AnhDuyVu/Data-Analysis-Projects/assets/119872105/4ffc02fb-0375-47d0-9146-69fbf9beab3f)

## Table of Contents
- [Problem Statement](#Problem-Statement)
- [Entity Relationship Diagram](#Entity-Relationship-Diagram)
- [Questions and my solutions](#questions-and-my-solutions)

All source data is in link: [here](https://8weeksqlchallenge.com/case-study-1/). 

# Problem Statement

Danny seriously loves Japanese food so in the beginning of 2021, he decides to embark upon a risky venture and opens up a cute little restaurant that sells his 3 favourite foods: sushi, curry and ramen.


Danny’s Diner is in need of your assistance to help the restaurant stay afloat - the restaurant has captured some very basic data from their few months of operation but have no idea how to use their data to help them run the business.


Danny wants to use the data to answer a few simple questions about his customers, especially about their visiting patterns, how much money they’ve spent and also which menu items are their favourite. He plans on using these insights to help him decide whether he should expand the existing customer loyalty program - additionally he needs help to generate some basic datasets so his team can easily inspect the data without needing to use SQL.


Danny has provided us with a sample of his overall customer data due to privacy issues - but he hopes that these examples are enough for us to write fully functioning SQL queries to help him answer his questions.

# Entity Relationship Diagram  
![image](https://github.com/AnhDuyVu/Data-Analysis-Projects/assets/119872105/b542d482-5671-4c6d-97c7-117eb769bd9d)

# Questions and my solutions

**1. What is the total amount each customer spent at the restaurant?**

````sql

Select sales.customer_id,
sum(price) as total_spent
from dannys_diner.sales as sales
join dannys_diner.menu as menu on sales.product_id = menu.product_id
group by sales.customer_id
order by sales.customer_id asc;

````

