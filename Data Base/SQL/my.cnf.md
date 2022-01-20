---
tags:
  - DB/SQL/Clients/mysql
date created: 2021-12-06 23:16
date updated: 2022-01-16 12:51
---

## Расположение:

Linux

```bash
mysql --help | grep .my.cnf # источники
# /etc/my.cnf 
# /etc/mysql/my.cnf 
# /usr/local/etc/my.cnf 
# ~/.my.cnf 

# $MYSQL_HOME/my.cnf
# [datadir]/my.cnf
```

Windows

```bash
C:\Windows\my.ini
C:\mysql5\my.ini

C:\Windows\my.cnf
C:\mysql5\my.cnf
```

## Секции `cnf`

```shell
# один конфиг может управлять работой нескольких серверов MySQL
[mysqld]	 # Сервер MySQL
[server]	 # Сервер MySQL
[mysqld-5.7] # Сервер MySQL версии 5.7
[mysqld-5.8] # Сервер MySQL версии 5.8
[client]	 # Любая клиентская утилита
[mysql]		 # Консольный клиент mysql
[mysqldump]	 # Утилита создания дампов mysqldump
```

## Пример `cnf`

```shell
# Вводит в конфиг для входа без пароля - mysql
vim ~/.my.cnf

cat ~/.my.cnf
# [mysql]	# на секцию - только консольный клиент 
# [client]	# на секцию - любой  консальный (+mysqldump)
# user=root
# password=YOUR_PASSWORD

##  Порт TCP/IP который прослушивает MySQL сервер, порт 3306 является
##  стандартным, однако можно назначить любой другой не занятый порт
# port=3307
```

## Кодировка

```sql
-- Изменение кодировки значения
SELECT CONVERT('May. 1945' USING utf8);
-- May. 1945
```
