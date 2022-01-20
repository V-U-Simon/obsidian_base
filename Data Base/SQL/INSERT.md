---
tags:
  - DB/SQL/DML-Manipulation/CRUD/create
date created: 2021-12-16 11:42
date updated: 2022-01-08 01:17
---

```sql
-- вставка нескольких строк
INSERT tb_name 
	(col_1, col_N)
	
VALUES	(val_1, val_N); -- ПАКЕТНАЯ ВСТАВКА
SET		col_1 = val_1;  -- ИМЕНОВАННАЯ ВСТАВКА (ключ =  значение)
SELECT	(col_1, col_N) 	-- ВСТАВКА ИЗ ТАБЛИЦЫ	
FROM 	tb_source
WHERE	условие;
```

## Пример

```sql
-- ПАКЕТНАЯ ВСТАВКА
INSERT users (col_name, col_age)
VALUES	('Max', 23), ('Vasia', 26);	
	
-- ИМЕНОВАННАЯ ВСТАВКА	
INSERT users
SET	col_name = 'Max'
	col_age = 23
	
-- ВСТАВКА ИЗ ТАБЛИЦЫ
SELECT count(*)
FROM customers
WHERE customer_id < 300;
```

## Источники

- <https://dev.mysql.com/doc/refman/8.0/en/truncate-table.html>
