# SQL Notes

## SQL Best Practices 

- Always "GROUP BY" by the attribute/column with the largest number of unique entities/values
- Avoid subqueries in WHERE clause 
- Use With Statements vs nested subqueries
- Always order you JOINs from largest tables to smallest tables
- Convert long list of IN clause into a temporary table
- Avoid UNIONs where possible
- User approx_distinc() vs count(distinct) and approx_percentil(metric, 0.5) for median
- User Max instead of Rank
- Use simple equi-joins 

## SQL Optimizations

[MySQL SELECT Optimizations](https://dev.mysql.com/doc/refman/8.0/en/select-optimization.html)

 

