# week3

## 2-3 题1(4)

求解初值问题 $\frac{\mathrm{d}y}{\mathrm{d}x}-\frac1{1-x^2}y=1+x$, $y\left(0\right)=1$.

### 解答 2-3 题1(4)

积分因子 $\mu=\sqrt{\frac{1-x}{1+x}}$. 积分得 $\mu{y}=1+\frac12\left(x\sqrt{1-x^2}+\arcsin{x}\right)$. 故 $y=\sqrt{\frac{1+x}{1-x}}\left[1+\frac12\left(x\sqrt{1-x^2}+\arcsin{x}\right)\right]$. $\blacksquare$

## 2-3 题3

证明: 若 $y'+a\left(x\right)y\le0$, 则 $\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^xa\left(s\right)\mathrm{d}s}$.

### 解答 2-3 题3

取积分因子 $A\left(x\right)=e^{\int_0^xa\left(s\right)\mathrm{d}s}$, 则 $\frac{\mathrm{d}}{\mathrm{d}x}\left(Ay\right)\le0$, 故 $Ay$ 单调不增. $\blacksquare$

## 2-3 题4

用常数变易法推导非齐次线性方程的通解.

### 解答 2-3 题4

设 $y=C\left(x\right)e^{-\int{p}\mathrm{d}x}$, 代入方程得 $C'\left(x\right)=q\left(x\right)e^{\int{p}\mathrm{d}x}$. 积分后即得与积分因子法一致的结果. $\blacksquare$

## 2-3 题5

证明: 若 $p,q$ 均以 $\omega$ 为周期, 则方程有唯一 $\omega$ 周期解当且仅当 $\overline{p}\ne0$.

### 解答 2-3 题5

由齐次线性方程的通解 与非齐次线性方程的通解 (积分因子法), $y\left(x+\omega\right)=y\left(x\right)$ 等价于 $e^{-\int_0^\omega{p}}=1$, 即 $\overline{p}=0$. 非齐次时唯一周期解当且仅当 $\overline{p}\ne0$. $\blacksquare$

## 2-4 题1(2)

求解 $y'=\frac{2y-x+5}{2x-y-4}$.

### 解答 2-4 题1(2)

由可化为齐次的方程, 平移 $x=\xi+1$, $y=\eta-2$. 令 $\eta=u\xi$, 分离变量积分得 $\frac{\eta-\xi}{\left(\eta+\xi\right)^3}=C$. 代回得 $y-x+3=C\left(x+y+1\right)^3$. $\blacksquare$

## 2-4 题1(4)

求解 $y'=x^3y^3-xy$.

### 解答 2-4 题1(4)

由伯努利方程, 令 $z=y^{-2}$, 得 $z'-2xz=-2x^3$. 积分因子 $e^{-x^2}$, 解得 $\frac1{y^2}=x^2+1+Ce^{x^2}$. 特解 $y\equiv0$. $\blacksquare$

## 2-4 题2(2)

求解 $\left(3uv+v^2\right)\mathrm{d}u+\left(u^2+uv\right)\mathrm{d}v=0$.

### 解答 2-4 题2(2)

由齐次方程, 令 $v=wu$, 分离变量积分得 $u^2v\left(v+2u\right)=C$. $\blacksquare$

## 2-4 题2(4)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{2x^3+3xy^2-7x}{3x^2y+2y^3-8y}$.

### 解答 2-4 题2(4)

令 $u=x^2$, $v=y^2$. 由可化为齐次的方程, 平移后令 $\eta=w\xi$, 积分得 $x^2+y^2-3=C\left(x^2-y^2-1\right)^5$. $\blacksquare$
