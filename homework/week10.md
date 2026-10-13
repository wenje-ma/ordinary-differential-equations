# 作业 10

> **定理 3.1**(皮卡存在和唯一性定理)<br>设初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$, 其中 $f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续, 则 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{(x,y)\in R}|f(x,y)|$.

> **定理 3.6**(第一比较定理)<br>设函数 $f(x,y)$ 与 $F(x,y)$ 都在平面区域 $G$ 内连续且满足不等式 $f(x,y)<F(x,y)$($(x,y)\in G$); 又设 $y=\varphi(x)$ 与 $y=\Phi(x)$ 在区间 $(a,b)$ 上分别是初值问题 $(E_1):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 与 $(E_2):\ \dfrac{dy}{dx}=F(x,y),\ y(x_0)=y_0$ 的解, 其中 $(x_0,y_0)\in G$. 则 $\varphi(x)<\Phi(x)$ 于 $(x_0,b)$, 而 $\varphi(x)>\Phi(x)$ 于 $(a,x_0)$. 其几何意义是: 斜率小的曲线向右不可能从斜率大的曲线下方穿越到上方.

> **最小解与最大解**<br>设初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 在矩形区域 $R$ 内连续, 若在区间 $[x_0-h,x_0+h]$ 上有两个解 $y=W(x)$ 与 $y=Z(x)$, 使 $(E)$ 的任何解 $y=y(x)$ 都满足 $W(x)\le y(x)\le Z(x)$, 则称 $y=W(x)$ 与 $y=Z(x)$ 分别为 $(E)$ 的最小解与最大解.

> **定理 3.7**(最小解与最大解的存在性)<br>存在正数 $\delta<h$, 使初值问题 $(E)$ 在区间 $[x_0-\delta,x_0+\delta]$ 上有最小解和最大解. 构造方法: 对 $\varepsilon>0$, 考虑 $(E_\varepsilon):\ \dfrac{dy}{dx}=f(x,y)\pm\varepsilon$, 由**定理 3.3**(佩亚诺存在定理)取其解并利用**阿斯科利引理**取极限, 即得最小解与最大解.

> **定理 3.8**(第二比较定理)<br>设函数 $f(x,y)$ 与 $F(x,y)$ 都在平面区域 $G$ 内连续且满足 $f(x,y)\le F(x,y)$; 又设 $y=\varphi(x)$ 与 $y=\Phi(x)$ 在 $(a,b)$ 上分别是 $(E_1):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 与 $(E_2):\ \dfrac{dy}{dx}=F(x,y),\ y(x_0)=y_0$ 的解, 其中 $y=\varphi(x)$ 是 $(E_1)$ 的右行最小解和左行最大解, $y=\Phi(x)$ 是 $(E_2)$ 的右行最大解和左行最小解. 则 $\varphi(x)\le\Phi(x)$ 于 $[x_0,b)$, 而 $\varphi(x)\ge\Phi(x)$ 于 $(a,x_0]$.

> **定理 3.3**(佩亚诺存在定理)<br>设函数 $f(x,y)$ 在矩形区域 $R$ 内连续, 则初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 在区间 $[x_0-h,x_0+h]$ 上至少有一个解.

> **定理 3.4**(解的延伸定理)<br>设 $f(x,y)$ 在开区域 $G$ 内连续, 则经过 $G$ 内任一点的积分曲线在 $G$ 内延伸到边界.

### 习题一

(习题 3-4 题1)设初值问题 $(E)$, 矩形区域 $R$ 和正数 $h$ 的意义同**定理 3.1**(皮卡存在和唯一性定理). 试证在 $(E)$ 的最小解 $y=W(x)$ 和最大解 $y=Z(x)$ 之间充满了 $(E)$ 的其他解: 即任取一点 $(x_1,y_1)$, 其中 $|x_1-x_0|\le h,\ W(x_1)\le y_1\le Z(x_1)$, 则 $(E)$ 在 $[x_0-h,x_0+h]$ 上至少有一个解 $y=u(x)$ 满足 $u(x_1)=y_1$.

### 解答 习题一

由**定理 3.3**(佩亚诺存在定理), 以 $(x_1,y_1)$ 为初值的初值问题在 $x_1$ 附近有局部解. 再由**定理 3.7**(最小解与最大解的存在性), 取过 $(x_1,y_1)$ 的最大解 $y=u(x)$. 下面证明它夹在 $W$ 与 $Z$ 之间, 并可延伸到整个区间.

