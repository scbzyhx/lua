#Lua——数据库访问  

简单的数据操作，我们用文件就可以处理。但是，某些时候文件操作存在性能、扩展性等问题。这时候，我们就需要使用数据库。LuaSQL 是提供不同 SQL 数据库操作支持的库。它包括：  

<ul>
	<li>SQLite</li>
	<li>MySQL</li>
	<li>ODBC</li>
</ul>  
在本教程中，我们会学到 Lua 中 MySQL 数据库的操作。其中的操作具有一般性，它们能也应该可以移植到其它类型的数据库中。首先让我们看一下如何操作 MySQL 数据库。  

##MySQL 数据库设置 

为了下面的例子可以正确演示，我们需要初始化数据库设置。我们假设你已经完成了如下的工作：  


<ul>
	<li>安装 MySQL 数据库，使用默认用户名 root， 密码为： 123456。</li>
	<li>创建数据库 test。</li>
	<li>已经阅读过关于 MySQL 的基本教程，并掌握了 MySQL 的基本知识。</li>
</ul>  

##导入 MySQL  

假设你已经安装配置正确了，那么我们可以使用 require　语句导入　sqlite 库。安装过程中会产生一个存储数据相关文件的目录 libsql。  

```
mysql = require "luasql.mysql"
```  

###建立连接 

先初始化 MySQL 的环境，再建立一个连接。如下所示：  

```
local env  = mysql.mysql()
local conn = env:connect('test','root','123456')
```  

**上面的程序会与已存在的 MySQL 文件建立连接，并与创建的文件建立一个连接。**

###执行函数  

