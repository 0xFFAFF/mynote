# 解决vscode下使用python相对路径报错问题

vscode插件会将工作目录设置在project下，导致报错
我们需要更改工作目录到要运行的python文件下
在python文件开头添加以下两行代码
```python
import os, sys
os.chdir(sys.path[0])
```