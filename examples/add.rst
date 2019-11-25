========
添加记录
========

.. code-block:: php

	use fize\db\Db;

	//设置默认连接
	$config = [
		'host'     => 'localhost',
		'user'     => 'root',
		'password' => '123456',
		'dbname'   => 'gm_test'
	];

	new Db('mysql', $config);

	$data = [
		'name'     => "!乱/七\八'糟\"的*字?符%串`一#大@堆(123",
		'add_time' => time()
	];
	$rst = Db::table('user')->insert($data);
	var_dump($rst);  //受影响行数(1)
	echo "<br/>";
	$sql = Db::getLastSql(true);
	print_r($sql);


	$id = Db::table('user')->insertGetId($data);
	var_dump($id);  //自增ID或则序列号