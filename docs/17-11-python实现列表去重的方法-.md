## 17-11-python实现列表去重的方法-

第一种方式：

\#encoding = utf-8

import time

time_start=time.time()

print u"列表去重的七种方法"

prnt u"第一种测试方法"

repeat_list=[1,2,4,1,5,1,2,5]

result=[]

for i in repeat_list:

if i not in result;

result.append(i)

print u"第一种去重结果：", result

第二种方法:

repeat_list=[1,2,4,1,5,1,2,5]

print u"第三种去重结果：",list(set( repeat_list))
