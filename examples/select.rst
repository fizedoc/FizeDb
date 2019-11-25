========
查询记录
========

.. code-block:: php

	use fize\db\Db;

	$config = [
		'host'     => 'localhost',
		'user'     => 'root',
		'password' => '123456',
		'dbname'   => 'gm_test'
	];

	new Db('mysql', $config);

	$map2 = [
		'name' => ['LIKE', '陈峰展%']
	];
	$list = Db::table('user')->where($map2)->limit(2)->select();
	echo Db::getLastSql();
	echo "<br/>";
	var_dump($list);
