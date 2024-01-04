## 9-38-有没有做过https接口，具体怎么做

https请求时在http请求中多了ssl证书，对于https请求的接口，

Requests可以为HTTPS请求验证SSL证书，就像web浏览器一样。要想检查某个主机的

SSL证书，你可以使用veiy参数

处理办法:

1、设置 verify= False，requests请求忽略证书的校验，会有警告，提示

r=requests.get(https：//www.baidu.com’,verify=false)

print (r.text)

2、在 verify中设置证书的路径

requests.get(https：//github.com’,verify=’/path/to/证书名字’)

3、 verify默认值为true，也可以指定一个本地证书用作客户端证书，可以是单个文件(包含密钥和证书)或一个包含两个文件路径的元组：

requests.get(‘https：//kennethreitz.com'，cert=(‘/path/server.crt'，/path/key))
