## Sales Data Analysis with SQL and Power BI

### Run Locally

Clone the project

```bash
  https://github.com/srigowri-12/Sales-Data-Analysis.git
```

Go to the project directory and open ``` .pbix ``` file with Microsoft Power BI Desktop

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


Power BI Dashboard Preview
============================

![Page1](https://github.com/srigowri-12/Sales-Data-Analysis/blob/43018e738a1610d973c9e1eea7e1b31fc4a2498d/Sales-key-insight.png)
![Page2](https://github.com/srigowri-12/Sales-Data-Analysis/blob/4deac907cf41668ddb8e1643ab4cc90fbed60907/sales-profit-analysis.png)
![Page3](https://github.com/srigowri-12/Sales-Data-Analysis/blob/4deac907cf41668ddb8e1643ab4cc90fbed60907/sales-performance-insight.png)



