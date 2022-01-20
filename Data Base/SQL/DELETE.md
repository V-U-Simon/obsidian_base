---
tags:
  - DB/SQL/DML-Manipulation/CRUD/delete
date created: 2021-12-16 11:42
date updated: 2022-01-10 14:31
---

```sql
DELETE FROM tbl_name
WHERE ...
ORDER BY ...
LIMIT ...;
```

## Пример

```sql
DELETE FROM users  
WHERE user_name in ('Max', 'Piter')
```

## Многотабличное удаление

```sql
DELETE products, catalogs			-- из каких таблиц удаляем значения 
FROM catalogs 						-- значения из таблицы	
JOIN products ON catalogs.id = products.catalog_id -- и таблицы
						 			-- где совподают id с catalogs
WHERE catalogs.name = 'Мат. платы';	-- и где имя каталога name		
```

## Источники:

- [DELETE оператор MySQL](https://oracleplsql.ru/delete-mysql.html)
- <https://dev.mysql.com/doc/refman/8.0/en/delete.html>
