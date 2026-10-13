# 作业 24

> **解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定)<br>考虑方程 $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}(t,\boldsymbol{x})$ 的某个解 $\boldsymbol{x} = \boldsymbol{\varphi}(t)$. 如果对任意给定的 $\varepsilon > 0$, 都存在 $\delta = \delta(\varepsilon, t_0) > 0$, 使得只要 $\|\boldsymbol{x}_0 - \boldsymbol{\varphi}(t_0)\| < \delta$, 方程以 $\boldsymbol{x}(t_0) = \boldsymbol{x}_0$ 为初值的解 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0)$ 就在 $t \ge t_0$ 有定义, 并且满足 $\|\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t)\| < \varepsilon$ 对一切 $t \ge t_0$ 成立, 则称解 $\boldsymbol{\varphi}(t)$ 是(在李雅普诺夫意义下)稳定的. 如果解 $\boldsymbol{\varphi}(t)$ 是稳定的, 而且存在 $\delta_0 > 0$, 使得只要 $\|\boldsymbol{x}_0 - \boldsymbol{\varphi}(t_0)\| < \delta_0$ 就有 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t) \to \boldsymbol{0}\ (t \to +\infty)$, 则称解 $\boldsymbol{\varphi}(t)$ 是渐近稳定的. 如果解 $\boldsymbol{\varphi}(t)$ 不是稳定的, 则称它是不稳定的. 如果吸引域是全空间, 即不论初值多大都有 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t) \to \boldsymbol{0}$, 则称解 $\boldsymbol{\varphi}(t)$ 是全局渐近稳定的.

> **定理 8.1**(常系数线性系统零解稳定性的特征根判别)<br>设线性方程 $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$ 中的矩阵 $A$ 为常矩阵, 则 (1) 零解是渐近稳定的, 当且仅当矩阵 $A$ 的全部特征根都有负的实部; (2) 零解是稳定的, 当且仅当矩阵 $A$ 的全部特征根的实部都是非正的, 并且那些实部为零的特征根所对应的若尔当块都是一阶的; (3) 零解是不稳定的, 当且仅当矩阵 $A$ 的特征根中至少有一个实部为正, 或者至少有一个实部为零且它所对应的若尔当块是高于一阶的.

> **定理 8.3**(按线性近似判断不稳定性)<br>设非线性方程 $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x} + \boldsymbol{N}(t,\boldsymbol{x})$ 中的 $A$ 为常矩阵, 而且 $A$ 的特征根中至少有一个具有正的实部, 则方程的零解是不稳定的.

> **定理 8.4**(李雅普诺夫的稳定性判定)<br>设自治系统 $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}(\boldsymbol{x})$ 的右端满足初值问题解的存在和唯一性条件, 且存在连续可微的标量函数 $V(\boldsymbol{x})$. 记 $V$ 沿轨线对 $t$ 的全导数为 $\frac{dV}{dt} = \sum_{i=1}^{n}\frac{\partial V}{\partial x_i}f_i(\boldsymbol{x})$. 若条件 $I$($V(\boldsymbol{0}) = 0,\ V(\boldsymbol{x}) > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 称 $V$ 为定正函数) 成立, 则 (1) 再若条件 $II$($\frac{dV}{dt} < 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 即全导数为定负函数) 成立, 零解是渐近稳定的; (2) 再若条件 $II^*$($\frac{dV}{dt} \le 0$, 即全导数为常负函数) 成立, 零解是稳定的; (3) 再若条件 $III$($\frac{dV}{dt} > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 即全导数为定正函数) 成立, 零解是不稳定的.

### 习题一

(习题 8-2 题1)证明: 线性方程零解的渐近稳定性等价于它的全局渐近稳定性.

### 解答 习题一

设线性方程为 $\frac{d\boldsymbol{x}}{dt} = A(t)\boldsymbol{x}$, 其基解矩阵为 $\Phi(t, t_0)$, 则以 $\boldsymbol{x}(t_0) = \boldsymbol{x}_0$ 为初值的解为

$$
\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) = \Phi(t, t_0)\boldsymbol{x}_0.
$$

