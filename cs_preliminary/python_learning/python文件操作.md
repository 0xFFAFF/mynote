# 使用pathlib对文件进行操作

```python
from pathlib import Path

'''
基本操作
'''
p1 = Path('.') # 当前目录
p2 = Path('xx/xx/xx') # 绝对路径
p3 = Path('python_learning', 'cpython','first.md') # 自动处理路径分隔符
p4 = Path.home() # 用户主目录
p5 = Path.cwd() # 当前的工作目录

'''
进阶操作
'''
p6 = Path('.') / 'XX' # 目录的拼接
p7 = Path.join('','') # 另外一种拼接的方式


'''
文件和目录的操作
'''
Path.exists() # 文件是否存在
Path.is_file() # 是否是文件
Path.is_dir() # 是否是目录
Path.iterdir() # 遍历目录下的目录和文件
```