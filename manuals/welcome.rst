========
欢迎使用
========

FizeDb 是一个全功能的易于扩展的数据库类库、ORM类库。

FizeDb 自创的DMR(定义层-中间层-实现层)模式使得其可以进行任意数据库、任意模式的扩展。

FizeDb 可以进行数据库连接模式选择，因此您可以根据系统环境自行选择连接模式。

通过隐藏各数据库之间的差异性，您会发现操作数据库是如此简单，对数据库选型不再是问题，您可以随时切换数据库类型。

众多 Fize 项目依赖 FizeDb ，同时欢迎您使用 Fize。

FizeDb 有非常完善的参考文档，且其功能追求简洁明了，相信您会喜欢上这样的一款ORM框架。


数据库支持
==========

目前 FizeDb 已支持的数据库如下：

-  :doc:`Access </libraries/realization/access/db>` : 支持模式 adodb 、odbc 、pdo 。
-  :doc:`MSSQL </libraries/realization/mssql/db>` : 支持模式 adodb 、odbc 、pdo 、sqlsrv 。
-  :doc:`MySQL </libraries/realization/mysql/db>` : 支持模式 mysqli 、 odbc 、 pdo 。
-  :doc:`Oracle </libraries/realization/oracle/db>` : 支持模式 oci 、 odbc 、 pdo 。
-  :doc:`PostgreSQL </libraries/realization/pgsql/db>` : 支持模式 odbc 、 pdo 、 pgsql 。
-  :doc:`SQLite </libraries/realization/sqlite/db>` : 支持模式 odbc 、 pdo 、 sqlite3 。


入门三部曲
==========

1.配置参数
----------

FizeDb 的主要参数分 3 个部分：type 、mode 、config

-  `type` : 数据库类型，小写即可。目前支持 access 、mssql 、mysql 、oracle 、 pgsql 、 sqlite 。
-  `mode` : 数据库支持模式。不同的数据库支持模式并不相同，请查看数据库支持进行支持模式选择。
-  `config` : 数据库参数。根据数据库的类型和支持模式，会有不同的参数设置。

2.设置默认连接或者设置新连接
----------------------------

使用 `new Db($config)`进行默认连接设置，或者 `Db::connect($config)` 方法设置新连接

3.进行数据库操作
----------------

FizeDb 内置了一系列的方法用于数据库的 `CURD` 等操作。我们主要使用 `\fize\db\Db` 类和 `\fize\db\Query` 进行数据库操作。

- `\fize\db\Db` 类 : 定义数据库操作。
- `\fize\db\Query` 类 : 定义数据库查询条件语句。


入门示例
========

.. code-block:: php

	use fize\db\Db;

	//设置默认连接
	$config = [
		'type'   => 'mysql',
		'mode'   => 'pdo',
		'config' => [
			'host'     => 'localhost',
			'user'     => 'root',
			'password' => '123456',
			'dbname'   => 'gm_test'
		]
	];

	new Db($config);

	$rows = Db::table('user')
		->where([
			'name' => ['LIKE', '陈某某%']
		])
		->limit(2)
		->select();
	var_dump($rows);

	//设置新连接
	$config = [
		'type'   => 'mysql',
		'mode'   => 'pdo',
		'config' => [
			'host'     => 'localhost',
			'user'     => 'root',
			'password' => '123456',
			'dbname'   => 'gm_test2',
			'prefix'   => 'gm_'
		]
	];
	$db = Db::connect($config);

	$rows = $db
		->table('admin')
		->limit(10)
		->select();
		var_dump($rows);
		
