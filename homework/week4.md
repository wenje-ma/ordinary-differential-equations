# week4

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

## 2-5 题2

证明: 存在形如 $\mu=\mu\left(\varphi\left(x,y\right)\right)$ 的积分因子的充要条件.

### 解答 2-5 题2

由 $\frac{\mu'}{\mu}=\frac{P_y-Q_x}{Q\varphi_x-P\varphi_y}=f\left(\varphi\right)$, 得 $\mu=e^{\int{f}\left(\varphi\right)\mathrm{d}\varphi}$.

$\blacksquare$

## 2-5 题4

证明定理 2.6 及其逆定理.

### 解答 2-5 题4

正方向: $\mu{g}\left(\Phi\right)$ 乘后为全微分. 逆定理: $d\Psi=\frac{\mu_1}{\mu}d\Phi$, 故 $\Psi$ 只是 $\Phi$ 的函数.

$\blacksquare$

## 3-1 题1

讨论 $y\left(0\right)=0$ 的解的唯一性: (1) $y'=\left|y\right|^\alpha$; (2) $y'=\begin{cases}0,&y=0\\y\ln\left|y\right|,&y\ne0\end{cases}$.

### 解答 3-1 题1

(1) $\alpha\ge1$ 时由**定理 3.1 (皮卡存在和唯一性定理)** 解唯一; $0<\alpha<1$ 时不唯一. (2) 不满足利普希茨条件, 但由反证法可证零解唯一.

$\blacksquare$

## 3-1 题2

求 $y'=x+y+1$, $y\left(0\right)=0$ 的皮卡序列并取极限求解.

### 解答 3-1 题2

由积分方程与初值问题的等价性, $y_1=x+\frac{x^2}2$, $y_2=x+x^2+\frac{x^3}6$. 极限解为 $y=2e^x-x-2$.

$\blacksquare$

## 3-2 题3

能用皮卡序列证明佩亚诺存在定理吗?

### 解答 3-2 题3

不能. 由**引理 3.2 (欧拉折线的积分关系式)**, 欧拉折线的误差一致趋于零, 故可取极限. 而皮卡序列在没有利普希茨条件时相邻两项可能收敛到不同极限, 无法同时取极限. 故不能用皮卡序列证明**定理 3.3 (佩亚诺存在定理)**.

$\blacksquare$

## 3-2 题4

用托内利序列和阿斯科利引理证明**定理 3.3 (佩亚诺存在定理)**.

### 解答 3-2 题4

先证明一致有界, 再证明等度连续, 接着由阿斯科利引理取收敛子列, 最后证明极限满足积分方程.

$\blacksquare$

## 3-3 题1

证明: 线性方程 $y'=a\left(x\right)y+b\left(x\right)$ 的每一个解以 $I$ 为最大存在区间.

### 解答 3-3 题1

由**定理 3.5 (条形区域上解的整体存在性)**, 取 $A=\left|a\right|$, $B=\left|b\right|$ 即得.

$\blacksquare$

## 3-3 题2(2)

讨论 $y'=y\left(y-1\right)$ 解的存在区间.

### 解答 3-3 题2(2)

由**推论 (局部利普希茨条件下解的存在唯一与延伸)**, 分离变量得 $y=\frac1{1-Ce^x}$. 平衡解 $y\equiv0,1$ 全局存在; $0<{}y_0<1$ 全局存在; $y_0<0$ 或 $y_0>1$ 时在有限点爆破.

$\blacksquare$

## 3-3 题2(4)

讨论 $y'=1+y^2$ 解的存在区间.

### 解答 3-3 题2(4)

$y=\tan\left(x+C\right)$, 最大存在区间为有限区间 $\left(-\frac\pi2-C,\frac\pi2-C\right)$.

$\blacksquare$
