# 作业 16

> **定理 5.1**(解对参数的连续依赖性)<br>设 $n$ 维向量值函数 $f\left(x,y,\lambda\right)$ 在区域 $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ 上连续, 且对 $y$ 满足利普希茨条件 $\left|f\left(x,y_1,\lambda\right)-f\left(x,y_2,\lambda\right)\right|\le L\left|y_1-y_2\right|$. 令 $M$ 为 $\left|f\left(x,y,\lambda\right)\right|$ 在 $G$ 上的一个上界, $h=\min\left\{a,\frac{b}{M}\right\}$, 则初值问题 $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ 的解 $y=\varphi\left(x,\lambda\right)$ 在区域 $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$ 上是连续的.

> **定理 5.1 的推论**(解对初值的连续依赖性)<br>设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 且对 $y$ 满足利普希茨条件, 则柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ 的解 $y=\varphi\left(x,\eta\right)$ 在区域 $Q:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$ 上连续, 其中 $h=\min\left\{a,\frac{b}{M}\right\}$, $M$ 为 $\left|f\left(x,y\right)\right|$ 在 $R$ 上的一个上界.

> **定理 5.2**(解对初值的大范围连续依赖性)<br>设 $n$ 维向量值函数 $f\left(x,y\right)$ 在开区域 $G$ 上连续, 且对 $y$ 满足局部利普希茨条件. 假设 $y=\xi\left(x\right)$ 是 $\frac{dy}{dx}=f\left(x,y\right)$ 的一个解, 存在区间为 $J$. 任取有界闭区间 $\left[a,b\right]\subset J$, 则存在常数 $\delta> 0$, 使对任何初值 $\left(x_0,y_0\right)$ 满足 $a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$, 柯西问题的解 $y=\varphi\left(x;x_0,y_0\right)$ 至少在 $\left[a,b\right]$ 上存在, 且在闭区域 $D_\delta:a\le x\le b,\ a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$ 上连续.

> **积分方程与柯西问题的等价性**<br>柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 等价于积分方程 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. 当近似解序列一致收敛且 $f$ 连续时, 可在积分号下取极限.

> **阿斯科利引理**<br>有界闭区间上一致有界且等度连续的函数列, 必有一致收敛的子列.

### 习题一

(习题 5-3 题2)设 $f\left(x,y\right)$ 在区域 $R$ 上连续, 而且微分方程 $\frac{dy}{dx}=f\left(x,y\right)$ 经过 $R$ 内任何一个内点的积分曲线都是(存在)唯一的, 则上述微分方程的解对初值是连续依赖的. 这里区域 $R$ 的定义见**定理 5.1 的推论**(解对初值的连续依赖性).

### 解答 习题一

取定 $R$ 内任一内点 $\left(\overline{x}_0,\overline{y}_0\right)$. 要证: 当 $\left(x_0,y_0\right)\to\left(\overline{x}_0,\overline{y}_0\right)$ 时, 柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 的解 $y=\varphi\left(x;x_0,y_0\right)$ 在某个公共区间上一致地趋于解 $\overline{\varphi}\left(x\right)=\varphi\left(x;\overline{x}_0,\overline{y}_0\right)$.

第一步, 缩小区域使 $f$ 有界. 由 $\left(\overline{x}_0,\overline{y}_0\right)$ 是 $R$ 的内点, 可取有界闭小矩形 $R':\left|x-\overline{x}_0\right|\le a',\ \left|y-\overline{y}_0\right|\le b'$ 含于 $R$ 内部. $f$ 在有界闭区域 $R'$ 上连续, 故有界, 记 $\left|f\left(x,y\right)\right|\le M$.

第二步, 取一列初值 $\left(x_0^{\left(k\right)},y_0^{\left(k\right)}\right)\to\left(\overline{x}_0,\overline{y}_0\right)$. 解序列 $\varphi_k\left(x\right)=\varphi\left(x;x_0^{\left(k\right)},y_0^{\left(k\right)}\right)$ 满足积分方程

$$
\varphi_k\left(x\right)=y_0^{\left(k\right)}+\int_{x_0^{\left(k\right)}}^{x}f\left(t,\varphi_k\left(t\right)\right)dt.
$$

由**积分方程与柯西问题的等价性**, 从 $\left|f\right|\le M$ 得 $\left|\varphi_k\left(x\right)-\overline{y}_0\right|\le\left|y_0^{\left(k\right)}-\overline{y}_0\right|+M\left|x-\overline{x}_0\right|$. 取充分小的 $h> 0$ 使 $Mh< \frac{b'}{2}$, 并取 $k$ 充分大使 $\left|y_0^{\left(k\right)}-\overline{y}_0\right|< \frac{b'}{2}$, 则 $\left|\varphi_k\left(x\right)-\overline{y}_0\right|< b'$, 即所有 $\varphi_k$ 都停留在 $R'$ 内, 因而在 $\left[\overline{x}_0-h,\overline{x}_0+h\right]$ 上有定义.

第三步, 一致有界且等度连续. 一致有界由第二步给出. 等度连续: 对任意 $x,x'$ 在该区间上,

$$
\left|\varphi_k\left(x\right)-\varphi_k\left(x'\right)\right|=\left|\int_{x'}^{x}f\left(t,\varphi_k\left(t\right)\right)dt\right|\le M\left|x-x'\right|,
$$

它与 $k$ 无关, 故序列等度连续.

