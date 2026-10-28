# week5

> **基础知识: 齐次方程**<br>若 $P,Q$ 为同次齐次函数, 令 $y=ux$ 化为变量分离方程.

> **基础知识: 可化为齐次的方程**<br>$\frac{\mathrm dy}{\mathrm dx}=\frac{ax+by+c}{mx+ny+l}$, 当 $\Delta=an-bm\ne0$ 时平移化为齐次方程.

> **基础知识: 伯努利方程**<br>$\frac{\mathrm dy}{\mathrm dx}+p\left(x\right)y=q\left(x\right)y^n$ ($n\ne0,1$). 令 $z=y^{1-n}$ 化为一阶线性方程.

> **基础知识: 里卡蒂方程**<br>$\frac{\mathrm dy}{\mathrm dx}=p\left(x\right)y^2+q\left(x\right)y+r\left(x\right)$.

---

## 2-4 题1(2)

求解 $y'=\frac{2y-x+5}{2x-y-4}$.

### 解答 2-4 题1(2)

由**基础知识: 可化为齐次的方程**, 平移 $x=\xi+1$, $y=\eta-2$. 令 $\eta=u\xi$, 分离变量积分得 $\frac{\eta-\xi}{\left(\eta+\xi\right)^3}=C$. 代回得 $y-x+3=C\left(x+y+1\right)^3$. $\blacksquare$

---

## 2-4 题1(4)

求解 $y'=x^3y^3-xy$.

### 解答 2-4 题1(4)

由**基础知识: 伯努利方程**, 令 $z=y^{-2}$, 得 $z'-2xz=-2x^3$. 积分因子 $e^{-x^2}$, 解得 $\frac1{y^2}=x^2+1+Ce^{x^2}$. 特解 $y\equiv0$. $\blacksquare$

---

## 2-4 题2(2)

求解 $\left(3uv+v^2\right)\mathrm du+\left(u^2+uv\right)\mathrm dv=0$.

### 解答 2-4 题2(2)

由**基础知识: 齐次方程**, 令 $v=wu$, 分离变量积分得 $u^2v\left(v+2u\right)=C$. $\blacksquare$

---

## 2-4 题2(4)

求解 $\frac{\mathrm dy}{\mathrm dx}=\frac{2x^3+3xy^2-7x}{3x^2y+2y^3-8y}$.

### 解答 2-4 题2(4)

令 $u=x^2$, $v=y^2$. 由**基础知识: 可化为齐次的方程**, 平移后令 $\eta=w\xi$, 积分得 $x^2+y^2-3=C\left(x^2-y^2-1\right)^5$. $\blacksquare$

---

## 2-4 题4

将二阶方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 化为里卡蒂方程.

### 解答 2-4 题4

令 $z=\frac{y'}y$, 则 $z'=-z^2-p\left(x\right)z-q\left(x\right)$, 即**基础知识: 里卡蒂方程**. $\blacksquare$
