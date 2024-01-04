## 11-12--seleniun库中用过哪些函数-

driver = Web Driver ChromeO

driver.quit()          #退出浏览器

driver.closed()         #关闭窗口

driver.implicitly_wait()    #设置隐性等待延迟

driver.current_url       #获取当前的URL

driver.page_source       #获取当前页面的源代码

driver.title          #获取当前页面的标题

driver.maximize_window()    #窗口最大化

driver.get()          #加载一个网页

元素定位的:

driver.find_element_by_id()

driver.find_element(By.xxx,’’)

frame跳转的:

driver.switch_to.frame()

driver.switch_to.parents_frame()

driver.switch_to.default_content()

窗口跳转:

driver.switch_to.window()

对话框的处理:

Driver_switch_to.alert

.accepto

.dismiss

.text

.send_keys()

执行js脚本的:

driver.execute_script(js)

Element类:

element.click()

element.submit()

element.send_keys()

element.clear()

element.text

element.get_attribute()

element.is_displayed()

element.find_element_by_xpath()
