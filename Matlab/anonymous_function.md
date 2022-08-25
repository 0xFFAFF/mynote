# matlab 匿名函数

匿名函数可以接收多个输入并返回一个输出。

eg:
```matlab
 fun = @(x, y) x.^2 + y.^2
```
利用匿名函数求解积分
$\int_{0}^{1}z\mathrm{d}z\int_{0}^{\sqrt{1-z^2}}x\mathrm{d}x\int_{0}^{\sqrt{1-x^2-z^2}}y\mathrm{d}y$

```matlab
 fun = @(z,x,y) x.*y.*z
 q = integral3(fun,0,1,0,@(z) sqrt(1-z.^2),0,@(x,y) sqrt(1-x.^2-y.^2))
 rat(q) # 将所得小数化为分数
```