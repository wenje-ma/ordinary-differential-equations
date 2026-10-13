# 常微分方程

## 1.1 微分方程及其解的定义

**定义 1.1**(常微分方程)

凡是联系自变量 $x$ 与这个自变量的未知函数 $y=y\left(x\right)$, 和它的导数 $y'=y'\left(x\right)$ 以及直到 $n$ 阶导数 $y^{\left(n\right)}=y^{\left(n\right)}\left(x\right)$ 在内的方程 $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$ 叫作常微分方程, 其中导数实际出现的最高阶数 $n$ 叫作常微分方程的阶. 若左端函数 $F$ 对未知函数 $y$ 及其各阶导数 $y',y'',\cdots,y^{\left(n\right)}$ 的全体而言是一次的, 则称它是线性常微分方程, 否则称它为非线性常微分方程.

**定义 1.2**(解)

设函数 $y=\varphi\left(x\right)$ 在区间 $J$ 上连续, 且有直到 $n$ 阶的导数. 如果把 $y=\varphi\left(x\right)$ 及其相应的各阶导数代入方程 $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$, 得到关于 $x$ 的恒等式 $F\left(x,\varphi\left(x\right),\varphi'\left(x\right),\cdots,\varphi^{\left(n\right)}\left(x\right)\right)=0$ 对一切 $x\in J$ 都成立, 则称 $y=\varphi\left(x\right)$ 为微分方程在区间 $J$ 上的一个解.

**定义 1.3**(通解与特解)

设 $n$ 阶微分方程的解 $y=\varphi\left(x,C_1,C_2,\cdots,C_n\right)$ 包含 $n$ 个独立的任意常数 $C_1,C_2,\cdots,C_n$, 则称它为通解. 这里 $n$ 个任意常数 $C_1,C_2,\cdots,C_n$ 是独立的, 其含义是雅可比行列式 $\frac{D\left(\varphi,\varphi',\cdots,\varphi^{\left(n-1\right)}\right)}{D\left(C_1,C_2,\cdots,C_n\right)}\neq0$, 其中 $\varphi^{\left(k\right)}=\varphi^{\left(k\right)}\left(x,C_1,C_2,\cdots,C_n\right)\ \left(k=0,1,\cdots,n-1\right)$. 如果微分方程的解 $y=\varphi\left(x\right)$ 不包含任意常数, 则称它为特解.

**初值问题**(柯西问题)

对 $n$ 阶微分方程, 初值条件的一般提法是 $y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$, 其中 $x_0$ 是自变量所取定的某个初值, 而 $y_0,\ y_0',\ \cdots,\ y_0^{\left(n-1\right)}$ 是未知函数及其相应导数所取定的初值. 这样, $n$ 阶微分方程的初值问题可以提成如下形式: $$\begin{cases}y^{\left(n\right)}=F\left(x,y,y',\cdots,y^{\left(n-1\right)}\right),\\y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}.\end{cases}$$ 初值问题又名柯西问题.

**微分方程的求解与积分运算**

微分方程的求解与一定的积分运算相联系. 因此常把求解微分方程的过程称为积分一个微分方程, 而把微分方程的解叫作积分. 由于每进行一次不定积分运算, 就会产生一个任意常数, 因此就微分方程本身的积分而言, $n$ 阶微分方程的通解应该包含 $n$ 个任意常数.

## 2.1 恰当方程

**恰当方程**(全微分方程)

考虑对称形式的一阶微分方程 $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$. 如果存在一个可微函数 $\Phi\left(x,y\right)$, 使得它的全微分为 $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy$, 亦即它的偏导数为 $\frac{\partial\Phi}{\partial x}=P\left(x,y\right),\ \frac{\partial\Phi}{\partial y}=Q\left(x,y\right)$, 则称该式为恰当方程或全微分方程. 当方程为恰当方程时, 可将它改写为全微分的形式 $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy=0$, 从而 $\Phi\left(x,y\right)=C$, 其中 $C$ 为任意常数, 称 $\Phi\left(x,y\right)=C$ 为方程的一个通积分.

**定理 2.1**(恰当方程的判别与通积分公式)

设函数 $P\left(x,y\right)$ 和 $Q\left(x,y\right)$ 在区域 $R:\alpha<x<\beta,\ \gamma<y<\delta$ 上连续, 且有连续的一阶偏导数 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$, 则微分方程 $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ 是恰当方程的充要条件为恒等式 $$\frac{\partial}{\partial y}P\left(x,y\right)\equiv\frac{\partial}{\partial x}Q\left(x,y\right)$$ 在 $R$ 内成立. 而且当该式成立时, 方程的通积分为 $$\int_{x_0}^{x}P\left(x,y\right)dx+\int_{y_0}^{y}Q\left(x_0,y\right)dy=C,$$ 或者 $$\int_{x_0}^{x}P\left(x,y_0\right)dx+\int_{y_0}^{y}Q\left(x,y\right)dy=C,$$ 其中 $\left(x_0,y_0\right)$ 是 $R$ 中任意取定的一点.

## 2.2 变量分离方程

**变量分离方程**

考虑对称形式的一阶微分方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0.$$ 若其中 $P\left(x,y\right)=X\left(x\right)Y_1\left(y\right)$ 与 $Q\left(x,y\right)=X_1\left(x\right)Y\left(y\right)$ 均可分解为 $x$ 的函数与 $y$ 的函数之积, 则称它为变量分离方程. 当 $X_1\left(x\right)Y_1\left(y\right)\neq0$ 时, 以 $X_1\left(x\right)Y_1\left(y\right)$ 除方程两端, 得 $$\frac{X\left(x\right)}{X_1\left(x\right)}dx+\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=0,$$ 它的通积分为 $$\int\frac{X\left(x\right)}{X_1\left(x\right)}dx+\int\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=C.$$ 此外还须补上不在通积分之内的特解 $x=a_i$($a_i$ 是 $X_1\left(x\right)=0$ 的根)与 $y=b_j$($b_j$ 是 $Y_1\left(y\right)=0$ 的根).

## 2.3 一阶线性方程

**一阶线性方程**

形如 $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$$ 的方程称为一阶线性方程, 其中 $p\left(x\right),q\left(x\right)$ 在区间 $I$ 上连续. 当 $q\left(x\right)\equiv0$ 时称为相应的齐次线性方程, 否则称为非齐次线性方程.

**齐次线性方程的通解**

对齐次线性方程 $$\frac{dy}{dx}+p\left(x\right)y=0,$$ 分离变量积分得通解 $$y=Ce^{-\int p\left(x\right)dx},$$ 其中任意常数 $C$ 可取零值, $C=0$ 对应特解 $y\equiv0$.

**非齐次线性方程的通解(积分因子法)**

以积分因子 $$\mu\left(x\right)=e^{\int p\left(x\right)dx}$$ 乘非齐次线性方程两端, 左端化为全微分 $$\frac{d}{dx}\left(e^{\int p\left(x\right)dx}y\right)=q\left(x\right)e^{\int p\left(x\right)dx}.$$ 积分得通解 $$y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C\right].$$

## 2.4 初等变换法

**齐次方程**

若一阶微分方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0$$ 中的 $P\left(x,y\right)$ 与 $Q\left(x,y\right)$ 是同次齐次函数, 即 $P\left(tx,ty\right)=t^mP\left(x,y\right),\ Q\left(tx,ty\right)=t^mQ\left(x,y\right)$, 则称它为齐次方程. 作变量替换 $y=ux$($u$ 为新未知函数), 方程化为关于 $u$ 与 $x$ 的变量分离方程.

**可化为齐次的方程**

对方程 $$\frac{dy}{dx}=\frac{ax+by+c}{mx+ny+l},$$ 当 $c,l$ 不全为零时, 若 $\Delta=an-bm\neq0$, 可由线性方程组 $a\alpha+b\beta+c=0,\ m\alpha+n\beta+l=0$ 定出 $\alpha,\beta$, 作平移变换 $x=\xi+\alpha,\ y=\eta+\beta$, 方程化为齐次方程 $\frac{d\eta}{d\xi}=\frac{a\xi+b\eta}{m\xi+n\eta}$; 再令 $\eta=u\xi$ 即化为变量分离方程.

**伯努利方程**

形如 $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)y^n$$ 的方程称为伯努利方程, 其中常数 $n\neq0,1$. 以 $\left(1-n\right)y^{-n}$ 乘方程两端, 再令 $z=y^{1-n}$, 方程化为关于 $z$ 的一阶线性方程 $$\frac{dz}{dx}+\left(1-n\right)p\left(x\right)z=\left(1-n\right)q\left(x\right).$$

**里卡蒂方程**

若一阶方程 $\frac{dy}{dx}=f\left(x,y\right)$ 的右端是关于 $y$ 的二次多项式, 即写成 $$\frac{dy}{dx}=p\left(x\right)y^2+q\left(x\right)y+r\left(x\right),$$ 则称它为里卡蒂方程, 其中 $p\left(x\right),q\left(x\right),r\left(x\right)$ 在区间上连续且 $p\left(x\right)$ 不恒为零.

## 2.5 积分因子法

**积分因子**

