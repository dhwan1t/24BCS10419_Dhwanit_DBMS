# Ques 2

## Aim
To retrieve data using JOIN operations.

## Question
Find the mutual friend between Karl and Hans.

## Query
```sql
SELECT u.user_id, u.user_name
FROM users u
JOIN friends f1
ON u.user_id = f1.friend_id
JOIN friends f2
ON u.user_id = f2.friend_id
WHERE f1.user_id = (
    SELECT user_id
    FROM users
    WHERE user_name = 'Karl'
)
AND f2.user_id = (
    SELECT user_id
    FROM users
    WHERE user_name = 'Hans'
);
```

## Output

![Output](./Screenshot%202026-07-16%20at%2014.19.13.png)
