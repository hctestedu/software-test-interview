## 9-21--对于POST请求，要求传递Json格式数据，-JMeter怎么做

对于这个其实在 JMeter的http请求这个组件中的参数配置栏目中，第二个栏目有个消息体数据，我们把需要上传的参数组装成json格式，然后编写到 body data里面，然后，需要在http信息头管理其中，需要将数据格式设置为json格式，这个就是设置Content-Type

为 application/json：charset=utf-8，这样就可以了。
