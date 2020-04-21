###### using `COUNT()` with `CASE WHEN`
```sql
SELECT COUNT(*) AS warning01
     , COUNT(CASE WHEN GRADE = 2 THEN 1 END) AS warning02
     , COUNT(CASE WHEN GRADE = 3 THEN 1 END) AS warning03
     , COUNT(CASE WHEN GRADE = 4 THEN 1 END) AS warning04
     , COUNT(CASE WHEN GRADE = 5 THEN 1 END) AS warning05
  FROM LOG_ALARM
 WHERE ETIME > CURRENT_DATE()
```
###### using `COUNT(`) with `IF`
```sql
SELECT COUNT(*) AS warning01
     , COUNT(IF(GRADE = 2, GRADE, NULL)) AS warning02
     , COUNT(IF(GRADE = 3, GRADE, NULL)) AS warning03
     , COUNT(IF(GRADE = 4, GRADE, NULL)) AS warning04
     , COUNT(IF(GRADE = 5, GRADE, NULL)) AS warning05
  FROM LOG_ALARM
 WHERE ETIME > CURRENT_DATE()
```

###### using `COUNT()` and `SUM()`
```sql
SELECT COUNT(*) AS warning01
     , SUM(GRADE=2) AS warning02
     , SUM(GRADE=3) AS warning03
     , SUM(GRADE=4) AS warning04
     , SUM(GRADE=5) AS warning05
  FROM LOG_ALARM
 WHERE ETIME > CURRENT_DATE()
```
