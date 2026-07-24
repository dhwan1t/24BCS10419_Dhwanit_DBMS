# Ques 2

## Aim
To calculate a rolling average using window functions.

## Question
Calculate the 3-day rolling average of tweet counts.

## Query
```sql
SELECT
    user_id,
    tweet_date,
    ROUND(
        AVG(tweet_count) OVER(
            PARTITION BY user_id
            ORDER BY tweet_date
            ROWS BETWEEN 2 PRECEDING AND CURRENT ROW
        ),
        2
    ) AS rolling_avg_3d
FROM tweets;
```

## Output

![Output](./Screenshot%202026-07-16%20at%2014.25.54.png)
