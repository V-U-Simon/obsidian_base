---
tags:
  - DB/SQL/DCL-Control/connection
date created: 2022-01-16 12:19
date updated: 2022-01-16 13:32
---

```sql
KILL 1 -- разорвать соединение


SHOW VARIABLES LIKE 'max_connections'; -- максимальное оличество соединений
SHOW PROCESSLIST; 					   -- список соединений
-- *************************** 1. row ***************************
--      Id: 5
--    User: event_scheduler
--    Host: localhost
--      db: NULL
-- Command: Daemon
--    Time: 403374					-- время соединения
--   State: Waiting on empty queue
--    Info: NULL
```

каждое соединение потребляет довольно много оперативной памяти, стоит быть осторожным

