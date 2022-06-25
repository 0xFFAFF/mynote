# 编译过程中makefile的使用
```makefile
#基本格式
#目标:源
#    命令
#example：

edit : main.o kbd.o command.o display.o \
        insert.o search.o files.o utils.o
    cc -o edit main.o kbd.o command.o display.o \
        insert.o search.o files.o utils.o

main.o : main.c defs.h
    cc -c main.c
kbd.o : kbd.c defs.h command.h
    cc -c kbd.c
command.o : command.c defs.h command.h
    cc -c command.c
display.o : display.c defs.h buffer.h
    cc -c display.c
insert.o : insert.c defs.h buffer.h
    cc -c insert.c
search.o : search.c defs.h buffer.h
    cc -c search.c
files.o : files.c defs.h buffer.h command.h
    cc -c files.c
utils.o : utils.c defs.h
    cc -c utils.c
clean :
    rm edit main.o kbd.o command.o display.o \
        insert.o search.o files.o utils.o
#其中的目标可以是一个目标文件，可以是一个执行文件，还可以是一个标签

#`\`是换行符，可以方便makefile的编写和阅读

#命令得以\t开头，也就是得敲一下`TAB`制表符按键，不然那个sb就不知道这是一条命令
```


---
## makefile的工作流程

总之，你的工程文件有更改，它能感知到这种更改，并且自动更新完成编译链接。

## 在makefile中使用变量
```makefile
objects = hello.o world.o
main : $(objects)
    cc -o main $(objects)
```
## 让makefile自动推导
make 看见.o文件会把就会把对应的.c文件添加到他的依赖项中去，并自己推导出相应的命令。

假设现在有一个hello.c hello.h 我们可以写这样的makefile
```makefile
var = hello.o
hello:$(var)
    gcc $(var) -o hello
$(var):hello.c hello.h
    gcc -c hello.c -o $(var)
```
但基于makefile的自动推导，我们省去一些代码
```makefile
var = hello.o
hello:$(var)
    gcc $(var) -o hello
$(var):hello.h
```

## 清空一下目标文件
```makefile
.PHONY: clean
clean :
    rm -f $(objects)
```

## makefile中文件的查找
可以在文件前加上路径名，但也可以将路径告诉makefile，这样makefile就可以自动查找文件了。

1. 特殊变量：`VPATH`
    ```makefile
    VPATH = src:../headers
    #这样makefile就可以查找src目录下的文件，如果没有找到，就去../headers目录下查找。
    ```
    多个目录使用冒号分隔

2. 使用关键字`vpath`
    1. vpath \<pattern> \<dir> # 为符合pattern的文件设置搜索路径
        ```makefile
        vpath %.c %.h ../headers
        # % 的意思是匹配零或若干字符
        ```

    2. vpath \<pattern> # 清除符合pattern的文件的搜索路径

    3. vpath # 清除所有的搜索路径