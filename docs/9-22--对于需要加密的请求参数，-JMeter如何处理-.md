## 9-22--对于需要加密的请求参数，-JMeter如何处理-

这里首先让开发给我们写一个加密，解密的jar， JMeter直接调用这个jar进行加密，解密处理

1、首先需要将开发给到的加解密的jar包文件放到 jmeter的lib/ext目录下

2、在测试计划中中有一个 add Directory or jar to classpath，在这里指定jar的路径，添加需要的jar包

3、在jmeter的前置处理器中添加 Beanshell PreProcessor然后在其中添加java代码

具体就是：

a.首先导入需要用到的加密包中的加密算法类，

b.如果要对json格式的请求参数加密，组装json格式的数据

c.调用加密类中的函数对json格式的参数数据进行加密，如果只对具体某个参数加密，

那就针对哪个参数加密即可。

d.然后将加密之后的数据保存到 jmeter的一个变量中就可以了

4、最后直接在消息体中引用这个变量就可以了

具体代码如下：

Jmeter调用

mport com changfu EncryptAnd Decryptinterface; #导入加密类

String json_str =

"{\"Username\":\"amycheno2\"，\"password\"：\"F59BD65F7EDAFB087A81D4DC

AO6c4910\",\"deviceNo\",\"35584806988942\")";      #请求的参数

调用加密类中的函数对请求参数实现加密处理。

String enpost= EncryptAndDecryptinterface.getEncryptPost(json_str);  #将请求参数加密

vars put("enpost"，enpost);    #将加密处理后的数据存到 jmeter变量中
