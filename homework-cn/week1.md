# week1

> **定义 1.2 (解)**
> 
> 若 $y=\varphi\left(x\right)$ 及其各阶导数代入方程后得到恒等式, 则称 $y=\varphi\left(x\right)$ 为该微分方程在区间 $J$ 上的一个解.

> **定理 2.1 (恰当方程的判别与通积分公式)**
> 
> 方程 $P\mathrm{d}x+Q\mathrm{d}y=0$ 为恰当方程的充要条件是 $\frac{\partial{P}}{\partial{y}}\equiv\frac{\partial{Q}}{\partial{x}}$.

## 1-1 题1(4)

验证 $y=\begin{cases}-\frac14\left(x-C_1\right)^2,&x<{}C_1\\0,&C_1\le{x}\le{C}_2\\\frac14\left(x-C_2\right)^2,&x>{}C_2\end{cases}$ 是 $y'=\sqrt{\left|y\right|}$ 的解.

### 解答 1-1 题1(4)

由**定义 1.2 (解)**, 分三段验证: (1) $x<{}C_1$ 时 $y'=-\frac12\left(x-C_1\right)=\frac12\left(C_1-x\right)=\sqrt{\left|y\right|}$; (2) $C_1\le{x}\le{C}_2$ 时 $y'=0=\sqrt{\left|y\right|}$; (3) $x>{}C_2$ 时 $y'=\frac12\left(x-C_2\right)=\sqrt{\left|y\right|}$. 故 $y$ 是解. $\blacksquare$

## 1-2 题2(3)

求初值问题 $\frac{\mathrm{d}R}{\mathrm{d}t}=-aR$, $R\left(0\right)=1$ 的解.

### 解答 1-2 题2(3)

由微分方程的求解与积分运算, 分离变量积分得 $R=Ce^{-at}$. 代入初值 $R\left(0\right)=1$, 得 $C=1$. 故 $R\left(t\right)=e^{-at}$. $\blacksquare$

## 1-2 题2(4)

求初值问题 $\frac{\mathrm{d}y}{\mathrm{d}x}=1+y^2$, $y\left(x_0\right)=y_0$ 的解.

### 解答 1-2 题2(4)

分离变量积分得 $\arctan{y}=x+C$. 代入初值, 得 $C=\arctan{y}_0-x_0$. 故 $y=\tan\left(x+\arctan{y}_0-x_0\right)$. $\blacksquare$

## 2-1 题3

判断并求解 $\left(ax+by\right)\mathrm{d}x+\left(bx+cy\right)\mathrm{d}y=0$.

### 解答 2-1 题3

$P=ax+by$, $Q=bx+cy$. 由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial{P}}{\partial{y}}=b=\frac{\partial{Q}}{\partial{x}}$. 积分得 $\Phi=\frac{a}2x^2+bxy+\frac{c}2y^2=C$. $\blacksquare$

## 2-1 题6

判断并求解 $\left(ye^x+2e^x+y^2\right)\mathrm{d}x+\left(e^x+2xy\right)\mathrm{d}y=0$.

### 解答 2-1 题6

由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial{P}}{\partial{y}}=e^x+2y=\frac{\partial{Q}}{\partial{x}}$. 积分得 $\Phi=e^x\left(y+2\right)+xy^2=C$. $\blacksquare$

## 2-1 题9

判断并求解 $\frac{2s-1}{t}\mathrm{d}s+\frac{s-s^2}{t^2}\mathrm{d}t=0$.

### 解答 2-1 题9

由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial{P}}{\partial{t}}=-\frac{2s-1}{t^2}=\frac{\partial{Q}}{\partial{s}}$. 积分得 $\Phi=\frac{s^2-s}{t}=C$. $\blacksquare$