对方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0,$$ 若存在可微的非零函数 $\mu\left(x,y\right)$, 使乘过它之后的方程 $$\mu\left(x,y\right)P\left(x,y\right)dx+\mu\left(x,y\right)Q\left(x,y\right)dy=0$$ 成为恰当方程, 即满足 $$\frac{\partial}{\partial y}\left(\mu P\right)=\frac{\partial}{\partial x}\left(\mu Q\right),$$ 则称 $\mu\left(x,y\right)$ 为原方程的一个积分因子.

**定理 2.4**(只依赖于 $x$ 的积分因子)

方程有一个只依赖于 $x$ 的积分因子的充要条件是表达式 $$\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q}=G\left(x\right)$$ 只依赖于 $x$ 而与 $y$ 无关; 此时 $\mu\left(x\right)=e^{\int G\left(x\right)dx}$ 是方程的一个积分因子.

**定理 2.5**(只依赖于 $y$ 的积分因子)

方程有一个只依赖于 $y$ 的积分因子的充要条件是表达式 $$\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=H\left(y\right)$$ 只依赖于 $y$; 此时 $\mu\left(y\right)=e^{\int H\left(y\right)dy}$ 是方程的一个积分因子.

**定理 2.6**(积分因子与通积分的任意函数之积)

若 $\mu=\mu\left(x,y\right)$ 是方程的一个积分因子, 使得 $$\mu P\left(x,y\right)dx+\mu Q\left(x,y\right)dy=d\Phi\left(x,y\right),$$ 则 $\mu\left(x,y\right)g\left(\Phi\left(x,y\right)\right)$ 也是方程的一个积分因子, 其中 $g\left(\cdot\right)$ 是任一可微的非零函数.

## 3.1 皮卡存在唯一性定理

**利普希茨条件**

设函数 $f(x,y)$ 在区域 $D$ 内满足不等式 $|f(x,y_1)-f(x,y_2)|\le L|y_1-y_2|$, 其中常数 $L>0$, 则称函数 $f(x,y)$ 在区域 $D$ 内对 $y$ 满足利普希茨条件. 若 $f(x,y)$ 在凸区域 $D$ 内对 $y$ 有连续的偏微商, 则它在 $D$ 内对 $y$ 满足利普希茨条件.

**定理 3.1**(皮卡存在和唯一性定理)

设初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$, 其中 $f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续, 而且对 $y$ 满足利普希茨条件. 则 $(E)$ 在区间 $I=[x_0-h,x_0+h]$ 上有并且只有一个解, 其中常数 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{(x,y)\in R}|f(x,y)|$.

**定理 3.2**(奥斯古德条件下解的唯一性)

设函数 $f(x,y)$ 在区域 $G$ 内连续, 且满足不等式 $|f(x,y_1)-f(x,y_2)|\le F(|y_1-y_2|)$, 其中 $F(r)>0$ 是 $r>0$ 的连续函数, 而且瑕积分 $\int_0^{r_1}\dfrac{dr}{F(r)}=+\infty$($r_1>0$ 为常数), 则称 $f(x,y)$ 在 $G$ 内对 $y$ 满足奥斯古德条件; 此时微分方程 $\dfrac{dy}{dx}=f(x,y)$ 在 $G$ 内经过每一点的解都是唯一的.

**积分方程与初值问题的等价性**

初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 有解 $y=\varphi(x)$, 等价于积分方程 $y=y_0+\displaystyle\int_{x_0}^x f(t,y(t))\,dt$ 有解. 其皮卡序列为 $y_{n+1}(x)=y_0+\displaystyle\int_{x_0}^x f(t,y_n(t))\,dt$, 其中取 $y_0(x)=y_0$.

## 3.2 佩亚诺存在定理

**欧拉折线**

设微分方程 $\dfrac{dy}{dx}=f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续, $M$ 为 $|f(x,y)|$ 在 $R$ 上的一个上界, 令 $h=\min\left\{a,\dfrac{b}{M}\right\}$. 把区间 $[x_0-h,x_0+h]$ 等分为 $2n$ 份, 从初值点 $P_0(x_0,y_0)$ 出发, 在每一节点沿该处线素方向作直线段, 得到一条停留在角形区域 $|y-y_0|\le M|x-x_0|$ 内的连续折线 $y=\rho_n(x)$, 称为初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 的欧拉折线.

**定理 3.1**(皮卡存在和唯一性定理)

设初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$, 其中 $f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续且对 $y$ 满足利普希茨条件, 则 $(E)$ 在区间 $I=[x_0-h,x_0+h]$ 上有且只有一个解, 其中 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{(x,y)\in R}|f(x,y)|$.

**积分方程与初值问题的等价性**

初值问题 $(E)$ 有解等价于积分方程 $y=y_0+\displaystyle\int_{x_0}^x f(t,y(t))\,dt$ 有解.

**一致有界与等度连续**

设在区间 $I$ 上给定函数序列 $f_1(x),f_2(x),\cdots$. 若存在常数 $K>0$ 使 $|f_n(x)|<K$ 对一切 $n$ 成立, 则称该序列在 $I$ 上一致有界; 若对任意正数 $\varepsilon$, 存在 $\delta=\delta(\varepsilon)$, 使只要 $|x_1-x_2|<\delta$ 就有 $|f_n(x_1)-f_n(x_2)|<\varepsilon$ 对一切 $n$ 成立, 则称该序列在 $I$ 上等度连续.

**阿斯科利引理**

设函数序列在有限闭区间 $I$ 上一致有界且等度连续, 则可以选取它的一个子序列, 使该子序列在区间 $I$ 上一致收敛.

**引理 3.1**(欧拉序列的收敛子序列)

欧拉折线序列 $\{\rho_n(x)\}$ 在区间 $[x_0-h,x_0+h]$ 上一致有界且等度连续, 因而至少含有一个一致收敛的子序列.

**引理 3.2**(欧拉折线的积分关系式)

欧拉折线 $y=\rho_n(x)$ 在区间 $[x_0-h,x_0+h]$ 上满足 $\rho_n(x)=y_0+\displaystyle\int_{x_0}^x f(t,\rho_n(t))\,dt+\delta_n(x)$, 其中 $\lim\limits_{n\to\infty}\delta_n(x)=0$ 对 $|x-x_0|\le h$ 一致成立.

**定理 3.3**(佩亚诺存在定理)

设函数 $f(x,y)$ 在矩形区域 $R$ 内连续, 则初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 在区间 $[x_0-h,x_0+h]$ 上至少有一个解, 这里矩形区域 $R$ 和正数 $h$ 的定义同**定理 3.1**(皮卡存在和唯一性定理).

## 3.3 解的延伸

**定理 3.4**(解的延伸定理)

设微分方程 $\dfrac{dy}{dx}=f(x,y)$ 中函数 $f(x,y)$ 在开区域 $G$ 内连续, $P_0(x_0,y_0)$ 为 $G$ 内任一点, 则经过 $P_0$ 的任一条积分曲线将在区域 $G$ 内延伸到边界: 即对任何有界闭区域 $G_1$($P_0\in G_1\subset G$), 积分曲线将延伸到 $G_1$ 之外. 换言之, 若解 $y=y(x)$ 的最大存在区间为 $(\alpha,\beta)$, 则当 $\beta<+\infty$ 时 $(x,y(x))$ 趋于 $G$ 的边界(在 $G=\mathbb{R}^2$ 时即 $|y|\to+\infty$).

**推论**(局部利普希茨条件下解的存在唯一与延伸)

设 $f(x,y)$ 在区域 $G$ 内连续, 且对 $y$ 满足局部利普希茨条件(即 $G$ 内每一点都有一个含于 $G$ 的邻域, 使 $f$ 在其中对 $y$ 满足利普希茨条件), 则微分方程经过 $G$ 内任一点 $P_0$ 存在唯一的积分曲线, 并且它在 $G$ 内延伸到边界.

**定理 3.5**(条形区域上解的整体存在性)

设微分方程 $\dfrac{dy}{dx}=f(x,y)$ 的右端函数在条形区域 $S:\ \alpha<x<\beta,\ -\infty<y<+\infty$ 内连续, 且满足不等式 $|f(x,y)|\le A(x)|y|+B(x)$, 其中 $A(x)\ge0$ 与 $B(x)\ge0$ 在 $(\alpha,\beta)$ 上连续, 则微分方程的每一个解都以区间 $(\alpha,\beta)$ 为最大存在区间.

## 3.4 比较定理及其应用

**定理 3.1**(皮卡存在和唯一性定理)

设初值问题 $(E)$: $\dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$, 其中 $f(x,y)$ 在矩形区域 $R:\ |x-x_0|\le a,\ |y-y_0|\le b$ 内连续, 则 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M=\max\limits_{(x,y)\in R}|f(x,y)|$.

**定理 3.6**(第一比较定理)

设函数 $f(x,y)$ 与 $F(x,y)$ 都在平面区域 $G$ 内连续且满足不等式 $f(x,y)<F(x,y)$($(x,y)\in G$); 又设 $y=\varphi(x)$ 与 $y=\Phi(x)$ 在区间 $(a,b)$ 上分别是初值问题 $(E_1):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 与 $(E_2):\ \dfrac{dy}{dx}=F(x,y),\ y(x_0)=y_0$ 的解, 其中 $(x_0,y_0)\in G$. 则 $\varphi(x)<\Phi(x)$ 于 $(x_0,b)$, 而 $\varphi(x)>\Phi(x)$ 于 $(a,x_0)$. 其几何意义是: 斜率小的曲线向右不可能从斜率大的曲线下方穿越到上方.

