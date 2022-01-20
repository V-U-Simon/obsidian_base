---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 11:41
date updated: 2022-01-03 18:14
---

```sql
-- Манипуляции со столбцами
ALTER TABLE table_name  
	ADD		COLUMN  col_name column_type; -- Добавить столбец 
	MODIFY	COLUMN 	col_name column_type; -- Изменить тип столбца
	RENAME	COLUMN	col_name TO col_new;  -- Переименовать столбец
	DROP	COLUMN  col_name;			  -- Удалить столбец
```

## Внешний ключ

```sql
--	CREATE TABLE Customers 
--	(
--	    Id INT PRIMARY KEY AUTO_INCREMENT,
--	    Age INT, 
--	    FirstName VARCHAR(20) NOT NULL,
--	    LastName VARCHAR(20) NOT NULL
--	);
--	CREATE TABLE Orders 
--	(
--	    Id INT PRIMARY KEY AUTO_INCREMENT,
--	    CustomerId INT,
--	    CreatedAt Date
-- 	);

ALTER TABLE Orders					-- для таблицы Orders
ADD 								-- добавить
	CONSTRAINT orders_customers_fk 	-- имя связи (ограничения)
	FOREIGN KEY(CustomerId) 		-- внешнений ключ столбцу CustomerId
	REFERENCES Customers(Id);		-- ссылается на Customers(Id)

ALTER TABLE Orders
DROP 								-- удалить
	FOREIGN KEY orders_customers_fk;-- связь (ограничение)
	
```

## Первичный ключ

```sql
--	CREATE TABLE Products
--	(
--	    Id INT,
--	    Model VARCHAR(20)
--	);
 
ALTER TABLE Products
ADD 					-- добавить
	PRIMARY KEY (Id);	-- ограничение первичного ключа

ALTER TABLE Products
DROP 					-- удалить
	PRIMARY KEY;		-- ограничение первичного ключа
```

## Источник

- <https://dev.mysql.com/doc/refman/8.0/en/update.html>
- [ALTER TABLE оператор MySQL](https://oracleplsql.ru/alter-table-mysql.html)