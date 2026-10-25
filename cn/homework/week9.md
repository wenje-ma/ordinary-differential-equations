# 作业 9

> **定理 3.4**(解的延伸定理)<br>设微分方程 $\frac{dy}{dx}=f\left(x,y\right)$ 中函数 $f\left(x,y\right)$ 在开区域 $G$ 内连续, $P_0\left(x_0,y_0\right)$ 为 $G$ 内任一点, 则经过 $P_0$ 的任一条积分曲线将在区域 $G$ 内延伸到边界: 即对任何有界闭区域 $G_1$($P_0\in G_1\subset G$), 积分曲线将延伸到 $G_1$ 之外. 换言之, 若解 $y=y\left(x\right)$ 的最大存在区间为 $\left(\alpha,\beta\right)$, 则当 $\beta< +\infty$ 时 $\left(x,y\left(x\right)\right)$ 趋于 $G$ 的边界(在 $G=\mathbb{R}^2$ 时即 $\left|y\right|\to+\infty$).

> **推论**(局部利普希茨条件下解的存在唯一与延伸)<br>设 $f\left(x,y\right)$ 在区域 $G$ 内连续, 且对 $y$ 满足局部利普希茨条件(即 $G$ 内每一点都有一个含于 $G$ 的邻域, 使 $f$ 在其中对 $y$ 满足利普希茨条件), 则微分方程经过 $G$ 内任一点 $P_0$ 存在唯一的积分曲线, 并且它在 $G$ 内延伸到边界.

> **定理 3.5**(条形区域上解的整体存在性)<br>设微分方程 $\frac{dy}{dx}=f\left(x,y\right)$ 的右端函数在条形区域 $S:\ \alpha< x< \beta,\ -\infty< y< +\infty$ 内连续, 且满足不等式 $\left|f\left(x,y\right)\right|\le A\left(x\right)\left|y\right|+B\left(x\right)$, 其中 $A\left(x\right)\ge0$ 与 $B\left(x\right)\ge0$ 在 $\left(\alpha,\beta\right)$ 上连续, 则微分方程的每一个解都以区间 $\left(\alpha,\beta\right)$ 为最大存在区间.

### 习题一

(习题 3-3 题1)利用**定理 3.5**(条形区域上解的整体存在性)证明: 线性微分方程 $\frac{dy}{dx}=a\left(x\right)y+b\left(x\right)$($x\in I$)的每一个解 $y=y\left(x\right)$ 的(最大)存在区间为 $I$, 这里假设 $a\left(x\right)$ 和 $b\left(x\right)$ 在区间 $I$ 上是连续的.

### 解答 习题一

该方程右端函数为 $f\left(x,y\right)=a\left(x\right)y+b\left(x\right)$, 它在条形区域 $S:\ x\in I,\ -\infty< y< +\infty$ 内连续. 估计

$$
\left|f\left(x,y\right)\right|=\left|a\left(x\right)y+b\left(x\right)\right|\le \left|a\left(x\right)\right|\,\left|y\right|+\left|b\left(x\right)\right|.
$$

取 $A\left(x\right)=\left|a\left(x\right)\right|$, $B\left(x\right)=\left|b\left(x\right)\right|$. 由 $a\left(x\right),b\left(x\right)$ 在 $I$ 上连续, 知 $A\left(x\right)\ge0$, $B\left(x\right)\ge0$ 都在 $I$ 上连续. 于是 $\left|f\left(x,y\right)\right|\le A\left(x\right)\left|y\right|+B\left(x\right)$ 满足**定理 3.5**(条形区域上解的整体存在性)的条件, 故该线性方程的每一个解都以区间 $I$ 为最大存在区间. $\blacksquare$

### 习题二

(习题 3-3 题2(2))讨论微分方程 $\frac{dy}{dx}=y\left(y-1\right)$ 解的存在区间.

### 解答 习题二

右端函数 $f\left(x,y\right)=y\left(y-1\right)$ 在全平面连续, 且对 $y$ 有连续偏导数, 由**推论**(局部利普希茨条件下解的存在唯一与延伸), 过任一点的解存在唯一. 分离变量, 由 $\frac{dy}{y\left(y-1\right)}=dx$ 及 $\frac{1}{y\left(y-1\right)}=\frac{1}{y-1}-\frac{1}{y}$, 积分得

$$
\ln\left|\frac{y-1}{y}\right|=x+C,\quad\text{即}\quad y=\frac{1}{1-Ce^x}.
$$

解的存在区间由初值点 $\left(x_0,y_0\right)$ 决定:

(1) 平衡解 $y\equiv0$ 与 $y\equiv1$ 在整个 $\left(-\infty,+\infty\right)$ 上存在.

(2) 若 $0< y_0< 1$, 则 $C=\frac{y_0-1}{y_0}< 0$, 分母 $1-Ce^x> 0$ 恒成立, 解在整个 $\left(-\infty,+\infty\right)$ 上存在.

(3) 若 $y_0< 0$ 或 $y_0> 1$, 则 $C> 0$, 分母 $1-Ce^x=0$ 在有限点 $x=\ln\frac{1}{C}$ 处成立, 解在该处爆破, 故最大存在区间为有限区间. $\blacksquare$

### 习题三

(习题 3-3 题2(4))讨论微分方程 $\frac{dy}{dx}=1+y^2$ 解的存在区间.

### 解答 习题三

