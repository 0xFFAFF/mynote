# python 文件操作
1. 获取文件路径
   1. dirname = os.path.dirname(__file__)
   2. filename = os.path.join(dirname, 'file.txt')

2. 打开文件
   1. with open(filename, 'a') as f:

3. 文件写入
    ```python
    with open(filename, 'a') as f:
        f.write('hello world!')
    ```