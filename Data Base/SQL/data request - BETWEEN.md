---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2022-01-06 15:46
date updated: 2022-01-06 15:47
---

```sql
BETWEEN	    -- вхождения в пределах диапазона (включительно)
```

Пример

```sql
SELECT * FROM tb_name
   WHERE id 
   BETWEEN 10 AND 15;
-- NOT BETWEEN 10 AND 15; 	-- значения не входящие в интервал
-- 10 <= id AND id >= 15;   -- аналогичное условие
```
