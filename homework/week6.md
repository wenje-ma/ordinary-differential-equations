# 作业 6

> **积分因子**<br>对方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0,$$ 若存在可微的非零函数 $\mu\left(x,y\right)$, 使乘过它之后的方程 $$\mu\left(x,y\right)P\left(x,y\right)dx+\mu\left(x,y\right)Q\left(x,y\right)dy=0$$ 成为恰当方程, 即满足 $$\frac{\partial}{\partial y}\left(\mu P\right)=\frac{\partial}{\partial x}\left(\mu Q\right),$$ 则称 $\mu\left(x,y\right)$ 为原方程的一个积分因子.

> **定理 2.4**(只依赖于 $x$ 的积分因子)<br>方程有一个只依赖于 $x$ 的积分因子的充要条件是表达式 $$\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q}=G\left(x\right)$$ 只依赖于 $x$ 而与 $y$ 无关; 此时 $\mu\left(x\right)=e^{\int G\left(x\right)dx}$ 是方程的一个积分因子.

> **定理 2.5**(只依赖于 $y$ 的积分因子)<br>方程有一个只依赖于 $y$ 的积分因子的充要条件是表达式 $$\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=H\left(y\right)$$ 只依赖于 $y$; 此时 $\mu\left(y\right)=e^{\int H\left(y\right)dy}$ 是方程的一个积分因子.

> **定理 2.6**(积分因子与通积分的任意函数之积)<br>若 $\mu=\mu\left(x,y\right)$ 是方程的一个积分因子, 使得 $$\mu P\left(x,y\right)dx+\mu Q\left(x,y\right)dy=d\Phi\left(x,y\right),$$ 则 $\mu\left(x,y\right)g\left(\Phi\left(x,y\right)\right)$ 也是方程的一个积分因子, 其中 $g\left(\cdot\right)$ 是任一可微的非零函数.

### 习题一

(习题 2-5 题1(2))求解微分方程 $y\,dx+\left(2xy-e^{-2y}\right)dy=0$.

### 解答 习题一

记 $P\left(x,y\right)=y,\ Q\left(x,y\right)=2xy-e^{-2y}$. 计算得
$$
\frac{\partial P}{\partial y}=1,\qquad\frac{\partial Q}{\partial x}=2y.
$$

二者不恒等, 方程非恰当. 由**定理 2.5**(只依赖于 $y$ 的积分因子), 检查表达式
$$
\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=\frac{2y-1}{y}=2-\frac{1}{y},
$$

它只依赖于 $y$, 故存在只依赖于 $y$ 的积分因子 $\mu\left(y\right)=e^{\int\left(2-\frac{1}{y}\right)dy}=e^{2y-\ln\left|y\right|}=\frac{e^{2y}}{y}$. 以 $\mu\left(y\right)$ 乘原方程, 得恰当方程
$$
e^{2y}dx+\left(2xe^{2y}-\frac{1}{y}\right)dy=0.
$$

设通积分为 $\Phi\left(x,y\right)=C$, 由 $\frac{\partial\Phi}{\partial x}=e^{2y}$ 对 $x$ 积分, 得 $\Phi\left(x,y\right)=xe^{2y}+\psi\left(y\right)$. 再由 $\frac{\partial\Phi}{\partial y}=2xe^{2y}+\psi'\left(y\right)=2xe^{2y}-\frac{1}{y}$, 得 $\psi'\left(y\right)=-\frac{1}{y}$, 即 $\psi\left(y\right)=-\ln\left|y\right|$. 故通积分为
$$
xe^{2y}-\ln\left|y\right|=C.
$$

此外, 乘积分因子时除以了 $y$, 应补上丢失的特解 $y\equiv0$. $\blacksquare$

### 习题二

(习题 2-5 题1(4))求解微分方程 $y\,dx-\left(x^2+y^2+x\right)dy=0$.

### 解答 习题二

把左端重新分组:
$$
\left(y\,dx-x\,dy\right)-\left(x^2+y^2\right)dy=0.
$$

注意到 $d\left(\arctan\frac{x}{y}\right)=\frac{y\,dx-x\,dy}{x^2+y^2}$, 取积分因子 $\mu\left(x,y\right)=\frac{1}{x^2+y^2}$. 由**定理 2.6**(积分因子与通积分的任意函数之积)的分组思想, 以 $\mu$ 乘方程两端, 得
$$
\frac{y\,dx-x\,dy}{x^2+y^2}-dy=0.
$$

第一项即全微分 $d\left(\arctan\frac{x}{y}\right)$, 故
$$
d\left(\arctan\frac{x}{y}\right)-dy=0.
$$

两端积分, 得通积分
$$
\arctan\frac{x}{y}=y+C.
$$

$\blacksquare$

### 习题三

(习题 2-5 题2)证明: 方程 $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ 有形如 $\mu=\mu\left(\varphi\left(x,y\right)\right)$ 的积分因子的充要条件是 $\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q\frac{\partial\varphi}{\partial x}-P\frac{\partial\varphi}{\partial y}}=f\left(\varphi\left(x,y\right)\right)$, 并写出这个积分因子. 然后将结果应用到下述各情形, 得出存在每一种类型积分因子的充要条件: (1) $\mu=\mu\left(x\pm y\right)$; (2) $\mu=\mu\left(x^2+y^2\right)$; (3) $\mu=\mu\left(xy\right)$; (4) $\mu=\mu\left(\frac{y}{x}\right)$; (5) $\mu=\mu\left(x^a y^b\right)$.

