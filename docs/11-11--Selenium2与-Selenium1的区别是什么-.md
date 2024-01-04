## 11-11--Selenium2与-Selenium1的区别是什么-

Selenium1.0使用的是 Javascript注入技术与浏览器打交道，需要 Selenium启动一个 Server，将操作Web元素的AP调用转化为一段段 Javascript，在 Selenium内核启动浏览器之后注入这段 Javascript，开发过Web应用的人都知道， Javascript可以获取并调用页面的任何元素，自如的进行操作，由此才实现了 Selenium的目的：自动化Web操作，这种 Javascript注入技术的缺点是速度不理想，而且稳定性大大依赖于 Selenium内核,对API翻译成的 Javascript 质量高低

Selenium2.0则是把 selenium1.0中 selenium RC替换为了 Web Driver

WebDriver利用浏览器原生的API，封装成一套更加面向对象的 SeleniumWebDriverAPI

直接操作浏览器页面里的元素，甚至操作浏览器本身(截屏，窗口大小，启动，关闭，安装播件，配置证书之类的)，由于使用的是浏览器原生的AP，速度大大提高，而且调用的稳定性交给了浏览器厂商本身，显然是更加科学，然而带来的一些副作用就是，不同的浏览器厂商，对Web元素的操作和呈现多少会有一些差异，这就直接导致了 SeleniumWebDriver要分浏览器厂商不同，而提供不同的实现例 Firefox就有专门的 Firefox Driver，

Chrome就有专门的 ChromeDriver等等
