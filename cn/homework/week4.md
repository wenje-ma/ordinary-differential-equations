# 作业 4

> **一阶线性方程**<br>形如 $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$$ 的方程称为一阶线性方程, 其中 $p\left(x\right),q\left(x\right)$ 在区间 $I$ 上连续. 当 $q\left(x\right)\equiv0$ 时称为相应的齐次线性方程, 否则称为非齐次线性方程.

> **齐次线性方程的通解**<br>对齐次线性方程 $$\frac{dy}{dx}+p\left(x\right)y=0,$$ 分离变量积分得通解 $$y=Ce^{-\int p\left(x\right)dx},$$ 其中任意常数 $C$ 可取零值, $C=0$ 对应特解 $y\equiv0$.

> **非齐次线性方程的通解(积分因子法)**<br>以积分因子 $$\mu\left(x\right)=e^{\int p\left(x\right)dx}$$ 乘非齐次线性方程两端, 左端化为全微分 $$\frac{d}{dx}\left(e^{\int p\left(x\right)dx}y\right)=q\left(x\right)e^{\int p\left(x\right)dx}.$$ 积分得通解 $$y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C\right].$$

### 习题一

(习题 2-3 题1(2))求解微分方程 $\frac{dy}{dx}+y\tan x=\sin 2x$.

### 解答 习题一

这是一阶线性方程, $p\left(x\right)=\tan x,\ q\left(x\right)=\sin 2x$. 由**非齐次线性方程的通解(积分因子法)**, 积分因子为
$$
\mu\left(x\right)=e^{\int\tan x\,dx}=e^{-\ln\left|\cos x\right|}=\sec x.
$$

以 $\sec x$ 乘方程两端, 得
$$
\frac{d}{dx}\left(y\sec x\right)=\sin 2x\sec x=2\sin x\cos x\cdot\frac{1}{\cos x}=2\sin x.
$$

两端积分, 得 $y\sec x=-2\cos x+C$, 故通解为
$$
y=C\cos x-2\cos^2x.
$$

$\blacksquare$

### 习题二

(习题 2-3 题1(4))求解初值问题 $\frac{dy}{dx}-\frac{1}{1-x^2}y=1+x,\ y\left(0\right)=1$.

### 解答 习题二

这是一阶线性方程, $p\left(x\right)=-\frac{1}{1-x^2},\ q\left(x\right)=1+x$. 由**非齐次线性方程的通解(积分因子法)**, 注意到解在 $x=0$ 附近即 $\left|x\right|< 1$ 上考虑, 积分因子为
$$
\mu\left(x\right)=e^{\int-\frac{1}{1-x^2}dx}=e^{-\frac{1}{2}\ln\frac{1+x}{1-x}}=\sqrt{\frac{1-x}{1+x}}.
$$

以 $\mu\left(x\right)$ 乘方程两端, 左端化为全微分, 右端为
$$
\mu\left(x\right)q\left(x\right)=\sqrt{\frac{1-x}{1+x}}\left(1+x\right)=\sqrt{1-x^2}.
$$

故 $\frac{d}{dx}\left(\mu y\right)=\sqrt{1-x^2}$, 从 $0$ 到 $x$ 积分. 由初值条件 $\mu\left(0\right)y\left(0\right)=1$, 得
$$
\mu\left(x\right)y=1+\int_0^x\sqrt{1-t^2}\,dt=1+\frac{1}{2}\left(x\sqrt{1-x^2}+\arcsin x\right).
$$

于是所求解为
$$
y=\sqrt{\frac{1+x}{1-x}}\left[1+\frac{1}{2}\left(x\sqrt{1-x^2}+\arcsin x\right)\right].
$$

$\blacksquare$

### 习题三

(习题 2-3 题3)设 $y=\varphi\left(x\right)$ 满足微分不等式 $y'+a\left(x\right)y\le0$($x\ge0$), 求证: $\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^x a\left(s\right)ds}$($x\ge0$).

### 解答 习题三

由**非齐次线性方程的通解(积分因子法)**的思想, 取积分因子 $A\left(x\right)=e^{\int_0^x a\left(s\right)ds}> 0$. 以 $A\left(x\right)$ 乘不等式 $y'+a\left(x\right)y\le0$ 两端, 得
$$
A\left(x\right)\left[y'+a\left(x\right)y\right]=\frac{d}{dx}\left(A\left(x\right)y\right)\le0.
$$

故 $A\left(x\right)y\left(x\right)$ 在 $x\ge0$ 上单调不增, 从而
$$
A\left(x\right)y\left(x\right)\le A\left(0\right)y\left(0\right)=y\left(0\right).
$$

代入 $A\left(x\right)=e^{\int_0^x a\left(s\right)ds}$, 整理得
$$
\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^x a\left(s\right)ds}\quad\left(x\ge0\right).
$$

