# 作业 12

> **定义 4.1**(奇解)<br>设一阶微分方程 $$F\left(x,y,\frac{dy}{dx}\right)=0$$ 有特解 $\Gamma:y=\varphi\left(x\right)$($x\in J$). 如果对每一点 $Q\in\Gamma$, 在 $Q$ 点的任何邻域内该方程有一个不同于 $\Gamma$ 的解在 $Q$ 点与 $\Gamma$ 相切, 则称 $\Gamma$ 是该微分方程的奇解.

> **定理 4.1**(奇解的必要条件即 $p$-判别式)<br>设函数 $F\left(x,y,p\right)$ 对 $\left(x,y,p\right)\in G$ 是连续的, 而且对 $y$ 和 $p$ 有连续的偏微商 $F_y'$ 和 $F_p'$. 若函数 $y=\varphi\left(x\right)$($x\in J$)是微分方程的一个奇解, 并且 $\left(x,\varphi\left(x\right),\varphi'\left(x\right)\right)\in G$, 则奇解 $y=\varphi\left(x\right)$ 满足 $p$-判别式 $$\begin{cases}F\left(x,y,p\right)=0,\\F_p'\left(x,y,p\right)=0,\end{cases}\quad\left(p=\frac{dy}{dx}\right).$$ 从 $p$-判别式中消去 $p$ 所得方程所决定的曲线称为 $p$-判别曲线. 奇解必是一条 $p$-判别曲线. 但须注意, 由 $p$-判别式确定的函数不一定是解, 即使是解也不一定是奇解, 仍须按**定义 4.1**(奇解)经过验证.

> **定理 4.2**(奇解的充分条件)<br>设函数 $F\left(x,y,p\right)$ 对 $\left(x,y,p\right)\in G$ 是二阶连续可微的. 又设由 $p$-判别式消去 $p$ 后得到的函数 $y=\psi\left(x\right)$($x\in J$)是微分方程的解, 而且条件 $$F_y'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0,\quad F_{pp}''\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0$$ 以及 $$F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$$ 对 $x\in J$ 成立, 则 $y=\psi\left(x\right)$ 是微分方程的奇解.

### 习题一

(习题 4-2 题1(3))利用 $p$-判别式求微分方程 $\left(y-1\right)^2\left(\frac{dy}{dx}\right)^2=\frac{4}{9}y$ 的奇解.

### 解答 习题一

记 $p=\frac{dy}{dx}$, 则 $F\left(x,y,p\right)=\left(y-1\right)^2p^2-\frac{4}{9}y=0$. 由**定理 4.1**(奇解的必要条件即 $p$-判别式), 先写出 $p$-判别式

$$
\begin{cases}
\left(y-1\right)^2p^2-\frac{4}{9}y=0,\\
F_p'\left(x,y,p\right)=2p\left(y-1\right)^2=0.
\end{cases}
$$

由第二式得 $p=0$(另一可能 $y=1$ 代入第一式得 $-\frac{4}{9}=0$, 不成立). 将 $p=0$ 代入第一式, 得 $-\frac{4}{9}y=0$, 即 $y=0$.

验证 $y=0$ 确是解: 此时 $p=y'=0$, $F\left(x,0,0\right)=\left(0-1\right)^2\cdot0-\frac{4}{9}\cdot0=0$. 再由**定理 4.2**(奇解的充分条件)检查条件: 在 $\left(x,0,0\right)$ 处, $F_y'=2\left(y-1\right)p^2-\frac{4}{9}=-\frac{4}{9}\neq0$, $F_{pp}''=2\left(y-1\right)^2=2\neq0$, $F_p'=2p\left(y-1\right)^2=0$, 三条件均满足. 故 $y=0$ 是该微分方程的奇解. $\blacksquare$

### 习题二

(习题 4-2 题3)研究下面的例子, 说明**定理 4.2**(奇解的充分条件)中条件 $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ 是不可缺少的: $y=2x+\frac{dy}{dx}-\frac{1}{3}\left(\frac{dy}{dx}\right)^3$.

### 解答 习题二

记 $p=\frac{dy}{dx}$, 则 $F\left(x,y,p\right)=y-2x-p+\frac{1}{3}p^3=0$. 由**定理 4.1**(奇解的必要条件即 $p$-判别式), $p$-判别式为

$$
\begin{cases}
y-2x-p+\frac{1}{3}p^3=0,\\
F_p'\left(x,y,p\right)=-1+p^2=0.
\end{cases}
$$

由第二式得 $p=\pm1$. 分别代回第一式: 当 $p=1$ 时, $y=2x+\frac{2}{3}$; 当 $p=-1$ 时, $y=2x-\frac{2}{3}$.

先验证这两条 $p$-判别曲线是否为解. 直线 $y=2x-\frac{2}{3}$ 的斜率为 $y'=2$, 代入方程左端 $F\left(x,2x-\frac{2}{3},2\right)=\left(2x-\frac{2}{3}\right)-2x-2+\frac{8}{3}=0$, 故它是解. 而直线 $y=2x+\frac{2}{3}$ 的斜率亦为 $2$, 代入得 $F\left(x,2x+\frac{2}{3},2\right)=\frac{2}{3}-2+\frac{8}{3}=\frac{4}{3}\neq0$, 不是解.

对解 $y=2x-\frac{2}{3}$, 检查**定理 4.2**(奇解的充分条件)的条件: $F_y'=1\neq0$, $F_{pp}''=2p=4\neq0$, 这两个不等式条件成立; 但第三个条件要求 $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$, 而此处 $\psi'\left(x\right)=2$, 故

$$
F_p'\left(x,2x-\frac{2}{3},2\right)=-1+2^2=3\neq0,
$$

即条件 $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ 不成立.

最后按**定义 4.1**(奇解)验证 $y=2x-\frac{2}{3}$ 是否为奇解. 在该直线上任取一点, 过该点的其他积分曲线满足 $F=0$, 即 $y_0-2x_0-p+\frac{1}{3}p^3=0$. 代入 $y_0=2x_0-\frac{2}{3}$, 得 $-\frac{2}{3}-p+\frac{1}{3}p^3=0$, 即 $p^3-3p-2=0=\left(p-2\right)\left(p+1\right)^2$. 故其他积分曲线在该点的斜率为 $p=-1$, 它与直线的斜率 $2$ 不相等, 即在该点只是相交而不相切. 因此 $y=2x-\frac{2}{3}$ 不是奇解. 这说明仅有 $y=\psi\left(x\right)$ 是解及两个不等式条件还不够, 条件 $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ 不可缺少. $\blacksquare$

### 习题三

(习题 4-2 题4)设连续函数 $E\left(y\right)$ 满足条件 $E\left(0\right)=0$, 而当 $0<y\le1$ 时 $E\left(y\right)\neq0$, 则 $y=0$ 是微分方程 $\frac{dy}{dx}=E\left(y\right)$ 的奇解当且仅当瑕积分 $\int_0^1\frac{dy}{E\left(y\right)}$ 收敛.

### 解答 习题三

记 $p=\frac{dy}{dx}$, 则 $F\left(x,y,p\right)=p-E\left(y\right)=0$. 因 $E\left(0\right)=0$, 故 $y=0$ 是方程的一个解.

先求通解. 分离变量得 $\frac{dy}{E\left(y\right)}=dx$, 积分得

$$
x=\int\frac{dy}{E\left(y\right)}+C.
$$

由**定义 4.1**(奇解), $y=0$ 是奇解, 当且仅当在 $y=0$ 上每一点的任何邻域内, 都有另一条积分曲线在该点与 $y=0$ 相切.

若瑕积分 $\int_0^1\frac{dy}{E\left(y\right)}$ 收敛, 则从某 $y_0>0$ 出发的非平凡积分曲线到达 $y=0$ 所走过的横坐标为有限量 $\int_0^{y_0}\frac{dy}{E\left(y\right)}$. 即非平凡积分曲线在有限横坐标处就与 $y=0$ 相遇; 相遇处其斜率 $p=E\left(y\right)\to E\left(0\right)=0$, 与 $y=0$ 的斜率 $0$ 相同, 故两者在该点相切. 因而在 $y=0$ 上任一点附近都有其他积分曲线与 $y=0$ 相切, $y=0$ 是奇解.

若瑕积分 $\int_0^1\frac{dy}{E\left(y\right)}$ 发散, 则从 $y_0>0$ 出发的非平凡积分曲线须经过无限长的横坐标才能使 $y\to0$, 即它们只在横坐标趋于无穷时渐近地逼近 $y=0$, 而不在任何有限点与 $y=0$ 相遇. 因而在 $y=0$ 上任一点附近都没有其他积分曲线与它相切, $y=0$ 不是奇解.

综上, $y=0$ 是奇解当且仅当 $\int_0^1\frac{dy}{E\left(y\right)}$ 收敛. $\blacksquare$
