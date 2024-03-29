======
模式
======


::

    MySQL数据库模型类


+-------------+-----------------------------+
|属性         |值                           |
+=============+=============================+
|命名空间     |fize\\db\\realization\\mysql |
+-------------+-----------------------------+
|类名         |Mode                         |
+-------------+-----------------------------+
|实现接口     |fize\\db\\definition\\Mode   |
+-------------+-----------------------------+


:方法:


+-----------------+-------------------+
|方法名           |说明               |
+=================+===================+
|`mysqli()`_      |mysqli方式构造     |
+-----------------+-------------------+
|`odbc()`_        |odbc方式构造       |
+-----------------+-------------------+
|`pdo()`_         |Pdo方式构造        |
+-----------------+-------------------+
|`getInstance()`_ |数据库实例         |
+-----------------+-------------------+


方法
======
mysqli()
--------
mysqli方式构造

.. code-block:: php

  public static function mysqli (
      string $host,
      string $user,
      string $pwd,
      string $dbname,
      mixed $port = "",
      string $charset = "utf8",
      array $opts = [],
      bool $real = true,
      string $socket = null,
      array $ssl_set = [],
      int $flags = null
  ) : \fize\db\realization\mysql\mode\Mysqli


:参数:
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |名称    |说明                                                                                                                                                          |
  +========+==============================================================================================================================================================+
  |host    |服务器地址                                                                                                                                                    |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |user    |用户名                                                                                                                                                        |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |pwd     |用户密码                                                                                                                                                      |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |dbname  |指定数据库                                                                                                                                                    |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |port    |端口号，MySQL默认是3306                                                                                                                                       |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |charset |指定编码，选填，默认utf8                                                                                                                                      |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |opts    |设置MYSQL连接选项                                                                                                                                             |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |real    |是否使用real方式，默认true                                                                                                                                    |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |socket  |指定应使用的套接字或命名管道，选填，默认不指定                                                                                                                |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |ssl_set |设置SSL选项，选填，为数组参数，其下有参数ENABLE、KEY、CERT、CA、CAPATH、CIPHER，如果ENABLE为true，则其余参数都需要填写                                        |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  |flags   |设置连接参数，选填，如MYSQLI_CLIENT_SSL等                                                                                                                     |
  +--------+--------------------------------------------------------------------------------------------------------------------------------------------------------------+
  
  


odbc()
------
odbc方式构造

.. code-block:: php

  public static function odbc (
      string $host,
      string $user,
      string $pwd,
      string $dbname,
      mixed $port = "",
      string $charset = "utf8",
      string $driver = null
  ) : \fize\db\realization\mysql\mode\Odbc


:参数:
  +--------+----------------------------------------+
  |名称    |说明                                    |
  +========+========================================+
  |host    |服务器地址                              |
  +--------+----------------------------------------+
  |user    |用户名                                  |
  +--------+----------------------------------------+
  |pwd     |用户密码                                |
  +--------+----------------------------------------+
  |dbname  |数据库名                                |
  +--------+----------------------------------------+
  |port    |端口号，选填，MySQL默认是3306           |
  +--------+----------------------------------------+
  |charset |指定编码，选填，默认utf8                |
  +--------+----------------------------------------+
  |driver  |指定ODBC驱动名称。                      |
  +--------+----------------------------------------+
  
  


pdo()
-----
Pdo方式构造

.. code-block:: php

  public static function pdo (
      string $host,
      string $user,
      string $pwd,
      string $dbname,
      int $port = null,
      string $charset = "utf8",
      array $opts = [],
      string $socket = null
  ) : \fize\db\realization\mysql\mode\Pdo


:参数:
  +--------+---------------------------------------------------------------------------------------+
  |名称    |说明                                                                                   |
  +========+=======================================================================================+
  |host    |服务器地址                                                                             |
  +--------+---------------------------------------------------------------------------------------+
  |user    |用户名                                                                                 |
  +--------+---------------------------------------------------------------------------------------+
  |pwd     |用户密码                                                                               |
  +--------+---------------------------------------------------------------------------------------+
  |dbname  |数据库名                                                                               |
  +--------+---------------------------------------------------------------------------------------+
  |port    |端口号，选填，MySQL默认是3306                                                          |
  +--------+---------------------------------------------------------------------------------------+
  |charset |指定编码，选填，默认utf8                                                               |
  +--------+---------------------------------------------------------------------------------------+
  |opts    |PDO连接的其他选项，选填                                                                |
  +--------+---------------------------------------------------------------------------------------+
  |socket  |指定应使用的套接字或命名管道,windows不可用，选填，默认不指定                           |
  +--------+---------------------------------------------------------------------------------------+
  
  


::

    强烈推荐使用


getInstance()
-------------
数据库实例

.. code-block:: php

  public static function getInstance (
      string $mode,
      array $config
  ) : \fize\db\realization\mysql\Db


:参数:
  +-------+----------------------+
  |名称   |说明                  |
  +=======+======================+
  |mode   |连接模式              |
  +-------+----------------------+
  |config |数据库参数选项        |
  +-------+----------------------+
  
  


