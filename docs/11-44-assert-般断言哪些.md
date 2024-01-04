## 11-44-assert-般断言哪些

1、提取元素text断言:

User_text=driver.find_element_by_css_selector(("#j_account>a").text  #获取实际的值

(展示账户名内容)

assert'admin'in user_text  #断言 admin在实际值里

2、提取元素属性去断言:

Login_button_value=driver.find_element_by_id("lajax-login-submit").get_attribute(value)#获取登录按钮的属性vaue值是登录

assert'登录'== login_button_value #断言‘登录’是这个按钮的属性

3、提取界面title值去断言:

assert"p2p信贷最大、最安全的网络借贷平台"in driver.title,"失败"或者in改为 not in

4、提取元素是否可用来进行断言

assert driver.find_element_by_css_selector("div.user_money > a:nth-child(1)").is en

abled==True，"元素不存在。不可用"

5、数据库断言，去数据库查询结果，是否跟预期一致
