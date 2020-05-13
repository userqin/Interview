# Code cademy practice

The schema of the database is:

| Column | Type | Notes |
| :--- | :--- | :--- |
| country | STRING |  |
| population | NUMBER | in millions |
| year | NUMBER |  |

```sql
SELECT DISTINCT year from population_years;

-- Add your additional queries below:
--4. What is the largest population size for Gabon in this dataset?

SELECT country,MAX(population)
FROM population_years
WHERE country = 'Gabon';

--5. What were the 10 lowest population countries in 2005?
SELECT country, population
FROM population_years
WHERE population is not NULL
ORDER BY population
LIMIT 10;

--6. What are all the distinct countries with a population of over 100 million in the year 2010?
SELECT country, population
FROM population_years
WHERE population > 100
AND year = 2010;

--7.How many countries in this dataset have the word “Islands” in their name?
SELECT DISTINCT country
FROM population_years
WHERE country LIKE "%Islands%";

--8. What is the difference in population between 2000 and 2010 in Indonesia?
#Note: it’s okay to figure out the difference by hand after pulling the correct data.
SELECT a.population 
FROM population_years AS a
WHERE country = 'Indonesia'
AND year in (2000, 2010);
```

