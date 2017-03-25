# xbatis
极简风格的RESTful无后端Node框架，只需要写SQL，然后直接RESTful请求，全自动CRUD，与xmodel项目相辅相成

使用说明
>
	1,config/default.js中设置数据库连接，执行npm install
	2,提前创建好数据表，或者使用xmodel自动生成数据库
	2,node app.js(启动)

命名规则
>
	RESTful名，【下划线分割】
	yml文件名，【下划线分割】
	yml方法名，【驼峰法】

框架目录结构（后台）
>
    xmodel
        src/app.js——系统入口
        yaml/*.yml——SQL文件，这是使用该框架开发唯一需要写的文件

RESTful规则
>
	[POST]http://host:port/xbatis/MODEL_NAME/METHOD_NAME
	[POST]http://host:port/xbatis/MODEL_NAME/METHOD_NAME
	[POST]http://host:port/xbatis/MODEL_NAME/METHOD_NAME
	[POST]http://host:port/xbatis/MODEL_NAME/METHOD_NAME

例子
>
	以一个用户模块为例，需要对用户进行定制查询:
	[POST]http://host:port/xbatis/user/find_by_username
		post body:{"username":"cheney"}
	user.yml文件:
		findByUsername:	
    		- select * from user where username = :username

框架整合（开源力量）
>
    "body-parser": "^1.17.1",
    "config": "^1.25.1",
    "connect-flash": "^0.1.1",
    "express": "^4.15.2",
    "express-session": "^1.15.1",
    "moment": "^2.17.1",
    "passport": "^0.3.2",
    "passport-local": "^1.0.0",
    "tracer": "^0.8.7",
    "nodebatis": "^2.1.1"

帮助联系
>
	作者:cheneyxu
	邮箱:457299596@qq.com
	QQ:457299596

更新日志
>
	2017.03.18:无后端理念确认，1.0版本推出
	2017.03.25:代码与文档整理
