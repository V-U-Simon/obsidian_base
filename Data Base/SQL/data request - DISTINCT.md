---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-06 22:25
---

```sql
DISTINCT -- вывод уникальных значений (отличающийся)
ALL 	 -- вывод всех значений (по умолчанию)
```

## Пример

```sql
SELECT DISTINCT val FROM tb_name; -- вывод уникальных значений
SELECT ALL val FROM tb_name; 	  -- вывод всех значений
```
