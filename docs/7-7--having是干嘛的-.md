## 7-7--having是干嘛的-

是一个条件查询，一般是跟着分组以后，比如

select title， count(title) as t from titles group by title having t>=2;
