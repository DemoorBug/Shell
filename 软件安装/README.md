|命令|常用参数|命令英文原意|简介|
|:--:|:--:|:--:|:--|
|yum|list||查询所有可用软件包列表|
|yum|search||搜索服务器上所有和关键词相关的包|
|yum|-y,install||yum -y install gcc|
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||
|||||
> service httpd start 实际搜索的是 /etc/rc.d/init.d/httpd start 目录

> error、warning或no 表示源码包安装报错

## RPM包安装默认位置
```
/etc/   配置文件安装目录
/usr/bin 可执行的命令安装目录
/usr/lib 程序所使用的函数库保存位置
/usr/share/doc/ 基本的软件使用手册保存位置
/usr/share/man/ 帮助文件保存位置
源码包一般安装在
/usr/local/软件名/
```

/usr/local/mongodb-3.2.9/bin/mongod --dbpath=/usr/local/mongodb-3.2.9/data/db --logpath=/usr/local/mongodb-3.2.9/mongodb/logs --logappend --bind_ip=0.0.0.0 --port=27017 --auth --fork  

mongod --dbpath=/usr/local/mongodb-3.2.9/data/db --logpath=/usr/local/mongodb-3.2.9/mongodb/logs --logappend --fork

/usr/local/mongodb-3.2.9