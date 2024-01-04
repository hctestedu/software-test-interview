## 9-36-requests如何做post请求接口

定义URL，定义data数据，参数用字典格式保存

\#表单格式数据请求

import requests

\#方维的注册接口

url = "http://47.95.118.117/fanwe/indexphp?ctl=user&act=doregister"

data={‘user name’:’cxy0o3’,

‘mobile’：’18312345676’,

‘user_pwd’：’cxy1234561’,

‘user_pwd confirm’：'cxy123456',

‘agreement’：’1’,

‘commit’：’注册’}

r=requests.post(url=url，data= data)

print(r.text)
