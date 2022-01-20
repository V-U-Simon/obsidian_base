---
tags:
  - DB/SQL/DML-Manipulation
date created: 2021-12-16 11:42
date updated: 2021-12-23 19:31
---

**DML (Data Manipulation Language)** - язык управления данными (строки)

```sql
SELECT 		-- извлекает
INSERT 		-- добавляет
UPDATE 		-- изменяет 
DELETE		-- удаляет
TRUNCATE 	-- удаляет + обнуляет счетчик

	
INSERT [IGNORE] [INTO] tb_name
    [PARTITION (partition_name [, partition_name] ...)]
    [AS row_alias[(col_alias [, col_alias] ...)]]
    SET assignment_list
    [ON DUPLICATE KEY UPDATE assignment_list]
```

```sql
DESCRIBE tb_name; 				-- список колонок


INSERT [IGNORE] [INTO] tb_name	-- пакетная вставка 
	[(col_1, col_N)],		    -- если не указано, то val - по порядку
VALUES
	(val_1, val_N),
	(val_1, val_N);



	
SELECT col FROM tb							-- извлекает
INSERT INTO tb (col) VALUES ('your_value');	-- добавляет

UPDATE tb SET col1 = 'val', col2 = 'val';	-- изменяет 
-- WHERE col = 'your_value';
DELETE FROM tb;								-- удаляет
-- WHERE | DELETE FROM tb WHERE id > 1;
-- LIMIT | DELETE FROM tb LIMIT 1;

```

^h6nx0d

## Источники:

- [INSERT Statement](https://dev.mysql.com/doc/refman/8.0/en/insert.html)
