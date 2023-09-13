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