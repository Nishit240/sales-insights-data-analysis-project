Data Analysis Using Power BI
============================
## Sales Insights Data Analysis Project

### Instructions to setup mysql on your local computer

1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer and import it as per instructions given in the tutorial video

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`



Screenshot:
============================
Total Revenue
![Screenshot 2025-03-28 193604](https://github.com/user-attachments/assets/9e6d37db-c073-45eb-8bc8-59b9b0456605)
============================
Revenue of 2017
![Screenshot 2025-03-28 193613](https://github.com/user-attachments/assets/ba2721a9-3632-47a0-a71c-1d4f2f2dc891)
============================
Revenue of 2018
![Screenshot 2025-03-28 193620](https://github.com/user-attachments/assets/3502eeb8-7ac5-419d-89e5-db62d999ef17)
============================
Revenue of 2019
![Screenshot 2025-03-28 193635](https://github.com/user-attachments/assets/4b75d551-3517-4d30-8360-ef6c26eb522d)
============================
Revenue of 2020
![Screenshot 2025-03-28 193654](https://github.com/user-attachments/assets/a082a495-f7f8-4323-b1e3-042694136a06)
============================


