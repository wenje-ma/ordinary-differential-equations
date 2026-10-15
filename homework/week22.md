# 作业 22

> **常点与奇点**<br>考虑二阶齐次线性微分方程 $A\left(x\right)y''+B\left(x\right)y'+C\left(x\right)y=0$. 如果 $A\left(x_0\right)\neq0$, 则在 $x_0$ 点附近 $A\left(x\right)\neq0$, 方程可写成 $y''+p\left(x\right)y'+q\left(x\right)y=0$, 其中 $p\left(x\right)=B\left(x\right)/A\left(x\right),\ q\left(x\right)=C\left(x\right)/A\left(x\right)$ 在 $x_0$ 附近解析. 称这样的点 $x_0$ 为微分方程的常点. 如果 $A\left(x_0\right)=0$, 则 $p\left(x\right)$ 和 $q\left(x\right)$ 中至少有一个在 $x_0$ 点不连续, 称 $x_0$ 为微分方程的奇点.

> **定理 7.2**(常点邻域内幂级数解的存在与递推)<br>设微分方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 中的系数函数 $p\left(x\right)$ 和 $q\left(x\right)$ 在区间 $\left(x_0-r,x_0+r\right)$ 内可以展成 $\left(x-x_0\right)$ 的收敛的幂级数, 则该方程在区间 $\left(x_0-r,x_0+r\right)$ 内有收敛的幂级数解 $y=\sum_{n=0}^{\infty}C_n\left(x-x_0\right)^n$, 其中 $C_0$ 和 $C_1$ 是两个任意常数(它们可通过在 $x_0$ 点的初值条件来决定, 即 $C_0=y_0$ 和 $C_1=y_0'$), 而 $C_n\ \left(n\ge2\right)$ 可以从 $C_0$ 和 $C_1$ 出发依次由递推公式确定.

### 习题一

(习题 7-2 题3)求解埃尔米特方程 $y''-2xy'+\lambda y=0\ \left(-\infty<x<+\infty\right)$, 其中 $\lambda$ 是常数.

### 解答 习题一

$x=0$ 是方程的常点(系数均为多项式). 由**定理 7.2**(常点邻域内幂级数解的存在与递推), 设方程有幂级数解

$$
y=\sum_{n=0}^{\infty}a_nx^n.
$$

逐项微分并调整求和指标, 得

$$
y'=\sum_{n=0}^{\infty}\left(n+1\right)a_{n+1}x^n,\qquad y''=\sum_{n=0}^{\infty}\left(n+2\right)\left(n+1\right)a_{n+2}x^n.
$$

代入方程 $y''-2xy'+\lambda y=0$, 其中 $-2xy'=-2\sum_{n=1}^{\infty}na_nx^n$, 比较 $x^n$ 的系数.

$n=0$ 时: $2a_2+\lambda a_0=0$, 即 $a_2=-\frac{\lambda}{2}a_0$.

$n\ge1$ 时: $\left(n+2\right)\left(n+1\right)a_{n+2}-2na_n+\lambda a_n=0$, 即递推公式

$$
a_{n+2}=\frac{2n-\lambda}{\left(n+2\right)\left(n+1\right)}\,a_n\qquad\left(n=0,1,2,\cdots\right).
$$

递推公式隔项分离, 分别写出偶次和奇次系数.

偶次项: $a_2=-\frac{\lambda}{2!}a_0,\ a_4=\frac{\left(-\lambda\right)\left(4-\lambda\right)}{4!}a_0,\ a_6=\frac{\left(-\lambda\right)\left(4-\lambda\right)\left(8-\lambda\right)}{6!}a_0$, 一般地

$$
a_{2k}=\frac{\left(-\lambda\right)\left(4-\lambda\right)\left(8-\lambda\right)\cdots\left(4k-4-\lambda\right)}{\left(2k\right)!}\,a_0\qquad\left(k\ge1\right).
$$

奇次项: $a_3=\frac{2-\lambda}{3!}a_1,\ a_5=\frac{\left(2-\lambda\right)\left(6-\lambda\right)}{5!}a_1$, 一般地

$$
a_{2k+1}=\frac{\left(2-\lambda\right)\left(6-\lambda\right)\left(10-\lambda\right)\cdots\left(4k-2-\lambda\right)}{\left(2k+1\right)!}\,a_1\qquad\left(k\ge1\right).
$$

因此方程的通解为

$$
y=a_0\left[1+\sum_{k=1}^{\infty}\frac{\left(-\lambda\right)\left(4-\lambda\right)\cdots\left(4k-4-\lambda\right)}{\left(2k\right)!}x^{2k}\right]+a_1\left[x+\sum_{k=1}^{\infty}\frac{\left(2-\lambda\right)\left(6-\lambda\right)\cdots\left(4k-2-\lambda\right)}{\left(2k+1\right)!}x^{2k+1}\right],
$$

其中 $a_0,a_1$ 为任意常数. 由比值法, $\left|\frac{a_{n+2}}{a_n}\right|=\frac{\left|2n-\lambda\right|}{\left(n+2\right)\left(n+1\right)}\to0$, 故两级数对一切 $x$ 收敛. $\blacksquare$

### 习题二

(习题 7-2 题4)求微分方程 $y''+\left(\sin x\right)y=0$ 在 $x=0$ 处展开的两个线性无关的幂级数解.

### 解答 习题二

$x=0$ 是方程的常点($\sin x$ 在 $x=0$ 附近解析). 由**定理 7.2**(常点邻域内幂级数解的存在与递推), 设

$$
y=\sum_{n=0}^{\infty}a_nx^n,\qquad y''=\sum_{n=0}^{\infty}\left(n+2\right)\left(n+1\right)a_{n+2}x^n.
$$

而 $\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots$, 故乘积 $\left(\sin x\right)y$ 中 $x^n$ 的系数为 $a_{n-1}-\frac{a_{n-3}}{3!}+\frac{a_{n-5}}{5!}-\cdots$(其中 $a_{-1}=a_{-2}=0$). 代入方程比较系数:

$$
\begin{aligned}
n=0:&\quad 2a_2=0,\quad a_2=0;\\
n=1:&\quad 6a_3+a_0=0,\quad a_3=-\frac{a_0}{6};\\
n=2:&\quad 12a_4+a_1=0,\quad a_4=-\frac{a_1}{12};\\
n=3:&\quad 20a_5+a_2-\frac{a_0}{6}=0,\quad a_5=\frac{a_0}{120};\\
n=4:&\quad 30a_6+a_3-\frac{a_1}{6}=0,\quad a_6=\frac{a_0}{180}+\frac{a_1}{180};\\
n=5:&\quad 42a_7+a_4-\frac{a_2}{6}+\frac{a_0}{120}=0,\quad a_7=\frac{a_1}{504}-\frac{a_0}{5040}.
\end{aligned}
$$

取 $a_0=1,\ a_1=0$, 得第一个解

$$
y_1=1-\frac{x^3}{6}+\frac{x^5}{120}+\frac{x^6}{180}-\frac{x^7}{5040}+\cdots.
$$

取 $a_0=0,\ a_1=1$, 得第二个解

$$
y_2=x-\frac{x^4}{12}+\frac{x^6}{180}+\frac{x^7}{504}+\cdots.
$$

两个解分别对应初值 $\left(y_1\left(0\right),y_1'\left(0\right)\right)=\left(1,0\right)$ 和 $\left(y_2\left(0\right),y_2'\left(0\right)\right)=\left(0,1\right)$, 朗斯基行列式在 $x=0$ 处为 $1$, 故二者线性无关. $\blacksquare$
