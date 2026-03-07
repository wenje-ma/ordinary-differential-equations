# week2

> **定理 2.1 (恰当方程的判别与通积分公式)**
> 
> 方程 $P\mathrm{d}x+Q\mathrm{d}y=0$ 为恰当方程的充要条件是 $\frac{\partial{P}}{\partial{y}}\equiv\frac{\partial{Q}}{\partial{x}}$.

## 2-2 题1(5)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}=\left(\cos{x}\cos2y\right)^2$.

### 解答 2-2 题1(5)

由变量分离方程, 分离变量积分得 $\tan2y=x+\frac12\sin2x+C$. 特解 $y=\frac{2k+1}4\pi$.

$\blacksquare$

## 2-2 题2(2)

求解初值问题 $x\mathrm{d}x+ye^{-x}\mathrm{d}y=0$, $y\left(0\right)=1$.

### 解答 2-2 题2(2)

分离变量积分得 $\frac{y^2}2=e^x\left(1-x\right)+C$. 代入初值得 $y^2=2e^x\left(1-x\right)-1$.

$\blacksquare$

## 2-2 题2(4)

求解初值问题 $\frac{\mathrm{d}y}{\mathrm{d}x}=\frac{\ln\left|x\right|}{1+y^2}$, $y\left(1\right)=0$.

### 解答 2-2 题2(4)

分离变量积分得 $y+\frac{y^3}3=x\ln\left|x\right|-x+C$. 代入初值得 $y+\frac{y^3}3=x\ln\left|x\right|-x+1$.

$\blacksquare$

## 2-2 题3(2)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}=ay$.

### 解答 2-2 题3(2)

由变量分离方程, $y=C_1e^{ax}$.

$\blacksquare$

## 2-2 题3(4)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}=y^n$ ($n=\frac13,1,2$).

### 解答 2-2 题3(4)

$n=\frac13$: $y=\pm\left[\frac23\left(x+C\right)\right]^{3/2}$; $n=1$: $y=Ce^x$; $n=2$: $y=-\frac1{x+C}$. 均补特解 $y\equiv0$.

$\blacksquare$

## 2-2 题5

证明: $y=a$ 上解局部唯一当且仅当 $\left|\int_a^{a\pm\varepsilon}\frac{\mathrm{d}y}{f\left(y\right)}\right|=+\infty$.

### 解答 2-2 题5

充分性: 若瑕积分发散, 则非常数解不能在有限横坐标处到达 $y=a$. 必要性: 若瑕积分收敛, 则可构造拼接解.

$\blacksquare$

## 2-3 题1(2)

求解 $\frac{\mathrm{d}y}{\mathrm{d}x}+y\tan{x}=\sin2x$.

### 解答 2-3 题1(2)

由非齐次线性方程的通解 (积分因子法), 积分因子 $\mu=\sec{x}$. 积分得 $y\sec{x}=-2\cos{x}+C$, 故 $y=C\cos{x}-2\cos^2x$.

$\blacksquare$

## 2-3 题1(4)

求解初值问题 $\frac{\mathrm{d}y}{\mathrm{d}x}-\frac1{1-x^2}y=1+x$, $y\left(0\right)=1$.

### 解答 2-3 题1(4)

积分因子 $\mu=\sqrt{\frac{1-x}{1+x}}$. 积分得 $\mu{y}=1+\frac12\left(x\sqrt{1-x^2}+\arcsin{x}\right)$. 故 $y=\sqrt{\frac{1+x}{1-x}}\left[1+\frac12\left(x\sqrt{1-x^2}+\arcsin{x}\right)\right]$.

$\blacksquare$

## 2-3 题3

证明: 若 $y'+a\left(x\right)y\le0$, 则 $\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^xa\left(s\right)\mathrm{d}s}$.

### 解答 2-3 题3

取积分因子 $A\left(x\right)=e^{\int_0^xa\left(s\right)\mathrm{d}s}$, 则 $\frac{\mathrm{d}}{\mathrm{d}x}\left(Ay\right)\le0$, 故 $Ay$ 单调不增.

$\blacksquare$