**最小解与最大解**

设初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 在矩形区域 $R$ 内连续, 若在区间 $[x_0-h,x_0+h]$ 上有两个解 $y=W(x)$ 与 $y=Z(x)$, 使 $(E)$ 的任何解 $y=y(x)$ 都满足 $W(x)\le y(x)\le Z(x)$, 则称 $y=W(x)$ 与 $y=Z(x)$ 分别为 $(E)$ 的最小解与最大解.

**定理 3.7**(最小解与最大解的存在性)

存在正数 $\delta<h$, 使初值问题 $(E)$ 在区间 $[x_0-\delta,x_0+\delta]$ 上有最小解和最大解. 构造方法: 对 $\varepsilon>0$, 考虑 $(E_\varepsilon):\ \dfrac{dy}{dx}=f(x,y)\pm\varepsilon$, 由**定理 3.3**(佩亚诺存在定理)取其解并利用**阿斯科利引理**取极限, 即得最小解与最大解.

**定理 3.8**(第二比较定理)

设函数 $f(x,y)$ 与 $F(x,y)$ 都在平面区域 $G$ 内连续且满足 $f(x,y)\le F(x,y)$; 又设 $y=\varphi(x)$ 与 $y=\Phi(x)$ 在 $(a,b)$ 上分别是 $(E_1):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 与 $(E_2):\ \dfrac{dy}{dx}=F(x,y),\ y(x_0)=y_0$ 的解, 其中 $y=\varphi(x)$ 是 $(E_1)$ 的右行最小解和左行最大解, $y=\Phi(x)$ 是 $(E_2)$ 的右行最大解和左行最小解. 则 $\varphi(x)\le\Phi(x)$ 于 $[x_0,b)$, 而 $\varphi(x)\ge\Phi(x)$ 于 $(a,x_0]$.

**定理 3.3**(佩亚诺存在定理)

设函数 $f(x,y)$ 在矩形区域 $R$ 内连续, 则初值问题 $(E):\ \dfrac{dy}{dx}=f(x,y),\ y(x_0)=y_0$ 在区间 $[x_0-h,x_0+h]$ 上至少有一个解.

**定理 3.4**(解的延伸定理)

设 $f(x,y)$ 在开区域 $G$ 内连续, 则经过 $G$ 内任一点的积分曲线在 $G$ 内延伸到边界.

## 4.1 一阶隐式微分方程

**一阶隐式微分方程**

作为对第二章初等积分法的补充, 本节讨论一阶隐式方程 $$F\left(x,y,\frac{dy}{dx}\right)=0$$ 的几个特殊解法. 这里隐式的含义, 是指在方程中未知函数的微商 $\frac{dy}{dx}$ 没有预先表示为 $x,y$ 的显函数.

**微分法**

设从一阶隐式方程中可显式解出未知函数 $$y=f(x,p),$$ 其中 $p=\frac{dy}{dx}$. 设函数 $f(x,p)$ 对 $(x,p)$ 连续可微, 则由上式对 $x$ 进行微分, 得到 $$\left[f_x(x,p)-p\right]dx+f_p(x,p)dp=0.$$ 这是关于变量 $x$ 和 $p$ 的一阶显式微分方程. 若能求得其通解 $p=u(x,C)$, 则原方程的通解为 $y=f(x,u(x,C))$; 若其通解易写成 $x=v(p,C)$ 的形式, 则原方程的通解可写成 $$\begin{cases}x=v(p,C),\\y=f(v(p,C),p),\end{cases}$$ 其中 $p$ 视作参变量.

**参数法**

设微分方程不明显包含自变量, 即 $$F(y,p)=0.$$ 作为 $y$ 和 $p$ 之间的联系, 在 $Oyp$ 平面上它一般表示若干条曲线. 设 $$y=g(t),\qquad p=h(t)$$ 是其中一条的参数表示, 其中设 $h(t)\neq0$. 由 $dy=p\,dx$ 可得 $dx=\frac{g'(t)}{h(t)}dt$, 再积分得原方程的通解 $$x=\int\frac{g'(t)}{h(t)}dt+C,\qquad y=g(t).$$ 同理, 对不明显包含未知函数的方程 $F(x,p)=0$, 可取参数表示 $x=f(t),\ p=h(t)$, 则由 $dy=p\,dx$ 得 $dy=h(t)f'(t)dt$, 通解为 $$y=\int h(t)f'(t)dt+C,\qquad x=f(t).$$

## 4.2 奇解

**定义 4.1**(奇解)

设一阶微分方程 $$F\left(x,y,\frac{dy}{dx}\right)=0$$ 有特解 $\Gamma:y=\varphi(x)$($x\in J$). 如果对每一点 $Q\in\Gamma$, 在 $Q$ 点的任何邻域内该方程有一个不同于 $\Gamma$ 的解在 $Q$ 点与 $\Gamma$ 相切, 则称 $\Gamma$ 是该微分方程的奇解.

**定理 4.1**(奇解的必要条件即 $p$-判别式)

