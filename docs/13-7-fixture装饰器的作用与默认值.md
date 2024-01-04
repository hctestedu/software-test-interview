## 13-7-fixture装饰器的作用与默认值

1. 装饰器：@pytest.fixture()

def open_l()：    #不再用test开头，

ea = element_action()  #实例化对象

ea.open_url()   #打开浏览器 driver，被其他用例所调用

Yield ea  1，装饰器使用的返回值，类似于 return方法   2，前置与后置处理分开

ea.close_browser()  #每次运行，关闭浏览器，闭环

设置了装饰器之后，可以被其他用例调用，有使每个用例都有打开网页和默认关闭网页的作用
