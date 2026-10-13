# 作业 8

> **欧拉折线**<br>设微分方程 $\dfrac{dy}{dx}=f\left(x,y\right)$ 在矩形区域 $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 内连续, $M$ 为 $\left|f\left(x,y\right)\right|$ 在 $R$ 上的一个上界, 令 $h=\min\left\{a,\dfrac{b}{M}\right\}$. 把区间 $\left[x_0-h,x_0+h\right]$ 等分为 $2n$ 份, 从初值点 $P_0\left(x_0,y_0\right)$ 出发, 在每一节点沿该处线素方向作直线段, 得到一条停留在角形区域 $\left|y-y_0\right|\le M\left|x-x_0\right|$ 内的连续折线 $y=\rho_n\left(x\right)$, 称为初值问题 $\left(E\right):\ \dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 的欧拉折线.

> **定理 3.1**(皮卡存在和唯一性定理)<br>设初值问题 $\left(E\right)$: $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, 其中 $f\left(x,y\right)$ 在矩形区域 $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 内连续且对 $y$ 满足利普希茨条件, 则 $\left(E\right)$ 在区间 $I=\left[x_0-h,x_0+h\right]$ 上有且只有一个解, 其中 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

> **积分方程与初值问题的等价性**<br>初值问题 $\left(E\right)$ 有解等价于积分方程 $y=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$ 有解.

> **一致有界与等度连续**<br>设在区间 $I$ 上给定函数序列 $f_1\left(x\right),f_2\left(x\right),\cdots$. 若存在常数 $K>0$ 使 $\left|f_n\left(x\right)\right|<K$ 对一切 $n$ 成立, 则称该序列在 $I$ 上一致有界; 若对任意正数 $\varepsilon$, 存在 $\delta=\delta\left(\varepsilon\right)$, 使只要 $\left|x_1-x_2\right|<\delta$ 就有 $\left|f_n\left(x_1\right)-f_n\left(x_2\right)\right|<\varepsilon$ 对一切 $n$ 成立, 则称该序列在 $I$ 上等度连续.

> **阿斯科利引理**<br>设函数序列在有限闭区间 $I$ 上一致有界且等度连续, 则可以选取它的一个子序列, 使该子序列在区间 $I$ 上一致收敛.

> **引理 3.1**(欧拉序列的收敛子序列)<br>欧拉折线序列 $\left\{\rho_n\left(x\right)\right\}$ 在区间 $\left[x_0-h,x_0+h\right]$ 上一致有界且等度连续, 因而至少含有一个一致收敛的子序列.

> **引理 3.2**(欧拉折线的积分关系式)<br>欧拉折线 $y=\rho_n\left(x\right)$ 在区间 $\left[x_0-h,x_0+h\right]$ 上满足 $\rho_n\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,\rho_n\left(t\right)\right)\,dt+\delta_n\left(x\right)$, 其中 $\lim\limits_{n\to\infty}\delta_n\left(x\right)=0$ 对 $\left|x-x_0\right|\le h$ 一致成立.

> **定理 3.3**(佩亚诺存在定理)<br>设函数 $f\left(x,y\right)$ 在矩形区域 $R$ 内连续, 则初值问题 $\left(E\right):\ \dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left[x_0-h,x_0+h\right]$ 上至少有一个解, 这里矩形区域 $R$ 和正数 $h$ 的定义同**定理 3.1**(皮卡存在和唯一性定理).

### 习题一

(习题 3-2 题3)我们知道: 皮卡序列满足阿斯科利引理的条件, 试问: 能用皮卡序列来证明佩亚诺的存在定理吗? 说明理由.

### 解答 习题一

不能. 理由如下.

佩亚诺存在定理的证明(见**定理 3.3**(佩亚诺存在定理))之所以成立, 关键在于**引理 3.2**(欧拉折线的积分关系式): 欧拉折线 $\rho_n$ 满足

$$
\rho_n\left(x\right)=y_0+\int_{x_0}^x f\left(t,\rho_n\left(t\right)\right)\,dt+\delta_n\left(x\right),
$$

其中误差项 $\delta_n\left(x\right)$ 一致趋于零. 于是由**阿斯科利引理**取出的一致收敛子序列 $\rho_{n_k}\to\varphi$, 在等式两端令 $k\to\infty$, 误差项消失, 直接得到 $\varphi\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,\varphi\left(t\right)\right)\,dt$, 即 $\varphi$ 是解.

