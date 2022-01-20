---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-11-13 17:46
date updated: 2022-01-08 00:32
---

Определяют

- характеристики сохраняемых значений
- количество памяти, которая под них отводится

```sql
SERIAL	 	-- псевдотип | BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE

-- ЧИСЛА
-- целочисленные
TINYINT(size)		-- до            			 256
SMALLINT(size) 		-- до         			  65 536
MEDIUMINT(size)		-- до     			  16 777 216
INT(size)			-- до  			   4 294 967 296
BIGINT(size)		-- до 18 446 744 073 709 551 616

-- вещественные (числа с плавающей точкой)
FLOAT(size, d)		-- небольшой точности
DOUBLE(size, d)		-- двойной точности
DECIMAL(size, d)	-- в виде строки

-- СТРОКИ
CHAR(size) 		-- до 255
VARCHAR(size) 	-- до 255 (переменная длина)
TINYTEXT		-- до 255
TEXT   			-- до 65 535
MEDIUMTEXT		-- до 16 777 215
LONGTEXT		-- до 4 294 967 295

-- БИНАРНЫЕ
TINYBLOB		-- 
BLOB   			-- до 65 535 (хранение бинарных файлов)
MEDIUMBLOB		-- до 16 777 215
LONGBLOB		-- до 4 294 967 295

-- КАЛЕНДАРНЫЕ
DATE()     		-- ГГГГ-ММ-ДД
DATETIME()  	-- ГГГГ-ММ-ДД ЧЧ:ММ:СС
TIMESTAMP()		-- ГГГГ-ММ-ДД ЧЧ:ММ:СС (от 1970 года до 2038)
TIME()     		--            ЧЧ:ММ:СС
YEAR()     		-- ГГГГ

-- КОЛЛЕКСЦИИ
ENUM(x, y, z...) -- список до 65 535 значений | ENUM(`x`, `y`, `z`)
SET  			 -- список до 64 значений
JSON 	
```

## Источники

- <https://docs.google.com/document/d/1Os4W1-eGgSAgF2CXzImHbTkVuaK-zxELLh7FMR83MC0/edit#>
- [SQL для чайников. Реляционные БД. Типы данных](https://pikabu.ru/story/sql_dlya_chaynikovrelyatsionnyie_bd_tipyi_dannyikh_7575706)
- [Типы данных MySQL](https://metanit.com/sql/mysql/2.3.php)
