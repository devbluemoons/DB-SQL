###### order by count(*)
```sql
SELECT COUNT(*)
     , COLUMN1
     , COLUMN2
     , COLUMN3
  FROM TABLE
 GROUP
    BY COLUMN1
 ORDER
    BY COUNT(*) DESC
```
