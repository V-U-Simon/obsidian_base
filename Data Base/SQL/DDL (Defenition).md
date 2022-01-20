---
tags:
  - DB/SQL/DDL-Defenition
date created: 2021-12-16 11:41
date updated: 2022-01-15 13:33
---

**DDL (Data Defenition languadge)** - язык определения структуры данных (БД, таблиц)

# Основные команды

## БД

```sql
SHOW DATABASES; 		 -- показать
USE db_name				 -- выбрать
CREATE DATABASE db_name; -- создать
DROP DATABASE db_name;	 -- удалить
```

## Таблицы

```sql
SHOW TABLES;			 				   -- список
ALTER TABLE tb_name RENAME TO tb_new_name; -- переименовать
DROP TABLE tb_name; 	 				   -- удалить
TRUNCATE tb;			 				   -- удаляет + обнуляет счетчик
CREATE TABLE tb_name	 				   -- содание
(
    tb_id SERIAL PRIMARY KEY, -- SERIAL = BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE
    tb_date DATE DEFAULT NOW() ON UPDATE NOW(),
    tb_var VARCHAR(100) UNIQUE COMMENT 'Переменная',
    tb_cost DECIMAL(10, 2),
    tb_bool BOOLEAN
);
```

## Столбцы

```sql
DESCRIBE tb_name    -- выводит описание и тип стобцов в талице
ALTER TABLE table_name  
	ADD		COLUMN  col_name column_type; -- Добавить 
	MODIFY	COLUMN 	col_name column_type; -- Изменить тип
	RENAME	COLUMN	col_name TO col_new;  -- Переименовать
	DROP	COLUMN  col_name;			  -- Удалить
```

# Источники

- [Изменение таблиц и столбцов](https://metanit.com/sql/mysql/2.6.php)

```sql
-- БД
SHOW DATABASES; 		 -- показать
USE db_name				 -- выбрать
CREATE DATABASE db_name; -- создать
DROP DATABASE db_name;	 -- удалить


-- ТАБЛИЦЫ
SHOW TABLES;			 				   -- список
ALTER TABLE tb_name RENAME TO tb_new_name; -- переименовать
DROP TABLE tb_name; 	 				   -- удалить
TRUNCATE tb;			 				   -- удаляет + обнуляет счетчик
CREATE TABLE tb_name	 				   -- содание
(
    tb_id SERIAL PRIMARY KEY, -- SERIAL = BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE
    tb_date DATE DEFAULT NOW() ON UPDATE NOW(),
    tb_var VARCHAR(100) UNIQUE COMMENT 'Переменная',
    tb_cost DECIMAL(10, 2),
    tb_bool BOOLEAN
);


-- СТОЛБЦЫ
DESCRIBE tb_name    -- выводит описание и тип стобцов в талице
ALTER TABLE table_name  
	ADD		COLUMN  col_name column_type; -- Добавить 
	MODIFY	COLUMN 	col_name column_type; -- Изменить тип
	RENAME	COLUMN	col_name TO col_new;  -- Переименовать
	DROP	COLUMN  col_name;			  -- Удалить
```
