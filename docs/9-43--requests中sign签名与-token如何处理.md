## 9-43--requests中sign签名与-token如何处理

Token值

token的意思是“令牌”，是服务端生成的一串字符串，作为客户端进行请求的一个标识。

当用户第一次登录后，服务器生成一个 token并将此 token返回给客户端，以后客户端只需带上这个 token前来请求数据即可，无需再次带上用户名和密码。

简单 token的组成;uid(用户唯一的身份标识、time当前时间的时间戳、sign(签名,token的前几位以哈希算法压缩成的一定长度的十六进制字符串。为防止 token泄露)

import requests

import re

url='http：//loclhost：8000/login'

Data={

'Username':'cxy002'

'Password':'123456'

}

r=requests.post(url=url,data= data)

print (r.text,type(r.text))

rk=re.findall("token":"(.*?)","r.text")

print(rk)

url="http://localhost:8000/recharge"

data=(

money：10000

Serial_number： 22222

token： rk

p=requests. post(url=url， data= data)

print(p.text)

sign签名：也是一种安全校验

sign的处理一个案例

post请求htps://{url地址}/ index.php/Platen/Card/active

参数:

Hotel_store_id=0123456&

Pack_id=4&

phone=175861263288&

sign=5dc6331b07fc097d013410353740f8e8168c499a

签名算法:

1.将发送数据按照参数名ASCLL码从小到大排序(字典序)，使用URL键值对的格式(如

key= value1&key2=vaue2...)，得到str，注意：sign不参与签名。

2.在str后面拼接"&key= YpLdvl2L3Rc5yYX"其中 YpLdvl2L3Rc5yYX为加密密钥

3.对字符串str进行sha1运算，得到签名sign

def test_xielv():

url="https://{url地址}/index.php/Platen/Card/active"

Json_v={

"Hotel_store_id"："0123456"

"pack_id"："4"

"phone"："18319011906"

}

\#字典添加新的key

Json_v["sign"]=sign_01(json_v)

\# print (json_v)打印发送请求的json值

r=requests.post(url=url,json=json_v)

print (r.content.decode("unicode_escape"))

assert'{"code：1002msg："ID错误或找不到

data"： "")==rcontent. decodeCunicode escape")
