# 所学命令的一些大致顺序 以及简介
|命令|常用参数|命令英文原意|简介|
|:--:|:--:|:--:|:--|
|2016-9-22|
|pwd|no|print working directory|查询所在目录位置|
|ls|-aldhi||查询目录内容|
|-rw-r--r--||no|r读w写x执行|
|mkdir|-p|make directories|建立目录|
|cd|~ - .. .|change directory|切换所在目录|
|tab|no||目录补全,命令补全,按两下就会显示当前目录的东西|
|rmdir|no|remove empty directories|删除，但是不常用，有文件内容就无法删除|
|rm|-rf|remove|删除文件或目录|
|cp|-rpd -a|copy|复制命令-a相当于-rpd|
|mv||move|剪切或改名命令|
|2016-9-23|
|ln|-s|link|链接命令 **最好使用-s(软链接)方式创建**|
|locate|||文件搜索命令，搜索速度快,在/var/lib/mlocate 下搜索后台数据库|
|updatedb|||每天更新一次，所以可以手动更新|
|whereis|-bm||搜索命令的命令,ls.1.gz 1 命令 man -f ls ，man 1 ls 一致|
|which|||搜索命令的命令。搜索命令所在路径及别名|
|find|||-iname -user -nouser **find / -name install.log**|
|* ? []|||通配符*任意内容?一个内容[]任意一个中括号中的内容|
|-exec {}\|||可以在其他命令之后再继续执行命令|
|grep|-iv||搜索字符串命令 grep [选项] 字符串 文件名|
|man|-f||帮助命令 man ls **man 需要下载包** 编辑模式\-d 然后按n就可以向下跳 shift上|
|||||
|||||
|||||
> locate 遵循/etc/updatedb.conf 配置文件
 
> find /var/log/ -mtime +10 查找10天前修改的文件
> -10 10天内修改的文件
> 10 10天当天修改的文件
> +10 10天前修改的文件
> 
>  atime 文件访问时间
>  ctime 改变文件属性
>  mtime 修改文件内容
>  
> find . -size 25k 查找文件大小是25K的文件
> **25M M要大写**
> -25k 小于25KB的文件
> 25K 等于25KB的文件
> + 大于 25KB的文件
> 
> find . -inum 262422
> 查找I节点是262422的文件 
> 
> find /etc -size +20k -a -size -50k
> \#查找/etc目录下，大于20KB并且小于50KB的文件
> -a and 逻辑于 
> -o or 逻辑或 
> 
> find /etc -size +20k -a -size -50k -exec ls -lh {} \;

## 常用目录的作用
```
/根目录
/bin命令保存目录 (普通用户就可使用) /sbin (root才可修改) /usr还有bin目录意思同前面
/boot 启动目录 保存的是启动数据
/dev 特殊文件目录
/etc 保存的是默认配置文件
/home 是普通用户目录
/root 超级管理员目录
/lib 函数库
/mis /media /mnt 挂载U盘 空目录，所有存储设备都要挂着后使用，挂载就是分配盘符，用着作为外接存储的盘符 /mnt挂U盘 移动硬盘，老师在/mnt目录下创建CDrm 挂载光盘，同时创建mst挂载U盘
*** 为什么呢 因为老式的linux 没有其他两个目录 /mis挂载磁带机 /media 挂载光盘  *** 

/proc /sys 不能直接操作，保存的是内存的挂载点，直接写在内存当中，无法写入数据
/tmp 临时目录
/usr 系统资源保存目录
/var 系统相关文档
*** 练习的话就在tmp和root，home下 ***

```