# 作业 3

> **变量分离方程**<br>考虑对称形式的一阶微分方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0.$$ 若其中 $P\left(x,y\right)=X\left(x\right)Y_1\left(y\right)$ 与 $Q\left(x,y\right)=X_1\left(x\right)Y\left(y\right)$ 均可分解为 $x$ 的函数与 $y$ 的函数之积, 则称它为变量分离方程. 当 $X_1\left(x\right)Y_1\left(y\right)\neq0$ 时, 以 $X_1\left(x\right)Y_1\left(y\right)$ 除方程两端, 得 $$\frac{X\left(x\right)}{X_1\left(x\right)}dx+\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=0,$$ 它的通积分为 $$\int\frac{X\left(x\right)}{X_1\left(x\right)}dx+\int\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=C.$$ 此外还须补上不在通积分之内的特解 $x=a_i$($a_i$ 是 $X_1\left(x\right)=0$ 的根)与 $y=b_j$($b_j$ 是 $Y_1\left(y\right)=0$ 的根).

### 习题一

(习题 2-2 题1(3))求解微分方程 $\frac{dy}{dx}+y^2\sin x=0$, 并指出该方程在 $Oxy$ 平面上有意义的区域.

### 解答 习题一

原方程即 $\frac{dy}{dx}=-y^2\sin x$, 右端在全平面 $Oxy$ 上连续, 故方程在全平面有意义. 由**变量分离方程**, 当 $y\neq0$ 时分离变量, 得
$$
\frac{dy}{y^2}=-\sin x\,dx.
$$

两端积分, 得 $-\frac{1}{y}=\cos x+C$, 即
$$
y=-\frac{1}{\cos x+C}.
$$

此外, 分离变量时假定了 $y\neq0$, 而 $y\equiv0$ 直接满足原方程, 是通积分之外应补上的特解. $\blacksquare$

### 习题二

(习题 2-2 题1(5))求解微分方程 $\frac{dy}{dx}=\left(\cos x\cos 2y\right)^2$, 并指出该方程在 $Oxy$ 平面上有意义的区域.

### 解答 习题二

右端 $\cos^2x\cos^22y$ 在全平面连续, 故方程在全平面有意义. 由**变量分离方程**, 当 $\cos 2y\neq0$ 时分离变量, 得
$$
\frac{dy}{\cos^22y}=\cos^2x\,dx.
$$

两端积分, 即 $\int\sec^22y\,dy=\int\cos^2x\,dx$, 得 $\frac{1}{2}\tan 2y=\frac{x}{2}+\frac{\sin 2x}{4}+C$, 整理为
$$
\tan 2y=x+\frac{1}{2}\sin 2x+C.
$$

此外, $\cos 2y=0$ 给出应补上的特解 $y=\frac{2k+1}{4}\pi$($k$ 为整数). $\blacksquare$

### 习题三

(习题 2-2 题2(2))求解初值问题 $x\,dx+ye^{-x}dy=0,\ y\left(0\right)=1$.

### 解答 习题三

由**变量分离方程**, 以 $e^x$ 乘方程两端后分离变量, 得
$$
y\,dy=-x e^x\,dx.
$$

两端积分. 右端分部积分 $\int x e^x dx=\left(x-1\right)e^x$, 故
$$
\frac{y^2}{2}=-\left(x-1\right)e^x+C=e^x\left(1-x\right)+C.
$$

即 $y^2=2e^x\left(1-x\right)+C_1$. 代入初值条件 $y\left(0\right)=1$, 得 $1=2+C_1$, 即 $C_1=-1$, 故所求解为
$$
y^2=2e^x\left(1-x\right)-1.
$$

$\blacksquare$

### 习题四

(习题 2-2 题2(4))求解初值问题 $\frac{dy}{dx}=\frac{\ln\left|x\right|}{1+y^2},\ y\left(1\right)=0$.

### 解答 习题四

由**变量分离方程**, 分离变量, 得
$$
\left(1+y^2\right)dy=\ln\left|x\right|\,dx.
$$

两端积分, 左端为 $y+\frac{y^3}{3}$, 右端分部积分 $\int\ln\left|x\right|dx=x\ln\left|x\right|-x$, 故
$$
y+\frac{y^3}{3}=x\ln\left|x\right|-x+C.
$$

代入初值条件 $y\left(1\right)=0$, 得 $0=-1+C$, 即 $C=1$, 故所求解为
$$
y+\frac{y^3}{3}=x\ln\left|x\right|-x+1.
$$

$\blacksquare$

### 习题五

(习题 2-2 题3(2))求解微分方程 $\frac{dy}{dx}=ay$($a\neq0$ 为常数), 并作出积分曲线族的简图.

### 解答 习题五

由**变量分离方程**, 当 $y\neq0$ 时分离变量, 得
$$
\frac{dy}{y}=a\,dx.
$$