设函数 $F(x,y,p)$ 对 $(x,y,p)\in G$ 是连续的, 而且对 $y$ 和 $p$ 有连续的偏微商 $F_y'$ 和 $F_p'$. 若函数 $y=\varphi(x)$($x\in J$)是微分方程的一个奇解, 并且 $(x,\varphi(x),\varphi'(x))\in G$, 则奇解 $y=\varphi(x)$ 满足 $p$-判别式 $$\begin{cases}F(x,y,p)=0,\\F_p'(x,y,p)=0,\end{cases}\qquad\left(p=\frac{dy}{dx}\right).$$ 从 $p$-判别式中消去 $p$ 所得方程所决定的曲线称为 $p$-判别曲线. 奇解必是一条 $p$-判别曲线. 但须注意, 由 $p$-判别式确定的函数不一定是解, 即使是解也不一定是奇解, 仍须按**定义 4.1**(奇解)经过验证.

**定理 4.2**(奇解的充分条件)

设函数 $F(x,y,p)$ 对 $(x,y,p)\in G$ 是二阶连续可微的. 又设由 $p$-判别式消去 $p$ 后得到的函数 $y=\psi(x)$($x\in J$)是微分方程的解, 而且条件 $$F_y'(x,\psi(x),\psi'(x))\neq0,\qquad F_{pp}''(x,\psi(x),\psi'(x))\neq0$$ 以及 $$F_p'(x,\psi(x),\psi'(x))=0$$ 对 $x\in J$ 成立, 则 $y=\psi(x)$ 是微分方程的奇解.

## 4.3 包络

**定义 4.2**(包络)

设在平面上有一条连续可微的曲线 $\Gamma$. 如果对于任一点 $q\in\Gamma$, 在单参数曲线族 $K(C):V(x,y,C)=0$ 中都有一条曲线 $K(C^*)$ 通过 $q$ 点并在该点与 $\Gamma$ 相切, 而且 $K(C^*)$ 在 $q$ 点的任一邻域内不同于 $\Gamma$, 则称曲线 $\Gamma$ 为该曲线族的一支包络.

**定理 4.3**(包络是奇解)

设微分方程 $F(x,y,\frac{dy}{dx})=0$ 有通积分 $U(x,y,C)=0$, 又设该积分曲线族有包络 $\Gamma:y=\varphi(x)$($x\in J$), 则包络 $y=\varphi(x)$ 是该微分方程的奇解. 因此, 求微分方程的奇解归结到求它的通积分的包络.

**定理 4.4**(包络满足 $C$-判别式)

设 $\Gamma$ 是曲线族 $K(C):V(x,y,C)=0$ 的一支包络, 并且它可表示为参数 $C$ 的光滑曲线, 则它满足 $C$-判别式 $$\begin{cases}V(x,y,C)=0,\\V_C'(x,y,C)=0,\end{cases}$$ 或消去 $C$ 后所得关系式 $\Omega(x,y)=0$.

**定理 4.5**($C$-判别式是包络的充分条件)

设由曲线族 $K(C):V(x,y,C)=0$ 的 $C$-判别式确定一支连续可微且不含于该曲线族的曲线 $$\Lambda:\begin{cases}x=\varphi(C),\\y=\psi(C),\end{cases}\qquad(C\in J),$$ 而且它满足非退化性条件 $$(\varphi'(C),\psi'(C))\neq(0,0),\qquad(V_x',V_y')\neq(0,0),$$ 则 $\Lambda$ 是该曲线族的一支包络.

## 5.1 几个例子

**自治(驻定)微分方程**

有一类微分方程不明显包含自变量, 这类方程叫作自治(或驻定)的微分方程. 对它们可以进行降阶. 例如对二阶自治方程 $y''=f\left(y,y'\right)$, 令 $z=\dfrac{dy}{dx}$, 则有 $y''=\dfrac{dz}{dx}=\dfrac{dz}{dy}\cdot\dfrac{dy}{dx}=z\dfrac{dz}{dy}$, 从而降为关于 $z=z\left(y\right)$ 的一阶方程 $z\dfrac{dz}{dy}=f\left(y,z\right)$.

**首次积分**

由高阶微分方程积分一次(因而包含一个任意常数)所得的关系式称为首次积分. 例如对自治方程 $y''=f\left(y,y'\right)$, 以 $y'$ 乘方程后左端恰为全微分 $\dfrac{d}{dx}\left[\dfrac{1}{2}\left(y'\right)^2-F\left(y\right)\right]$, 其中 $F'\left(y\right)=-f\left(y,0\right)$ 的相应原函数, 直接积分即得首次积分.

**相平面, 轨线与相图**

对于二阶自治方程 $\dfrac{d^2x}{dt^2}=f\left(x,\dfrac{dx}{dt}\right)$, 在相平面 $O\left(x,v\right)$($v=\dfrac{dx}{dt}$)上, 由首次积分 $\dfrac{1}{2}v^2+V\left(x\right)=E$ 确定的曲线称为轨线; 轨线在相平面上的分布图称为相图. 静止点对应于方程的零解(平凡解), 封闭轨线表示周期运动.

**单摆方程与线性单摆方程**

单摆的运动方程为 $\dfrac{d^2\theta}{dt^2}+a^2\sin\theta=0$, 其中常数 $a=\sqrt{\dfrac{g}{l}}$, $g$ 为重力加速度大小, $l$ 为摆长. 取 $\sin\theta$ 的一次近似 $\sin\theta\approx\theta$, 得线性单摆方程 $\dfrac{d^2\theta}{dt^2}+a^2\theta=0$, 其通解为 $\theta=A\sin\left(at+D\right)$, 其中 $A,D$ 为任意常数, 振动周期为 $T=\dfrac{2\pi}{a}=2\pi\sqrt{\dfrac{l}{g}}$.

## 5.2 n维线性空间中的微分方程

**标准微分方程组与向量形式**

把未知函数的个数取成等于微分方程的阶数, 所得标准方程组为 $\dfrac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$($i=1,\cdots,n$). 采用列向量 $y=\left(y_1,\cdots,y_n\right)^T$, $f=\left(f_1,\cdots,f_n\right)^T$, 则向量形式为 $\dfrac{dy}{dx}=f\left(x,y\right)$, 其中 $f\left(x,y\right)$ 在区域 $D\subset R^{n+1}$ 上连续. 附加初值条件 $y\left(x_0\right)=y_0$ 即得柯西问题.

**向量的模(范数)及其基本性质**

在 $n$ 维线性空间 $R^n$ 中可定义向量的模 $\left|y\right|$, 例如欧几里得模 $\left|y\right|=\sqrt{y_1^2+\cdots+y_n^2}$. 模的基本性质: 对任何 $y,z\in R^n$, 有三角不等式 $\left|y+z\right|\le\left|y\right|+\left|z\right|$. 在引进模以后, $R^n$ 成为 $n$ 维赋范线性空间, 其中可建立相应的微积分学与一致收敛等概念.

**利普希茨条件**

设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 如果存在常数 $L\ge0$, 使对一切 $\left(x,y_1\right),\left(x,y_2\right)\in R$ 都有 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, 则称 $f$ 在 $R$ 上对 $y$ 满足利普希茨条件.

**皮卡存在唯一性定理($n$ 维向量形式)**

设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 且对 $y$ 满足利普希茨条件. 令 $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\dfrac{b}{M}\right\}$, 则柯西问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left|x-x_0\right|\le h$ 上存在唯一解.

**佩亚诺存在定理($n$ 维向量形式)**

设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 令 $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\dfrac{b}{M}\right\}$, 则柯西问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left|x-x_0\right|\le h$ 上至少存在一个解(不保证唯一性).

**皮卡序列及其一致收敛估计**

与柯西问题等价的积分方程为 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. 作皮卡序列 $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. 归纳可证 $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\dfrac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$, 它蕴涵皮卡序列在 $\left|x-x_0\right|\le h$ 上一致收敛.

**阿斯科利引理与格朗沃尔不等式**

阿斯科利引理: 有界闭区间上一致有界且等度连续的函数列必有一致收敛的子列. 格朗沃尔不等式: 若非负连续函数 $u\left(x\right)$ 满足 $u\left(x\right)\le A+L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$, 则 $u\left(x\right)\le Ae^{L\left|x-x_0\right|}$.

**魏尔斯特拉斯判别法(一致收敛)**

若函数项级数 $\displaystyle\sum_{k=0}^{\infty}u_k\left(x\right)$ 的通项满足 $\left|u_k\left(x\right)\right|\le M_k$ 对一切 $x$ 成立, 且数项级数 $\displaystyle\sum_{k=0}^{\infty}M_k$ 收敛, 则函数项级数在相应区间上一致收敛.

## 5.3 解对初值和参数的连续依赖性

**定理 5.1**(解对参数的连续依赖性)

设 $n$ 维向量值函数 $f\left(x,y,\lambda\right)$ 在区域 $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ 上连续, 且对 $y$ 满足利普希茨条件 $\left|f\left(x,y_1,\lambda\right)-f\left(x,y_2,\lambda\right)\right|\le L\left|y_1-y_2\right|$. 令 $M$ 为 $\left|f\left(x,y,\lambda\right)\right|$ 在 $G$ 上的一个上界, $h=\min\left\{a,\dfrac{b}{M}\right\}$, 则初值问题 $\dfrac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ 的解 $y=\varphi\left(x,\lambda\right)$ 在区域 $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$ 上是连续的.

**定理 5.1 的推论**(解对初值的连续依赖性)

设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 且对 $y$ 满足利普希茨条件, 则柯西问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ 的解 $y=\varphi\left(x,\eta\right)$ 在区域 $Q:\left|x-x_0\right|\le\dfrac{h}{2},\ \left|\eta-y_0\right|\le\dfrac{b}{2}$ 上连续, 其中 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M$ 为 $\left|f\left(x,y\right)\right|$ 在 $R$ 上的一个上界.

**定理 5.2**(解对初值的大范围连续依赖性)

设 $n$ 维向量值函数 $f\left(x,y\right)$ 在开区域 $G$ 上连续, 且对 $y$ 满足局部利普希茨条件. 假设 $y=\xi\left(x\right)$ 是 $\dfrac{dy}{dx}=f\left(x,y\right)$ 的一个解, 存在区间为 $J$. 任取有界闭区间 $\left[a,b\right]\subset J$, 则存在常数 $\delta>0$, 使对任何初值 $\left(x_0,y_0\right)$ 满足 $a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$, 柯西问题的解 $y=\varphi\left(x;x_0,y_0\right)$ 至少在 $\left[a,b\right]$ 上存在, 且在闭区域 $D_\delta:a\le x\le b,\ a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$ 上连续.

**积分方程与柯西问题的等价性**

柯西问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 等价于积分方程 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. 当近似解序列一致收敛且 $f$ 连续时, 可在积分号下取极限.

**阿斯科利引理**

有界闭区间上一致有界且等度连续的函数列, 必有一致收敛的子列.

## 5.4 解对初值和参数的连续可微性

**定理 5.3**(解对参数的连续可微性)

设 $n$ 维向量值函数 $f\left(x,y,\lambda\right)$ 在区域 $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ 上连续, 而且对 $y$ 和 $\lambda$ 有连续的偏微商, 则初值问题 $\dfrac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ 的解 $y=\varphi\left(x,\lambda\right)$ 在区域 $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$ 上是连续可微的, 其中 $h=\min\left\{a,\dfrac{b}{M}\right\}$, $M$ 为 $\left|f\left(x,y,\lambda\right)\right|$ 在 $G$ 上的一个上界.

**定理 5.3 的推论**(解对初值的连续可微性)

设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 而且对 $y$ 有连续的偏微商 $f_y\left(x,y\right)$, 则初值问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ 的解 $y=\varphi\left(x,\eta\right)$ 在区域 $D:\left|x-x_0\right|\le\dfrac{h}{2},\ \left|\eta-y_0\right|\le\dfrac{b}{2}$ 上是连续可微的.

**变分方程**

设 $y=\varphi\left(x;x_0,y_0,\lambda\right)$ 是 $\dfrac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(x_0\right)=y_0$ 的解. 与柯西问题等价的积分方程为 $\varphi\left(x;x_0,y_0,\lambda\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(s,\varphi\left(s;x_0,y_0,\lambda\right),\lambda\right)ds$. 记 $A\left(x,x_0,y_0,\lambda\right)=\dfrac{\partial f}{\partial y}\left(x,\varphi,\lambda\right)$, $B\left(x,x_0,y_0,\lambda\right)=\dfrac{\partial f}{\partial\lambda}\left(x,\varphi,\lambda\right)$. 则 $z=\dfrac{\partial\varphi}{\partial\lambda}$ 满足 $\dfrac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z+B\left(x,x_0,y_0,\lambda\right)$, $z\left(x_0\right)=0$; $z=\dfrac{\partial\varphi}{\partial y_0}$ 满足 $\dfrac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=1$; $z=\dfrac{\partial\varphi}{\partial x_0}$ 满足 $\dfrac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=-f\left(x_0,y_0,\lambda\right)$. 这些方程统称为原方程关于初值和参数的变分方程.

**雅可比矩阵**

向量值函数 $f\left(x,y,\lambda\right)=\left(f_1,\cdots,f_n\right)^T$ 对 $y=\left(y_1,\cdots,y_n\right)^T$ 的雅可比矩阵为 $f_y=\left(\dfrac{\partial f_i}{\partial y_j}\right)_{n\times n}$, 对参数 $\lambda=\left(\lambda_1,\cdots,\lambda_m\right)^T$ 的雅可比矩阵为 $f_\lambda=\left(\dfrac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. 复合函数求导按矩阵乘法进行: $\dfrac{\partial f\left(x,\varphi,\lambda\right)}{\partial\lambda_k}=\displaystyle\sum_{j=1}^{n}\dfrac{\partial f}{\partial y_j}\dfrac{\partial\varphi_j}{\partial\lambda_k}+\dfrac{\partial f}{\partial\lambda_k}$.

## 6.1 一般理论

**存在和唯一性定理**(线性微分方程组初值问题)

线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 满足初值条件 $y\left(x_0\right)=y_0$ 的解 $y=y\left(x\right)$ 在区间 $\left(a,b\right)$ 上是存在和唯一的, 其中 $x_0\in\left(a,b\right)$ 和 $y_0\in\mathbb{R}^n$ 是任意给定的.

**引理 6.1**(齐次线性方程组解的叠加原理)

设 $y=y_1\left(x\right)$ 和 $y=y_2\left(x\right)$ 是齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 的解, 则它们的线性组合 $y=C_1y_1\left(x\right)+C_2y_2\left(x\right)$ 也是该方程组的解, 其中 $C_1$ 和 $C_2$ 是任意常数.

**引理 6.2**(齐次线性方程组解空间的维数)

齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 在区间 $\left(a,b\right)$ 上所有解组成的线性空间 $S$ 是 $n$ 维的, 其中 $n$ 是微分方程组的阶数.

**定理 6.1**(齐次线性微分方程组的通解结构)

齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 在区间 $\left(a,b\right)$ 上有 $n$ 个线性无关的解 $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$, 而且它的通解为 $y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right)$, 其中 $C_1,C_2,\cdots,C_n$ 是任意常数. 通常称齐次线性微分方程组的 $n$ 个线性无关的解为一个基本解组.

**引理 6.3**(朗斯基行列式的刘维尔公式)

设 $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ 是齐次线性微分方程组的 $n$ 个解, 其朗斯基行列式为 $W\left(x\right)$, 则 $$W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^{x}\mathrm{tr}\left[A\left(s\right)\right]ds},$$ 其中 $x_0\in\left(a,b\right)$, 而 $\mathrm{tr}\left[A\left(x\right)\right]$ 表示矩阵 $A\left(x\right)$ 的迹.

**定理 6.2**(朗斯基行列式判别法)

齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 的解组 $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ 是线性无关的充要条件为 $W\left(x\right)\neq0\ \left(a<x<b\right)$.

**推论 2**(基解矩阵的性质)

(1) 设 $\Phi\left(x\right)$ 是齐次线性微分方程组的一个基解矩阵, 则对于任一个非奇异的 $n$ 阶常数矩阵 $C$, 矩阵 $\Phi\left(x\right)C$ 也是该方程组的一个基解矩阵; (2) 设 $\Phi\left(x\right)$ 和 $\Psi\left(x\right)$ 都是该方程组的基解矩阵, 则必存在一个非奇异的 $n$ 阶常数矩阵 $C$, 使得 $\Psi\left(x\right)=\Phi\left(x\right)C$.

**引理 6.4**(非齐次线性方程组解的结构)

如果 $\Phi\left(x\right)$ 是与非齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 相应的齐次线性微分方程组的一个基解矩阵, $y^*\left(x\right)$ 是非齐次方程组的一个特解, 则非齐次方程组的任一解 $y=\varphi\left(x\right)$ 可以表示为 $\varphi\left(x\right)=\Phi\left(x\right)c+y^*\left(x\right)$, 其中 $c$ 是一个与 $\varphi\left(x\right)$ 有关的常数列向量.

**定理 6.3**(非齐次线性微分方程组的通解结构)

设 $\Phi\left(x\right)$ 是相应齐次线性微分方程组的一个基解矩阵, 则非齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 在区间 $\left(a,b\right)$ 上的通解可以表示为 $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^{x}\Phi^{-1}\left(s\right)f\left(s\right)ds$, 其中 $c$ 是 $n$ 维的任意常数列向量.

## 6.2 常系数线性微分方程组

**命题 1**(矩阵幂级数的绝对收敛性与矩阵指数函数的定义)

对 $n$ 阶实常数矩阵 $A$, 矩阵幂级数 $$E+A+\frac{1}{2!}A^2+\cdots+\frac{1}{k!}A^k+\cdots$$ 是绝对收敛的, 其和记为 $$e^A=\sum_{k=0}^{\infty}\frac{1}{k!}A^k,$$ 并称它为矩阵 $A$ 的指数函数, 其中 $E$ 为 $n$ 阶单位矩阵.

**命题 2**(矩阵指数函数的性质)

矩阵指数函数有如下性质: (1) 若矩阵 $A$ 与 $B$ 可交换(即 $AB=BA$), 则 $$e^{A+B}=e^A e^B;$$

(2) 对任何矩阵 $A$, 指数函数 $e^A$ 是可逆的, 且 $$(e^A)^{-1}=e^{-A};$$

(3) 若 $P$ 是一个非奇异的 $n$ 阶矩阵, 则 $$e^{PAP^{-1}}=Pe^AP^{-1}.$$

**定理 6.4**(矩阵指数函数是常系数齐次线性微分方程组的标准基解矩阵)

矩阵指数函数 $$\Phi(x)=e^{xA}$$ 是常系数齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$$ 的一个标准基解矩阵(即基解矩阵 $\Phi(x)$ 满足 $\Phi(0)=E$).

**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解)

常系数非齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$$ 在区间 $(a,b)$ 上的通解为 $$\boldsymbol{y}=e^{xA}\boldsymbol{c}+\int_{x_0}^{x}e^{(x-s)A}\boldsymbol{f}(s)\,ds,$$ 其中 $c$ 为任意的常数列向量; 而该方程组满足初值条件 $y(x_0)=y_0$ 的解为 $$\boldsymbol{y}=e^{(x-x_0)A}\boldsymbol{y}_0+\int_{x_0}^{x}e^{(x-s)A}\boldsymbol{f}(s)\,ds,$$ 其中 $x_0\in(a,b)$.

**引理 6.6**(方程组有指数型非零解的充要条件)

常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有非零解 $y=e^{\lambda x}r$, 当且仅当 $\lambda$ 是矩阵 $A$ 的特征根, 而 $\boldsymbol{r}$ 是与 $\lambda$ 相应的特征向量, 即 $\boldsymbol{r}$ 满足齐次线性代数方程组 $(A-\lambda E)\boldsymbol{r}=\boldsymbol{0}$.

**定理 6.5**($n$ 个互不相同特征根时的基解矩阵)

设 $n$ 阶矩阵 $A$ 有 $n$ 个互不相同的特征根 $\lambda_1,\lambda_2,\cdots,\lambda_n$, 则矩阵函数 $$\Phi(x)=\left(e^{\lambda_1 x}\boldsymbol{r}_1,e^{\lambda_2 x}\boldsymbol{r}_2,\cdots,e^{\lambda_n x}\boldsymbol{r}_n\right)$$ 是方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的一个基解矩阵, 其中 $r_i$ 是 $A$ 的与 $\lambda_i$ 相应的特征向量.

**引理 6.7**(重特征根时确定向量多项式系数的方法)

设 $\lambda_i$ 是矩阵 $A$ 的 $n_i$ 重特征根, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{(n_i-1)!}\boldsymbol{r}_{n_i-1}\right)$$ 的非零解的充要条件是: $r_0$ 是齐次线性代数方程组 $(A-\lambda_i E)^{n_i}\boldsymbol{r}=\boldsymbol{0}$ 的一个非零解, 而且 $r_1,r_2,\cdots,r_{n_i-1}$ 由下面的关系式逐次确定 $$\boldsymbol{r}_1=(A-\lambda_i E)\boldsymbol{r}_0,\ \boldsymbol{r}_2=(A-\lambda_i E)\boldsymbol{r}_1,\ \cdots,\ \boldsymbol{r}_{n_i-1}=(A-\lambda_i E)\boldsymbol{r}_{n_i-2}.$$

**定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵)

设 $n$ 阶实值常数矩阵 $A$ 在复域中互不相同的特征根是 $\lambda_1,\lambda_2,\cdots,\lambda_s$, 相应的重数分别为 $n_1,n_2,\cdots,n_s$, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的任一解都是形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{(n_i-1)!}\boldsymbol{r}_{n_i-1}\right)$$ 的向量函数的线性组合, 其中 $i=1,2,\cdots,s$.