由**解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定), 全局渐近稳定性蕴含渐近稳定性是显然的, 只需证明反之亦然. 设零解是渐近稳定的. 由定义, 零解是稳定的, 故存在常数 $M > 0$ 使 $\|\Phi(t, t_0)\| \le M\ (t \ge t_0)$; 而且存在 $\delta_0 > 0$, 使得只要 $\|\boldsymbol{x}_0\| < \delta_0$ 就有 $\Phi(t, t_0)\boldsymbol{x}_0 \to \boldsymbol{0}\ (t \to +\infty)$.

现任取初值 $\boldsymbol{x}_0^*$(其模可以任意大). 若 $\boldsymbol{x}_0^* \ne \boldsymbol{0}$, 令

$$
\boldsymbol{y}_0 = \frac{\delta_0}{2\|\boldsymbol{x}_0^*\|}\boldsymbol{x}_0^*.
$$

则 $\|\boldsymbol{y}_0\| = \delta_0/2 < \delta_0$, 由渐近稳定性知 $\Phi(t, t_0)\boldsymbol{y}_0 \to \boldsymbol{0}$. 由解对初值的线性性,

$$
\Phi(t, t_0)\boldsymbol{y}_0 = \frac{\delta_0}{2\|\boldsymbol{x}_0^*\|}\Phi(t, t_0)\boldsymbol{x}_0^*.
$$

因系数 $\frac{\delta_0}{2\|\boldsymbol{x}_0^*\|}$ 是正的常数, 故 $\Phi(t, t_0)\boldsymbol{x}_0^* \to \boldsymbol{0}$. 这说明任一初值(不论大小)所对应的解都趋于零向量, 即吸引域为全空间. 再结合已证的稳定性(解对任意初值都有界), 零解是全局渐近稳定的. $\blacksquare$

### 习题二

(习题 8-2 题2)设 $x$ 与 $t$ 都是标量, 试求出方程 $\frac{dx}{dt} = a(t)x$ 的零解为稳定或渐近稳定的充要条件.

### 解答 习题二

方程是可分离变量的, 以 $x(t_0) = x_0$ 为初值的解为

$$
x(t) = x_0\exp\!\left(\int_{t_0}^{t}a(s)\,ds\right).
$$

记 $A(t) = \int_{t_0}^{t}a(s)\,ds$, 则 $|x(t)| = |x_0|\,e^{A(t)}$.

先论渐近稳定性. 由**解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定), 零解渐近稳定要求对一切初值 $x_0$ 都有 $x(t) \to 0\ (t \to +\infty)$, 即 $e^{A(t)} \to 0$, 等价于

$$
\lim_{t \to +\infty}A(t) = -\infty.
$$

故零解渐近稳定的充要条件是 $\int_{t_0}^{t}a(s)\,ds \to -\infty\ (t \to +\infty)$.

再论稳定性. 零解稳定要求: 对任意 $\varepsilon > 0$, 存在 $\delta > 0$, 使 $|x_0| < \delta$ 时 $|x(t)| < \varepsilon$ 对一切 $t \ge t_0$ 成立, 即 $e^{A(t)}$ 对 $t \ge t_0$ 有上界. 这等价于 $A(t)$ 在 $t \ge t_0$ 上有上界:

$$
\sup_{t \ge t_0}\int_{t_0}^{t}a(s)\,ds < +\infty.
$$

故零解稳定的充要条件是 $\int_{t_0}^{t}a(s)\,ds$ 在 $t \to +\infty$ 时保持有上界. $\blacksquare$

### 习题三

(习题 8-2 题3)对于极坐标下的方程 $\frac{d\theta}{dt} = 1,\ \frac{dr}{dt} = \begin{cases} r^2\sin\frac{1}{r}, & r > 0, \\ 0, & r = 0, \end{cases}$ 试作出原点附近的相图, 并研究平衡点 $r = 0$ 的稳定性质.

### 解答 习题三

