## 13-4-bytes如何去运行多个文件或者整个目录

1. 执行多个文件

pytest.main(["../test_case/test_01","../test_case/test_login"])

2. 执行整个目录

pytest.main(["../test_case/"])  --列表里是目录路径
