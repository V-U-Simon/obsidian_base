---
tags:
  - DB/SQL/Clients/mysql
date created: 2021-12-06 23:16
date updated: 2021-12-19 12:43
---

## Соединение с сервером (Вход)

```shell
# ПОДКЛЮЧЕНИЕ
mysql -u root -p
-u # имя MySQL-пользователя
-p # запросить пароль

# К СЕРВЕРУ
mysql -u root -h 192.168.0.10 -P 3306
-h # IP-адрес или домен удаленного сервера
-P # порт
```


## Внутренние команды клиента MySQL

```sql
-- ВЫВОД
\s, status 		-- вывод информации о состоянии сервера
\G 				-- вывод результата в вертикальном формате | some_command\G

-- ВЫПОЛНЕНИЕ
\., source 	-- SQL-команды из файла | source ~/Desktop/script.sql
\!, system 	-- команды ОС 			| \! pwd
```


## Расположение БД

![[Архитектура MySQL#^ioy53j]]



## Ошибки

```sql
Key   is not allowed 
-- проверить запущен ли сервер sql
-- настройка соединения > настройка драйвера > allowPublicKeyRetrieval - True
```

## Источники:

- [Документация](https://dev.mysql.com/doc/refman/8.0/en/explain.html)

```sql
HELP;
HELP DESCRIBE;
```
