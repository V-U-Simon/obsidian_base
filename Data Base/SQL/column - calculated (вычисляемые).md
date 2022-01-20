---
tags:
  - DB/SQL/DDL-Defenition/column
date created: 2021-12-16 11:42
date updated: 2021-12-16 21:33
---

**Вычисляемые столбцы** - столбцы, значения которых вычисляются при запросе в БД

```sql
CREATE TABLE tbl (
	x INT,
	y INT,
	-- значения не сохраняются на диск, каждый раз вычисляются по новой
	summ INT AS (x + y), -- вычисляемый столбец (суммы x, y)
	-- принудительная запись на диск (с возможностью индексации)
	subt INT AS (x - y) STORED 
);	

-- ПРИМЕР
DROP TABLE IF EXISTS triangles;
CREATE TABLE triangles (
  id SERIAL PRIMARY KEY,
  a DOUBLE NOT NULL COMMENT 'Сторона треугольника',
  b DOUBLE NOT NULL COMMENT 'Сторона треугольника',
  angle INT NOT NULL COMMENT 'Угол треугольника в градусах',
  square DOUBLE AS (a * b * SIN(RADIANS(angle)) / 2.0)
) COMMENT = 'Площадь треугольника';
