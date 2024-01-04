## 11-36-自动化中如何去操作excel表格-

需要用到xlrd库，调用这个库中的API函数来实现的。

1.第一步：导包 import xlrd

2.第二步：book= xrd.open_workbook(文件路径)

3.第三步：table= book.sheet_by_name表名)

4.第四步：读某行数据一般都技行来读取

Table.row_values(x)

如果要读全部的数据，多行数据，利用循环读取就可以

List=[]

for i in range(1,table.nrows):

List.append(table.row_values(i))

return list
