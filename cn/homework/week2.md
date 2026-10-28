# week2

> **基础知识: 恰当方程 (全微分方程)**<br>若存在 $\Phi\left(x,y\right)$ 使 $\mathrm d\Phi=P\mathrm dx+Q\mathrm dy$, 则称 $P\mathrm dx+Q\mathrm dy=0$ 为恰当方程, 通积分为 $\Phi\left(x,y\right)=C$.

> **定理 2.1 (恰当方程的判别与通积分公式)**<br>方程 $P\mathrm dx+Q\mathrm dy=0$ 为恰当方程的充要条件是 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$.

---

## 2-1 题3

判断并求解 $\left(ax+by\right)\mathrm dx+\left(bx+cy\right)\mathrm dy=0$.

### 解答 2-1 题3

$P=ax+by$, $Q=bx+cy$. 由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial P}{\partial y}=b=\frac{\partial Q}{\partial x}$. 积分得 $\Phi=\frac a2x^2+bxy+\frac c2y^2=C$. $\blacksquare$

---

## 2-1 题6

判断并求解 $\left(ye^x+2e^x+y^2\right)\mathrm dx+\left(e^x+2xy\right)\mathrm dy=0$.

### 解答 2-1 题6

由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial P}{\partial y}=e^x+2y=\frac{\partial Q}{\partial x}$. 积分得 $\Phi=e^x\left(y+2\right)+xy^2=C$. $\blacksquare$

---

## 2-1 题9

判断并求解 $\frac{2s-1}{t}\mathrm ds+\frac{s-s^2}{t^2}\mathrm dt=0$.

### 解答 2-1 题9

由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial P}{\partial t}=-\frac{2s-1}{t^2}=\frac{\partial Q}{\partial s}$. 积分得 $\Phi=\frac{s^2-s}{t}=C$. $\blacksquare$

---

## 2-1 题10

判断并求解 $xf\left(x^2+y^2\right)\mathrm dx+yf\left(x^2+y^2\right)\mathrm dy=0$.

### 解答 2-1 题10

由**定理 2.1 (恰当方程的判别与通积分公式)**, $\frac{\partial P}{\partial y}=2xyf'=\frac{\partial Q}{\partial x}$. 设 $F'=f$, 则 $\Phi=\frac12F\left(x^2+y^2\right)=C$. $\blacksquare$