由 $\frac{d\theta}{dt} = 1$ 知轨线沿逆时针方向绕原点旋转, 角速度恒为 $1$. 径向方程 $\frac{dr}{dt} = r^2\sin\frac{1}{r}$ 的右端在 $r > 0$ 时当 $\sin\frac{1}{r} = 0$, 即

$$
r = r_n = \frac{1}{n\pi}\quad(n = 1, 2, 3, \cdots)
$$

时取零值. 因而每个圆周 $r = r_n$ 都是径向方程的平衡圆, 亦即原系统的一条闭轨(周期轨线).

在相邻两圆之间, $\sin\frac{1}{r}$ 恒有定号: 当 $r \in \left(\frac{1}{(2k+1)\pi}, \frac{1}{2k\pi}\right)$ 时 $\sin\frac{1}{r} > 0$, 轨线径向单调向外边界 $r = \frac{1}{2k\pi}$ 逼近; 当 $r \in \left(\frac{1}{(2k+2)\pi}, \frac{1}{(2k+1)\pi}\right)$ 时 $\sin\frac{1}{r} < 0$, 轨线径向单调向内边界 $r = \frac{1}{(2k+2)\pi}$ 逼近. 故相图为: 原点附近布满无穷多条同心圆闭轨, 相邻闭轨之间的环形区域内, 轨线在逆时针旋转的同时单调地旋向其中一条边界闭轨.

下面研究平衡点 $r = 0$ 的稳定性. 由**解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定), 任给 $\varepsilon > 0$, 取充分大的正整数 $N$ 使 $r_N = \frac{1}{N\pi} < \varepsilon$, 并令 $\delta = r_N$. 当初值 $r_0 < \delta$ 时, 由于各圆周 $r = r_n$ 都是不变闭轨, 轨线不能穿越它们, 故初值所在环形区间 $\left(r_{k+1}, r_k\right)$(其中 $k \ge N$)是正不变的, 从而

$$
r(t) < r_k \le r_N = \delta < \varepsilon\quad(t \ge 0).
$$

于是 $r = 0$ 是稳定的. 但它不是渐近稳定的: 任一闭轨 $r = r_n$ 本身就是周期轨线, 其上的轨线永远不会趋于原点; 任何从某环形区域内出发的轨线也永远停留在该区域内, 不趋于原点. 故平衡点 $r = 0$ 是稳定的, 但不是渐近稳定的. $\blacksquare$

### 习题四

(习题 8-2 题4)设二阶常系数线性方程 $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$, 其中 $A$ 是一个 $2 \times 2$ 的常矩阵. 记 $p = -\text{tr}[A]$(与矩阵 $A$ 的迹反号), $q = \det[A]$, 再设 $p^2 + q^2 \ne 0$, 试证: (1) 当 $p > 0$ 且 $q > 0$ 时, 零解是渐近稳定的; (2) 当 $p > 0$ 且 $q = 0$, 或 $p = 0$ 且 $q > 0$ 时, 零解是稳定的, 但不是渐近稳定的; (3) 在其他情形下, 零解都是不稳定的.

### 解答 习题四

矩阵 $A$ 的特征方程为

$$
\det(\lambda I - A) = \lambda^2 - \text{tr}[A]\,\lambda + \det[A] = \lambda^2 + p\lambda + q = 0.
$$

故两特征根 $\lambda_1, \lambda_2$ 满足 $\lambda_1 + \lambda_2 = -p,\ \lambda_1\lambda_2 = q$. 由**定理 8.1**(常系数线性系统零解稳定性的特征根判别), 分三种情形讨论.

(1) 当 $p > 0$ 且 $q > 0$ 时, $\lambda_1\lambda_2 > 0$ 说明两特征根同号(或为实根同号, 或为共轭复根); 而 $\lambda_1 + \lambda_2 = -p < 0$ 说明它们的实部之和为负, 故两特征根的实部都为负. 由定理 8.1(1), 零解是渐近稳定的.

