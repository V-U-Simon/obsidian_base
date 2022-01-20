---
tags:
  - DB/SQL/DDL-Defenition/table
date created: 2021-12-16 11:41
date updated: 2022-01-08 00:56
---

простая с первичным ключем

```sql
CREATE TABLE tb_name
(
    tb_id SERIAL PRIMARY KEY, -- SERIAL = BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE
    tb_date DATE DEFAULT NOW() ON UPDATE NOW(),
    tb_var VARCHAR(100) UNIQUE COMMENT 'Переменная',
    tb_cost DECIMAL(10, 2),
    tb_bool BOOLEAN
);
```

Пример

```sql
DROP TABLE IF EXISTS tb_name;
CREATE TABLE tb_name
(
    tb_id SERIAL, -- SERIAL = BIGINT UNSIGNED NOT NULL AUTO_INCREMENT UNIQUE
    tb_date DATE,
    tb_var VARCHAR(100) COMMENT 'Переменная',
    tb_cost DECIMAL(10, 2),
    tb_bool BOOLEAN,
	PRIMARY KEY (tb_id, tb_var) -- ограничение: первичный ключ
);
```

## Скопировать таблицу

```sql
CREATE TABLE local_companies 
AS 
  SELECT *				  -- выбор столбцов которые будут копированны
  FROM companies		  -- источник копирования
  WHERE state = 'Nevada'; -- выбор строк которые будут копированны
```
