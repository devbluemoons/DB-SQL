## Date_Format() 내장 함수 사용시 주의할 점
  
`mysql` 에서 `date를 포맷할 때` 주로 `date_format() 내장함수`를 사용한다  
  
###### 사용법  
```sql
date_format(target-date, format)
``` 
아래와 같은 포맷팅을 경우 `시:분:초`가 정확히 포맷팅되지 않는 경우가 있다  
```mysql
date_format(now(), '%Y-%m-%d %H:%m:%s')
```

같은 포맷팅을 좀 더 안정적으로 사용하려면
```
ex) date_format(now(), '%Y-%m-%d %T') 
```  
형태로 사용한다
