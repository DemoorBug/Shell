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
|||||
|||||

## 常用目录的作用
`
/根目录
/bin命令保存目录 (普通用户就可使用) /sbin (root才可修改) /usr还有bin目录意思同前面
/boot 启动目录 保存的是启动数据
/dev 特殊文件目录
/etc 保存的是默认配置文件
/home 是普通用户目录
/root 超级管理员目录
/lib 函数库
/mis /media /mnt 挂载U盘 空目录，所有存储设备都要挂着后使用，挂载就是分配盘符，用着作为外接存储的盘符 /mnt挂U盘 移动硬盘，老师在/mnt目录下创建CDrm 挂载光盘，同时创建mst挂载U盘
> 为什么呢 因为老式的linux 没有其他两个目录 /mis挂载磁带机 /media 挂载光盘 

/proc /sys 不能直接操作，保存的是内存的挂载点，直接写在内存当中，无法写入数据
/tmp 临时目录
/usr 系统资源保存目录
/var 系统相关文档
> 练习的话就在tmp和root，home下

`