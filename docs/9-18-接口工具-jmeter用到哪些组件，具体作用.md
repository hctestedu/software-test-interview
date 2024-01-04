## 9-18-接口工具-jmeter用到哪些组件，具体作用

**取样器**:

http请求         向服务器发htp请求

JDBC Requst      向数据库发请求

Debug Sampler       调试，看执行过程

Bean Shel取样器     把某个变量设置定位全局变量

**后置处理器**:

正则表达式提取器

\#提取接口的响应内容或请求内容中的数据具体要提什么数据根据需求来，比如我们充值接口依赖登录接口，需要用到登录

接口的 cookie，需要提取 cookie

边界值提取器

JSON提取器

Bean Shell Post Precessor     #在请求结束之后需要做的某些事情

比如转码

**断言**：  #检验结果，验证本接口是否有问题

响应断言

Json断言

**配置元件**:

CSV data Set Config           #读取CSV文件，txt文件

JDBC Connection Confiquration      #连接数据库

Http Cookie管理器

HTTP信息头管理器

用户定义的变量

计数器

**定时器**:

同步定时器，主要用来设置集合点

**监听器**:

查看结果数
