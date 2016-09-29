|命令|常用参数|命令英文原意|简介|
|:--:|:--:|:--:|:--|
|yum|list||查询所有可用软件包列表|
|yum|search||搜索服务器上所有和关键词相关的包|
|yum|-y,install||yum -y install gcc|
|yum -y upgrade|||--setopt=protected_multilib=false|
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
 
##源码包安装
```
源码包保存位置:/usr/local/src
软件安装位置:/usr/local/
如何确定安装过程报错:
    安装过程停止
    并出现error、warning或no的提示

tar -zxvf
./configure 软件配置与检查
定义需要的功能选项
检测系统环境是否符合安装要求
把定义好的功能选项和检测系统环境的信息都写入Makefile文件，用于后续的编辑
./configure --help
./configure --prefix=/usr/local/node/
```

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

##配置文件的一些选项，最后一个为准
```
/usr/local/mongodb-3.2.9/bin/mongod --dbpath=/usr/local/mongodb-3.2.9/data/db --logpath=/usr/local/mongodb-3.2.9/mongodb/logs --logappend --bind_ip=0.0.0.0 --port=27017 --auth --fork  

mongod --dbpath=/usr/local/mongodb-3.2.9/data/db --logpath=/usr/local/mongodb-3.2.9/mongodb/logs --logappend --fork

/usr/local/mongodb-3.2.9

dbpath = /usr/local/mongodb-3.2.9/mongodb/data/db #数据文件存放目录
logpath = /usr/local/mongodb-3.2.9/mongodb/logs #日志文件存放目录
port = 27017  #端口
fork = true  #以守护程序的方式启用，即在后台运行
logappend = true # 追加
nohttpinterface = true
```

./configure --prefix=/usr/local/gcc-4.8.5 --enable-threads=posix --disable-checking --enable--long-long --host=i386-redhat-linux--with-system-zlib --enable-languages=c,c++,java

./configure --prefix=/usr/local/gcc-4.8.5 --enable-languages=c,c++,java

./configure --prefix=/usr/local/gcc-4.8.5 --enable-threads=posix --disable-checking --enable--long-long --enable-languages=c,c++,java

ftp://ftp.gnu.org/gnu/mpc/mpc-1.0.1.tar.gz

vi /etc/sysconfig/network-scripts/ifcfg-eth0

service network restart