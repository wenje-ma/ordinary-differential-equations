# 作业 11

> **一阶隐式微分方程**<br>作为对第二章初等积分法的补充, 本节讨论一阶隐式方程 $$F\left(x,y,\frac{dy}{dx}\right)=0$$ 的几个特殊解法. 这里隐式的含义, 是指在方程中未知函数的微商 $\frac{dy}{dx}$ 没有预先表示为 $x,y$ 的显函数.

> **微分法**<br>设从一阶隐式方程中可显式解出未知函数 $$y=f\left(x,p\right),$$ 其中 $p=\frac{dy}{dx}$. 设函数 $f\left(x,p\right)$ 对 $\left(x,p\right)$ 连续可微, 则由上式对 $x$ 进行微分, 得到 $$\left[f_x\left(x,p\right)-p\right]dx+f_p\left(x,p\right)dp=0.$$ 这是关于变量 $x$ 和 $p$ 的一阶显式微分方程. 若能求得其通解 $p=u\left(x,C\right)$, 则原方程的通解为 $y=f\left(x,u\left(x,C\right)\right)$; 若其通解易写成 $x=v\left(p,C\right)$ 的形式, 则原方程的通解可写成 $$\begin{cases}x=v\left(p,C\right),\\y=f\left(v\left(p,C\right),p\right),\end{cases}$$ 其中 $p$ 视作参变量.

> **参数法**<br>设微分方程不明显包含自变量, 即 $$F\left(y,p\right)=0.$$ 作为 $y$ 和 $p$ 之间的联系, 在 $Oyp$ 平面上它一般表示若干条曲线. 设 $$y=g\left(t\right),\quad p=h\left(t\right)$$ 是其中一条的参数表示, 其中设 $h\left(t\right)\neq0$. 由 $dy=p\,dx$ 可得 $dx=\frac{g'\left(t\right)}{h\left(t\right)}dt$, 再积分得原方程的通解 $$x=\int\frac{g'\left(t\right)}{h\left(t\right)}dt+C,\quad y=g\left(t\right).$$ 同理, 对不明显包含未知函数的方程 $F\left(x,p\right)=0$, 可取参数表示 $x=f\left(t\right),\ p=h\left(t\right)$, 则由 $dy=p\,dx$ 得 $dy=h\left(t\right)f'\left(t\right)dt$, 通解为 $$y=\int h\left(t\right)f'\left(t\right)dt+C,\quad x=f\left(t\right).$$

### 习题一

(习题 4-1 题1(1))求解微分方程 $2y=p^2+4px+2x^2$(其中 $p=\frac{dy}{dx}$).

### 解答 习题一

由**微分法**, 先把方程解出 $y=f\left(x,p\right)$ 的形式. 原方程即

$$
y=\frac{1}{2}p^2+2px+x^2.
$$

对 $x$ 进行微分, 注意 $\frac{dy}{dx}=p$, 且 $f_x=2p+2x,\ f_p=p+2x$, 得

$$
p=\left(2p+2x\right)+\left(p+2x\right)\frac{dp}{dx}.
$$

整理得

$$
-\left(p+2x\right)=\left(p+2x\right)\frac{dp}{dx}.
$$

于是或者 $p+2x=0$, 或者 $\frac{dp}{dx}=-1$.

当 $\frac{dp}{dx}=-1$ 时, $p=-x+C$, 代回 $y=\frac{1}{2}p^2+2px+x^2$, 得通解

$$
y=-\frac{1}{2}x^2+Cx+\frac{C^2}{2}.
$$

当 $p+2x=0$ 即 $p=-2x$ 时, 代回得特解

$$
y=-x^2.
$$

其中特解 $y=-x^2$ 不含于通解之中. $\blacksquare$

### 习题二

(习题 4-1 题1(3))求解微分方程 $2xp=2\tan y+p^3\cos^2 y$(其中 $p=\frac{dy}{dx}$).

### 解答 习题二

由**微分法**, 把方程解出 $x=f\left(y,p\right)$ 的形式, 并视 $y$ 为自变量, 此时 $\frac{dx}{dy}=\frac{1}{p}$. 原方程即

$$
x=\frac{\tan y}{p}+\frac{p^2}{2}\cos^2 y.
$$

对 $y$ 进行微分, 其中 $\frac{\partial}{\partial y}\left(\frac{\tan y}{p}\right)=\frac{\sec^2 y}{p}$, $\frac{\partial}{\partial y}\left(\frac{p^2}{2}\cos^2 y\right)=-p^2\sin y\cos y$, $\frac{\partial}{\partial p}=-\frac{\tan y}{p^2}+p\cos^2 y$, 得

$$
\frac{1}{p}=\frac{\sec^2 y}{p}-p^2\sin y\cos y+\left(-\frac{\tan y}{p^2}+p\cos^2 y\right)\frac{dp}{dy}.
$$