右端函数 $f\left(x,y\right)=1+y^2$ 在全平面连续且对 $y$ 有连续偏导数, 由**推论**(局部利普希茨条件下解的存在唯一与延伸), 解存在唯一并可延伸到全平面. 分离变量 $\frac{dy}{1+y^2}=dx$, 积分得 $\arctan y=x+C$, 即 $y=\tan\left(x+C\right)$. 正切函数的定义域要求 $x+C\in\left(-\frac{\pi}{2},\frac{\pi}{2}\right)$, 故每一解的最大存在区间为有限区间 $\left(-\frac{\pi}{2}-C,\ \frac{\pi}{2}-C\right)$, 区间端点由初值决定.

$\blacksquare$

### 习题四

(习题 3-3 题3)考虑对称形式的微分方程 $x\,dx+y\,dy=0$, 定义域为 $G=\left\{\left(x,y\right)\mid x^2+y^2> 0\right\}$, 则单位圆 $\left(x^2+y^2=1\right)$ 是一条积分曲线, 它在区域 $G$ 的内部, 并没有延伸到 $G$ 的边界. 这一点是否与上述解的延伸定理相矛盾? 为什么?

### 解答 习题四

不矛盾.

**定理 3.4**(解的延伸定理)及其推论针对的是正规形式 $\frac{dy}{dx}=f\left(x,y\right)$, 其中要求右端函数 $f\left(x,y\right)$ 在整个开区域 $G$ 内连续. 本题中若把对称形式 $x\,dx+y\,dy=0$ 写成正规形式 $\frac{dy}{dx}=-\frac{x}{y}$, 则右端函数在直线 $y=0$(即 $x$ 轴)上无定义, 因而并非在整个 $G$(挖去原点的平面)内连续. $x$ 轴上的点完全落在 $G$ 内部, 所以**定理 3.4**(解的延伸定理)在整个 $G$ 上的前提并不成立.

积分曲线 $x^2+y^2=C$ 不能作为一个单值函数 $y=\varphi\left(x\right)$ 贯穿全圆. 它只能分成上下两支 $y=\pm\sqrt{C-x^2}$, 每支的最大 $x$ 存在区间为 $\left(-\sqrt{C},\sqrt{C}\right)$. 当 $x\to\pm\sqrt{C}$ 时, 曲线到达点 $\left(\pm\sqrt{C},0\right)$, 即 $y=0$ 的直线, 这正是正规形式右端函数失去连续性的位置, 也就是该函数有定义区域的有效边界. 因此每支积分曲线都延伸到了其相应定义域的边界, 与延伸定理一致, 并无矛盾. $\blacksquare$

### 习题五

(习题 3-3 题4)设初值问题 $\left(E\right)$: $\frac{dy}{dx}=\left(y^2-2y-3\right)e^{\left(x+y\right)^2},\ y\left(x_0\right)=y_0$ 的解的最大存在区间为 $\left(a,b\right)$, 其中 $\left(x_0,y_0\right)$ 是平面上任一点. 则 $a=-\infty$ 和 $b=+\infty$ 中至少有一个成立.

### 解答 习题五

右端函数 $f\left(x,y\right)=\left(y^2-2y-3\right)e^{\left(x+y\right)^2}$ 在全平面连续且对 $y$ 有连续偏导数, 由**推论**(局部利普希茨条件下解的存在唯一与延伸), 过 $\left(x_0,y_0\right)$ 的解唯一存在, 并由**定理 3.4**(解的延伸定理)延伸到全平面的边界; 而全平面没有有限边界点, 故若某一端点有限, 则该端必有 $\left|y\right|\to+\infty$.

注意 $y^2-2y-3=\left(y-3\right)\left(y+1\right)$, 而 $e^{\left(x+y\right)^2}> 0$, 故 $y'$ 的符号由 $\left(y-3\right)\left(y+1\right)$ 决定: 当 $y> 3$ 或 $y< -1$ 时 $y'> 0$, 当 $-1< y< 3$ 时 $y'< 0$.

先看右端点 $b$. 若 $b< +\infty$, 则必有 $y\to+\infty$. 事实上, 在 $y< -1$ 时 $y'> 0$, 函数单调递增, 不可能在 $x\to b^{-}$ 时趋于 $-\infty$; 故右端爆破只能是 $y\to+\infty$, 此时解最终落入 $y> 3$ 区域并单调上升.

再看左端点 $a$. 若 $a> -\infty$, 同理解最终落入 $y< -1$ 区域, 此时 $y'> 0$, 当 $x\to a^{+}$ 时只能有 $y\to-\infty$.

反设 $a> -\infty$ 与 $b< +\infty$ 同时成立. 则解须从 $x\to a^{+}$ 时的 $y\to-\infty$ 单调增长到 $x\to b^{-}$ 时的 $y\to+\infty$, 因而必须穿过区间 $\left(-1,3\right)$. 但在 $\left(-1,3\right)$ 内 $y'< 0$, 函数单调下降, 与它由 $-\infty$ 单调上升到 $+\infty$ 相矛盾. 更确切地说: 解一旦在 $y< -1$ 区域因 $y'> 0$ 上升而接近 $y=-1$, 在 $y=-1$ 处 $y'=0$, 而刚进入 $\left(-1,3\right)$ 时 $y'< 0$, 又把它压回 $y=-1$ 下方, 故解不能穿过 $y=-1$ 进入 $\left(-1,3\right)$, 更不可能到达 $y> 3$ 而爆破到 $+\infty$.

因此 $a> -\infty$ 与 $b< +\infty$ 不能同时成立, 即 $a=-\infty$ 与 $b=+\infty$ 中至少有一个成立. $\blacksquare$
