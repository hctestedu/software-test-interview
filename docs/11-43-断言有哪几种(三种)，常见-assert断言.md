## 11-43-断言有哪几种(三种)，常见-assert断言

selenium提供了三种模式的断言： assert、verify、 waitfor

Assert失败时，该测试将终止。

Verify失败时，该测试将继续执行，并将错误记入日显示屏。也就是说允许此单个验证通过。确保应用程序在正确的页面上。

Waitfor用于等待某些条件变为真。可用于AJAX应用程序的测试

常见的 assert断言：

assertTitle(检查当前页面的title是否正确)

assertText(检查指定元素的文本)

assert Attribute(检查当前指定元素的属性的值)

如果该条件为真，他们将立即成功执行。如果该条件不为真，则将失败并暂停测试。直到超过当前所设定的超过时间。一般跟 setTimeout时间一起使用
