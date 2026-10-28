# week3

> **基础知识: 变量分离方程**<br>若 $P\left(x,y\right)=X\left(x\right)Y_1\left(y\right)$, $Q\left(x,y\right)=X_1\left(x\right)Y\left(y\right)$, 则方程可分离变量为 $\frac{X\left(x\right)}{X_1\left(x\right)}\mathrm dx+\frac{Y\left(y\right)}{Y_1\left(y\right)}\mathrm dy=0$, 通积分为两端积分之和等于常数.

---

## 2-2 题1(3)

求解 $\frac{\mathrm dy}{\mathrm dx}+y^2\sin x=0$.

### 解答 2-2 题1(3)

由**基础知识: 变量分离方程**, 分离变量积分得 $y=-\frac1{\cos x+C}$. 特解 $y\equiv0$. $\blacksquare$

---

## 2-2 题1(5)

求解 $\frac{\mathrm dy}{\mathrm dx}=\left(\cos x\cos2y\right)^2$.

### 解答 2-2 题1(5)

由**基础知识: 变量分离方程**, 分离变量积分得 $\tan2y=x+\frac12\sin2x+C$. 特解 $y=\frac{2k+1}4\pi$. $\blacksquare$

---

## 2-2 题2(2)

求解初值问题 $x\mathrm dx+ye^{-x}\mathrm dy=0$, $y\left(0\right)=1$.

### 解答 2-2 题2(2)

分离变量积分得 $\frac{y^2}2=e^x\left(1-x\right)+C$. 代入初值得 $y^2=2e^x\left(1-x\right)-1$. $\blacksquare$

---

## 2-2 题2(4)

求解初值问题 $\frac{\mathrm dy}{\mathrm dx}=\frac{\ln|x|}{1+y^2}$, $y\left(1\right)=0$.

### 解答 2-2 题2(4)

分离变量积分得 $y+\frac{y^3}3=x\ln|x|-x+C$. 代入初值得 $y+\frac{y^3}3=x\ln|x|-x+1$. $\blacksquare$

---

## 2-2 题3(2)

求解 $\frac{\mathrm dy}{\mathrm dx}=ay$.

### 解答 2-2 题3(2)

由**基础知识: 变量分离方程**, $y=C_1e^{ax}$. $\blacksquare$

---

## 2-2 题3(4)

求解 $\frac{\mathrm dy}{\mathrm dx}=y^n$ ($n=\frac13,1,2$).

### 解答 2-2 题3(4)

$n=\frac13$: $y=\pm\left[\frac23\left(x+C\right)\right]^{3/2}$; $n=1$: $y=Ce^x$; $n=2$: $y=-\frac1{x+C}$. 均补特解 $y\equiv0$. $\blacksquare$

---

## 2-2 题5

证明: $y=a$ 上解局部唯一当且仅当 $\left|\int_a^{a\pm\varepsilon}\frac{\mathrm dy}{f\left(y\right)}\right|=+\infty$.

### 解答 2-2 题5

充分性: 若瑕积分发散, 则非常数解不能在有限横坐标处到达 $y=a$. 必要性: 若瑕积分收敛, 则可构造拼接解. $\blacksquare$
