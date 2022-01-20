---
tags:
  - DB/SQL/DDL-Defenition
date created: 2021-12-06 23:16
date updated: 2021-12-19 17:33
---

```shell
# КОПИРОВАНИЕ (резевное/для переноса на другой сервер)
mysqldump -u -h 82.82.82.82 -p database > database.sql
-u # имя MySQL-пользователя
-p # запросить пароль
-h # IP-адрес или домен удаленного сервера

# СОЗДАНИЕ bump
mysqldump example > sample.sql	 
mysqldump -B db1 db2 > db.sql	 # нескольких БД
mysqldump -A > all_db.sql		 # всех БД


# РАЗВЕРТЫВАНИЕ
mysql new_db < sample.sql	
zcat newdb.sql.gz | mysql newdb	# из архива gzip
use new_db; source db.sql;		# через консоль SQL


# ФИЛЬТРЫ
mysqldump db table > db_table_backup.sql # бэкап только 1 таблицы
mysqldump \
db > db.sql	 
			


mysqldump \
--where="true limit 100" \ # не более 100 записей
--no-create-info \
--no-data \			# структура, без данных
--triggers \		# триггеры
--routines \		# процедуры
--events \			# события
--lock-tables		# ДЛЯ РАБОЧЕЙ БД, все блокировка на время копирования
sample | gzip > ~/database.sql.gz	# запоковать в архив
```

^l53xkr

## Источники

- [MySQLDUMP на примерах](https://maxidrom.net/archives/1396)
- [Утилита mysqldump и шпаргалка по параметрам](https://adw0rd.com/2009/06/07/mysqldump-and-cheat-sheet/)
