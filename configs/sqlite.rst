======
SQLite
======

SQLite 数据库配置
=================

:type:

+-------------+----------------------+---------+
|可选值       |说明                  |是否可选 |
+=============+======================+=========+
|sqlite       |指明数据库为SQLite    |否       |
+-------------+----------------------+---------+

`SQLite2 不再受支持，请升级至 SQLite3`


:mode:

+-------------+-------------------+---------+
|可选值       |说明               |是否可选 |
+=============+===================+=========+
|odbc         |指明模式为 Odbc    |是       |
+-------------+-------------------+---------+
|pdo          |指明模式为 Pdo     |是       |
+-------------+-------------------+---------+
|sqlite3      |指明模式为 Sqlite3 |是       |
+-------------+-------------------+---------+

`在 SQLite 中 mode 参数默认为 pdo`


:config:

+---------------+-----------------------------------------------------------+---------+--------+
|参数名         |说明                                                       |是否可选 |默认值  |
+===============+===========================================================+=========+========+
|file           |数据库文件                                                 |否       |\       |
+---------------+-----------------------------------------------------------+---------+--------+
|prefix         |表前缀                                                     |是       |        |
+---------------+-----------------------------------------------------------+---------+--------+
|long_names     |参数LongNames，使用模式 odbc 时有效                        |是       |0       |
+---------------+-----------------------------------------------------------+---------+--------+
|time_out       |参数Timeout，使用模式 odbc 时有效                          |是       |1000    |
+---------------+-----------------------------------------------------------+---------+--------+
|no_txn         |参数NoTXN，使用模式 odbc 时有效                            |是       |0       |
+---------------+-----------------------------------------------------------+---------+--------+
|sync_pragma    |参数SyncPragma，使用模式 odbc 时有效                       |是       |NORMAL  |
+---------------+-----------------------------------------------------------+---------+--------+
|step_api       |参数StepAPI，使用模式 odbc 时有效                          |是       |0       |
+---------------+-----------------------------------------------------------+---------+--------+
|driver         |驱动名，使用模式 odbc 时有效                               |是       |null    |
+---------------+-----------------------------------------------------------+---------+--------+
|flags          |模式，使用模式 sqlite3 时有效                              |是       |2       |
+---------------+-----------------------------------------------------------+---------+--------+
|encryption_key |加密密钥，使用模式 sqlite3 时有效                          |是       |null    |
+---------------+-----------------------------------------------------------+---------+--------+
|busy_timeout   |超时时间，使用模式 sqlite3 时有效                          |是       |30000   |
+---------------+-----------------------------------------------------------+---------+--------+
