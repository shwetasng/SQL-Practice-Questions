## Not equal to in SQL
In SQL, you can use the <> operator to represent "not equal to." Here's an example:

`SELECT column1, column2
FROM your_table
WHERE column1 <> 'some_value';`

Replace column1 with the column you want to check for inequality, your_table with the actual table name, and 'some_value' with the value you want to compare against. This query will return rows where column1 is not equal to the specified value.

Alternatively, you can also use the != operator instead of <> for the same purpose:

`SELECT column1, column2
FROM your_table
WHERE column1 != 'some_value';`

Both <> and != are commonly used to express "not equal to" in SQL, and you can choose the one that you find more readable or that aligns with your coding style.
