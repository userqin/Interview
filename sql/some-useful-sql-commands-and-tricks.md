# Some useful SQL commands and tricks

* We can order by a column that is not included in the select list.
* Likewise, we can also use `where` to filter results from a column that is not in the select list.

## BETWEEN AND

```sql
SELECT col2, col2
FROM table
WHERE
col3 BETWEEN 10 AND 20
ORDER BY
col4 DESC
```

## NULL values

* Note: use `IS NULL`

```sql
SELECT col2, col2
FROM table
WHERE
col3 IS NOT NULL
```



