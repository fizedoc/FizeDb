===============
未找到数据
===============


::

    未找到指定数据时触发该错误


+-------------+-------------------------------+
|属性         |值                             |
+=============+===============================+
|命名空间     |fize\\db\\exception            |
+-------------+-------------------------------+
|类名         |DataNotFoundException          |
+-------------+-------------------------------+
|父类         |fize\\db\\exception\\Exception |
+-------------+-------------------------------+
|实现接口     |Throwable                      |
+-------------+-------------------------------+


:方法:


+----------------------+-------------------------------+
|方法名                |说明                           |
+======================+===============================+
|`__construct()`_      |Exception constructor.         |
+----------------------+-------------------------------+
|`getSql()`_           |返回出错的相关SQL语句          |
+----------------------+-------------------------------+
|`__wakeup()`_         |                               |
+----------------------+-------------------------------+
|`getMessage()`_       |                               |
+----------------------+-------------------------------+
|`getCode()`_          |                               |
+----------------------+-------------------------------+
|`getFile()`_          |                               |
+----------------------+-------------------------------+
|`getLine()`_          |                               |
+----------------------+-------------------------------+
|`getTrace()`_         |                               |
+----------------------+-------------------------------+
|`getPrevious()`_      |                               |
+----------------------+-------------------------------+
|`getTraceAsString()`_ |                               |
+----------------------+-------------------------------+
|`__toString()`_       |                               |
+----------------------+-------------------------------+


方法
======
__construct()
-------------
Exception constructor.

.. code-block:: php

  public function __construct (
      string $message = "",
      int $code = 0,
      string $sql = ""
  )


:参数:
  +--------+-------------+
  |名称    |说明         |
  +========+=============+
  |message |错误信息     |
  +--------+-------------+
  |code    |错误码       |
  +--------+-------------+
  |sql     |SQL语句      |
  +--------+-------------+
  
  


getSql()
--------
返回出错的相关SQL语句

.. code-block:: php

  public function getSql () : string



__wakeup()
----------


.. code-block:: php

  public function __wakeup ()



getMessage()
------------


.. code-block:: php

  final public function getMessage ()



getCode()
---------


.. code-block:: php

  final public function getCode ()



getFile()
---------


.. code-block:: php

  final public function getFile ()



getLine()
---------


.. code-block:: php

  final public function getLine ()



getTrace()
----------


.. code-block:: php

  final public function getTrace ()



getPrevious()
-------------


.. code-block:: php

  final public function getPrevious ()



getTraceAsString()
------------------


.. code-block:: php

  final public function getTraceAsString ()



__toString()
------------


.. code-block:: php

  public function __toString ()



