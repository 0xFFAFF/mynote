# 指针问题

1. 空指针问题
   ```c++
   int *pointer = 0;
   int *pointer = NULL;
   //表明这两个指针是空指针，指向的内存空间位全0
   //这个内存空间是不允许访问的，所以不可以对这块内存空间进行操作

   //
    *pointer = 10; //error,不可以写这块内存空间
   //
   ```

   