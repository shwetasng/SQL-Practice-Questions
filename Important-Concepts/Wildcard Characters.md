# WILDCARD CHARACTERS

In SQL, wildcard characters are special symbols used in conjunction with the LIKE keyword to perform pattern matching within string data. These wildcard characters allow you to search for strings that match a specific pattern, rather than an exact match.

The two primary wildcard characters used in SQL are:

1. **% (Percent Sign)**: This wildcard represents zero or more characters. It can be used to match any sequence of characters of any length.
   
   For example:
   - `'cat%'` would match any string that starts with 'cat', followed by zero or more characters.
   - `'%dog'` would match any string that ends with 'dog', preceded by zero or more characters.
   - `'%bird%'` would match any string that contains the substring 'bird' anywhere within it.

2. **_ (Underscore)**: This wildcard represents exactly one character. It can be used to match any single character in the specified position.

   For example:
   - `'h_t'` would match strings like 'hat', 'hot', 'hit', etc., where the underscore represents any single character.

These wildcard characters provide powerful capabilities for searching and filtering data based on patterns rather than exact values, making them essential tools for text-based searches in SQL queries.

## List of wildcard characters:
| Symbol | Description                                                  |
|--------|--------------------------------------------------------------|
| %      | Represents zero or more characters                           |
| _      | Represents a single character                                |
| []     | Represents any single character within the brackets *        |
| ^      | Represents any character not in the brackets *               |
| -      | Represents any single character within the specified range * |
| {}     | Represents any escaped character **                          |

* Not supported in PostgreSQL and MySQL databases.

** Supported only in Oracle databases.

### EXAMPLES OF USAGE OF WILDCARDS:
1. Using the % Wildcard

```
Return all customers that ends with the pattern 'es':

SELECT * FROM Customers
WHERE CustomerName LIKE '%es';
```

```
Return all customers that contains the pattern 'mer':

SELECT * FROM Customers
WHERE CustomerName LIKE '%mer%';
```

2. Using the _ Wildcard

```
Return all customers with a City starting with any character, followed by "ondon":

SELECT * FROM Customers
WHERE City LIKE '_ondon';
```

```
Return all customers with a City starting with "L", followed by any 3 characters, ending with "on":

SELECT * FROM Customers
WHERE City LIKE 'L___on';
```

3. Using the [] Wildcard

```
Return all customers starting with either "b", "s", or "p":

SELECT * FROM Customers
WHERE CustomerName LIKE '[bsp]%';
```

4. Using the - Wildcard

```
Return all customers starting with "a", "b", "c", "d", "e" or "f":

SELECT * FROM Customers
WHERE CustomerName LIKE '[a-f]%';
```

5. Combine Wildcards

```
Return all customers that starts with "a" and are at least 3 characters in length:

SELECT * FROM Customers
WHERE CustomerName LIKE 'a__%';
```

```
Return all customers that have "r" in the second position:

SELECT * FROM Customers
WHERE CustomerName LIKE '_r%';
```

6. Without Wildcard

```
Return all customers from Spain:

SELECT * FROM Customers
WHERE Country LIKE 'Spain';

```

## Use of LIKE keyword:

- In SQL, the LIKE keyword is used in conjunction with pattern matching to search for specific patterns within string data. It allows you to perform wildcard searches, where you can specify placeholders for unknown characters using the '%' symbol for zero or more characters, or '_' for exactly one character.
- To write a query to get rows that begin and end with specific characters, you can use the LIKE keyword along with the '%' wildcard symbol at the beginning and end of the search pattern. Here's an example:
- ```
  SELECT *
  FROM your_table
  WHERE your_column LIKE 'specific_character%specific_character';
  ```

- 'specific_character%specific_character' is the pattern you're searching for. Replace 'specific_character' with the actual specific characters you want to match.
- For example, if you want to retrieve rows where the values in the column start with 'A' and end with 'Z', you would use:
- ```
  SELECT *
  FROM your_table
  WHERE your_column LIKE 'A%Z';
  ```
