===================
ODBC预处理语句
===================


+-------------+-----------------------------------+
|属性         |值                                 |
+=============+===================================+
|命名空间     |fize\\db\\middleware\\driver\\odbc |
+-------------+-----------------------------------+
|类名         |Statement                          |
+-------------+-----------------------------------+


:方法:


+--------------------+--------------------------------------------------------------------------------------------------+
|方法名              |说明                                                                                              |
+====================+==================================================================================================+
|`__construct()`_    |构造                                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`binmode()`_        |对结果集设置处理二进制数据的模式                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------+
|`cursor()`_         |返回结果游标名称                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------+
|`execute()`_        |执行当前预处理语句                                                                                |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fetchArray()`_     |以数组形式遍历结果集                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fetchInto()`_      |遍历结果集到指定数组                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fetchObject()`_    |以对象形式遍历结果集                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fetchRow()`_       |移动结果集指针，使用该方法后，下次使用odbc_result()将返回下一行的结果                             |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldLen()`_       |获取字段的长度(精度)                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldName()`_      |获取字段名称                                                                                      |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldNum()`_       |获取字段下标(从1开始)                                                                             |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldPrecision()`_ |获取字段的长度(精度)                                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldScale()`_     |获取字段的小数位数                                                                                |
+--------------------+--------------------------------------------------------------------------------------------------+
|`fieldType()`_      |获取字段的类型                                                                                    |
+--------------------+--------------------------------------------------------------------------------------------------+
|`freeResult()`_     |释放当前结果内存                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------+
|`longreadlen()`_    |设置允许的最长字段列处理                                                                          |
+--------------------+--------------------------------------------------------------------------------------------------+
|`nextResult()`_     |对于多个结果集，将指针移到下个结果集                                                              |
+--------------------+--------------------------------------------------------------------------------------------------+
|`numFields()`_      |返回结果中的列数                                                                                  |
+--------------------+--------------------------------------------------------------------------------------------------+
|`numRows()`_        |返回结果中的行(记录)数,对于操作，则返回受影响的行数                                               |
+--------------------+--------------------------------------------------------------------------------------------------+
|`resultAll()`_      |将结果以HTML表格形式打印出来。                                                                    |
+--------------------+--------------------------------------------------------------------------------------------------+
|`result()`_         |获取当前结果记录的某列值                                                                          |
+--------------------+--------------------------------------------------------------------------------------------------+
|`setoption()`_      |改变属性                                                                                          |
+--------------------+--------------------------------------------------------------------------------------------------+


方法
======
__construct()
-------------
构造

.. code-block:: php

  public function __construct (
      resource &$statement
  )


:参数:
  +----------+----------------------------+
  |名称      |说明                        |
  +==========+============================+
  |statement |预处理语句资源对象          |
  +----------+----------------------------+
  
  


binmode()
---------
对结果集设置处理二进制数据的模式

.. code-block:: php

  public function binmode (
      int $mode
  ) : bool


:参数:
  +-------+---------------------------------------------------------------------------------------------+
  |名称   |说明                                                                                         |
  +=======+=============================================================================================+
  |mode   |指定模式， 可选值 ODBC_BINMODE_PASSTHRU | ODBC_BINMODE_RETURN | ODBC_BINMODE_CONVERT         |
  +-------+---------------------------------------------------------------------------------------------+
  
  


cursor()
--------
返回结果游标名称

.. code-block:: php

  public function cursor () : string



execute()
---------
执行当前预处理语句

.. code-block:: php

  public function execute (
      array $parameters_array = []
  )


:参数:
  +-----------------+----------------+
  |名称             |说明            |
  +=================+================+
  |parameters_array |可选的参数      |
  +-----------------+----------------+
  
  


fetchArray()
------------
以数组形式遍历结果集

.. code-block:: php

  public function fetchArray (
      int $rownumber = null
  ) : array


:参数:
  +----------+-------------------------+
  |名称      |说明                     |
  +==========+=========================+
  |rownumber |指定要检索的行数         |
  +----------+-------------------------+
  
  


fetchInto()
-----------
遍历结果集到指定数组

.. code-block:: php

  public function fetchInto (
      array &$result_array,
      int $rownumber = null
  ) : int


:参数:
  +-------------+-------------------------------+
  |名称         |说明                           |
  +=============+===============================+
  |result_array |结果集将添加到该数组           |
  +-------------+-------------------------------+
  |rownumber    |指定要检索的行数               |
  +-------------+-------------------------------+
  
  

:返回值:
  返回结果行数


fetchObject()
-------------
以对象形式遍历结果集

.. code-block:: php

  public function fetchObject (
      int $rownumber = null
  ) : object


:参数:
  +----------+-------------------------+
  |名称      |说明                     |
  +==========+=========================+
  |rownumber |指定要检索的行数         |
  +----------+-------------------------+
  
  

:返回值:
  一个对象表示一个行


fetchRow()
----------
移动结果集指针，使用该方法后，下次使用odbc_result()将返回下一行的结果

.. code-block:: php

  public function fetchRow (
      int $row_number = null
  ) : bool


:参数:
  +-----------+-------------------------+
  |名称       |说明                     |
  +===========+=========================+
  |row_number |指定要检索的行数         |
  +-----------+-------------------------+
  
  

:返回值:
  成功返回true，失败返回false


fieldLen()
----------
获取字段的长度(精度)

.. code-block:: php

  public function fieldLen (
      int $field_number
  ) : bool|int


:参数:
  +-------------+-------------------------+
  |名称         |说明                     |
  +=============+=========================+
  |field_number |字段下标(从1开始)        |
  +-------------+-------------------------+
  
  

:返回值:
  失败时返回false


fieldName()
-----------
获取字段名称

.. code-block:: php

  public function fieldName (
      int $field_number
  ) : bool|string


:参数:
  +-------------+-------------------------+
  |名称         |说明                     |
  +=============+=========================+
  |field_number |字段下标(从1开始)        |
  +-------------+-------------------------+
  
  

:返回值:
  失败时返回false


fieldNum()
----------
获取字段下标(从1开始)

.. code-block:: php

  public function fieldNum (
      string $field_name
  ) : bool|int


:参数:
  +-----------+-------------+
  |名称       |说明         |
  +===========+=============+
  |field_name |字段名称     |
  +-----------+-------------+
  
  

:返回值:
  失败时返回false


fieldPrecision()
----------------
获取字段的长度(精度)

.. code-block:: php

  public function fieldPrecision (
      int $field_number
  ) : bool|int


:参数:
  +-------------+-------------------------+
  |名称         |说明                     |
  +=============+=========================+
  |field_number |字段下标(从1开始)        |
  +-------------+-------------------------+
  
  

:返回值:
  失败时返回false


fieldScale()
------------
获取字段的小数位数

.. code-block:: php

  public function fieldScale (
      int $field_number
  ) : bool|int


:参数:
  +-------------+-------------------------+
  |名称         |说明                     |
  +=============+=========================+
  |field_number |字段下标(从1开始)        |
  +-------------+-------------------------+
  
  

:返回值:
  失败时返回false


fieldType()
-----------
获取字段的类型

.. code-block:: php

  public function fieldType (
      int $field_number
  ) : bool|string


:参数:
  +-------------+-------------------------+
  |名称         |说明                     |
  +=============+=========================+
  |field_number |字段下标(从1开始)        |
  +-------------+-------------------------+
  
  

:返回值:
  失败时返回false


freeResult()
------------
释放当前结果内存

.. code-block:: php

  public function freeResult () : bool



longreadlen()
-------------
设置允许的最长字段列处理

.. code-block:: php

  public function longreadlen (
      int $length
  ) : bool


:参数:
  +-------+-------------------+
  |名称   |说明               |
  +=======+===================+
  |length |最长字段长度       |
  +-------+-------------------+
  
  


nextResult()
------------
对于多个结果集，将指针移到下个结果集

.. code-block:: php

  public function nextResult () : bool



numFields()
-----------
返回结果中的列数

.. code-block:: php

  public function numFields () : int



numRows()
---------
返回结果中的行(记录)数,对于操作，则返回受影响的行数

.. code-block:: php

  public function numRows () : int



resultAll()
-----------
将结果以HTML表格形式打印出来。

.. code-block:: php

  public function resultAll (
      string $format = null
  ) : int


:参数:
  +-------+-------------------------------+
  |名称   |说明                           |
  +=======+===============================+
  |format |附加的整体表格格式。           |
  +-------+-------------------------------+
  
  

:返回值:
  返回结果集大小，失败返回false


result()
--------
获取当前结果记录的某列值

.. code-block:: php

  public function result (
      mixed $field
  ) : mixed


:参数:
  +-------+----------------------------+
  |名称   |说明                        |
  +=======+============================+
  |field  |字段名或者字段顺序          |
  +-------+----------------------------+
  
  


setoption()
-----------
改变属性

.. code-block:: php

  public function setoption (
      int $option,
      int $param
  ) : bool


:参数:
  +-------+----------+
  |名称   |说明      |
  +=======+==========+
  |option |属性名    |
  +-------+----------+
  |param  |属性值    |
  +-------+----------+
  
  