**附注 2**(从复值解提取实值解的方法)

设方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有一个复值解 $\boldsymbol{y}_1=\boldsymbol{u}(x)+i\boldsymbol{v}(x)$, 其中 $A$ 为实矩阵, 则 $\boldsymbol{y}_1$ 的共轭 $\boldsymbol{y}_2=\boldsymbol{u}(x)-i\boldsymbol{v}(x)$ 也是方程组的复值解, 从而 $\boldsymbol{y}_1$ 的实部 $\boldsymbol{u}(x)$ 和虚部 $\boldsymbol{v}(x)$ 都是方程组的实值解, 即由一对共轭的复值解可以得到两个实值解.

## 6.3 高阶线性微分方程

**定理 6.1***(齐次线性微分方程解的结构)

齐次线性微分方程 (6.47) 在区间 $(a,b)$ 上存在 $n$ 个线性无关的解. 如果这 $n$ 个线性无关的解如 $\varphi_1(x),\varphi_2(x),\cdots,\varphi_n(x)$ 所示, 则方程 (6.47) 的通解为 $$y=C_1\varphi_1(x)+C_2\varphi_2(x)+\cdots+C_n\varphi_n(x),$$ 其中 $C_1,C_2,\cdots,C_n$ 为任意常数. 这 $n$ 个线性无关的解称为一个基本解组.

