# 函数与极限

---

## 错题点

 1. 注意极限进行四则运算的条件

    两个式子极限都要存在

    $$
    \begin{aligned}
    &\lim_{n \to \infty}X_n=A \\
    &\lim_{n \to \infty}Y_n=B \\
    \Rightarrow &\lim_{n \to \infty}(X_n \pm Y_n)=A\pm B
    \end{aligned}
    $$

    例子：下式完全错误XXX，不满足四则运算的条件

    $$
    %绝对错误XXX
    \begin{aligned}
    \lim_{x \to 0}\frac{x-tanx}{x^3} = \lim_{x \to 0}\frac{x}{x^3} - \lim_{x \to 0}\frac{tanx}{x^3} = 0
    \end{aligned}
    $$


 2. 无穷小可以整体替换，部分加减有前提

  $$
  \begin{aligned}
    \alpha\sim \alpha ' \quad \beta \sim \beta ' \\
    若\lim\frac{\alpha}{\beta}\neq -1，则\alpha+\beta \sim \alpha'+\beta' \\
    若\lim\frac{\alpha}{\beta}\neq 1，则\alpha-\beta \sim \alpha'-\beta' \\
  \end{aligned}
  $$
  例子：
  $$ 
  \begin{aligned}
    &\lim_{x \to 0}\frac{\sin3x-\tan2x}{x}\\
    &\because \lim_{x \to 0}\frac{\sin3x}{\tan2x}\neq 0 \\
    &\therefore \lim_{x \to 0}\frac{\sin 3x - \tan 2x}{x} =\lim_{x \to 0}\frac{3x-2x}{x}=1
  \end{aligned}
  $$