# Ques 1

## Aim
To retrieve records that do not exist in another table.

## Question
Find products that have never been sold.

## Query
```sql
SELECT product_id, product_name
FROM inventory_current_stock
WHERE product_id NOT IN(
    SELECT product_id
    FROM sales_transactions
);
```

## Output

![Output](Screenshot 2026-07-16 at 14.16.34.png)
