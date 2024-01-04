## 10-17--requests中如何进行动态关联

1，如果返回的是 cookies值，可以直接返回接口的 r.cookies

2，返回的是str类型数据，可以导入re模块进行正则表达式提取返回数据格式是json格式，

导入json，把json数据格式转化 python对象

| json.dumps | 将 Python对象编码成JSON字符串          |
| ---------- | -------------------------------------- |
| json.loads | 将已编码的JSON字符串解码为  Python对象 |
