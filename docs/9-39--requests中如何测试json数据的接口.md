## 9-39--requests中如何测试json数据的接口

定义参数json

\#json格式数据请求

import requests

Requests可以为 Https请求验证SSL证书，就像web浏览器一样。要想检查某个主机的ssl证书，你可以使用verify参数

处理办法:

1，设置 verify= False，requests请求忽略证书的校验，会有警告，提示

r=requests.get("https：/www.baidu.com"，verify=False）

print(r.text)

2，在verify中设置证书的路径

Requests.get(https：// github.com; verify=/atho/证书名字)

3，very默认值为true，也可以指定一个本地证书用作客户端证书，可以是单个文件(包含密钥和证书)或一个包含两个文件路径的元组

requests.get(‘https：//kennethreitz.com’,cert=(‘/path/server.crt',’/path/key’))

注册接口

import requests

Url="http：//localhost：8000/register"

json={

"username":"Cxy002"

"Password":"12345"

}

r=requests.post(url=url,json=json)

print (r.text)