$\blacksquare$

### 习题四

(习题 2-3 题4)用常数变易法求解非齐次线性方程 $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$, 即假设它有形如齐次通解的形式, 但将其中任意常数 $C$ 变易为 $x$ 的待定函数 $C\left(x\right)$, 再代入方程确定 $C\left(x\right)$.

### 解答 习题四

由**齐次线性方程的通解**, 相应齐次方程的通解为 $y=Ce^{-\int p\left(x\right)dx}$. 视 $C$ 为 $x$ 的函数, 设非齐次方程有形如
$$
y=C\left(x\right)e^{-\int p\left(x\right)dx}
$$

的解. 对 $x$ 求导, 得
$$
y'=C'\left(x\right)e^{-\int p\left(x\right)dx}-C\left(x\right)p\left(x\right)e^{-\int p\left(x\right)dx}.
$$

代入 $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$, 含 $C\left(x\right)$ 的两项相消, 得
$$
C'\left(x\right)e^{-\int p\left(x\right)dx}=q\left(x\right),
$$

即 $C'\left(x\right)=q\left(x\right)e^{\int p\left(x\right)dx}$. 积分得
$$
C\left(x\right)=\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C_1.
$$

代回所设解, 即得与**非齐次线性方程的通解(积分因子法)**一致的通解
$$
y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C_1\right].
$$

$\blacksquare$

### 习题五

(习题 2-3 题5)考虑方程 $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$, 其中 $p\left(x\right),q\left(x\right)$ 都是以 $\omega> 0$ 为周期的连续函数. 试证: (1) 若 $q\left(x\right)\equiv0$, 则方程的任一非零解以 $\omega$ 为周期, 当且仅当函数 $p\left(x\right)$ 的平均值 $\overline p\equiv\frac{1}{\omega}\int_0^\omega p\left(x\right)dx=0$; (2) 若 $q\left(x\right)$ 不恒为零, 则方程有唯一的 $\omega$ 周期解, 当且仅当 $\overline p\neq0$, 试求出此解.

### 解答 习题五

由**齐次线性方程的通解**, 当 $q\left(x\right)\equiv0$ 时, 任一解为 $y\left(x\right)=Ce^{-\int_0^x p\left(t\right)dt}$. 由 $p\left(x\right)$ 的 $\omega$ 周期性, $\int_x^{x+\omega}p\left(t\right)dt=\int_0^\omega p\left(t\right)dt$. 于是
$$
y\left(x+\omega\right)=Ce^{-\int_0^{x+\omega}p}=Ce^{-\int_0^x p}\cdot e^{-\int_0^\omega p}=y\left(x\right)e^{-\int_0^\omega p}.
$$

非零解以 $\omega$ 为周期即 $y\left(x+\omega\right)=y\left(x\right)$, 当且仅当 $e^{-\int_0^\omega p}=1$, 亦即 $\int_0^\omega p\left(t\right)dt=0$, 等价于 $\overline p=0$. (1) 得证.

由**非齐次线性方程的通解(积分因子法)**, 当 $q\left(x\right)$ 不恒为零时, 方程的通解为
$$
y\left(x\right)=e^{-\int_0^x p}\left[C+\int_0^x q\left(s\right)e^{\int_0^s p}ds\right].
$$

记 $P_\omega=\int_0^\omega p\left(t\right)dt,\ I=\int_0^\omega q\left(s\right)e^{\int_0^s p}ds$. 解以 $\omega$ 为周期等价于 $y\left(\omega\right)=y\left(0\right)=C$. 代入通解, 得
$$
e^{-P_\omega}\left(C+I\right)=C.
$$

当 $P_\omega\neq0$ 即 $\overline p\neq0$ 时, $e^{-P_\omega}\neq1$, 可唯一解出
$$
C=\frac{e^{-P_\omega}I}{1-e^{-P_\omega}}=\frac{I}{e^{P_\omega}-1},
$$

故存在唯一的 $\omega$ 周期解. 当 $P_\omega=0$ 即 $\overline p=0$ 时, 上式化为 $C+I=C$, 即 $I=0$; 而 $q\left(x\right)$ 不恒为零时一般 $I\neq0$, 此时无解, 即使 $I=0$ 也有无穷多个 $C$ 使解为周期解, 唯一性不成立. 故有唯一周期解当且仅当 $\overline p\neq0$, 该唯一周期解为
$$
y\left(x\right)=e^{-\int_0^x p\left(t\right)dt}\left[\frac{\int_0^\omega q\left(s\right)e^{\int_0^s p\left(t\right)dt}ds}{e^{\int_0^\omega p\left(t\right)dt}-1}+\int_0^x q\left(s\right)e^{\int_0^s p\left(t\right)dt}ds\right].
$$

$\blacksquare$
