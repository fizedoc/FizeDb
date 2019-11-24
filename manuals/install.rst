========
安装说明
========

FizeDb 的环境要求如下：

-  "php": ">=7.0.0"
-  如果使用 Adodb 中间层，请开启com_dotnet 、iconv 扩展。
-  如果 MySQL 使用 mysqli 模式，请开启 mysqli 扩展。
-  如果 Orcale 使用 oci 模式，请开启 oci8 扩展。
-  如果使用 Odbc 中间层，请开启 odbc 扩展。
-  如果使用 Pdo 中间层，请开启 pdo 扩展，并开启相应数据库的 pdo 扩展。
-  如果 PostgreSQL 使用 pgsql 模式，请开启 pgsql 扩展。
-  如果 SQLite 使用 sqlite3 模式，请开启 sqlite3 扩展。
-  如果 MSSQL 使用 sqlsrv 模式，请开启 sqlsrv 扩展，sqlsrv 扩展请在微软官方下载。

使用Composer安装
================

FizeDb 支持使用 `Composer <https://www.phpcomposer.com/>`_ 安装，也是唯一官方推荐的安装方法。

.. note::

   如果您尚未安装 composer ，请参考 `安装 composer <https://docs.phpcomposer.com/00-intro.html>`_ 。
   
   使用 `阿里云镜像 <https://developer.aliyun.com/composer?spm=a2c4e.11153940.0.0.40eb6995lM3bEz>`_ 以提高下载速度及稳定性。


在命令行下面，切换到您的项目根目录下面并执行下面的命令：

.. code-block:: bash

  composer require fize/db
  
好了！一步到位，您现在可以开始使用 FizeDb 了，就是这么简单！~

.. note::

   Fize 项目(包括所有子项目)严格遵守 `语义化版本 <https://semver.org/lang/zh-CN/spec/v2.0.0.html>`_ ，您可以放心大胆的使用。