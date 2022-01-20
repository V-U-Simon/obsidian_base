---
tags:
  - DB/SQL/DCL-Control/user
date created: 2022-01-16 12:19
date updated: 2022-01-16 18:32
---

```sql
SHOW GRANTS FOR user_name;
-- SHOW GRANTS FOR 'root'@'localhost';

GRANT 	-- назначает права
REVOKE	-- отменяет  права
FLUSH PRIVILEGES; -- обновить список прав

GRANT ALL ON '.' TO 'foo'@'localhost' IDENTIFIED WITH sha256_password BY 'pass';
```

## Привелегии

```sql
ALL PRIVILEGES 	 -- все, кроме GRANT
USAGE PRIVILEGES -- никаких привилегий

-- CRUD
SELECT 	-- получать данные 
INSERT 	-- вставлять данные 
UPDATE 	-- обновлять данные 
DELETE 	-- удалять данные 

-- Defenition
CREATE 	-- создавать
ALTER 	-- изменять
DROP 	-- удалять
INDEX 	-- создавать индексы для таблиц

EVENT 	-- обработка событий
TRIGGER -- создание триггеров
FILE 	-- разрешает читать файлы на сервере
```

## Привилегии администрирования БД
```sql
-- ПРАВА
SUPER	-- суперпользователь
CREATE USER	-- создание пользователей
GRANT	-- изменять права пользователей
RELOAD	-- позволяет перезагружать таблицы привилегий

PROCESS	-- получение информации о состоянии MySQL
SHOW DATABASES	-- просмотр списка баз данных

SHUTDOWN	-- позволяет отключать/перезапускать БД;
REFERENCES	-- создание внешних ключей для связываниятаблиц;
LOCK TABLES	-- блокирование таблиц при использовании SELECT
```

## Пример
```sql
GRANT 
	SELECT,
	UPDATE,
	INSERT 
ON name_database . * TO 'user'@'localhost';


GRANT 
	ALL PRIVILEGES 
ON name_database . * TO 'user'@'localhost';
```

## Уровни привелегий

Глобальный уровень — касается всех БД и таблиц, входящих в их состав. 

	пользователь с полномочиями на глобальном уровне может обращаться ко всем БД
	
Если текущая база данных не была выбрана при помощи оператора USE, данное предложение эквивалентно ON *.*, если произведен выбор текущей базы данных, то устанавливаемые при помощи оператора GRANT привилегии относятся ко всем таблицам текущей базы данных
Уровень базы данных — данное предложение означает, что привилегии распространяются на таблицы базы данных db.
Уровень таблицы — данное предложение означает, что привилегии распространяются на таблицу tbl базы данных db.
Уровень столбца — привилегии уровня столбца касаются отдельных столбцов в таблице tbl базы данных db.


```sql
GRANT USAGE ON *.* TO foo; 	-- Глобальный (все БД и таблицы)
GRANT USAGE ON * TO foo;	-- ?
GRANT USAGE ON shop.* TO foo;	-- БД 
GRANT USAGE ON shop.catalogs TO foo;	-- таблицы

-- столбца
GRANT 
	SELECT (id, name), 
	UPDATE (name) 
ON shop.catalogs TO foo; 

```