### 解答 习题三

设 $\mu=\mu\left(\varphi\left(x,y\right)\right)$. 由**积分因子**的充要条件 $\frac{\partial\left(\mu P\right)}{\partial y}=\frac{\partial\left(\mu Q\right)}{\partial x}$, 展开得
$$
\mu'\left(\varphi\right)\varphi_y P+\mu\frac{\partial P}{\partial y}=\mu'\left(\varphi\right)\varphi_x Q+\mu\frac{\partial Q}{\partial x}.
$$

整理出 $\mu'/\mu$:
$$
\frac{\mu'\left(\varphi\right)}{\mu\left(\varphi\right)}=\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q\varphi_x-P\varphi_y}.
$$

左端只是 $\varphi$ 的函数, 故右端必须也只依赖于 $\varphi\left(x,y\right)$. 反之, 若右端等于某 $\varphi$ 的函数 $f\left(\varphi\right)$, 则 $\frac{d\mu}{\mu}=f\left(\varphi\right)d\varphi$, 积分得 $\mu=e^{\int f\left(\varphi\right)d\varphi}$. 充要条件得证, 该积分因子即
$$
\mu=e^{\int f\left(\varphi\left(x,y\right)\right)d\varphi}.
$$

分别代入各 $\varphi$:

(1) $\varphi=x\pm y$, 则 $\varphi_x=1,\ \varphi_y=\pm1$, 充要条件为
$$
\frac{P_y-Q_x}{Q\mp P}=f\left(x\pm y\right).
$$

(2) $\varphi=x^2+y^2$, 则 $\varphi_x=2x,\ \varphi_y=2y$, 充要条件为
$$
\frac{P_y-Q_x}{2\left(xQ-yP\right)}=f\left(x^2+y^2\right).
$$

(3) $\varphi=xy$, 则 $\varphi_x=y,\ \varphi_y=x$, 充要条件为
$$
\frac{P_y-Q_x}{yQ-xP}=f\left(xy\right).
$$

(4) $\varphi=\frac{y}{x}$, 则 $\varphi_x=-\frac{y}{x^2},\ \varphi_y=\frac{1}{x}$, 充要条件为
$$
\frac{x^2\left(P_y-Q_x\right)}{-\left(yQ+xP\right)}=f\left(\frac{y}{x}\right).
$$

(5) $\varphi=x^a y^b$, 则 $\varphi_x=ax^{a-1}y^b,\ \varphi_y=bx^ay^{b-1}$, 充要条件为
$$
\frac{P_y-Q_x}{x^{a-1}y^{b-1}\left(axQ-byP\right)}=f\left(x^ay^b\right).
$$

$\blacksquare$

### 习题四

(习题 2-5 题4)证明定理 2.6 及其逆定理: 在定理 2.6 的假定下, 若 $\mu_1$ 是微分方程的另一个积分因子, 则 $\mu_1$ 必可表为 $\mu_1=\mu g\left(\Phi\right)$ 的形式, 其中函数 $g$ 和 $\Phi$ 的意义与在定理 2.6 中的相同.

### 解答 习题四

先证正方向即**定理 2.6**(积分因子与通积分的任意函数之积)本身. 已知 $\mu P dx+\mu Q dy=d\Phi$. 两端乘任一可微非零函数 $g\left(\Phi\right)$, 得
$$
g\left(\Phi\right)\left(\mu P dx+\mu Q dy\right)=g\left(\Phi\right)d\Phi=d\left(\int g\left(\Phi\right)d\Phi\right),
$$

右端是某函数的全微分, 故 $\mu g\left(\Phi\right)$ 仍是积分因子.

再证逆定理. 设 $\mu_1$ 是另一个积分因子, 则存在函数 $\Psi\left(x,y\right)$ 使 $\mu_1 P dx+\mu_1 Q dy=d\Psi$. 又 $d\Phi=\mu P dx+\mu Q dy$, 于是
$$
d\Psi=\mu_1P dx+\mu_1Q dy=\frac{\mu_1}{\mu}\left(\mu P dx+\mu Q dy\right)=\frac{\mu_1}{\mu}d\Phi.
$$

记 $r=\frac{\mu_1}{\mu}$, 则 $d\Psi=r\,d\Phi$. 在 $\Phi$ 的任一等值线上 $d\Phi=0$, 从而 $d\Psi=0$, 即 $\Psi$ 在 $\Phi$ 的等值线上为常数, 故 $\Psi$ 只是 $\Phi$ 的函数, $\Psi=\Psi\left(\Phi\right)$. 于是 $d\Psi=\Psi'\left(\Phi\right)d\Phi$, 与 $d\Psi=r\,d\Phi$ 比较得
$$
r=\Psi'\left(\Phi\right)=g\left(\Phi\right).
$$

即 $\frac{\mu_1}{\mu}=g\left(\Phi\right)$, 亦即 $\mu_1=\mu g\left(\Phi\right)$. 逆定理得证. $\blacksquare$
