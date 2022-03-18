# 函数的极限

极限证明的中心思想：
无论你有多么接近这个点，总有人比你更加接近这个点

## 自变量趋于有限值$X\rightarrow X_0$

   1. 符号语言:$\forall \varepsilon \gt 0,\exists \delta \gt 0 ,对0 \lt \left|x-x_0\right|\lt \delta,\left|f(x)-A\right|\lt \varepsilon$

   2. 对任意的$\varepsilon >0, 总存在以x_0为中心的去心邻域，其中的f(x)比\varepsilon更接近A$

证明: $当x_0\gt 0 时，\lim_{x \to x_0} \sqrt{X} = \sqrt{x_0}$
$$
\begin{aligned}
&\forall \varepsilon \gt 0, \left|f(x)-A\right| \lt \varepsilon \\
\Rightarrow &\left|\sqrt{x}-\sqrt{x_0}\right|=\left| \frac{x-x_0}{\sqrt{x}+\sqrt{x_0}}\right| \leq \left| \frac{x-x_0}{\sqrt{x_0}}\right| \\
\Rightarrow & \left|x-x_0 \right| \lt \varepsilon\sqrt{x_0} \\
&因为x_0 \gt 0 \quad所以 \left|x-x_0\right| \leq x_0 \\
& 取\delta = \min(x_0,\varepsilon x_0), 可以满足条件 \\
&所以证明成立
\end{aligned}
$$

---

## 自变量趋于无穷大

$\forall \varepsilon \gt 0, \exists X\gt 0,当\left|x\right| \gt X时, \left|
f(x)-A\right| \lt \varepsilon 成立$
单侧无穷大 x\<X 或 x>X

### 函数极限的性质

1. 函数极限的唯一性，如果$\lim_{x \to x_0}存在，那么这个极限唯一$

2. （了解一下）函数极限的局部有界性

3. 函数极限的保号性，如果函数在某一点的极限大于或小于0，那么总存在以这一点为中心的去心邻域，邻域内的f(x)总是大于或小于0
