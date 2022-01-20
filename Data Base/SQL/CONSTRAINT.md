---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 11:42
date updated: 2021-12-23 17:25
---

**Constraints (ограничения)** - правила к записываемым данным в таблице

```sql
SERIAL 		-- псевдотип
-- BIGINT UNSIGNED, NOT NULL, AUTO_INCREMENT

AUTO_INCREMENT	-- автосчетчик
UNSIGNED    	-- запрет знака '-'
NOT NULL 		-- не нулевое значение
NULL 			-- м.б. нулевым значением
DEFAULT 		-- значение по умолчанию
UNIQUE 			-- уникальные значения 
CHECK			-- значения подходит по условию
STORED          -- записывает ВЫЧЕСЯЕМЫЙ стобец в БД

PRIMARY KEY 	-- первичный ключ
FOREIGN KEY 	-- внешний ключ  (в другой таблице)
INDEX 			-- быстрая запись/извлечение
```

## [[CONSTRAINT - foreign key]]
## PRIMARY KEY

```sql
CREATE TABLE tb_name
	(id INT PRIMARY KEY),		-- атрибут
	[col_name col_type],
	PRIMARY KEY(id),			-- после объявлений стобцов
	PRIMARY KEY(id, col_name)	-- составной
```

## AUTO_INCREMENT

```sql
CREATE TABLE Customers
(
    Id INT PRIMARY KEY AUTO_INCREMENT,
    Age INT,
    FirstName VARCHAR(20),
    LastName VARCHAR(20)
);
```

## UNIQUE

```sql
CREATE TABLE Customers
(
    Id INT PRIMARY KEY AUTO_INCREMENT,
    Age INT,
    FirstName VARCHAR(20),
    LastName VARCHAR(20),
    Phone VARCHAR(13) UNIQUE
);
```

## DEFAULT

```sql
CREATE TABLE Customers
(
    Id INT PRIMARY KEY AUTO_INCREMENT,
    Age INT DEFAULT 18,
    FirstName VARCHAR(20) NOT NULL,
    LastName VARCHAR(20) NOT NULL,
    Email VARCHAR(30) NOT NULL UNIQUE,
    Phone VARCHAR(20) NOT NULL UNIQUE
);
```

## CHECK

```sql
CREATE TABLE Customers
(
    Id INT AUTO_INCREMENT,
    Age INT DEFAULT 18 CHECK(Age >0 AND Age < 100),
    FirstName VARCHAR(20) NOT NULL,
    LastName VARCHAR(20) NOT NULL,
    Email VARCHAR(30) CHECK(Email !=''),
    Phone VARCHAR(20) CHECK(Phone !='')
);
```

## NULL

обозначает неопределенное значение, отсутствие информации

```sql
NULL -- неизвестное значение
SELECT NULL;
SELECT NULL + 2;	-- Все операции с NULL возвращают NULL
```

## CONSTRAINT

Задает имя для ограничений, впоследствии через эти имена мы сможем управлять ограничениями - удалять или изменять их

Установить имя можно для ограничений `PRIMARY KEY`, `CHECK`, `UNIQUE`, `FOREIGN KEY`

```sql
CREATE TABLE Customers
(
    Id INT AUTO_INCREMENT,
    Age INT,
    FirstName VARCHAR(20) NOT NULL,
    LastName VARCHAR(20) NOT NULL,
    Email VARCHAR(30),
    Phone VARCHAR(20) NOT NULL,
    CONSTRAINT customers_pk PRIMARY KEY(Id),
    CONSTRAINT customer_phone_uq UNIQUE(Phone),
    CONSTRAINT customer_age_chk CHECK(Age >0 AND Age<100)
);
```

В данном случае ограничение для `PRIMARY KEY` называется `customers_pk`, для `UNIQUE` - `customer_phone_uq`, а для `CHECK` - `customer_age_chk`. 

## Источники:
- [Атрибуты столбцов и таблиц](https://metanit.com/sql/mysql/2.4.php)