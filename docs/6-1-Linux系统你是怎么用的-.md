## 6-1-Linux系统你是怎么用的-

[在测试1、执行的过程中，我们发现的bug，有时候需要定位bug，协助开发修复bug时需要在linux里通过命令tail-200或tail-500查看当天的日志的**后面**多少行或者**前面**多少行定位bug或者通过tail -f来查看日志里的关键字 exception(异常) error(错误)。

[后台程序运行久了会对系统造成卡顿等诸多隐患或我们做性能测试的时候我们都会通过linux的命令Ps -ef显示所有进程)、top(监控程序执行状况)、free -m显示内存使用情况)

来查看系统资源如果服务器出现故障时我们也会用（service httpd status）看下服务器是否启动，用ps -ef|grep httpd查看apache进程是否启动，用ps -ef|grepjava查看jdk进程是否启动如果服务器起不来，常见的问题有端口可能被占用，用 netstat- an|grep 8080查看端口是否已被占用。]

[搭建测试环境的时候我们在是在linux下进行的，搭建LAMP时在线用命令 yum install

安装 apache，php以及mysql;或通过 xshell来导入需要的环境包来搭建LTMJ(Tomcat、Mysql、jdk)
