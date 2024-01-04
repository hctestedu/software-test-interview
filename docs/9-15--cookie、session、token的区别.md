## 9-15--cookie、session、token的区别

它们都是用来做鉴权的，区别的话，大概是这样的

1、现在 cookie、session一般是配合使用的用户第一次登陆时，服务器会创建一个 session

生成一个 sessionID，sessionID保存在 cookie中，然后返回到客户端，保存在浏览器中。

客户端每次发请求都会把这个值带到服务器，做一个鉴权和会话的跟踪，或者时效的验证

2、token和 cookie、session差不多，通过算法，每次验陆，会产生一串很长的随机字符串，一般是在放在返回的body里面，或者返回的头里面，他们都是服务器产生，带过来是要做验证和时效的验证的。一般在app中使用token比较多一点，Web端使用cookie、session的鉴权方式会多一点。