第四步, 由**阿斯科利引理**, 存在子列 $\varphi_{k_j}\left(x\right)$ 在 $\left[\overline{x}_0-h,\overline{x}_0+h\right]$ 上一致收敛于某连续函数 $\psi\left(x\right)$.

第五步, 证明极限 $\psi$ 满足积分方程. 在 $\varphi_{k_j}\left(x\right)=y_0^{\left(k_j\right)}+\displaystyle\int_{x_0^{\left(k_j\right)}}^{x}f\left(t,\varphi_{k_j}\left(t\right)\right)dt$ 两端令 $j\to\infty$. 由 $f$ 在 $R'$ 上一致连续且 $\varphi_{k_j}\rightrightarrows\psi$, 得 $f\left(t,\varphi_{k_j}\left(t\right)\right)\rightrightarrows f\left(t,\psi\left(t\right)\right)$; 又 $x_0^{\left(k_j\right)}\to\overline{x}_0$, $y_0^{\left(k_j\right)}\to\overline{y}_0$, 故

$$
\psi\left(x\right)=\overline{y}_0+\int_{\overline{x}_0}^{x}f\left(t,\psi\left(t\right)\right)dt.
$$

由**积分方程与柯西问题的等价性**, $\psi\left(x\right)$ 是经过 $\left(\overline{x}_0,\overline{y}_0\right)$ 的解.

第六步, 用题设的唯一性条件. 题设保证经过 $\left(\overline{x}_0,\overline{y}_0\right)$ 的积分曲线唯一, 故 $\psi\left(x\right)=\overline{\varphi}\left(x\right)$. 于是序列 $\left\{\varphi_k\right\}$ 的任一收敛子列都一致收敛于同一极限 $\overline{\varphi}$; 若整个序列不一致收敛于 $\overline{\varphi}$, 则必有某 $\varepsilon> 0$ 与子列 $\left|\varphi_{k_j}\left(x_j\right)-\overline{\varphi}\left(x_j\right)\right|\ge\varepsilon$, 而该子列由阿斯科利引理又含收敛子列, 矛盾. 因此 $\varphi_k\rightrightarrows\overline{\varphi}$. 由序列的任意性, 解对初值连续依赖.

$\blacksquare$

### 习题二

(习题 5-3 题3)试举例说明, 如果微分方程不满足解的唯一性条件, 则它的积分曲线族在局部范围内也不能视作平行直线族.

### 解答 习题二

反例: 取微分方程

$$
\frac{dy}{dx}=3y^{\frac{2}{3}},
$$

在原点 $\left(0,0\right)$ 附近讨论.

首先, 它的解不唯一. $y\equiv0$ 显然是一个解. 其次, $y=\left(x-c\right)^3$ 也是解: 直接验证 $y'=3\left(x-c\right)^2$, 而 $3y^{\frac{2}{3}}=3\left[\left(x-c\right)^3\right]^{\frac{2}{3}}=3\left(x-c\right)^2$, 故 $y'=3y^{\frac{2}{3}}$. 进一步, 对任意常数 $c\le0$, 分段函数

$$
y\left(x\right)=\begin{cases}0,&x\le c,\\\left(x-c\right)^3,&x> c\end{cases}
$$

在 $x=c$ 处连续且一阶连续可微(左右两侧函数值与导数值均为 $0$), 仍是方程的解. 令 $c$ 遍取 $\left(-\infty,0\right]$ 中一切值, 就得到经过 $\left(0,0\right)$ 的无穷多条积分曲线.

其次, 看附近初值出发的解如何汇集. 对初值 $y\left(0\right)=\eta> 0$, 经过 $\left(0,\eta\right)$ 的解为 $\varphi\left(x;\eta\right)=\left(x+\eta^{\frac{1}{3}}\right)^3$. 令 $\eta\to0^{+}$, 则在固定的 $x> 0$ 处 $\varphi\left(x;\eta\right)\to x^3$. 即: 从右半侧邻近原点的初值出发的积分曲线族, 其极限是曲线 $y=x^3$(一条经过原点且离开原点的解); 而从原点本身出发的解却可以取 $y\equiv0$. 也就是说, 极限曲线究竟是哪一条, 取决于逼近原点的方向与方式, 不存在唯一确定的邻近解的极限曲线.

最后, 说明不能局部视作平行直线族. 在**定理 5.1 的推论**(解对初值的连续依赖性)中, 把积分曲线族局部"拉直"的变换 $T:\left(x,\eta\right)\mapsto\left(x,\varphi\left(x,\eta\right)\right)$ 之所以是一对一的拓扑变换, 用到的关键依据正是解的唯一性: $\eta_1\ne\eta_2$ 时 $\varphi\left(x,\eta_1\right)\ne\varphi\left(x,\eta_2\right)$. 本反例中唯一性失效: 任取 $x< 0$, 曲线 $\varphi\left(x;\eta\right)=\left(x+\eta^{\frac{1}{3}}\right)^3$ 在 $\eta=\left(-x\right)^3< 0$ 时穿过零线 $y=0$, 即不同初值 $\eta$ 出发的积分曲线在原点附近相互交叉; 同时无穷多条曲线挤在同一个出发点 $\left(0,0\right)$ 附近. 因而 $T$ 不再是一一映射, 积分曲线族在原点附近扇形展开, 不能局部视作平行直线族.

$\blacksquare$