(2) 当 $p > 0$ 且 $q = 0$ 时, 特征方程为 $\lambda(\lambda + p) = 0$, 特征根为 $\lambda = 0$ 与 $\lambda = -p < 0$. 零根对应的若尔当块是一阶的(两特征根互异), 其余特征根实部为负. 由定理 8.1(2), 零解是稳定的; 但因存在实部为零的特征根, 由定理 8.1(1), 它不是渐近稳定的.

当 $p = 0$ 且 $q > 0$ 时, 特征根为 $\lambda = \pm i\sqrt{q}$, 是一对纯虚根, 对应的若尔当块都是一阶的. 由定理 8.1(2), 零解是稳定的; 但两特征根实部皆为零而非负, 由定理 8.1(1), 它不是渐近稳定的.

(3) 其他情形. 若 $q < 0$, 则 $\lambda_1\lambda_2 < 0$, 两特征根为异号实根, 必有一个实部为正, 由定理 8.1(3), 零解不稳定. 若 $q > 0$ 且 $p < 0$, 则两特征根实部之和为 $-p > 0$, 实部皆为正(实根或共轭复根), 由定理 8.1(3), 零解不稳定. 若 $q = 0$ 且 $p < 0$, 则特征根为 $\lambda = 0$ 与 $\lambda = -p > 0$, 后者实部为正, 由定理 8.1(3), 零解不稳定. 而 $p = q = 0$ 已被 $p^2 + q^2 \ne 0$ 排除. 故其他情形下零解都是不稳定的. $\blacksquare$

### 习题五

(习题 8-2 题5)讨论二维的微分方程组 $\begin{cases}\frac{dx}{dt} = y - xf(x,y), \\ \frac{dy}{dt} = -x - yf(x,y)\end{cases}$ 零解的稳定性, 其中函数 $f(x,y)$ 在 $(0,0)$ 点附近是连续可微的.

### 解答 习题五

取李雅普诺夫函数 $V(x,y) = x^2 + y^2$. 它满足 $V(0,0) = 0$, 且 $V(x,y) > 0$ 当 $(x,y) \ne (0,0)$, 即 $V$ 为定正函数. 计算 $V$ 沿轨线的全导数:

$$
\frac{dV}{dt} = 2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 2x\bigl(y - xf\bigr) + 2y\bigl(-x - yf\bigr) = -2f(x,y)\bigl(x^2 + y^2\bigr).
$$

由**定理 8.4**(李雅普诺夫的稳定性判定), 分情形讨论.

若在原点附近 $f(x,y) > 0$ (特别地, 当 $f(0,0) > 0$ 时, 由连续性它在原点附近恒正), 则 $\frac{dV}{dt} < 0$ 当 $(x,y) \ne (0,0)$, 即全导数为定负函数, 由定理 8.4(1), 零解是渐近稳定的.

若在原点附近 $f(x,y) < 0$ (特别地, 当 $f(0,0) < 0$ 时), 则 $\frac{dV}{dt} > 0$ 当 $(x,y) \ne (0,0)$, 即全导数为定正函数, 由定理 8.4(3), 零解是不稳定的.

若 $f(0,0) = 0$, 则全导数的符号取决于 $f(x,y)$ 在原点附近的高阶性态: 当 $f(x,y)$ 在原点附近保持正号时零解渐近稳定, 保持负号时零解不稳定; 当 $f(x,y)$ 在原点附近变号时, 仅凭本李雅普诺夫函数不能判定, 需结合更高阶的分析. $\blacksquare$

### 习题六

(习题 8-2 题6)设 $x \in \mathbb{R}^1$, 函数 $g(x)$ 连续, 且当 $x \ne 0$ 时 $xg(x) > 0$. 试证方程 $\ddot{x} + g(x) = 0$ 的零解是稳定的, 但不是渐近稳定的.

### 解答 习题六

将二阶方程化为一阶方程组 $\frac{dx}{dt} = y,\ \frac{dy}{dt} = -g(x)$. 取李雅普诺夫函数

$$
V(x,y) = \frac{1}{2}y^2 + \int_{0}^{x}g(s)\,ds.
$$

