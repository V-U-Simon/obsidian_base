---
tags:
  - DB/SQL/DML-Manipulation/CRUD/update
date created: 2021-12-16 11:42
date updated: 2022-01-10 14:31
---

```sql
UPDATE tb_name
    SET col_1 = value
WHERE ...
ORDER BY ...
LIMIT ...;
```

## Примеры

```sql
-- обновление столбцов
UPDATE customers
SET state = 'Nevada',
    customer_rep = 23
WHERE customer_id > 200;


-- обновления таблицы данными из другой таблицы
UPDATE tbl_1  
SET col_1 = (SELECT val_1  
			 FROM tbl_2  
			 WHERE ...)  
WHERE ...;

UPDATE customers
SET city = (SELECT city
            FROM suppliers
            WHERE suppliers.supplier_name = customers.customer_name)
WHERE customer_id > 5000;


-- обновления нескольких таблиц
UPDATE 	tbl_1, tbl_2, ...  
SET 	col_1 = val_1
WHERE 	tbl_1.col = tbl_2.col

UPDATE customers, suppliers
SET customers.city = suppliers.city
WHERE customers.customer_id = suppliers.supplier_id;
```

## Многотабличное обновление

```sql
UPDATE catalogs	-- обновить таблицу
JOIN products ON catalogs.id = products.catalog_id -- и таблицы
SET
	-- в таблице product
	price = price * 1.1	-- увеличить цену на 10% 
WHERE catalogs.name = 'Мат. платы'	-- где имя каталога name	
```

## Источники:

- <https://dev.mysql.com/doc/refman/8.0/en/update.html>
