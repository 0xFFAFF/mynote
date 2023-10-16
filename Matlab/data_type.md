# matlab中的数据类型

1. 数字
2. 字符与字符串
3. 矩阵
4. 元胞数组
5. 结构体


## syms 详解
1. `syms var1 ... varN`
2. `syms var1 ... varN [n1 ...nM]`
   创建矩阵化的符号标量变量
   ```matlab
   syms A [3 4]
   % 创建一个三行四列的变量矩阵
   ```
3. `syms var1 ... varN n`
   创建$n *n$的矩阵变量
4. `syms f(var1,var2,...,varN)`
   创建带参的符号函数
   ```matlab
   syms f(x,y);
   f(x,y) = x + 2*y;
   % f(1,2) = 5;
   ```