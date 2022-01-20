---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-08 01:49
---

```sql
-- ОГРАНИЧЕНИЯ
LIMIT [start] number_str 		-- первые диапозон вывидимых значений
LIMIT number_str OFFSET start	-- указание на смещение (offset)
```

## Пример

```sql
SELECT ... 
FROM ...
LIMIT 2; 		  -- первые 2е записи
LIMIT 5, 2; 	  -- первые 2е записи, начиная с 5ой
LIMIT 2 OFFSET 5; -- первые 2е записи, начиная с 5ой


-- ПРИМЕР
select id, firstname from users 
order by id 
limit 4 offset 6;
-- +----+-----------+
-- | id | firstname |
-- +----+-----------+
-- |  7 | Fabian    |
-- |  8 | Jazmyn    |
-- |  9 | Constance |
-- | 10 | Marquise  |
-- +----+-----------+

select id, firstname from users 
order by id 
limit 4 offset 6;
-- +----+-----------+
-- | id | firstname |
-- +----+-----------+
-- |  7 | Fabian    |
-- |  8 | Jazmyn    |
-- |  9 | Constance |
-- | 10 | Marquise  |
-- +----+-----------+
```