**定理 6.2***(解组线性无关的朗斯基行列式判据)

方程 (6.47) 的解组 $\varphi_1(x),\cdots,\varphi_n(x)$ 是线性无关的充要条件为它的朗斯基行列式 $$W(x)=\left|\begin{matrix}\varphi_1(x)&\cdots&\varphi_n(x)\\\varphi_1'(x)&\cdots&\varphi_n'(x)\\\vdots&&\vdots\\\varphi_1^{(n-1)}(x)&\cdots&\varphi_n^{(n-1)}(x)\end{matrix}\right|$$ 在区间 $(a,b)$ 上恒不为零.

**刘维尔公式**(朗斯基行列式的演化公式 (6.54))

若 $\varphi_1(x),\cdots,\varphi_n(x)$ 是方程 (6.47) 的解组, 其朗斯基行列式为 $W(x)$, 则 $$W(x)=W(x_0)e^{-\int_{x_0}^{x}a_1(s)ds}\qquad(a<x<b),$$ 其中 $x_0\in(a,b)$, 而 $a_1(x)$ 是方程 (6.47) 中 $y^{(n-1)}$ 项的系数. 特别地, 对二阶方程 $y''+p(x)y'+q(x)y=0$ 有 $a_1(x)=p(x)$.

**例 1**(由一个非零解构造通解的公式 (6.56))

设 $y=\varphi(x)$ 是二阶齐次线性微分方程 $y''+p(x)y'+q(x)y=0$ 的一个非零解, 其中 $p(x)$ 和 $q(x)$ 是区间 $(a,b)$ 上的连续函数, 则在 $\varphi(x)\neq0$ 的子区间上方程的通解为 $$y=\varphi(x)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2(s)}e^{-\int_{x_0}^{s}p(t)dt}ds\right],$$ 其中 $C_1$ 和 $C_2$ 为任意常数.

**定理 6.3***(非齐次线性微分方程的通解结构与常数变易公式 (6.57)(6.58))

设 $\varphi_1(x),\cdots,\varphi_n(x)$ 是齐次线性微分方程 (6.47) 在区间 $(a,b)$ 上的一个基本解组, 则非齐次线性微分方程 (6.46) 的通解为 $$y=C_1\varphi_1(x)+\cdots+C_n\varphi_n(x)+\varphi^*(x),$$ 其中 $$\varphi^*(x)=\sum_{k=1}^{n}\varphi_k(x)\int_{x_0}^{x}\frac{W_k(s)}{W(s)}f(s)ds$$ 是方程 (6.46) 的一个特解, $W(x)$ 是基本解组的朗斯基行列式, 而 $W_k(x)$ 是 $W(x)$ 中第 $n$ 行第 $k$ 列元素的代数余子式.

**定理 6.6***(常系数齐次线性微分方程的特征根解法)

常系数齐次线性微分方程 $y^{(n)}+a_1y^{(n-1)}+\cdots+a_ny=0$ 的特征方程为 $$\lambda^n+a_1\lambda^{n-1}+\cdots+a_{n-1}\lambda+a_n=0.$$ 设特征方程在复数域中共有 $s$ 个互不相同的根 $\lambda_1,\cdots,\lambda_s$, 相应重数分别为 $n_1,\cdots,n_s$, 则函数组 $e^{\lambda_kx},\ xe^{\lambda_kx},\ \cdots,\ x^{n_k-1}e^{\lambda_kx}\ (k=1,\cdots,s)$ 是一个基本解组. 复根成对共轭出现, 取复值解的实部和虚部即得相应的实值解.

**待定系数法**(对特殊非齐次项预先设定特解形式)

当非齐次项为 $f(x)=P_m(x)e^{\mu x}$(其中 $P_m(x)$ 是 $m$ 次多项式) 时, 若 $\mu$ 不是特征根, 设特解 $\varphi^*(x)=Q_m(x)e^{\mu x}$; 若 $\mu$ 是 $k$ 重特征根, 则设 $$\varphi^*(x)=x^kQ_m(x)e^{\mu x},$$ 其中 $Q_m(x)$ 是系数待定的 $m$ 次多项式. 当非齐次项为 $f(x)=\left[A_m(x)\cos\beta x+B_l(x)\sin\beta x\right]e^{\alpha x}$ 时, 设 $$\varphi^*(x)=x^k\left[C_n(x)\cos\beta x+D_n(x)\sin\beta x\right]e^{\alpha x},$$ 其中 $k$ 是 $\alpha\pm i\beta$ 作为特征根的重数 (不是特征根时取 $k=0$), $n=\max\{m,l\}$, 多项式 $C_n(x),D_n(x)$ 的系数待定.

**初值问题解的存在唯一性**

$n$ 阶线性微分方程满足初值条件 $y(x_0)=y_0,\ y'(x_0)=y_0',\ \cdots,\ y^{(n-1)}(x_0)=y_0^{(n-1)}$ 的解在系数与非齐次项的公共连续区间上存在而且唯一. 特别地, 初值条件全取零的初值问题只有零解.

## 7.1 柯西定理

**优级数与优函数**

假设有两个幂级数 $\sum_{i,j=0}^{\infty}a_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j$ 和 $\sum_{i,j=0}^{\infty}A_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j\ \left(A_{ij}\ge0\right)$, 其中系数 $a_{ij}$ 和 $A_{ij}$ 满足不等式 $\left|a_{ij}\right|\le A_{ij}\ \left(i,j=0,1,2,\cdots\right)$, 则称第二个幂级数是第一个的一个优级数(或强级数). 如果该优级数在区域 $D:\left|x-x_0\right|<\alpha,\ \left|y-y_0\right|<\beta$ 内又是收敛的, 则它的和函数 $F\left(x,y\right)$ 叫作原幂级数在 $D$ 内的一个优函数(或强函数).

**定理 7.1**(柯西定理)

如果函数 $f\left(x,y\right)$ 在矩形区域 $R:\left|x-x_0\right|<\alpha,\ \left|y-y_0\right|<\beta$ 上可以展开成 $\left(x-x_0\right)$ 和 $\left(y-y_0\right)$ 的一个收敛的幂级数, 则初值问题 $\dfrac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在 $x_0$ 点的邻域 $\left(x_0-\rho,x_0+\rho\right)$ 内有一个解析解 $y=y\left(x\right)$, 而且它是唯一的. 此处形式解的系数 $C_n=\dfrac{1}{n!}y^{\left(n\right)}\left(x_0\right)=P_n\left(a_{00},a_{01},a_{10},\cdots,a_{n-1,0}\right)$, 其中 $P_n$ 是关于各系数的正系数多项式, 只与标号 $n$ 有关而与函数 $f$ 无关.

**附注 3**(优级数方法对微分方程组的应用)

优级数方法可以应用于微分方程组的情形. 考虑微分方程组的初值问题 $\dfrac{dy_k}{dx}=f_k\left(x,y_1,\cdots,y_n\right),\ y_k\left(0\right)=0\ \left(k=1,2,\cdots,n\right)$. 假设右端函数在区域 $\left|x\right|\le\alpha,\ \left|y_1\right|\le\beta,\ \cdots,\ \left|y_n\right|\le\beta$ 内可以展成收敛的幂级数, 则与引理 7.1 类似可证存在优函数, 再用与定理 7.1 同样的推理可知该初值问题在 $x=0$ 的某邻域内有收敛的幂级数解.

## 7.2 幂级数解法

**常点与奇点**

考虑二阶齐次线性微分方程 $A\left(x\right)y''+B\left(x\right)y'+C\left(x\right)y=0$. 如果 $A\left(x_0\right)\neq0$, 则在 $x_0$ 点附近 $A\left(x\right)\neq0$, 方程可写成 $y''+p\left(x\right)y'+q\left(x\right)y=0$, 其中 $p\left(x\right)=B\left(x\right)/A\left(x\right),\ q\left(x\right)=C\left(x\right)/A\left(x\right)$ 在 $x_0$ 附近解析. 称这样的点 $x_0$ 为微分方程的常点. 如果 $A\left(x_0\right)=0$, 则 $p\left(x\right)$ 和 $q\left(x\right)$ 中至少有一个在 $x_0$ 点不连续, 称 $x_0$ 为微分方程的奇点.

