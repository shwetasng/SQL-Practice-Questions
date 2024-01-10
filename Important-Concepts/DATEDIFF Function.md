## DATEDIFF() Function:

The DATEDIFF function in MySQL is used to calculate the difference between two dates. It returns the number of days between two date values. The syntax for the DATEDIFF function is as follows:

`DATEDIFF(date1, date2)`

date1 and date2 are the two dates you want to find the difference between.
Here's an example of how you can use the DATEDIFF function:

```
-- Example 1: Calculate the difference in days between two specific dates
SELECT DATEDIFF('2022-01-15', '2022-01-10') AS day_difference;
```

In Example 1, the query calculates the difference in days between January 15, 2022, and January 10, 2022. The result would be 5.

```
-- Example 2: Calculate the difference in days between a column and the current date
SELECT DATEDIFF(NOW(), your_date_column) AS days_since_date
FROM your_table;
```

In Example 2, the query calculates the difference in days between the current date and a date stored in the your_date_column column in the your_table table. This can be useful for scenarios where you want to know how many days have passed since a specific date.

Note: It's important to note that the DATEDIFF function returns a signed integer, where positive values indicate that the first date is later than the second date, and negative values indicate that the first date is earlier than the second date.

### USE OF DATEDIFF FUNTION IN CONDITION OF A JOIN:
```
SELECT b.id 
FROM Weather AS a
JOIN Weather AS b
ON DATEDIFF(b.recordDate, a.recordDate) = 1
WHERE b.temperature > a.temperature;
```

In the join condition, we are using the DATEDIFF function to find pairs of records where the recordDate differs by exactly one day. This condition ensures that we are comparing each day's temperature with the temperature of the previous day.Refer Ques.197 on Leetcode for SQL
