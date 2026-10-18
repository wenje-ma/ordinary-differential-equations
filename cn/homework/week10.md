# 作业 10

> **定理 3.1**(皮卡存在和唯一性定理)<br>设初值问题 $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, 其中 $f\left(x,y\right)$ 在矩形区域 $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 内连续, 则 $h=\min\left\{a,\frac{b}{M}\right\}$, $M=\max\limits_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

> **定理 3.6**(第一比较定理)<br>设函数 $f\left(x,y\right)$ 与 $F\left(x,y\right)$ 都在平面区域 $G$ 内连续且满足不等式 $f\left(x,y\right)<F\left(x,y\right)$($\left(x,y\right)\in G$); 又设 $y=\varphi\left(x\right)$ 与 $y=\Phi\left(x\right)$ 在区间 $\left(a,b\right)$ 上分别是初值问题 $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 与 $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$ 的解, 其中 $\left(x_0,y_0\right)\in G$. 则 $\varphi\left(x\right)<\Phi\left(x\right)$ 于 $\left(x_0,b\right)$, 而 $\varphi\left(x\right)>\Phi\left(x\right)$ 于 $\left(a,x_0\right)$. 其几何意义是: 斜率小的曲线向右不可能从斜率大的曲线下方穿越到上方.

> **最小解与最大解**<br>设初值问题 $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在矩形区域 $R$ 内连续, 若在区间 $\left[x_0-h,x_0+h\right]$ 上有两个解 $y=W\left(x\right)$ 与 $y=Z\left(x\right)$, 使 $\left(E\right)$ 的任何解 $y=y\left(x\right)$ 都满足 $W\left(x\right)\le y\left(x\right)\le Z\left(x\right)$, 则称 $y=W\left(x\right)$ 与 $y=Z\left(x\right)$ 分别为 $\left(E\right)$ 的最小解与最大解.

> **定理 3.7**(最小解与最大解的存在性)<br>存在正数 $\delta<h$, 使初值问题 $\left(E\right)$ 在区间 $\left[x_0-\delta,x_0+\delta\right]$ 上有最小解和最大解. 构造方法: 对 $\epsilon>0$, 考虑 $\left(E_\epsilon\right):\ \frac{dy}{dx}=f\left(x,y\right)\pm\epsilon$, 由**定理 3.3**(佩亚诺存在定理)取其解并利用**阿斯科利引理**取极限, 即得最小解与最大解.

> **定理 3.8**(第二比较定理)<br>设函数 $f\left(x,y\right)$ 与 $F\left(x,y\right)$ 都在平面区域 $G$ 内连续且满足 $f\left(x,y\right)\le F\left(x,y\right)$; 又设 $y=\varphi\left(x\right)$ 与 $y=\Phi\left(x\right)$ 在 $\left(a,b\right)$ 上分别是 $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 与 $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$ 的解, 其中 $y=\varphi\left(x\right)$ 是 $\left(E_1\right)$ 的右行最小解和左行最大解, $y=\Phi\left(x\right)$ 是 $\left(E_2\right)$ 的右行最大解和左行最小解. 则 $\varphi\left(x\right)\le\Phi\left(x\right)$ 于 $\left[x_0,b\right)$, 而 $\varphi\left(x\right)\ge\Phi\left(x\right)$ 于 $\left(a,x_0\right]$.

> **定理 3.3**(佩亚诺存在定理)<br>设函数 $f\left(x,y\right)$ 在矩形区域 $R$ 内连续, 则初值问题 $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left[x_0-h,x_0+h\right]$ 上至少有一个解.

> **定理 3.4**(解的延伸定理)<br>设 $f\left(x,y\right)$ 在开区域 $G$ 内连续, 则经过 $G$ 内任一点的积分曲线在 $G$ 内延伸到边界.

### 习题一

(习题 3-4 题1)设初值问题 $\left(E\right)$, 矩形区域 $R$ 和正数 $h$ 的意义同**定理 3.1**(皮卡存在和唯一性定理). 试证在 $\left(E\right)$ 的最小解 $y=W\left(x\right)$ 和最大解 $y=Z\left(x\right)$ 之间充满了 $\left(E\right)$ 的其他解: 即任取一点 $\left(x_1,y_1\right)$, 其中 $\left|x_1-x_0\right|\le h,\ W\left(x_1\right)\le y_1\le Z\left(x_1\right)$, 则 $\left(E\right)$ 在 $\left[x_0-h,x_0+h\right]$ 上至少有一个解 $y=u\left(x\right)$ 满足 $u\left(x_1\right)=y_1$.

### 解答 习题一

由**定理 3.3**(佩亚诺存在定理), 以 $\left(x_1,y_1\right)$ 为初值的初值问题在 $x_1$ 附近有局部解. 再由**定理 3.7**(最小解与最大解的存在性), 取过 $\left(x_1,y_1\right)$ 的最大解 $y=u\left(x\right)$. 下面证明它夹在 $W$ 与 $Z$ 之间, 并可延伸到整个区间.

