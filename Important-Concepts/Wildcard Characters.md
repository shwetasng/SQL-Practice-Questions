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
