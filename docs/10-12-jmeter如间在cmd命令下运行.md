## 10-12-jmeter如间在cmd命令下运行

Jmeter -n -t文件路径\fw-zhuce.jmx -l result.jtl -e -o E:\resultreport

讲解：非GUI界面，压测参数讲解

-h帮助

-n非GUl模式

-t指定要运行的 JMeter测试脚本文件

-l记录结果的文件每次运行之前，(要确保之前没有运行过即xxx.jtl不存在，不然报错)

-r Jmter.properties文件中指定的所有远程服务器

-e脚本运行结束后生成html报告

-o用于存放html报告的目录(目录要为空，不然报错)

-R表示选择执行=远程启动

XXX.XXX. XXX. XXX：5174 ，XXX. XXX. XXX. XXX：5172

官方配置文件地址http：//jmeter.apache.org/usermanual/get-started.html
