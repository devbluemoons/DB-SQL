###### using count with case when
```sql
SELECT COUNT(*) AS warning01
     , COUNT(CASE WHEN GRADE = 2 THEN 1 END) AS warning02
     , COUNT(CASE WHEN GRADE = 3 THEN 1 END) AS warning03
     , COUNT(CASE WHEN GRADE = 4 THEN 1 END) AS warning04
     , COUNT(CASE WHEN GRADE = 5 THEN 1 END) AS warning05
  FROM LOG_ALARM
 WHERE ETIME > CURRENT_DATE()
```

###### using count and sum
```sql
SELECT COUNT(*) AS warning01
     , SUM(GRADE=2) AS warning02
     , SUM(GRADE=3) AS warning03
     , SUM(GRADE=4) AS warning04
     , SUM(GRADE=5) AS warning05
  FROM LOG_ALARM
 WHERE ETIME > CURRENT_DATE()
```