由条件 $xg(x) > 0$ 当 $x \ne 0$ 知: 当 $x > 0$ 时 $g(x) > 0$, 当 $x < 0$ 时 $g(x) < 0$. 因而当 $x \ne 0$ 时 $\int_{0}^{x}g(s)\,ds > 0$, 加上 $\frac{1}{2}y^2 \ge 0$, 故 $V(0,0) = 0$ 且 $V(x,y) > 0$ 当 $(x,y) \ne (0,0)$, 即 $V$ 为定正函数. 计算全导数:

$$
\frac{dV}{dt} = y\frac{dy}{dt} + g(x)\frac{dx}{dt} = y\bigl(-g(x)\bigr) + g(x)y = 0.
$$

全导数恒为零, 当然满足常负条件. 由**定理 8.4**(李雅普诺夫的稳定性判定)的结论 (2), 零解是稳定的.

它不是渐近稳定的: 由于 $\frac{dV}{dt} \equiv 0$, 轨线始终停留在等值线 $V(x,y) = C$ 上. 取 $C > 0$, 等值线 $V = C$ 是围绕原点的闭曲线(或至少不含原点), 其上的轨线不会趋于 $V = 0$ 的原点. 故零解稳定但不是渐近稳定的. $\blacksquare$

### 习题七

(习题 8-2 题7)研究二维微分方程组 $\begin{cases}\frac{dx}{dt} = y, \\ \frac{dy}{dt} = -1 + x^2\end{cases}$ 的两个平衡点的稳定性.

### 解答 习题七

平衡点满足 $y = 0,\ -1 + x^2 = 0$, 故两个平衡点为 $(1,0)$ 与 $(-1,0)$.

先研究平衡点 $(1,0)$. 右端函数 $(y,\ x^2 - 1)$ 在 $(1,0)$ 处的雅可比矩阵为

$$
J = \begin{pmatrix}0 & 1 \\ 2x & 0\end{pmatrix}\bigg|_{x = 1} = \begin{pmatrix}0 & 1 \\ 2 & 0\end{pmatrix}.
$$

其特征方程为 $\lambda^2 - 2 = 0$, 特征根 $\lambda = \pm\sqrt{2}$, 其中 $\sqrt{2} > 0$ 为正实部. 由**定理 8.3**(按线性近似判断不稳定性), 平衡点 $(1,0)$ 是不稳定的.

再研究平衡点 $(-1,0)$. 其雅可比矩阵为

$$
J = \begin{pmatrix}0 & 1 \\ 2x & 0\end{pmatrix}\bigg|_{x = -1} = \begin{pmatrix}0 & 1 \\ -2 & 0\end{pmatrix}.
$$

特征方程为 $\lambda^2 + 2 = 0$, 特征根 $\lambda = \pm i\sqrt{2}$ 为纯虚根, 线性近似不能判定, 改用李雅普诺夫第二方法. 取函数

$$
V(x,y) = \frac{1}{2}y^2 + x - \frac{1}{3}x^3 + \frac{2}{3}.
$$

计算全导数:

$$
\frac{dV}{dt} = y\frac{dy}{dt} + (1 - x^2)\frac{dx}{dt} = y(x^2 - 1) + (1 - x^2)y = 0.
$$

令 $u = x + 1$, 在 $(-1,0)$ 附近展开:

$$
V = \frac{1}{2}y^2 + u^2 - \frac{1}{3}u^3.
$$

其二次项 $\frac{1}{2}y^2 + u^2$ 是定正的, 三次项 $-\frac{1}{3}u^3$ 是高阶小量, 故在 $(-1,0)$ 的小邻域内 $V$ 为定正函数, 且全导数恒为零(常负). 由**定理 8.4**(李雅普诺夫的稳定性判定)的结论 (2), 平衡点 $(-1,0)$ 是稳定的; 又因全导数恒为零, 附近轨线沿等值线 $V = C$ 运动而不趋于该点, 故它不是渐近稳定的. $\blacksquare$

### 习题八

(习题 8-2 题8(2))讨论方程组 $\begin{cases}\frac{dx}{dt} = -y^3 - x^5, \\ \frac{dy}{dt} = x^3 - y^5\end{cases}$ 零解的稳定性.

