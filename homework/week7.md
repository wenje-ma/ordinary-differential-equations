# 作业 7

> **利普希茨条件**<br>设函数 $f(x,y)$ 在区域 $D$ 内满足不等式 $|f(x,y_1)-f(x,y_2)|\le L|y_1-y_2|$, 其中常数 $L>0$, 则称函数 $f(x,y)$ 在区域 $D$ 内对 $y$ 满足利普希茨条件. 若 $f(x,y)$ 在凸区域 $D$ 内对 $y$ 有连续的偏微商, 则它在 $D$ 内对 $y$ 满足利普希茨条件.

> **定理 3.1**(皮卡存在和唯一性定理)<br>设初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$, 其中 $f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续, 而且对 $y$ 满足利普希茨条件. 则 $(E)$ 在区间 $I=[x_0-h,x_0+h]$ 上有并且只有一个解, 其中常数 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{(x,y)\in R}|f(x,y)|$.

> **定理 3.2**(奥斯古德条件下解的唯一性)<br>设函数 $f(x,y)$ 在区域 $G$ 内连续, 且满足不等式 $|f(x,y_1)-f(x,y_2)|\le F(|y_1-y_2|)$, 其中 $F(r)>0$ 是 $r>0$ 的连续函数, 而且瑕积分 $\int_0^{r_1}\dfrac{dr}{F(r)}=+\infty$($r_1>0$ 为常数), 则称 $f(x,y)$ 在 $G$ 内对 $y$ 满足奥斯古德条件; 此时微分方程 $\dfrac{dy}{dx}=f(x,y)$ 在 $G$ 内经过每一点的解都是唯一的.

> **积分方程与初值问题的等价性**<br>初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 有解 $y=\varphi(x)$, 等价于积分方程 $y=y_0+\displaystyle\int_{x_0}^x f(t,y(t))\,dt$ 有解. 其皮卡序列为 $y_{n+1}(x)=y_0+\displaystyle\int_{x_0}^x f(t,y_n(t))\,dt$, 其中取 $y_0(x)=y_0$.

### 习题一

(习题 3-1 题1)利用右端函数的性质讨论下列微分方程满足初值条件 $y(0)=0$ 的解的唯一性问题: (1) $\dfrac{dy}{dx}=|y|^{\alpha}$, 常数 $\alpha>0$; (2) $\dfrac{dy}{dx}=\begin{cases}0,&y=0,\\ y\ln|y|,&y\ne0.\end{cases}$

### 解答 习题一

(1) 右端函数 $f(x,y)=|y|^{\alpha}$ 与 $x$ 无关, 分两种情形讨论.

当 $\alpha\ge1$ 时, $f(x,y)$ 对 $y$ 满足利普希茨条件: 若 $\alpha=1$, 则 $|f(x,y_1)-f(x,y_2)|=||y_1|-|y_2||\le|y_1-y_2|$; 若 $\alpha>1$, 则 $f(x,y)=|y|^{\alpha}$ 在 $y=0$ 附近有连续且有界的导数 $f_y=\alpha|y|^{\alpha-1}\operatorname{sign}(y)$, 由利普希茨条件的判别(凸区域内有连续偏微商即满足利普希茨条件)即得. 由**定理 3.1**(皮卡存在和唯一性定理), 过 $(0,0)$ 的解唯一, 即零解 $y\equiv0$.

当 $0<\alpha<1$ 时, $f(x,y)=|y|^{\alpha}$ 在 $y=0$ 附近不是利普希茨的(导数 $\alpha|y|^{\alpha-1}$ 在 $y\to0$ 时无界), 故**定理 3.1**(皮卡存在和唯一性定理)不能保证唯一性. 事实上, $y\equiv0$ 是一个解; 另取函数

$$
y(x)=\begin{cases}0,&x\le0,\\ \big[(1-\alpha)x\big]^{\frac{1}{1-\alpha}},&x\ge0.\end{cases}
$$

它连续可微且 $y(0)=0$. 对 $x>0$, 直接求导得 $y'=\big[(1-\alpha)x\big]^{\frac{\alpha}{1-\alpha}}=y^{\alpha}=|y|^{\alpha}$, 故它也是一个解. 两个解不同, 因此解不唯一.

(2) 右端函数 $f(x,y)=\begin{cases}0,&y=0,\\ y\ln|y|,&y\ne0\end{cases}$ 与 $x$ 无关, 且由 $\lim\limits_{y\to0}y\ln|y|=0$ 知它连续. 它对 $y$ 不满足利普希茨条件(在 $y\ne0$ 处 $f_y=\ln|y|+1$, 当 $y\to0$ 时无界), 故不能用**定理 3.1**(皮卡存在和唯一性定理). 下面与**定理 3.2**(奥斯古德条件下解的唯一性)的证明同理, 用反证法证明零解唯一.

设 $y=y(x)$ 是满足 $y(0)=0$ 的一个解. 反设有 $x_1>0$ 使 $y(x_1)>0$(出现负值的情形同理). 令 $x_0=\inf\{x\ge0:\ y(x)>0\ \text{于}\ (x,x_1]\}$, 则 $y(x_0)=0$, 且在 $(x_0,x_1]$ 上 $y>0$. 在该区间上令 $u=\ln y$, 则

$$
\frac{du}{dx}=\frac{y'}{y}=\ln y=u.
$$

该方程的解为 $u=Ce^x$, 即在 $(x_0,x_1]$ 上 $y=e^{Ce^x}$. 但由 $y(x_0)=0$ 应有 $u(x_0)=-\infty$, 而 $Ce^{x_0}$ 是有限数, 矛盾. 故不存在使 $y(x_1)\ne0$ 的点, 即 $y\equiv0$ 是唯一解. 这说明不满足利普希茨条件并不必然导致解不唯一. $\blacksquare$

### 习题二

(习题 3-1 题2)试求初值问题 $\dfrac{dy}{dx}=x+y+1,\ y(0)=0$ 的皮卡序列, 并由此取极限求解.

### 解答 习题二

由积分方程与初值问题的等价性, 该初值问题等价于积分方程 $y(x)=\displaystyle\int_0^x\big[t+y(t)+1\big]\,dt$, 皮卡序列为

$$
y_{n+1}(x)=\int_0^x\big[t+y_n(t)+1\big]\,dt,\qquad y_0(x)=0.
$$

逐项计算前几项:

$$
y_1(x)=\int_0^x(t+1)\,dt=x+\frac{x^2}{2},
$$

$$
y_2(x)=\int_0^x\left[t+\left(t+\frac{t^2}{2}\right)+1\right]dt=\int_0^x\left(\frac{t^2}{2}+2t+1\right)dt=x+x^2+\frac{x^3}{6},
$$

$$
y_3(x)=\int_0^x\left[t+\left(t+t^2+\frac{t^3}{6}\right)+1\right]dt=x+x^2+\frac{x^3}{3}+\frac{x^4}{24}.
$$

若皮卡序列收敛到解 $y=y(x)$, 则极限函数满足积分方程 $y(x)=\displaystyle\int_0^x\big[t+y(t)+1\big]\,dt$, 即微分方程 $y'=x+y+1$ 及初值条件 $y(0)=0$. 这是一阶线性方程 $y'-y=x+1$, 两端乘积分因子 $e^{-x}$, 得

$$
\big(ye^{-x}\big)'=(x+1)e^{-x}.
$$

积分得 $ye^{-x}=-(x+2)e^{-x}+C$, 代入 $y(0)=0$ 得 $C=2$, 故

$$
y(x)=2e^x-x-2.
$$

$\blacksquare$
