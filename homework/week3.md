# week3

> **定理 2.5 (只依赖于 $y$ 的积分因子)**
> 
> 充要条件为 $\frac{\frac{\partial{Q}}{\partial{x}}-\frac{\partial{P}}{\partial{y}}}P=H\left(y\right)$ 只依赖于 $y$, 此时 $\mu\left(y\right)=e^{\int{H}\left(y\right)\mathrm{d}y}$.

> **定理 2.6 (积分因子与通积分的任意函数之积)**
> 
> 若 $\mu$ 是积分因子且 $\mu{P}\mathrm{d}x+\mu{Q}\mathrm{d}y=d\Phi$, 则 $\mu{g}\left(\Phi\right)$ 也是积分因子.

> **定理 3.1 (皮卡存在和唯一性定理)**
> 
> $f$ 连续且满足利普希茨条件时初值问题有唯一解.

> **引理 3.2 (欧拉折线的积分关系式)**
> 
> $\rho_n\left(x\right)=y_0+\int_{x_0}^xf\left(t,\rho_n\left(t\right)\right)\mathrm{d}t+\delta_n\left(x\right)$, 其中 $\delta_n\to0$ 一致.

> **定理 3.2 (奥斯古德条件下解的唯一性)**
> 
> 若 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le{F}\left(\left|y_1-y_2\right|\right)$ 且 $\int_0^{r_1}\frac{\mathrm{d}r}{F\left(r\right)}=+\infty$, 则解唯一.

> **定理 3.3 (佩亚诺存在定理)**
> 
> $f$ 连续时初值问题至少有一个解.

## 2-3 题4

用常数变易法推导非齐次线性方程的通解.

### 解答 2-3 题4

设 $y=C\left(x\right)e^{-\int{p}\mathrm{d}x}$, 代入方程得 $C'\left(x\right)=q\left(x\right)e^{\int{p}\mathrm{d}x}$. 积分后即得与积分因子法一致的结果.

$\blacksquare$

## 2-3 题5

证明: 若 $p,q$ 均以 $\omega$ 为周期, 则方程有唯一 $\omega$ 周期解当且仅当 $\overline{p}\ne0$.

### 解答 2-3 题5

由齐次线性方程的通解 与非齐次线性方程的通解 (积分因子法), $y\left(x+\omega\right)=y\left(x\right)$ 等价于 $e^{-\int_0^\omega{p}}=1$, 即 $\overline{p}=0$. 非齐次时唯一周期解当且仅当 $\overline{p}\ne0$.

$\blacksquare$

## 2-4 题1(2)

求解 $y'=\frac{2y-x+5}{2x-y-4}$.

### 解答 2-4 题1(2)

由可化为齐次的方程, 平移 $x=\xi+1$, $y=\eta-2$. 令 $\eta=u\xi$, 分离变量积分得 $\frac{\eta-\xi}{\left(\eta+\xi\right)^3}=C$. 代回得 $y-x+3=C\left(x+y+1\right)^3$.

$\blacksquare$

## 2-4 题1(4)

求解 $y'=x^3y^3-xy$.

### 解答 2-4 题1(4)

由伯努利方程, 令 $z=y^{-2}$, 得 $z'-2xz=-2x^3$. 积分因子 $e^{-x^2}$, 解得 $\frac1{y^2}=x^2+1+Ce^{x^2}$. 特解 $y\equiv0$.

$\blacksquare$

## 2-4 题2(2)

求解 $\left(3uv+v^2\right)\mathrm{d}u+\left(u^2+uv\right)\mathrm{d}v=0$.

### 解答 2-4 题2(2)

由齐次方程, 令 $v=wu$, 分离变量积分得 $u^2v\left(v+2u\right)=C$.

$\blacksquare$

## 2-4 题2(4)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{2x^3+3xy^2-7x}{3x^2y+2y^3-8y}$.

### 解答 2-4 题2(4)

令 $u=x^2$, $v=y^2$. 由可化为齐次的方程, 平移后令 $\eta=w\xi$, 积分得 $x^2+y^2-3=C\left(x^2-y^2-1\right)^5$.

$\blacksquare$

## 2-4 题4

将二阶方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 化为里卡蒂方程.

### 解答 2-4 题4

令 $z=\frac{y'}y$, 则 $z'=-z^2-p\left(x\right)z-q\left(x\right)$, 即里卡蒂方程.

$\blacksquare$

## 2-5 题1(2)

求解 $y\mathrm{d}x+\left(2xy-e^{-2y}\right)\mathrm{d}y=0$.

### 解答 2-5 题1(2)

由**定理 2.5 (只依赖于 $y$ 的积分因子)**, $\mu=\frac{e^{2y}}y$. 乘后得 $xe^{2y}-\ln\left|y\right|=C$. 特解 $y\equiv0$.

$\blacksquare$

## 2-5 题1(4)

求解 $y\mathrm{d}x-\left(x^2+y^2+x\right)\mathrm{d}y=0$.

### 解答 2-5 题1(4)

由**定理 2.6 (积分因子与通积分的任意函数之积)**, 取 $\mu=\frac1{x^2+y^2}$. 积分得 $\arctan\frac{x}y=y+C$.

$\blacksquare$
