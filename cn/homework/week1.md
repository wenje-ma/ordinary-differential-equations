# 作业 1

> **定义 1.1**(常微分方程)<br>凡是联系自变量 $x$ 与这个自变量的未知函数 $y=y\left(x\right)$, 和它的导数 $y'=y'\left(x\right)$ 以及直到 $n$ 阶导数 $y^{\left(n\right)}=y^{\left(n\right)}\left(x\right)$ 在内的方程 $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$ 叫作常微分方程, 其中导数实际出现的最高阶数 $n$ 叫作常微分方程的阶. 若左端函数 $F$ 对未知函数 $y$ 及其各阶导数 $y',y'',\cdots,y^{\left(n\right)}$ 的全体而言是一次的, 则称它是线性常微分方程, 否则称它为非线性常微分方程.

> **定义 1.2**(解)<br>设函数 $y=\varphi\left(x\right)$ 在区间 $J$ 上连续, 且有直到 $n$ 阶的导数. 如果把 $y=\varphi\left(x\right)$ 及其相应的各阶导数代入方程 $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$, 得到关于 $x$ 的恒等式 $F\left(x,\varphi\left(x\right),\varphi'\left(x\right),\cdots,\varphi^{\left(n\right)}\left(x\right)\right)=0$ 对一切 $x\in J$ 都成立, 则称 $y=\varphi\left(x\right)$ 为微分方程在区间 $J$ 上的一个解.

> **定义 1.3**(通解与特解)<br>设 $n$ 阶微分方程的解 $y=\varphi\left(x,C_1,C_2,\cdots,C_n\right)$ 包含 $n$ 个独立的任意常数 $C_1,C_2,\cdots,C_n$, 则称它为通解. 这里 $n$ 个任意常数 $C_1,C_2,\cdots,C_n$ 是独立的, 其含义是雅可比行列式 $\frac{D\left(\varphi,\varphi',\cdots,\varphi^{\left(n-1\right)}\right)}{D\left(C_1,C_2,\cdots,C_n\right)}\neq0$, 其中 $\varphi^{\left(k\right)}=\varphi^{\left(k\right)}\left(x,C_1,C_2,\cdots,C_n\right)\ \left(k=0,1,\cdots,n-1\right)$. 如果微分方程的解 $y=\varphi\left(x\right)$ 不包含任意常数, 则称它为特解.

> **初值问题**(柯西问题)<br>对 $n$ 阶微分方程, 初值条件的一般提法是 $y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$, 其中 $x_0$ 是自变量所取定的某个初值, 而 $y_0,\ y_0',\ \cdots,\ y_0^{\left(n-1\right)}$ 是未知函数及其相应导数所取定的初值. 这样, $n$ 阶微分方程的初值问题可以提成如下形式: $$\begin{cases}y^{\left(n\right)}=F\left(x,y,y',\cdots,y^{\left(n-1\right)}\right),\\y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}.\end{cases}$$ 初值问题又名柯西问题.

> **微分方程的求解与积分运算**<br>微分方程的求解与一定的积分运算相联系. 因此常把求解微分方程的过程称为积分一个微分方程, 而把微分方程的解叫作积分. 由于每进行一次不定积分运算, 就会产生一个任意常数, 因此就微分方程本身的积分而言, $n$ 阶微分方程的通解应该包含 $n$ 个任意常数.

### 习题一

(习题 1-1 题1(4))验证函数 $y=\begin{cases}-\frac{1}{4}\left(x-C_1\right)^2,&-\infty<x<C_1,\\0,&C_1\le x\le C_2,\\\frac{1}{4}\left(x-C_2\right)^2,&C_2<x<+\infty\end{cases}$ 是右侧相应微分方程 $y'=\sqrt{\left|y\right|}$ 的解.

### 解答 习题一

由**定义 1.2**(解), 只需验证 $y=y\left(x\right)$ 满足 $y'=\sqrt{\left|y\right|}$. 将 $y=y\left(x\right)$ 分三段验证.

(1) 当 $-\infty<x<C_1$ 时, $y=-\frac{1}{4}\left(x-C_1\right)^2<0$, 故 $y'=-\frac{1}{2}\left(x-C_1\right)$, 且 $\left|y\right|=\frac{1}{4}\left(x-C_1\right)^2$. 由于 $x<C_1$, $\left|x-C_1\right|=C_1-x$, 于是
$$
\sqrt{\left|y\right|}=\frac{1}{2}\left|x-C_1\right|=\frac{1}{2}\left(C_1-x\right)=-\frac{1}{2}\left(x-C_1\right)=y'.
$$

(2) 当 $C_1\le x\le C_2$ 时, $y=0$, 故 $y'=0$, 且 $\sqrt{\left|y\right|}=0$, 故 $y'=\sqrt{\left|y\right|}$.

(3) 当 $C_2<x<+\infty$ 时, $y=\frac{1}{4}\left(x-C_2\right)^2>0$, 故 $y'=\frac{1}{2}\left(x-C_2\right)$, 且 $\left|y\right|=\frac{1}{4}\left(x-C_2\right)^2$. 由于 $x>C_2$, $\left|x-C_2\right|=x-C_2$, 于是
$$
\sqrt{\left|y\right|}=\frac{1}{2}\left|x-C_2\right|=\frac{1}{2}\left(x-C_2\right)=y'.
$$

综上, 在三个区间上均有 $y'=\sqrt{\left|y\right|}$, 故 $y$ 是微分方程 $y'=\sqrt{\left|y\right|}$ 的解. $\blacksquare$

### 习题二

(习题 1-2 题2(3))求初值问题 $\frac{dR}{dt}=-aR,\ R\left(0\right)=1$ 的解(这里 $a>0$ 是一个常数).

### 解答 习题二

由**初值问题**(柯西问题), 其解需满足初值条件 $R\left(0\right)=1$. 由微分方程的求解与积分运算相联系, 对该方程分离变量两端积分求解. 当 $R\neq0$ 时分离变量, 得
$$
\frac{dR}{R}=-a\,dt.
$$

两端积分, 得 $\ln\left|R\right|=-at+C$, 即 $R=Ce^{-at}$($C\neq0$ 为任意常数; $C=0$ 对应零解 $R\equiv0$, 亦满足方程). 代入初值条件 $R\left(0\right)=1$, 得 $C=1$, 故所求解为
$$
R\left(t\right)=e^{-at}.
$$

$\blacksquare$

### 习题三

(习题 1-2 题2(4))求初值问题 $\frac{dy}{dx}=1+y^2,\ y\left(x_0\right)=y_0$ 的解.

### 解答 习题三

由微分方程的求解与积分运算相联系, 对该方程分离变量两端积分求解. 由于 $1+y^2\neq0$ 恒成立, 分离变量, 得
$$
\frac{dy}{1+y^2}=dx.
$$

两端积分, 得 $\arctan y=x+C$, 即 $y=\tan\left(x+C\right)$. 代入初值条件 $y\left(x_0\right)=y_0$, 得 $\arctan y_0=x_0+C$, 即 $C=\arctan y_0-x_0$, 故所求解为
$$
y=\tan\left(x+\arctan y_0-x_0\right).
$$

$\blacksquare$
