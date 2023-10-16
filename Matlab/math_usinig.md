1. matlab 求极限
   ```matlab
    syms x
    y = f(x)
    limit(y, x, 0)
   ```

2. matlab 求导
   ```matlab
    syms x
    y = f(x)
    diff(y, x)
   ```

3. matlab 求定积分
   ```matlab
    syms x
    y = f(x)
    int(y, x, a, b)
   ```
   用matlab求解下式的积分值
   $$ \int_{0}^{\infty}4e^{-t}dt $$
   ```matlab
   syms t;
   f = 4 * exp(-t);
   ans = int(f, t, 0, Inf);
   % >> ans = 4
   ```

4. 利用matlab求解多项式的根
   $k$的值分别为3，4，40
   $$ \lambda^2 + 4\lambda +k = 0 $$ 
   ```matlab
   r = roots([1 4 3]);
   r = roots([1 4 4]);
   r = roots([1 4 40]);
   ```

5. 利用matlab求解微分方程的零输入分量
   $$ (D^2 + 4D + 40)y(t) = (3D + 5)x(t) \\
   y_0(t) = 3 \quad \overset{.}{y_0}(t) = -7 $$
   ```matlab
   syms y(t);
   eqn = diff(y,t,2) + 4*diff(y,t) + 40*y ==0;
   Dy = diff(y,t);
   cond = [y(0)==3, Dy(0)==-7];
   s = dsolve(eqn,cond)
   ```