# Experiment 3.1

## Aim
To retrieve data from database tables using SQL queries with appropriate conditions and clauses.

## Question
Write SQL queries to retrieve the required information from the given database tables as specified in the experiment.

## Query

```sql
SELECT department,
COUNT(CASE WHEN marks > 80 THEN 1 ELSE NULL END) as Dept_HighScore_Count
FROM student
GROUP BY department;
```

## Output

![Output](./Screenshot%202026-07-20%20at%2012.49.09.png)