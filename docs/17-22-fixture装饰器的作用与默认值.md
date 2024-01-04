## 17-22-fixture装饰器的作用与默认值

可以使用此装饰器(带或不带参数)来定义 fixture功能。 fixture功能的名称可以在以后，使用引用它会在运行测试之前调用它：test模块或类可以使用 pytest.mark.usefixtures

（fixturename标记。测试功能可以直接使用 fixture名称作为输入参数，在这种情况下，夹具实例从 fixture返回功能将被注入。