先证右行段 $x\in[x_1,x_0+h]$. 已知 $u(x_1)=y_1\le Z(x_1)$, 且 $u$ 与 $Z$ 满足同一方程 $y'=f(x,y)$. 反设 $u$ 在某点超过 $Z$, 由连续性存在第一个接触点 $\beta>x_1$, 使 $u(\beta)=Z(\beta)$ 而在 $(x_1,\beta)$ 上 $u<Z$. 在该接触点处二者导数相等, 即 $u'(\beta)=f(\beta,u(\beta))=f(\beta,Z(\beta))=Z'(\beta)$, 曲线不可能在此交叉. 这与**定理 3.6**(第一比较定理)所揭示的"同一右端函数的两条积分曲线一经接触便不能穿越"相矛盾. 故 $u(x)\le Z(x)$. 同理, 由 $u(x_1)=y_1\ge W(x_1)$ 可得 $u(x)\ge W(x)$. 因此在右行段上 $W(x)\le u(x)\le Z(x)$.

既然 $u$ 始终停留在矩形区域 $R$ 内的有界条形区域 $W\le u\le Z$ 中, 由**定理 3.4**(解的延伸定理), 它可向右延伸至 $R$ 的边界即 $x_0+h$. 左行段 $x\in[x_0-h,x_1]$ 完全同理, 可得 $W(x)\le u(x)\le Z(x)$ 并延伸至 $x_0-h$.

于是 $y=u(x)$ 在 $[x_0-h,x_0+h]$ 上是 $(E)$ 的解, 且 $u(x_1)=y_1$. $\blacksquare$

### 习题二

(习题 3-4 题2)证明**定理 3.8**(第二比较定理).

### 解答 习题二

设 $f(x,y)\le F(x,y)$ 在 $G$ 内成立. 分左右两段证明.

先证右行段 $x\in[x_0,b)$, 即证 $\varphi(x)\le\Phi(x)$. 对任意 $\varepsilon>0$, 考虑扰动方程 $(E_{1,\varepsilon}):\ \dfrac{dy}{dx}=f(x,y)-\varepsilon,\ y(x_0)=y_0$. 由**定理 3.3**(佩亚诺存在定理), 它存在解 $u_\varepsilon(x)$; 由**定理 3.7**(最小解与最大解的存在性), 当 $\varepsilon\to0^{+}$ 时 $u_\varepsilon(x)\to\varphi(x)$(因 $\varphi$ 是 $(E_1)$ 的右行最小解). 由于 $f(x,y)-\varepsilon<F(x,y)$ 严格成立, 对 $u_\varepsilon$ 与 $\Phi$ 应用**定理 3.6**(第一比较定理), 得

$$
u_\varepsilon(x)<\Phi(x),\qquad x\in(x_0,b).
$$

令 $\varepsilon\to0^{+}$, 由 $u_\varepsilon(x)\to\varphi(x)$ 取极限, 即得 $\varphi(x)\le\Phi(x)$ 于 $[x_0,b)$.

再证左行段 $x\in(a,x_0]$, 即证 $\varphi(x)\ge\Phi(x)$. 仍取上述解 $u_\varepsilon$ 对应 $(E_{1,\varepsilon}):\ y'=f(x,y)-\varepsilon$. 由**定理 3.7**(最小解与最大解的存在性), $u_\varepsilon$ 在左行趋于 $(E_1)$ 的左行最大解, 亦即 $u_\varepsilon(x)\to\varphi(x)$. 由于 $f(x,y)-\varepsilon<F(x,y)$, 对左行段应用**定理 3.6**(第一比较定理)(其第二部分给出斜率小的曲线在 $x_0$ 左侧位于斜率大的曲线之上), 得

$$
u_\varepsilon(x)>\Phi(x),\qquad x\in(a,x_0).
$$

令 $\varepsilon\to0^{+}$, 取极限即得 $\varphi(x)\ge\Phi(x)$ 于 $(a,x_0]$.

两段合起来, $\varphi(x)\le\Phi(x)$ 于 $[x_0,b)$, 且 $\varphi(x)\ge\Phi(x)$ 于 $(a,x_0]$, **定理 3.8**(第二比较定理)得证. $\blacksquare$
