###### how to get table columns
```sql
SELECT *
  FROM INFORMATION_SCHEMA.COLUMNS
 WHERE TABLE_NAME = "TABLE_NAME"
```
###### how to get table lists
```sql
SELECT * 
  FROM INFORMATION_SCHEMA.TABLES
 WHERE TABLE_NAME = "TABLE_NAME"
```