两端乘以 $p$ 并整理, 利用 $1-\sec^2 y=-\tan^2 y$, 得

$$
-\tan^2 y+p^3\sin y\cos y=\left(-\frac{\tan y}{p}+p^2\cos^2 y\right)\frac{dp}{dy}.
$$

令 $u=p\cos y$, 则左端 $=\frac{\sin y}{\cos^2 y}\left(u^3-\sin y\right)$, 右端括号 $=\frac{u^3-\sin y}{u}$, 故上式化为

$$
\left(u^3-\sin y\right)\left(\frac{\sin y}{\cos^2 y}-\frac{1}{u}\frac{dp}{dy}\right)=0.
$$

当 $\frac{\sin y}{\cos^2 y}=\frac{1}{u}\frac{dp}{dy}$ 时, 由 $\frac{du}{dy}=\frac{dp}{dy}\cos y-p\sin y=\frac{u\sin y}{\cos y}-\frac{u\sin y}{\cos y}=0$, 得 $u=C$, 即 $p\cos y=C$. 代回 $x=\frac{\tan y}{p}+\frac{p^2}{2}\cos^2 y$, 得 $\frac{\tan y}{p}=\frac{\sin y}{C}$ 及 $\frac{p^2}{2}\cos^2 y=\frac{C^2}{2}$, 故通解为

$$
x=\frac{\sin y}{C}+\frac{C^2}{2},
$$

亦即 $\sin y=Cx-\frac{C^3}{2}$.

当 $u^3=\sin y$ 时, 即 $\left(\sin y\right)^{1/3}=u$, 代回得 $\frac{\tan y}{p}=\frac{\sin y}{u}=\left(\sin y\right)^{2/3}$ 及 $\frac{p^2}{2}\cos^2 y=\frac{u^2}{2}=\frac{1}{2}\left(\sin y\right)^{2/3}$, 故特解为

$$
x=\frac{3}{2}\left(\sin y\right)^{2/3}.
$$

$\blacksquare$

### 习题三

(习题 4-1 题2(2))用参数法求解微分方程 $x^2-3\left(\frac{dy}{dx}\right)^2=1$.

### 解答 习题三

由**参数法**, 该方程不明显包含未知函数 $y$, 属 $F\left(x,p\right)=0$ 型, 其中 $p=\frac{dy}{dx}$. 对曲线 $x^2-3p^2=1$ 取参数表示

$$
x=\cosh t,\quad p=\frac{1}{\sqrt{3}}\sinh t.
$$

由 $dy=p\,dx$, 且 $\frac{dx}{dt}=\sinh t$, 得

$$
dy=\frac{1}{\sqrt{3}}\sinh t\cdot\sinh t\,dt=\frac{1}{\sqrt{3}}\sinh^2 t\,dt.
$$

积分, 利用 $\int\sinh^2 t\,dt=\frac{1}{2}\left(\sinh t\cosh t-t\right)$, 得

$$
y=\frac{1}{2\sqrt{3}}\left(\sinh t\cosh t-t\right)+C.
$$

故原方程的通解为参数式

$$
\begin{cases}
x=\cosh t,\\
y=\frac{1}{2\sqrt{3}}\left(\sinh t\cosh t-t\right)+C.
\end{cases}
$$

$\blacksquare$

### 习题四

(习题 4-1 题2(4))用参数法求解微分方程 $x^3+\left(\frac{dy}{dx}\right)^3=4x\frac{dy}{dx}$.

### 解答 习题四

由**参数法**, 该方程不明显包含未知函数 $y$, 属 $F\left(x,p\right)=0$ 型, 其中 $p=\frac{dy}{dx}$. 对曲线 $x^3+p^3=4xp$ 取参数 $p=tx$, 代入得 $x^3\left(1+t^3\right)=4tx^2$, 故

$$
x=\frac{4t}{1+t^3},\quad p=\frac{4t^2}{1+t^3}.
$$

由 $dy=p\,dx$, 且 $\frac{dx}{dt}=\frac{4\left(1-2t^3\right)}{\left(1+t^3\right)^2}$, 得

$$
dy=\frac{4t^2}{1+t^3}\cdot\frac{4\left(1-2t^3\right)}{\left(1+t^3\right)^2}dt=\frac{16t^2\left(1-2t^3\right)}{\left(1+t^3\right)^3}dt.
$$

令 $u=1+t^3$, 则 $du=3t^2dt$ 且 $1-2t^3=3-2u$, 积分得

$$
y=\frac{16}{3}\int\frac{3-2u}{u^3}du+C=-\frac{8}{u^2}+\frac{32}{3u}+C.
$$

故原方程的通解为参数式

$$
\begin{cases}
x=\frac{4t}{1+t^3},\\
y=-\frac{8}{\left(1+t^3\right)^2}+\frac{32}{3\left(1+t^3\right)}+C.
\end{cases}
$$

$\blacksquare$
