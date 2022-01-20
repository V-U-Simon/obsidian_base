---
tags:
  - DB/SQL/Clients/sqlite3
  - Python/library/db
date created: 2021-11-13 17:51
date updated: 2021-12-19 11:56
---

![Python DB-API METOAbI.png](./_resources/SQLite3_-_in_python.resources/Python DB-API METOAbI.png)

```python
import sqlite3

# СОЕДИНЕНИЕ
conn = sqlite3.connect('my_db.sqlite') # соединение с БД
conn.close() 						   # закрыть соединение
cursor = conn.cursor() # курсор - объект делающий запросы/получающий результаты

# ЗАПИСЬ
cursor.execute("insert into Artist values (Null, 'For to add') ") # SQL-синтаксис
conn.commit() # сохранить транзакцию

# ЧТЕНИЕ
cursor.execute("SELECT Name FROM Artist ORDER BY Name LIMIT 1")
results = cursor.fetchall()
print(results)  # [('For to add!',), ]
```