**定理 7.2**(常点邻域内幂级数解的存在与递推)

设微分方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 中的系数函数 $p\left(x\right)$ 和 $q\left(x\right)$ 在区间 $\left(x_0-r,x_0+r\right)$ 内可以展成 $\left(x-x_0\right)$ 的收敛的幂级数, 则该方程在区间 $\left(x_0-r,x_0+r\right)$ 内有收敛的幂级数解 $y=\sum_{n=0}^{\infty}C_n\left(x-x_0\right)^n$, 其中 $C_0$ 和 $C_1$ 是两个任意常数(它们可通过在 $x_0$ 点的初值条件来决定, 即 $C_0=y_0$ 和 $C_1=y_0'$), 而 $C_n\ \left(n\ge2\right)$ 可以从 $C_0$ 和 $C_1$ 出发依次由递推公式确定.

## 7.3 勒让德多项式

**勒让德方程与勒让德多项式**

勒让德方程为 $\left(1-x^2\right)y''-2xy'+n\left(n+1\right)y=0$, 其中 $n$ 是常数. 当 $n$ 是非负整数时, 方程的一个解是 $n$ 次多项式, 即勒让德多项式 $P_n\left(x\right)$, 其统一表达式为 $P_n\left(x\right)=\dfrac{1}{2^n}\sum_{k=0}^{\left[n/2\right]}\dfrac{\left(-1\right)^k\left(2n-2k\right)!}{k!\left(n-k\right)!\left(n-2k\right)!}x^{n-2k}$.

**勒让德多项式的母函数**

令函数 $G\left(x,t\right)=\left(1-2xt+t^2\right)^{-1/2}$, 则 $G\left(x,t\right)$ 关于 $t$ 展开的幂级数为 $G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n$, 其中 $P_n\left(x\right)$ 是勒让德多项式. 函数 $G\left(x,t\right)$ 称为勒让德多项式的母函数. 它满足恒等式 $\left(1-2xt+t^2\right)\dfrac{\partial G}{\partial t}=\left(x-t\right)G$.

## 8.2 解的稳定性

**解的稳定性**(李雅普诺夫意义下的稳定, 渐近稳定, 不稳定与全局渐近稳定)

考虑方程 $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}(t,\boldsymbol{x})$ 的某个解 $\boldsymbol{x} = \boldsymbol{\varphi}(t)$. 如果对任意给定的 $\varepsilon > 0$, 都存在 $\delta = \delta(\varepsilon, t_0) > 0$, 使得只要 $\|\boldsymbol{x}_0 - \boldsymbol{\varphi}(t_0)\| < \delta$, 方程以 $\boldsymbol{x}(t_0) = \boldsymbol{x}_0$ 为初值的解 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0)$ 就在 $t \ge t_0$ 有定义, 并且满足 $\|\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t)\| < \varepsilon$ 对一切 $t \ge t_0$ 成立, 则称解 $\boldsymbol{\varphi}(t)$ 是(在李雅普诺夫意义下)稳定的. 如果解 $\boldsymbol{\varphi}(t)$ 是稳定的, 而且存在 $\delta_0 > 0$, 使得只要 $\|\boldsymbol{x}_0 - \boldsymbol{\varphi}(t_0)\| < \delta_0$ 就有 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t) \to \boldsymbol{0}\ (t \to +\infty)$, 则称解 $\boldsymbol{\varphi}(t)$ 是渐近稳定的. 如果解 $\boldsymbol{\varphi}(t)$ 不是稳定的, 则称它是不稳定的. 如果吸引域是全空间, 即不论初值多大都有 $\boldsymbol{x}(t, t_0, \boldsymbol{x}_0) - \boldsymbol{\varphi}(t) \to \boldsymbol{0}$, 则称解 $\boldsymbol{\varphi}(t)$ 是全局渐近稳定的.

**定理 8.1**(常系数线性系统零解稳定性的特征根判别)

设线性方程 $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$ 中的矩阵 $A$ 为常矩阵, 则 (1) 零解是渐近稳定的, 当且仅当矩阵 $A$ 的全部特征根都有负的实部; (2) 零解是稳定的, 当且仅当矩阵 $A$ 的全部特征根的实部都是非正的, 并且那些实部为零的特征根所对应的若尔当块都是一阶的; (3) 零解是不稳定的, 当且仅当矩阵 $A$ 的特征根中至少有一个实部为正, 或者至少有一个实部为零且它所对应的若尔当块是高于一阶的.

**定理 8.3**(按线性近似判断不稳定性)

设非线性方程 $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x} + \boldsymbol{N}(t,\boldsymbol{x})$ 中的 $A$ 为常矩阵, 而且 $A$ 的特征根中至少有一个具有正的实部, 则方程的零解是不稳定的.

**定理 8.4**(李雅普诺夫的稳定性判定)

设自治系统 $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}(\boldsymbol{x})$ 的右端满足初值问题解的存在和唯一性条件, 且存在连续可微的标量函数 $V(\boldsymbol{x})$. 记 $V$ 沿轨线对 $t$ 的全导数为 $\frac{dV}{dt} = \sum_{i=1}^{n}\frac{\partial V}{\partial x_i}f_i(\boldsymbol{x})$. 若条件 $I$($V(\boldsymbol{0}) = 0,\ V(\boldsymbol{x}) > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 称 $V$ 为定正函数) 成立, 则 (1) 再若条件 $II$($\frac{dV}{dt} < 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 即全导数为定负函数) 成立, 零解是渐近稳定的; (2) 再若条件 $II^*$($\frac{dV}{dt} \le 0$, 即全导数为常负函数) 成立, 零解是稳定的; (3) 再若条件 $III$($\frac{dV}{dt} > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, 即全导数为定正函数) 成立, 零解是不稳定的.

## 8.3 平面上的动力系统, 奇点与极限环

**初等奇点**(与高阶奇点)

以 $(0,0)$ 为奇点的线性系统 $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$. 当矩阵 $A$ 非退化(即 $A$ 不以零为特征根)时, 称 $(0,0)$ 点为系统的初等奇点; 否则称它为高阶奇点. 初等奇点都是孤立奇点, 而线性高阶奇点都是非孤立的.

**特殊方向**

当 $t \to +\infty$(或 $-\infty$)时, 有的轨线能沿某一确定的直线 $y = kx$(或 $x = ky$)趋于奇点 $(0,0)$, 这个直线的走向称为一个特殊方向. 星形结点有无穷个特殊方向, 两向结点和鞍点有两个特殊方向, 单向结点有一个特殊方向, 而焦点和中心没有特殊方向; 并且当直线 $y = kx$ 给出线性系统的一个特殊方向时, 此直线被奇点分割的两条射线都是系统的轨线.

**定理 8.5**(初等奇点类型的判定)

对于线性系统 $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$, 记 $p = -\text{tr}[A]$(矩阵 $A$ 的迹的反号), $q = \det[A]$, 则我们有 (1) 当 $q < 0$ 时, $(0,0)$ 为鞍点; (2) 当 $q > 0$ 且 $p^2 > 4q$ 时, $(0,0)$ 为两向结点; (3) 当 $q > 0$ 且 $p^2 = 4q$ 时, $(0,0)$ 为单向结点或星形结点; (4) 当 $q > 0$ 且 $0 < p^2 < 4q$ 时, $(0,0)$ 为焦点; (5) 当 $q > 0$ 且 $p = 0$ 时, $(0,0)$ 为中心点. 此外, 在情形 (2) 至 (4) 中, 当 $p > 0$ 时奇点 $(0,0)$ 是稳定的, 而当 $p < 0$ 时则是不稳定的.

**定理 8.6**(非线性系统在初等奇点附近与线性化系统有相同的定性结构)

设非线性系统 $\frac{dx}{dt} = ax + by + \varphi(x,y),\ \frac{dy}{dt} = cx + dy + \psi(x,y)$ 以 $(0,0)$ 为孤立奇点, 其线性化系统 $\frac{dx}{dt} = ax + by,\ \frac{dy}{dt} = cx + dy$ 以 $(0,0)$ 为初等奇点, 其中 $r = \sqrt{x^2 + y^2}$. 则 (1) 若线性化系统以 $(0,0)$ 为焦点且条件 $A$($\varphi(x,y) = o(r),\ \psi(x,y) = o(r),\ r \to 0$) 成立, 则 $(0,0)$ 也是原系统的焦点, 且稳定性相同; (2) 若线性化系统以 $(0,0)$ 为鞍点或两向结点且条件 $A$ 与条件 $B$($\varphi, \psi$ 在原点的一个小邻域内对 $x, y$ 连续可微) 成立, 则 $(0,0)$ 也分别是原系统的鞍点或两向结点, 且稳定性相同; (3) 若线性化系统以 $(0,0)$ 为单向结点且条件 $A^*$($|\varphi|/r$ 与 $|\psi|/r$ 当 $r \to 0$ 时一致趋于零) 成立, 则 $(0,0)$ 也是原系统的单向结点, 且稳定性相同; (4) 若线性化系统以 $(0,0)$ 为星形结点且条件 $A^*$ 与条件 $B$ 成立, 则 $(0,0)$ 也是原系统的星形结点, 且稳定性相同.

