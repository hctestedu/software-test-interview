## 12-5--Unittest框架如何使用-

1. 导包

import unittest

from selenium import webdriver

import ddt

2.定义一个类继承 unittest.TestCase基类

重写 setUp(),tearDown()方法

3.setUp()方法实现一个初始化的准备工作，比如，实例化 webdriver对象，对 driver进行初始化配置，连接数据库.....

4.tearDown()方法实现释放资源的任务。

编写用例方法，用例方法必须以test开头

5. Unittest如何去运行多个文件或者整个目录

因为我们用例全部是放在 test_case目录下统一管理的，基本每个某块都是一个.py文件，要全量跑的话，需要调用 unittest.default.discover()函数，指定用例目录的路径，加载所有的.py文件，它会自动创建测试套件，井把用例加入测试套件中，然后利用unittest.TestRunner()创建一个执行器利用这个执行器去运行测试雷件中的所有用例。
