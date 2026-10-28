# week7

> **基础知识: 利普希茨条件**<br>若 $|f\left(x,y_1\right)-f\left(x,y_2\right)|\le L|y_1-y_2|$, 则称 $f$ 对 $y$ 满足利普希茨条件.

> **基础知识: 积分方程与初值问题的等价性**<br>初值问题等价于 $y=y_0+\int_{x_0}^x f\left(t,y\left(t\right)\right)\mathrm dt$. 皮卡序列 $y_{n+1}=y_0+\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\mathrm dt$.

> **定理 3.1 (皮卡存在和唯一性定理)**<br>若 $f$ 连续且满足利普希茨条件, 则初值问题在 $|x-x_0|\le h$ 上有唯一解.

> **定理 3.2 (奥斯古德条件下解的唯一性)**<br>若 $|f\left(x,y_1\right)-f\left(x,y_2\right)|\le F\left(|y_1-y_2|\right)$ 且 $\int_0^{r_1}\frac{\mathrm dr}{F\left(r\right)}=+\infty$, 则解唯一.

---

## 3-1 题1

讨论 $y\left(0\right)=0$ 的解的唯一性: (1) $y'=|y|^\alpha$; (2) $y'=\begin{cases}0,&y=0\\ y\ln|y|,&y\ne0\end{cases}$.

### 解答 3-1 题1

(1) $\alpha\ge1$ 时由**定理 3.1 (皮卡存在和唯一性定理)** 解唯一; $0<\alpha<1$ 时不唯一. (2) 不满足利普希茨条件, 但由反证法可证零解唯一. $\blacksquare$

---

## 3-1 题2

求 $y'=x+y+1$, $y\left(0\right)=0$ 的皮卡序列并取极限求解.

### 解答 3-1 题2

由**基础知识: 积分方程与初值问题的等价性**, $y_1=x+\frac{x^2}2$, $y_2=x+x^2+\frac{x^3}6$. 极限解为 $y=2e^x-x-2$. $\blacksquare$
