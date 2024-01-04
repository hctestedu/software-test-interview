## 9-44-request框架有哪些方法-

像用来发送请求的一般都是调用以下方法

reponse=requests.get()

reponse=requests.post()

获取响应数据一般都是调用以下方法

reponse.status_code

reponse.reason

reponse.text

reponse.json()

reponse.headers

reponse.cookies
