# MATLAB 中的简单操作

## 代数操作

MATLAB预定义$\mathrm{i} = \mathrm{j} = \sqrt{-1}$，我们可以很容易的用直角坐标创建一个复向量
`z = 3 - 4j`
1. z的实部与虚部可以通过real和imag运算符提取出来
    ```matlab
    z_real = real(z);
    z_imag = imag(z);
    ```

2. 复数的共轭可以由命令conj来计算
   ```matlab
   z_conj = conj(z);
   ```

3. 复数的模值可由abs命令来计算；复数的相位值可以由angle命令来计算,还可以通过反正切函数确保结果出现在正确的象限上；
   ```matlab
   z_mag = abs(z);
   z_rad = angle(z); %此处求得是弧度值
   z_rad_ = atan2(z_imag, z_real);
   ```

## 向量运算

1. 生成一个元素为实数且元素等间距取值的行向量
   ```matlab
   k = 0:2:11
   %k = 0 2 4 6 8 10
   ```
   :star:向量法为快速的生成和研究各种信号提供了基础
   ```matlab
   interval = 0.2/500;
   t = 0:interval:0.2-interval;
   f = sin(2 * pi * 10 * t + pi /6);
   % f为 1 * 500 的向量
   % f(1)为取其第一个元素
   ```

## 矩阵运算
1. 一些常用矩阵的生成方法
   - `eye(m)`生成$m \times m$的恒等矩阵
   - `ones(m, n)`生成$m \times n$ 的全1矩阵
   - `zeros(m, n)` 生成$m \times n$的全0矩阵
   - `diag(x)` 会使向量生成一个对角矩阵

2. 普通矩阵的生成，转置，拼接
   ```matlab
   r = [1 0 0];
   A = [2 3; 4 5; 0 6];
   B = r'; %B = [1;0;0]
   %由于r是实向量，复共轭转置就只是简单转置。如果r是复数向量，则简单转置就要通过r.'或者(conj(r))'来完成
   C = [A B]
   ```

3. 向量中元素的选取
   $$ \begin{matrix}
      C = &2 &3 &1 \\
      &4 &5 &0 \\
      &0 &6 &0
   \end{matrix} $$
   ```matlab
   C(1, 2) %取第一行第二列的元素 ans = 3
   C(1:2, 2:3)%取第一第二行与第三第四列交叉的元素 ans = 3 1; 5 0
   C(2, :) %取第二行的所有元素 ans = 4 5 0
   ```

4. 线性方程组的求解-逆矩阵法或者左乘法
   $$ \begin{align}
      x_1 - 2x_2 + 3x_3 &= 1 \\
      -\sqrt{3}x_1 + x_2 -\sqrt{5}x_3 &= \pi \\
      3x_1 - \sqrt{7}x_2 + x_3 &= e
   \end{align} $$
   ```matlab
   A = [1 -2 3; -\sqrt(3) 1 -\sqrt(5); 3 -\sqrt(7) 1];
   y = [1; pi; exp(1)];
   X_1 = inv(A) * Y; %利用逆矩阵
   X_2 = A\Y; %利用矩阵左乘，据说效率比逆矩阵好
   ```

5. 用来生成一簇曲线
   $ h_{\alpha}(t) = e^{- \alpha t}\sin (2\pi 10t + \frac{\pi}{6})\quad 0\le t \le 0.2 $
   $\Delta t = 0.001$，生成$\alpha$从0取到10的曲线，间隔为1，并将其展示在一张图上
   ```matlab
   alpha = 0:10;
   t = (0:0.001:0.2)';
   T = t * ones(1, 11); % 为11条曲线每个都生成一条时间向量，矩阵大小为201*11
   H = exp(-T * diag(alpha)).*sin(2 * pi * 10 * T + pi/6);
   plot(t, H);
   xlabel('t');
   ylabel('h(t)');
   ```
## 简单绘图
绘制:star:处的函数
```matlab
plot(t, f);
xlabel('t'); ylabel('f(t)'); % 为坐标轴添加标注
```
MATLAB也有很多专门的绘图函数。列如，MATLAB的semilogx，semilogy和loglog命令，分别表示横坐标以10为底的对数坐标，纵坐标以10为底的对数坐标，横纵坐标以10为底的对数坐标。单色或者彩色图像显示可以使用image命令，等值线图可以轻松使用contour命令进行绘制。进一步，各种三维绘图函数也可以利用，如plot3，contour3，mesh和surf。建议查看MATLAB帮助。


## 部分分式展开

计算部分分式展开$F(x) = \frac{B(x)}{A(x)}$利用MATLAB中的`residue`命令，这个命令的基本形式为`[R, P, L] = residue(B, A)`，两个输入向量分子和分母的多项式系数，向量元素是以自变量的**降幂**顺序排列的。输出为三个向量，其中向量R包含了每个部分分式**系数**，向量P包含每个部分分式对应的根。对于重复r次的根，r个部分分式是按照升幂顺序排列的。当有理函数不是真有理函数时，向量k包含了部分分式的余式，它们按照自变量的降幂顺序排列。
$$ F(x) = \frac{x^5 + \pi}{(x + \sqrt{2})(x - \sqrt{2})^3} = \frac{x^5 + \pi}{x^4 - \sqrt{8}x^3 + \sqrt{32}x - 4}$$

```matlab
[R, P, K] = residue([1 0 0 0 0 pi], [1 -sqrt(8) 0 sqrt(32) -4])
% R = 7.8888 5.9173 3.1107  0.1112
% P = 1.4142 1.4142 1.4142 -1.4142
% K = 1.0000 2.8284
```
写成标准形式为
$$ F(x) = x + 2.8284 + \frac{7.8888}{x - \sqrt{2}} + \frac{5.9713}{(x - \sqrt{2})^2} + \frac{3.1107}{(x-\sqrt{2})^3} + \frac{0.1112}{x + \sqrt{2}}$$

信号处理工具箱函数residuez 和 residue 命令相似，但它为某些有理函数，像那些在研究离散时间系统时会经常遇到的函数，提供了更为方便的展开式。