# 100 commands we need to know in SQL

### Highlights:

The `WHERE` clause filters rows, whereas the `HAVING` clause filter groups.  


### Common command

* `SELECT`  query information from a database.
* `AS` renames a column or table.
* `DISTINCT` return unique values.
* `WHERE` filter the results of the query based on conditions.
* `LIKE` and `BETWEEN` are special operators.
* `AND` and `OR` combines multiple conditions.
* `ORDER BY` sorts the result.
* `LIMIT` specifies the maximum number of rows that the query will return.
* `CASE` creates different outputs.

### Case statement

Learn from an example: Use a `CASE` statement to change the rating system

```sql
SELECT name, CASE 
  WHEN review > 4.5 THEN 'Extraordinary'
  WHEN review > 4 THEN 'Excellent'
  WHEN review > 3 THEN 'Good'
  WHEN review > 2 THEN 'Fair'
  ELSE 'Poor'
  END AS 'Review'
 FROM NOMNOM;
```

### Aggregate functions

Aggregate functions combine multiple rows to form a single value of more meaningful information.

* `COUNT()`: count the number of rows
* `SUM()`: the sum of the values in a column
* `MAX()`/`MIN()`: the max/min value
* `AVG()`: the average of the values in a column
* `ROUND()`: round the values in the column
* `GROUP BY:` often used with aggregate functions to combine data from one or more columns.
* `HAVING:` limit the results of a query based on an aggregate property.

**Having:** 

the condition is `group by` is realized by `having`

```sql
SELECT category, count(*)
FROM table_data
GROUP BY 1
HAVING count(*) > 3
ORDER BY 2 DESC;
```

