## 11-23、如何去处理上传-Windows文件-

1.可直接赋值 send_keys输入图片的地址

其实上传文件的按钮就是一个 input元素，只是它的type类型是file类型，

我们在处理这种上传文件的按钮的时候，可以直接通过普通定位方式去定位它，

再利用 send_keys方法去输入图片的地址就可以了。

Load_file_element=driver.find_element_by_xpath(‘/html/body/div(8l/div(1)/div(2/div/div[3]/form/div/div/div/inpu’)

2.需要用到一个工具，Autolt工具

帮助我们识 Windows控件信息利用Autolt生成一个操作 Windows对话框的exe执行文件

然后在 python代码中去调用这个可执行文件

这里需要用到os模块，利用 os.system去执行 windows的exe文件，

把exe文件的路径传入，并传入需要上传的图片的路径即可

Drver.fnd_ement_by_xpath(‘html/body/divoiv1/dw2]/div/div3form/dvd/di)cick()#点击浏览

time.sleep(1)

ossystem(C:\Users\\Administrator\\ Desktop\\AA.exe D:\\QQ.png)
