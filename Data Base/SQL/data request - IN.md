---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-06 15:48
---

```sql
IN ( )	    -- Соответствует значению в списке
```

Пример

```sql
SELECT * FROM tb_name
   WHERE id 
   IN (1, 2, 4);		-- значения входящие в список
-- NOT IN (1, 2, 4);	-- значения не входящие в список
```