## 10.2 首次积分的性质

**定理 10.1**(首次积分的充要条件)

设微分方程组 $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$($i=1,\cdots,n$) 的右端 $f_1,\cdots,f_n$ 在区域 $G_1$ 内对 $\left(x,y_1,\cdots,y_n\right)$ 连续, 且对 $\left(y_1,\cdots,y_n\right)$ 连续可微. 设函数 $\Phi\left(x,y_1,\cdots,y_n\right)$ 在 $G_1$ 内连续可微, 则 $\Phi\left(x,y_1,\cdots,y_n\right)=C$ 是该方程组在 $G_1$ 内的首次积分的充要条件为恒等式 $$\frac{\partial\Phi}{\partial x}+\frac{\partial\Phi}{\partial y_1}f_1+\cdots+\frac{\partial\Phi}{\partial y_n}f_n\equiv0$$ 在 $G_1$ 内成立.

**定理 10.2**(已知一个首次积分可降低一阶)

若已知微分方程组 (10.17) 的一个首次积分 $\Phi\left(x,y_1,\cdots,y_n\right)=C$, 则可把该微分方程组降低一阶. 其依据是 $\frac{\partial\Phi}{\partial y_1},\cdots,\frac{\partial\Phi}{\partial y_n}$ 不能全为零, 不妨设 $\frac{\partial\Phi}{\partial y_n}\neq0$, 再用隐函数定理由首次积分解出 $y_n=g\left(x,y_1,\cdots,y_{n-1},C\right)$, 代回原方程组前 $n-1$ 式消去 $y_n$.

**互相独立的首次积分**(雅可比行列式非零)

设微分方程组 (10.17) 有 $k$ 个首次积分 $V_i\left(x,y_1,\cdots,y_n\right)=C_i$($i=1,\cdots,k$). 若在某区域内它们的矩阵 $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ 的秩等于 $k$, 亦即不妨设雅可比行列式 $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$, 则称它们在该区域内是互相独立的.

**隐函数定理**

若函数 $F\left(x,y_1,\cdots,y_k\right)$ 连续可微且 $\frac{\partial F}{\partial y_k}\neq0$, 则由方程 $F\left(x,y_1,\cdots,y_k\right)=0$ 可在局部解出 $y_k$ 为其余变元的连续可微函数.

## 10.4 大范围的首次积分

**定理 10.7**(大范围首次积分与保守系统)

对于三维自治系统 $\frac{dx}{dt}=E,\ \frac{dy}{dt}=F,\ \frac{dz}{dt}=G$, 若它在大范围区域 $\Omega$ 内有两个互相独立的驻定首次积分 $\Phi_1=C_1,\ \Phi_2=C_2$, 则该系统在 $\Omega$ 内是一个保守系统或等价于一个保守系统. 其推导为: 由首次积分充要条件 $\frac{\partial\Phi_i}{\partial x}E+\frac{\partial\Phi_i}{\partial y}F+\frac{\partial\Phi_i}{\partial z}G\equiv0$ 解出 $(E,F,G)$ 与雅可比量 $L=\frac{D(\Phi_1,\Phi_2)}{D(y,z)},\ M=\frac{D(\Phi_1,\Phi_2)}{D(z,x)},\ N=\frac{D(\Phi_1,\Phi_2)}{D(x,y)}$ 成比例, 即 $L=\mu E,\ M=\mu F,\ N=\mu G$; 再由恒等式 $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$ 得 $\frac{\partial(\mu E)}{\partial x}+\frac{\partial(\mu F)}{\partial y}+\frac{\partial(\mu G)}{\partial z}\equiv0$.

**散度与保守系统**

向量场 $(E,F,G)$ 的散度为 $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}$. 当 $\mu$ 为常数时, 上式成为 $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}=0$, 即散度等于零, 称该系统为保守系统. 当 $\mu$ 不是常数时, 称 $\mu(x,y,z)$ 为拟积分因子, 此时原系统经参数变换 $d\tau=\frac{dt}{\mu}$ 化为等价的保守系统 $\frac{dx}{d\tau}=\mu E,\ \frac{dy}{d\tau}=\mu F,\ \frac{dz}{d\tau}=\mu G$.

**定理 2.1**(恰当方程的判别与通积分公式)

对于对称形式的一阶方程 $Pdx+Qdy=0$, 它是恰当方程(即存在 $\Phi$ 使 $d\Phi=Pdx+Qdy$)的充要条件为 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$; 当它不是恰当方程时, 若有因子 $\mu(x,y)$ 使 $\mu Pdx+\mu Qdy=0$ 成为恰当方程, 则称 $\mu$ 为该方程的积分因子.

## 11.1 一阶齐次线性偏微分方程

**定理 11.1**(齐次线性偏微分方程的通解)

设有一阶齐次线性偏微分方程 $\sum_{i=1}^nA_i\left(x_1,\cdots,x_n\right)\frac{\partial u}{\partial x_i}=0$, 其中系数 $A_1,\cdots,A_n$ 连续可微且不同时为零. 其特征方程为对称形式的常微分方程组 $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$, 它是一个 $n-1$ 阶方程组, 有 $n-1$ 个独立的首次积分 $\varphi_i\left(x_1,\cdots,x_n\right)=C_i$($i=1,\cdots,n-1$). 则原偏微分方程的通解为 $u=\psi\left[\varphi_1,\cdots,\varphi_{n-1}\right]$, 其中 $\psi$ 是任意的 $n-1$ 元连续可微函数. 换言之, 函数 $\varphi$ 为特征方程首次积分的充要条件是恒等式 $\sum_{i=1}^nA_i\frac{\partial\varphi}{\partial x_i}\equiv0$ 成立.

## 11.2 一阶拟线性偏微分方程

**定理 11.2**(拟线性偏微分方程的隐式通解)

设有一阶拟线性偏微分方程 $X\left(x,y,z\right)\frac{\partial z}{\partial x}+Y\left(x,y,z\right)\frac{\partial z}{\partial y}=Z\left(x,y,z\right)$, 其中 $X,Y,Z$ 连续可微且 $X,Y$ 不同时为零. 其相应特征方程为 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$. 设 $u\left(x,y,z\right)=C_1,\ v\left(x,y,z\right)=C_2$ 是该特征方程的两个独立首次积分, 则原拟线性偏微分方程的隐式通解为 $\Phi\left[u\left(x,y,z\right),v\left(x,y,z\right)\right]=0$, 其中 $\Phi$ 是任意连续可微函数, 并要求 $\frac{\partial\Phi}{\partial z}\neq0$ 以便由隐函数解出 $z=z\left(x,y\right)$.

**定理 11.1**(齐次线性偏微分方程的通解)

特征方程 $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$ 的 $n-1$ 个独立首次积分 $\varphi_i=C_i$ 给出齐次线性方程 $\sum_{i=1}^nA_i\frac{\partial u}{\partial x_i}=0$ 的通解 $u=\psi\left(\varphi_1,\cdots,\varphi_{n-1}\right)$. 求特征方程首次积分的方法同样适用于定理 11.2 中 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$ 的情形.

## 11.3 几何解释

**定理 11.2**(拟线性偏微分方程的隐式通解与特征线)

一阶拟线性方程 $X\frac{\partial z}{\partial x}+Y\frac{\partial z}{\partial y}=Z$ 的特征方程为 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$, 其积分曲线称特征曲线, 它在每点以特征向量 $\left(X,Y,Z\right)$ 为切向量. 偏微分方程的解 $z=z\left(x,y\right)$ 所确定的积分曲面 $S$ 由特征曲线编织而成: 通过 $S$ 上每点的特征曲线整个落在 $S$ 上.

**特征线法**(初值问题的解法)

给定初始曲线 $\Lambda:\ x=\alpha\left(\sigma\right),\ y=\beta\left(\sigma\right),\ z=\gamma\left(\sigma\right)$. 设特征方程有两个独立首次积分 $\varphi=C_1,\ \psi=C_2$. 在 $\Lambda$ 上取点 $M$, 过 $M$ 的特征曲线为 $\varphi=\overline{C}_1,\ \psi=\overline{C}_2$, 其中 $\overline{C}_1=\varphi\left(\alpha,\beta,\gamma\right),\ \overline{C}_2=\psi\left(\alpha,\beta,\gamma\right)$. 消去参数 $\sigma$ 得 $\overline{C}_1,\overline{C}_2$ 间的关系式 $E\left(\overline{C}_1,\overline{C}_2\right)=0$, 则 $E\left(\varphi\left(x,y,z\right),\psi\left(x,y,z\right)\right)=0$ 即为所求积分曲面.

**特征线法附注**(初始曲线为特征曲线时解不唯一)

若过初始曲线 $\Lambda$ 的每点所作特征曲线与 $\Lambda$ 在交点处横截相交, 则这些特征曲线组成唯一的光滑积分曲面 $z=z\left(x,y\right)$; 但若初始曲线 $\Lambda$ 本身就是一条特征曲线, 则过 $\Lambda$ 的特征曲线只是 $\Lambda$ 自己, 不能张成曲面, 此时任何包含 $\Lambda$ 的积分曲面都是初值问题的解, 即解存在但不唯一.
