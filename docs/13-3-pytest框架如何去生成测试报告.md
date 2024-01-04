## 13-3-pytest框架如何去生成测试报告

1. 要安装 pytest-html

pip install pytest-html、在 pycharm里安装 pytest-html、或者源码安装

2. 在运行用例模块中执行用例时添加html路径： pytest.main(["要运行的文件的路径","--html=. /report/report.html"])
