# Ques 1

## Aim
To rank records using the DENSE_RANK window function.

## Question
Find the top-ranked customers based on purchase value.

## Query
```sql
SELECT *
FROM (
    SELECT
        customer_id,
        total_purchase_value,
        DENSE_RANK() OVER (
            ORDER BY total_purchase_value DESC
        ) AS customer_rank
    FROM customer_purchase
) t
WHERE customer_rank <= 5;
```

## Output

![Output](./Screenshot%202026-07-16%20at%2014.22.59.png)
