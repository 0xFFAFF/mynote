# makefile 的使用

- makefile 中特殊字符的含义
  ```makefile
  $@ #表示目标输出
  $< #表示第一个依赖文件
  $^ #表示所有的依赖
  ```

makefile取文件所在目录的相对路径
  ```makefile
  $(dir include/test.h)
  # 返回 include/
  ```
