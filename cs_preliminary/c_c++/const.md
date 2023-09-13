# const

- 指定变量的值是常量防止程序员对其修改

```c++
int main()
{
    const int i = 0;
    i = 10; //error
    i++; //error
}
```
- 在c++中，可以使用`const`关键字而不是`#define`来定义常量值，使用const定义的值需要接受类型检查，并且可以代替常量表达式,在c++中，可以使用const定义数组长度
```c++
int main()
{
    const int maxlength = 100;
    char array[maxlength];// allowed in c++ ;not allowed in c
}
```
- 在c语言中，常量值默认为外部链接，因此只能出现在源文件中；在c++中，常量值默认为内部链接，因此可以出现在标头文件中

内部链接：如果一个名称对编译单元（.cpp）来说是局部的，在链接的时候，其他单元无法链接到它且不会产生同名冲突。

外部链接：可以与其他编译单元进行交互

- const 可以在指针的声名中使用

```c++
int main()
{
    char this_char{'a'}, that_char{'b'};
    char* mybuf = &this_char, youbuf = &that_char;
    char* const aptr = mybuf;
    *aptr = 'c'; //ok
    aptr = &youbuf //error
}
```

- const 可以将指向常量数据的指针用作函数参数，防止函数修改通过指针传递的参数；对于声名为const的对象，只能调用常量成员函数，从而确保不会修改常量对象

- const 可以作为关键词重载成员函数，不能使用const关键词修饰构造或者析构函数

- const 成员函数指定该函数是一个“只读函数”，它不会修改调用它的对象

