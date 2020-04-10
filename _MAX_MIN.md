## how to get max value / min value without `MAX()`, `MIN()` function
###### get max value
```sql
SELECT *
  FROM table-name
 ORDER
    BY base-column DESC
 LIMIT 1
```
###### get min value
```sql
SELECT *
  FROM table-name
 ORDER
    BY base-column ASC
 LIMIT 1
```
