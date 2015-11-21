GoOut-shadowsocks-manyuser 是shadowsocks-manyuser 的一个分支

主要更新：
1.支持多服务器支持判断标识
2.配合GoOut.wang前端支持
3.添加流量套餐与时间套餐双套餐判断
4.优化数据库读取方式

支持库
1.Python
2.python-cymysql
3.python-m2crypto

配置文件
1.~/shadowsocks/Config.py

	#Config
	MYSQL_HOST = '数据库服务器地址'
	MYSQL_PORT = 3306
	MYSQL_USER = '用户名'
	MYSQL_PASS = '密码'
	MYSQL_DB = '数据库'
	ServerSign = '唯一标识符'

	MANAGE_PASS = '管理密码'
	#管理IP
	MANAGE_BIND_IP = '127.0.0.1'
	#管理端口
	MANAGE_PORT = 22222

数据库需要配合前端使用，后台不提供数据库

2.~/shadowsocks/config.json
	{
	    "server":"0.0.0.0",
	    "server_ipv6": "[::]",
	    "server_port":8388,
	    "local_address": "127.0.0.1",
	    "local_port":1080,
	    "password":"m",
	    "timeout":300,
	    "method":"aes-256-cfb"
	}
该配置文件只需要修改method 加密方式即可，其他参数基本没用但不可删除