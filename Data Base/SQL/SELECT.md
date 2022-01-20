---
tags:
  - DB/SQL/DML-Manipulation/CRUD/read
date created: 2021-12-16 11:42
date updated: 2022-01-10 12:42
---

```sql
SELECT col_1, col_N  
FROM tables 		-- из какой табоицы выбрать

WHERE conditions    -- фильтрация
GROUP BY expression -- группировка
HAVING condition    -- фильтрация для уже сформированной выборки
ORDER BY expression -- сортировка
LIMIT number_rows 	-- ограничение по колличеству строк
```

#todo ==вставить пример со всеми условиями==

## Подрообно

```sql
SELECT [ ALL           -- все записи (по умолчанию)
	   | DISTINCT      -- уникальные записи (отчетливый, отличающийся)
       | DISTINCTROW ]  

	   [ HIGH_PRIORITY ]  
	   [ STRAIGHT_JOIN ]  
	   [ SQL_SMALL_RESULT 
	   | SQL_BIG_RESULT ] 
   
       [ SQL_BUFFER_RESULT ]  
	   [ SQL_CACHE
	   | SQL_NO_CACHE ]  
   
	   [ SQL_CALC_FOUND_ROWS ]  
	
col_1, col_N  

FROM tables  -- из какой табоицы выбрать
	[WHERE conditions]     -- фильтрация
	[GROUP BY expressions] -- группировка
	[HAVING condition]     -- условия для уже сформированной выборки
	[ORDER BY expression   -- сортировка
			[ ASC          -- по возрастанию
            | DESC ]]      -- по убывагию

	[LIMIT [offset_value] number_rows -- ограничение по колличеству выводимых записей
    |LIMIT number_rows OFFSET offset_value]  -- offset (смещение) - перемещение курсора

	[PROCEDURE procedure_name]  
	
[INTO   -- куда послать выборку
	 [ OUTFILE 'file_name' options  			-- файл
     | DUMPFILE 'file_name'                     -- дамп
     | @variable1, @variable2, ... @variable_n] -- переменную

[FOR UPDATE 
   | LOCK IN SHARE MODE];
```

## Запись в файл

```mysql
SELECT order_id, quantity, unit_price
FROM order_details
WHERE quantity < 300
ORDER BY quantity
INTO OUTFILE 'result.txt'
     FIELDS TERMINATED BY ',' OPTIONALLY ENCLOSED BY '"'
     LINES TERMINATED BY '\n';
```

## Источники

- (<https://oracleplsql.ru/select-mysql.html>)
- [документация](https://dev.mysql.com/doc/refman/8.0/en/select.html)
