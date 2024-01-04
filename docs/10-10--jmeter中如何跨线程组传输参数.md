## 10-10--jmeter中如何跨线程组传输参数

正则表达式或者边界值提取器或者JSON Extractor提取的值

后置处理器- beanshell处理器

定义成全局变量

${_setProperty(newtoken,${access_token},)}

其他线程组，引入变量值

${_P(newtoken,)}或者${_property(newtoken,)}
