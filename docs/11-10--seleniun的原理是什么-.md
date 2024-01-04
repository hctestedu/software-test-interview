## 11-10--seleniun的原理是什么-

我们用的 selenium3x以上的版本，对于 selenium2x以上的版本原理是这样的：

Selenium2.0则是把 selenium1.0中 selenium RC替换为了 WebDriver

WebDriver利用浏览器原生的API，封装成一套更加面向对象的 SeleniumWeb Driver API

直接操作浏览器页面里的元素，甚至操作浏器本身(截屏，回口大小，启动，关闭，安装插件，配置证书之类的)，由于使用的是浏览器原生的API速度大大提高，而且调用的稳定性交给了浏览器厂商本身，显然是更加科学，然而带来的一些副作用就是，不同的浏器厂商，对Web元素的操作和呈现多少会有一些差异，这就直接导致了 SeleniumWebDriver要分浏览器厂商不同，而提供不同的实现，例如 Firefox就有专门的 FirefoxDriver，

Chrome就有专门的 ChromeDriver等等
