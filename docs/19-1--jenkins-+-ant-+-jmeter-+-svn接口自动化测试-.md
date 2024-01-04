## 19-1--jenkins-+-ant-+-jmeter-+-svn接口自动化测试-

jenkins + ant + jmeter + svn环境搭建

原来这个环境是我这边搭建的，

主要是几个步骤，

第一 Jenkins安装、第二，ant安装、第三， jmeter安装、第四， jmeter与ant连接

第五，Sn安装、第六，任务的构建

首先我们要确定jdk已经安装好了，jdk安装，可以下载jdk包，配置环境变量就行

再 jenkins搭建，原来我们是用yum安装命令， yum install -y jenkins安装 jelkins

如果yum安装不能进行，yum仓库添加 jenkins连接信息

或者就用下载安装包进行安装

ant安装，我们可以百度去下载，

像原来我们这边一般会把常见安装包文件执行，我都会保存一个安装文档，

当下载ant安装包以后，只需要解压，并且配置环境就可以了

jmeter安装，也是先下载安装包，把安装包导入到linux服务器，解压，配置环境变量就ok了

jmeter跟ant连接，主要是配置 build.xml的文件，

文件目录放在 jmeter目录下，build文件主要是配置,

jmeter的路径，保存生成html跟jtl报告的路径，还运行jmx脚本的路径

把 jmeter文件 ant-jmeter-1.1.1.jar放在ant目录下

把 jmeter-results-shanhe-me.xsl上传至 jmeter安装目录的 extras文件夹下

也要配置 jmeter.properties文件把输出结果由csv修改成xml

配置完成后，我们可以用 ant run运行调试下，能否运行脚本成功

svn服务器安装，原来已经安装好

安装，通过yum安装到服务器里面，建立资源库，配置里面配置文件，添加用户，修改权限，再通过,

svnserve -d -r /data/svn/启动服务器，同时我们要考虑防火墙是否允许访问或者关闭防火墙

jenkins任务的构建

在jmeter系统配置中，先要添加环境变量，主要是jdk的路径，ant的路径(linux服务器里面的路径)

添加2个插件，一个 html publisher pulin主要生成HTML报告，一个 performance

pgn运行 jmeter脚本生成jtl报告

再构建一个任务，

在任务中

丢弃旧的构建，

再源码管理，配置svn服务器路径，导出文件位置，还有svn用户与密码

配置生成jtl报告的位置

配置生成html报告的位置

配置定时构建，原来我们设置设置半个月跑一次

还配置邮件发送( jenkins，系统配置，配置邮件服务器地址)

原来我们持续集成是半个月运行一次，当然我们也可以手动构建

1，我们一般把写完的jmeter的脚本

2，通过svn把写好的脚本检入到svn服务器

3，在 jenkins任务下，选择定时构建，或者手动构建，检出svn上传最新脚本，去运行一般我们项目在修改新的功能模块，上线，转测之前，都会自动去运行脚本。

运行完成，我们再 jenkins下，查看脚本运行结果。
