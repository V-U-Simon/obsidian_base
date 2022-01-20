---
tags:
  - DB/SQL/DML-Manipulation/request
date created: 2021-12-16 11:42
date updated: 2022-01-09 21:15
---

**GROUP BY** - группирует одинаковые поля получая _уникальные значения_ (по сути являясь аналогом [[data request - DISTINCT]]) <small>например, нужно узнать какое количество клиентов живет в каждом из городов</small>

Каждая строка результирующего запроса с GROUP BY - отдельная группа

```sql
GROUP BY col_name


-- ПРИМЕР (Группировка количества клиентов по стране и городу)
select 
	-- указываем столбцы, по которым делается разрез
	Country, City, 
	-- указваем агрегатную функцию  
	count(CustomerID) -- (SUM, AVG, COUNT, MAX, MIN)
from Customers 
GROUP BY Country, City
```

## Пример

```sql
SELECT
	CATALOG,					-- и столбец по которому группируется
	GROUP_CONCAT(col_name), 	-- посмотреть содержимое группы
	COUNT(col_name) AS total	-- отображаются только агрегатные столцы


FROM PRODUCT
GROUP BY CATALOG 	-- группировка 
ORDER BY totalй		-- сортировка
LIMIT 5;			-- ограничение вывода 
```

## Запрет вывода сторонних полей

```sql
 select @@sql_mode;
 -- Запрещает вывод не относящихся к группировке полей
 set @@sql_mode = concat(@@sql_mode, ',ONLY_FULL_GROUP_BY');
 ANY_VALUE(value) -- обход запрета
 
 -- Разрешает вывод не относящихся к группировке полей
 set @@sql_mode = 'STRICT_TRANS_TABLES,NO_ENGINE_SUBSTITUTION';
```
