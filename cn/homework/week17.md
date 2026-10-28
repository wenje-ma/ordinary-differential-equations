# week17

> **基础知识: 变分方程**<br>$z=\frac{\partial\varphi}{\partial\lambda}$ 满足 $\frac{\mathrm dz}{\mathrm dx}=Az+B$, $z\left(x_0\right)=0$; $z=\frac{\partial\varphi}{\partial y_0}$ 满足 $\frac{\mathrm dz}{\mathrm dx}=Az$, $z\left(x_0\right)=I$.

> **基础知识: 雅可比矩阵**<br>$f_y=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$.

> **定理 5.3 (解对参数的连续可微性)**<br>$f$ 对 $y$ 和 $\lambda$ 有连续偏微商时, 解连续可微.

> **定理 5.3 的推论 (解对初值的连续可微性)**<br>$f_y$ 连续时, 解对初值连续可微.

---

## 5-4 题1

证明 $z=\frac{\partial\varphi}{\partial\lambda}$ 满足变分方程.

### 解答 5-4 题1

由**定理 5.3 (解对参数的连续可微性)** 与**基础知识: 雅可比矩阵**, 对积分方程两端关于 $\lambda$ 求导, 得 $\frac{\mathrm dz}{\mathrm dx}=Az+B$, $z\left(x_0\right)=0$. $\blacksquare$

---

## 5-4 题2

求 $z=\frac{\partial\varphi}{\partial\eta}$ 满足的方程.

### 解答 5-4 题2

由**定理 5.3 的推论 (解对初值的连续可微性)** 与**基础知识: 变分方程**, 对积分方程 $\varphi=\eta+\int f\mathrm dt$ 关于 $\eta$ 求导, 得 $\frac{\mathrm dz}{\mathrm dx}=f_y\left(x,\varphi\right)z$, $z\left(x_0\right)=I_n$. $\blacksquare$
