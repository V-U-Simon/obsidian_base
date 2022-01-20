---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-09 21:17
---

**ORDER BY** - отвечает за сортировку таблицы

```sql
-- СОРТИРОВКА
ORDER BY col_name ASC	-- сортировка по возрастанию (по умлочанию)
ORDER BY col_name DESC 	-- сортировка по убыванию
```

```sql
-- ПРИМЕР (простая сортировка)
SELECT * FROM tb_name
ORDER BY name;
```

## Сортировка по нескольким стобцам

```sql
SELECT * FROM tb_name
ORDER BY  
сol_name1, 		-- отсортирует по первому стобцу (верхний уровень)
col_name2 DESC; -- отсортерует по второму (нижний уровень) 
			  	-- не изменив сортировку в верхнем
				-- + DESC - сортировка в обратном порядке
```

## Случайный порядок - RAND()

```sql
SELECT * FROM users
ORDER BY RAND(); -- вывод в случайном порядке
```
