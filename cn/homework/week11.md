# week11

> **基础知识: 微分法**<br>若 $y=f\left(x,p\right)$, 对 $x$ 微分得 $\left(f_x-p\right)\mathrm dx+f_p\mathrm dp=0$.

> **基础知识: 参数法**<br>对 $F\left(y,p\right)=0$ 或 $F\left(x,p\right)=0$, 取参数表示后由 $\mathrm dy=p\mathrm dx$ 积分.

---

## 4-1 题1(1)

求解 $2y=p^2+4px+2x^2$.

### 解答 4-1 题1(1)

由**基础知识: 微分法**, $y=\frac12p^2+2px+x^2$. 微分得 $\left(p+2x\right)\left(\frac{\mathrm dp}{\mathrm dx}+1\right)=0$. 通解 $y=-\frac12x^2+Cx+\frac{C^2}2$, 特解 $y=-x^2$. $\blacksquare$

---

## 4-1 题1(3)

求解 $2xp=2\tan y+p^3\cos^2y$.

### 解答 4-1 题1(3)

由**基础知识: 微分法**, 令 $u=p\cos y$, 得通解 $\sin y=Cx-\frac{C^3}2$, 特解 $x=\frac32\left(\sin y\right)^{2/3}$. $\blacksquare$

---

## 4-1 题2(2)

用参数法求解 $x^2-3p^2=1$.

### 解答 4-1 题2(2)

由**基础知识: 参数法**, $x=\cosh t$, $p=\frac1{\sqrt3}\sinh t$. 积分得 $y=\frac1{2\sqrt3}\left(\sinh t\cosh t-t\right)+C$. $\blacksquare$

---

## 4-1 题2(4)

用参数法求解 $x^3+p^3=4xp$.

### 解答 4-1 题2(4)

由**基础知识: 参数法**, $x=\frac{4t}{1+t^3}$, $p=\frac{4t^2}{1+t^3}$. 积分得 $y=-\frac8{\left(1+t^3\right)^2}+\frac{32}{3\left(1+t^3\right)}+C$. $\blacksquare$