两端积分, 得 $\ln\left|y\right|=ax+C$, 即
$$
y=C_1 e^{ax}.
$$

当 $C_1=0$ 时即得特解 $y\equiv0$, 它已包含在通解之中. 积分曲线族是一族以 $x$ 轴为渐近线, 按指数规律升降的曲线, $a>0$ 时随 $x$ 增大而指数增长, $a<0$ 时随 $x$ 增大而指数衰减. $\blacksquare$

### 习题六

(习题 2-2 题3(4))求解微分方程 $\frac{dy}{dx}=y^n$($n=\frac{1}{3},1,2$), 并作出积分曲线族的简图.

### 解答 习题六

由**变量分离方程**, 分别讨论三个 $n$ 值.

当 $n=\frac{1}{3}$ 时, $y\neq0$, 分离变量得 $y^{-1/3}dy=dx$, 积分得 $\frac{3}{2}y^{2/3}=x+C$, 即
$$
y=\pm\left[\frac{2}{3}\left(x+C\right)\right]^{3/2},
$$

外加应补上的特解 $y\equiv0$. 积分曲线为半立方抛物线, 并在 $x$ 轴上与 $y=0$ 相接.

当 $n=1$ 时, $y\neq0$, 分离变量得 $\frac{dy}{y}=dx$, 积分得
$$
y=Ce^x,
$$

其中 $C=0$ 对应特解 $y\equiv0$, 已包含在通解中. 积分曲线为指数曲线族.

当 $n=2$ 时, $y\neq0$, 分离变量得 $\frac{dy}{y^2}=dx$, 积分得 $-\frac{1}{y}=x+C$, 即
$$
y=-\frac{1}{x+C},
$$

外加应补上的特解 $y\equiv0$. 积分曲线为双曲线族, 以直线 $x=-C$ 为铅直渐近线. $\blacksquare$

### 习题七

(习题 2-2 题5)设微分方程 $\frac{dy}{dx}=f\left(y\right)$, 其中 $f\left(y\right)$ 在 $y=a$ 的某邻域(例如区间 $\left[a-\epsilon,a+\epsilon\right]$)内连续, 而且 $f\left(y\right)=0$ 当且仅当 $y=a$. 试证: 在直线 $y=a$ 上的每一点, 方程的解是局部唯一的, 当且仅当瑕积分 $\left|\int_a^{a\pm\epsilon}\frac{dy}{f\left(y\right)}\right|=+\infty$(发散).

### 解答 习题七

由于 $f\left(y\right)$ 在 $\left[a-\epsilon,a+\epsilon\right]$ 上连续且仅在 $y=a$ 处为零, 故 $f\left(y\right)$ 在 $\left(a,a+\epsilon\right)$ 与 $\left(a-\epsilon,a\right)$ 上均保持固定的符号. 直线 $y\equiv a$ 本身恒为方程的解. 问题在于能否另有非常数解在某一点 $\left(x_0,a\right)$ 处到达直线 $y=a$.

先证充分性. 设两个单侧瑕积分均发散. 任取过 $\left(x_0,a\right)$ 的一个解 $y=y\left(x\right)$, 设它非常数, 则在 $x_0$ 附近 $y\left(x\right)\neq a$. 由**变量分离方程**, 分离变量后对非常数解有
$$
x-x_0=\int_a^{y\left(x\right)}\frac{ds}{f\left(s\right)}.
$$

当 $y\left(x\right)\to a$ 时, 右端按假设发散到 $+\infty$, 即 $x-x_0\to+\infty$, 与 $x-x_0$ 为有限值矛盾. 故过 $\left(x_0,a\right)$ 不可能有非常数解, 唯一解即 $y\equiv a$, 局部唯一成立.

再证必要性. 设某一侧瑕积分收敛, 例如 $\int_a^{a+\epsilon}\frac{dy}{f\left(y\right)}=I$ 为有限值. 不妨设在 $\left(a,a+\epsilon\right)$ 上 $f\left(y\right)>0$. 取定 $x_1$, 由**变量分离方程**, 过 $\left(x_1,a+\epsilon\right)$ 的解满足
$$
x-x_1=\int_{a+\epsilon}^{y}\frac{ds}{f\left(s\right)}.
$$

令 $y\to a^{+}$, 右端趋于 $\int_{a+\epsilon}^{a}\frac{ds}{f\left(s\right)}=-I$, 为有限值. 于是该解在有限横坐标 $x_1-I$ 处到达 $y=a$. 将此解在 $x\le x_1-I$ 时与直线 $y=a$ 拼接, 即得过 $\left(x_1-I,a\right)$ 而区别于 $y\equiv a$ 的另一个解, 局部唯一性被破坏. 故瑕积分必须发散. $\blacksquare$