先证右行段 $x\in\left[x_1,x_0+h\right]$. 已知 $u\left(x_1\right)=y_1\le Z\left(x_1\right)$, 且 $u$ 与 $Z$ 满足同一方程 $y'=f\left(x,y\right)$. 反设 $u$ 在某点超过 $Z$, 由连续性存在第一个接触点 $\beta>x_1$, 使 $u\left(\beta\right)=Z\left(\beta\right)$ 而在 $\left(x_1,\beta\right)$ 上 $u<Z$. 在该接触点处二者导数相等, 即 $u'\left(\beta\right)=f\left(\beta,u\left(\beta\right)\right)=f\left(\beta,Z\left(\beta\right)\right)=Z'\left(\beta\right)$, 曲线不可能在此交叉. 这与**定理 3.6**(第一比较定理)所揭示的"同一右端函数的两条积分曲线一经接触便不能穿越"相矛盾. 故 $u\left(x\right)\le Z\left(x\right)$. 同理, 由 $u\left(x_1\right)=y_1\ge W\left(x_1\right)$ 可得 $u\left(x\right)\ge W\left(x\right)$. 因此在右行段上 $W\left(x\right)\le u\left(x\right)\le Z\left(x\right)$.

既然 $u$ 始终停留在矩形区域 $R$ 内的有界条形区域 $W\le u\le Z$ 中, 由**定理 3.4**(解的延伸定理), 它可向右延伸至 $R$ 的边界即 $x_0+h$. 左行段 $x\in\left[x_0-h,x_1\right]$ 完全同理, 可得 $W\left(x\right)\le u\left(x\right)\le Z\left(x\right)$ 并延伸至 $x_0-h$.

于是 $y=u\left(x\right)$ 在 $\left[x_0-h,x_0+h\right]$ 上是 $\left(E\right)$ 的解, 且 $u\left(x_1\right)=y_1$. $\blacksquare$

### 习题二

(习题 3-4 题2)证明**定理 3.8**(第二比较定理).

### 解答 习题二

设 $f\left(x,y\right)\le F\left(x,y\right)$ 在 $G$ 内成立. 分左右两段证明.

先证右行段 $x\in\left[x_0,b\right)$, 即证 $\varphi\left(x\right)\le\Phi\left(x\right)$. 对任意 $\epsilon>0$, 考虑扰动方程 $\left(E_{1,\epsilon}\right):\ \frac{dy}{dx}=f\left(x,y\right)-\epsilon,\ y\left(x_0\right)=y_0$. 由**定理 3.3**(佩亚诺存在定理), 它存在解 $u_\epsilon\left(x\right)$; 由**定理 3.7**(最小解与最大解的存在性), 当 $\epsilon\to0^{+}$ 时 $u_\epsilon\left(x\right)\to\varphi\left(x\right)$(因 $\varphi$ 是 $\left(E_1\right)$ 的右行最小解). 由于 $f\left(x,y\right)-\epsilon<F\left(x,y\right)$ 严格成立, 对 $u_\epsilon$ 与 $\Phi$ 应用**定理 3.6**(第一比较定理), 得

$$
u_\epsilon\left(x\right)<\Phi\left(x\right),\quad x\in\left(x_0,b\right).
$$

令 $\epsilon\to0^{+}$, 由 $u_\epsilon\left(x\right)\to\varphi\left(x\right)$ 取极限, 即得 $\varphi\left(x\right)\le\Phi\left(x\right)$ 于 $\left[x_0,b\right)$.

再证左行段 $x\in\left(a,x_0\right]$, 即证 $\varphi\left(x\right)\ge\Phi\left(x\right)$. 仍取上述解 $u_\epsilon$ 对应 $\left(E_{1,\epsilon}\right):\ y'=f\left(x,y\right)-\epsilon$. 由**定理 3.7**(最小解与最大解的存在性), $u_\epsilon$ 在左行趋于 $\left(E_1\right)$ 的左行最大解, 亦即 $u_\epsilon\left(x\right)\to\varphi\left(x\right)$. 由于 $f\left(x,y\right)-\epsilon<F\left(x,y\right)$, 对左行段应用**定理 3.6**(第一比较定理)(其第二部分给出斜率小的曲线在 $x_0$ 左侧位于斜率大的曲线之上), 得

$$
u_\epsilon\left(x\right)>\Phi\left(x\right),\quad x\in\left(a,x_0\right).
$$

令 $\epsilon\to0^{+}$, 取极限即得 $\varphi\left(x\right)\ge\Phi\left(x\right)$ 于 $\left(a,x_0\right]$.

两段合起来, $\varphi\left(x\right)\le\Phi\left(x\right)$ 于 $\left[x_0,b\right)$, 且 $\varphi\left(x\right)\ge\Phi\left(x\right)$ 于 $\left(a,x_0\right]$, **定理 3.8**(第二比较定理)得证. $\blacksquare$
