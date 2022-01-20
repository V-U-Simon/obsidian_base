---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 11:41
date updated: 2022-01-10 14:48
---

```sql



-- Ограничение (в конце)
CONSTRAINT cons_name -- имя ограничения
FOREIGN KEY 		 -- внешний ключ в текущей таблице
	col_1 
REFERENCES 
	tb_source col_id -- указывает внешний ключ
ON DELETE действие
ON UPDATE действие


-- действия (при удалении/обновлении в таблице-предке):
CASCADE 	-- дублируктся в таблице-потомке
SET NULL 	-- устанавливаются в NULL  
NO ACTION 	-- никаких действий не предпринимать   
RESTRICT 	-- возвратит ошибки   
SET DEFAULT -- выставляется значение по умолчанию. (В MySQL не используется)
```

```ad-warning
title: Тип **foreign key** и **primary key** должны совпадать
```

## Пример

```sql
CREATE TABLE Orders
(
    Id INT PRIMARY KEY AUTO_INCREMENT,
    CustomerId INT,
	DivizionId INT REFERENCES Company_divzion (Id) -- внешняя ссылка 
				   ON DELETE CASCADE, 			   -- действия по удалении
    CreatedAt Date,
	
    CONSTRAINT orders_custonmers_fk -- имя ограничения
    FOREIGN KEY (CustomerId) 	-- столбец содержащий ссылку
	REFERENCES Customers (Id)	-- внешняя таблица и ссылка на primary key
	ON DELETE CASCADE 			-- действия по удалении
);
```


##  Удаление FOREIGN KEY

```sql
ALTER TABLE tbl_name 
DROP FOREIGN KEY fk_symbol;


```
## Источники:

- [Руководство по проектированию реляционных баз данных. Каскадное удаление данных](https://habr.com/ru/post/194738/)
- [проектирование баз данных](https://habr.com/ru/search/?target_type=posts&order=relevance&q=%5Bпроектирование%20баз%20данных%5D)
