======
Oracle
======

Oracle 数据库配置
=================

:type:

+-------------+-------------------+---------+
|可选值       |说明               |是否可选 |
+=============+===================+=========+
|oracle       |指明数据库为Oracle |否       |
+-------------+-------------------+---------+


:mode:

+-------------+-------------------+---------+
|可选值       |说明               |是否可选 |
+=============+===================+=========+
|oci          |指明模式为 Oci     |是       |
+-------------+-------------------+---------+
|odbc         |指明模式为 Odbc    |是       |
+-------------+-------------------+---------+
|pdo          |指明模式为 Pdo     |是       |
+-------------+-------------------+---------+

`在 Oracle 中 mode 参数默认为 pdo`


:config:

+-------------+-----------------------------------------------------------+---------+--------+
|参数名       |说明                                                       |是否可选 |默认值  |
+=============+===========================================================+=========+========+
|host         |主机名                                                     |否       |\       |
+-------------+-----------------------------------------------------------+---------+--------+
|user         |用户名                                                     |否       |\       |
+-------------+-----------------------------------------------------------+---------+--------+
|password     |密码                                                       |否       |\       |
+-------------+-----------------------------------------------------------+---------+--------+
|dbname       |数据库名                                                   |否       |\       |
+-------------+-----------------------------------------------------------+---------+--------+
|port         |端口                                                       |是       |        |
+-------------+-----------------------------------------------------------+---------+--------+
|charset      |编码                                                       |是       |UTF8    |
+-------------+-----------------------------------------------------------+---------+--------+
|prefix       |表前缀                                                     |是       |        |
+-------------+-----------------------------------------------------------+---------+--------+
|session_mode |会话模式，使用模式 oci 时有效                              |是       |null    |
+-------------+-----------------------------------------------------------+---------+--------+
|connect_type |连接模式，使用模式 oci 时有效                              |是       |1       |
+-------------+-----------------------------------------------------------+---------+--------+
|opts         |其他选项，使用模式 pdo 时有效                              |是       |[]      |
+-------------+-----------------------------------------------------------+---------+--------+
|driver       |驱动名，使用模式 odbc 时有效                               |是       |null    |
+-------------+-----------------------------------------------------------+---------+--------+

