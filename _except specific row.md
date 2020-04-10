###### 특정행 하나만 제외하고 나머지 data 가져오기
```sql
# 인덱스가 하나의 컬럼일 경우
SELECT *
  FROM table
 WHERE index-column <> value
```
```sql
# 인덱스가 하나 이상의 컬럼일 경우
SELECT *
  FROM table
 WHERE (index-column01, index-column02) <> (SELECT value01, value02)
```
