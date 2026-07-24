# Ques 1

## Aim
To delete specific records from a table.

## Question
Delete the specified customer record and display the remaining orders.

## Query
```sql
DELETE FROM Customers WHERE customer_name = 'John Doe';
SELECT * FROM Orders;
```

## Output

![Output](Screenshot 2026-07-16 at 14.30.00.png)
