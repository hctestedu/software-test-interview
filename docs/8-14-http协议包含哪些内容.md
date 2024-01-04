## 8-14-http协议包含哪些内容

(1)请求信息

1）请求行：请求方式、请求地址http版本1.1

2）请求头

HTTP消息报头包括普通报头、请求报头、响应报头、实体报头

Cache- Control：no- cache 缓存

Connection：close/keep-aive  是否关闭或者保持连接

Accept-Charset：ios-859-1 字符集

Accept-Encoding：gzip.deflate 编码格式

Accept-Language：zh-cn 语言

Authorization：服务器授权验证

Host：主机

User-Agent：

Location：重定向

Server：服务器版本信息

Content-Encoding：实体报头的编码格式

请求正文

data

(2)响应信息

1）状态行：http版本、状态码、状态信息

2）响应头：跟请求头一样

3）响应正文：
