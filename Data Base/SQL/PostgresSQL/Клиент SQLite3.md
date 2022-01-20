---
tags:
  - DB/SQL/Clients/sqlite3
date created: 2021-12-19 12:00
date updated: 2021-12-19 15:05
---

```shell
sqlite3 DatabaseName.db # coздание БД


.databases 				# список БД
.tables					# список таблиц
.quit					# выход

# КОПИРОВАНИЕ БД
sqlite3 testDB.db .dump > testDB.sql # dump
```

## Источники

- [Документация SQLite, изменение таблицы](https://unetway.com/tutorial/sqlite-alter-table).
- [Документация SQLite, выборка данных](https://unetway.com/tutorial/sqlite-command-select).
- [Документация SQLite, вставка данных](https://unetway.com/tutorial/sqlite-command-insert).
- [Документация SQLite, обновление данных](https://unetway.com/tutorial/sqlite-operator-update).
- [Документация SQLite, удаление данных](https://unetway.com/tutorial/sqlite-operator-delete).
- [Руководство по стилю SQL](https://www.sqlstyle.guide/ru/).**