皮卡序列则不然. 它满足的是递推式 $y_{n+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt$, 即两端分别是序列的相邻两项 $y_{n+1}$ 与 $y_n$. 在仅有连续性而没有利普希茨条件时, 即使由**阿斯科利引理**得到 $y_{n_k}\to\varphi$, 由于下标平移后的 $y_{n_k+1}$ 是另一个子序列, 二者可能收敛到不同的极限, 从而无法在递推式中同时取极限得到不动点方程. 本节米勒反例正说明了这一点: 其皮卡序列为 $y_n\left(x\right)=\left(-1\right)^{n+1}x^2$, 偶子列收敛到 $-x^2$, 奇子列收敛到 $x^2$, 二者都不是初值问题的解.

究其根源, 皮卡序列收敛性的证明依赖利普希茨条件来估计相邻两项之差 $\left|y_{n+1}-y_n\right|$, 进而证明相应级数一致收敛(见**定理 3.1**(皮卡存在和唯一性定理)证明的第三步). 佩亚诺定理只假定 $f$ 连续, 不具备该估计, 皮卡序列可不收敛. 因此皮卡序列不能用来证明佩亚诺存在定理. $\blacksquare$

### 习题二

(习题 3-2 题4)对于与初值问题 $\left(E\right)$ 等价的积分方程 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$, 在区间 $I=\left[x_0,x_0+h\right]$ 上构造托内利序列如下: 任给正整数 $n$, 令 $d_n=\dfrac{h}{n}$, $x_k=x_0+kd_n$($k=0,1,\cdots,n$), 则分点 $x_0,x_1,\cdots,x_n\left(=x_0+h\right)$ 把 $I$ 分成 $n$ 等份, 用分段递推法定义函数 $y_n\left(x\right)=\begin{cases}y_0,&x\in\left[x_0,x_1\right],\\ y_0+\displaystyle\int_{x_0}^{x-d_n}f\left(t,y_n\left(t\right)\right)\,dt,&x\in\left[x_1,x_0+h\right].\end{cases}$ 试用托内利序列和阿斯科利引理证明佩亚诺存在定理(即**定理 3.3**(佩亚诺存在定理)).

### 解答 习题二

分四步证明.

第一步, 证明 $\left\{y_n\left(x\right)\right\}$ 在 $I$ 上一致有界. 在 $\left[x_0,x_1\right]$ 上 $y_n\equiv y_0$. 在 $\left[x_1,x_0+h\right]$ 上用归纳法估计: 设对 $t\le x-d_n$ 已有 $\left|y_n\left(t\right)-y_0\right|\le M\left(t-x_0\right)$, 则

$$
\left|y_n\left(x\right)-y_0\right|\le\int_{x_0}^{x-d_n}\left|f\left(t,y_n\left(t\right)\right)\right|\,dt\le M\left(x-d_n-x_0\right)\le M\left(x-x_0\right)\le Mh\le b.
$$

故 $\left|y_n\left(x\right)-y_0\right|\le b$ 对一切 $n$ 与 $x\in I$ 成立, 序列一致有界.

第二步, 证明 $\left\{y_n\left(x\right)\right\}$ 等度连续. 在 $\left[x_1,x_0+h\right]$ 上几乎处处有 $y_n'\left(x\right)=f\left(x-d_n,y_n\left(x-d_n\right)\right)$, 故 $\left|y_n'\left(x\right)\right|\le M$; 在 $\left[x_0,x_1\right]$ 上 $y_n$ 为常数. 于是对任意 $s,t\in I$, 有 $\left|y_n\left(s\right)-y_n\left(t\right)\right|\le M\left|s-t\right|$, 序列等度连续.

第三步, 由**阿斯科利引理**, $\left\{y_n\left(x\right)\right\}$ 存在一致收敛的子序列 $y_{n_k}\left(x\right)\to\varphi\left(x\right)$, 极限函数 $\varphi$ 在 $I$ 上连续.

第四步, 证明 $\varphi$ 满足积分方程. 对 $x\in\left[x_1,x_0+h\right]$, 把积分上限 $x-d_n$ 改写为 $x$, 得

$$
y_n\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,y_n\left(t\right)\right)\,dt-\int_{x-d_n}^{x}f\left(t,y_n\left(t\right)\right)\,dt.
$$

右端第二个积分长度为 $d_n$, 且 $\left|f\right|\le M$, 故其绝对值不超过 $Md_n$, 当 $n\to\infty$ 时一致趋于零. 即 $y_n\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt+\varepsilon_n\left(x\right)$, 其中 $\varepsilon_n\left(x\right)$ 一致趋于零. 沿子序列令 $k\to\infty$, 由 $y_{n_k}\to\varphi$ 一致及 $f$ 的连续性, 在积分号下取极限, 得

$$
\varphi\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,\varphi\left(t\right)\right)\,dt.
$$

由积分方程与初值问题的等价性, $y=\varphi\left(x\right)$ 在 $I=\left[x_0,x_0+h\right]$ 上是 $\left(E\right)$ 的解. 左行段同理可证. 这就用托内利序列证明了**定理 3.3**(佩亚诺存在定理). $\blacksquare$
