## 10-18--你们-python接口自动化怎么去处理-cookie，-session的-

对于 cookie，session的处理一般有三种方式:

第一种就是先获取登录请求的 cookie值，然后发送其他请求的时候，在 requests提供的

两个方法get或post方法中有一个 cookies参数，我们可以通过这个参数来传递 cookies值

第二种就是通过订制请求头，然后把获取到的coookies放在请求头中，通过请求头来进行传递

第三种就是通过创建一个 session会话对象，后期所有的请求发送都通过调用这个 session会话对象来进行发请求，如果是登录请求，它会自动保存 cookies值，然后其他需要用到cookies值的请求，也通过 session对象来发送，它会自动把 cookies发送出去,对于 cookies， session的处理，我们差不多都是通过以上三种方式来实现的
