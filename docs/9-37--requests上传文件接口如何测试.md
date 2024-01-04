## 9-37--requests上传文件接口如何测试

url="http：//106.12.126.197/fanwe/file.php"

data={

"upload_type"："0",

"localUrl"："E： \\fanwe.png",

"m"："File",

"a"："do_upload}

\#文件上传功能，files参数编写

files={"imgFile"：(‘fanwe.png’, open(‘E：\\fanwe.png’,’rb’)，image/png)}

\#fes={‘文件参数的名称’：(文件名 open(E：\\fanwe.png：读的属性)文件的类型}

r=erequests.post(url=url,data=data,cookies=login(),files=files)

print (r.text,type(r.text))