### 解答 习题八

取李雅普诺夫函数 $V(x,y) = x^4 + y^4$. 显然 $V(0,0) = 0$, 且 $V(x,y) > 0$ 当 $(x,y) \ne (0,0)$, 即 $V$ 为定正函数. 计算全导数:

$$
\frac{dV}{dt} = 4x^3\frac{dx}{dt} + 4y^3\frac{dy}{dt} = 4x^3\bigl(-y^3 - x^5\bigr) + 4y^3\bigl(x^3 - y^5\bigr).
$$

展开后交叉项 $-4x^3y^3$ 与 $+4x^3y^3$ 相消, 得

$$
\frac{dV}{dt} = -4x^8 - 4y^8 < 0\quad((x,y) \ne (0,0)).
$$

即全导数为定负函数. 由**定理 8.4**(李雅普诺夫的稳定性判定)的结论 (1), 零解是渐近稳定的. $\blacksquare$

### 习题九

(习题 8-2 题8(4))讨论方程组 $\begin{cases}\frac{dx}{dt} = 2x^2y + y^3, \\ \frac{dy}{dt} = -xy^2 + 2x^5\end{cases}$ 零解的稳定性.

### 解答 习题九

先尝试李雅普诺夫函数 $V(x,y) = x^2 + y^2$, 它是定正的. 计算全导数:

$$
\frac{dV}{dt} = 2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 2x(2x^2y + y^3) + 2y(-xy^2 + 2x^5) = 4x^3y(1 + x^2).
$$

其符号随 $xy$ 变号而改变, 不是定号函数, 故本函数不能直接判定. 下面直接由不稳定的定义分析.

考察正 $x$ 轴上方的楔形区域 $R = \{(x,y): x > 0,\ 0 < y < x^2\}$. 在 $R$ 内, 由于 $y < x^2$, 有 $y^2 < x^4$, 于是

$$
\frac{dy}{dt} = -xy^2 + 2x^5 > -x\cdot x^4 + 2x^5 = x^5 > 0,
$$

且 $\frac{dx}{dt} = y(2x^2 + y^2) > 0$.

再验证 $R$ 是正不变区域. 在边界 $y = 0$ 上, $\frac{dy}{dt} = 2x^5 > 0$, 轨线不能从 $y > 0$ 一侧穿出; 在边界 $y = x^2$ 上, 计算

$$
\frac{d}{dt}(y - x^2) = \frac{dy}{dt} - 2x\frac{dx}{dt} = -xy^2 + 2x^5 - 4x^3y - 2xy^3.
$$

代入 $y = x^2$, 得

$$
\frac{d}{dt}(y - x^2)\bigg|_{y = x^2} = -x^5 + 2x^5 - 4x^5 - 2x^7 = -3x^5 - 2x^7 < 0\quad(x > 0),
$$

即轨线在该边界上被压向 $y < x^2$ 的一侧. 故楔形区域 $R$ 是正不变的.

现任取充分小的正数 $\rho > 0$, 从正 $x$ 轴上一点 $(x_0, 0)$($x_0 > 0$ 任意小)出发的轨线, 因 $\frac{dy}{dt} = 2x_0^5 > 0$ 立即进入 $R$, 并在 $R$ 内单调演化. 若它永远留在圆盘 $x^2 + y^2 < \rho^2$ 内, 则 $\frac{dx}{dt} > 0$ 迫使 $x(t)$ 单调递增并趋于某有限极限 $x^*$, 从而 $\frac{dx}{dt} \to 0$, 即 $y(2x^2 + y^2) \to 0$. 因 $x \to x^* > 0$, 必有 $y(t) \to 0$, 但此时 $\frac{dy}{dt} \to 2x^{*5} > 0$, 与 $y(t) \to 0$ 矛盾. 故该轨线必在有限时间内穿出圆盘 $x^2 + y^2 < \rho^2$.

由**解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定), 不论原点多小的邻域, 都存在从其内出发的轨线穿出给定的 $\varepsilon$-邻域, 故零解是不稳定的. $\blacksquare$
