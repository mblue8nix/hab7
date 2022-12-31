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

### MySQL for max query performance 

- In schema design: 
   - Use the same CHARSETS encoding across tables to utilise the better indexing.
   - Make sure your indexes are proparyly veted before pushing schema to prod.  
   - Understand:
      - When two columns with different datatypes get compared in a query it might not use the index.
      - When a query compares different datatype values, it uses implicit datatype conversion.

It may not be easy to avoid some of these:

- Avoid using DISTINCT and GROUP BY at the same time
- Avoid using UNION and DISTINCT at the same time
- Avoid subquery where possible
- Avoid using Function-based clause in where condition
- Avoid joining tables with OR condition:
- Avoid join with not equal condition

Obviously having the right index is important. Finding unsused indexes and removing them can free up memory a resource you may need. 
You can use the sys schema to find unused indexing. `sys.schema_unused_indexes`

## SQL Optimizations

[MySQL SELECT Optimizations](https://dev.mysql.com/doc/refman/8.0/en/select-optimization.html)

 

