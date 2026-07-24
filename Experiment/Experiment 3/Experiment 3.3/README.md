# Experiment 3.3

## Aim
To retrieve the names of customers who have never placed an order using a subquery in SQL.

## Question
Write an SQL query to find the names of all customers who have never placed any order.

## Query

```sql
SELECT name AS Customers
FROM Customers
WHERE id NOT IN (
    SELECT customerId
    FROM Orders
);
```

## Output

![Output](./Screenshot%202026-07-24%20at%2012.24.49.png)