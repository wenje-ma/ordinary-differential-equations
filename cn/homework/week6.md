# week6

> **基础知识: 积分因子**<br>若 $\mu\left(x,y\right)P\mathrm dx+\mu Q\mathrm dy=0$ 为恰当方程, 则称 $\mu$ 为积分因子.

> **定理 2.5 (只依赖于 $y$ 的积分因子)**<br>充要条件为 $\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}P=H\left(y\right)$ 只依赖于 $y$, 此时 $\mu\left(y\right)=e^{\int H\left(y\right)\mathrm dy}$.

> **定理 2.6 (积分因子与通积分的任意函数之积)**<br>若 $\mu$ 是积分因子且 $\mu P\mathrm dx+\mu Q\mathrm dy=d\Phi$, 则 $\mu g\left(\Phi\right)$ 也是积分因子.

---

## 2-5 题1(2)

求解 $y\mathrm dx+\left(2xy-e^{-2y}\right)\mathrm dy=0$.

### 解答 2-5 题1(2)

由**定理 2.5 (只依赖于 $y$ 的积分因子)**, $\mu=\frac{e^{2y}}y$. 乘后得 $xe^{2y}-\ln|y|=C$. 特解 $y\equiv0$. $\blacksquare$

---

## 2-5 题1(4)

求解 $y\mathrm dx-\left(x^2+y^2+x\right)\mathrm dy=0$.

### 解答 2-5 题1(4)

由**定理 2.6 (积分因子与通积分的任意函数之积)**, 取 $\mu=\frac1{x^2+y^2}$. 积分得 $\arctan\frac xy=y+C$. $\blacksquare$

---

## 2-5 题2

证明: 存在形如 $\mu=\mu\left(\varphi\left(x,y\right)\right)$ 的积分因子的充要条件.

### 解答 2-5 题2

由 $\frac{\mu'}{\mu}=\frac{P_y-Q_x}{Q\varphi_x-P\varphi_y}=f\left(\varphi\right)$, 得 $\mu=e^{\int f\left(\varphi\right)\mathrm d\varphi}$. $\blacksquare$

---

## 2-5 题4

证明定理 2.6 及其逆定理.

### 解答 2-5 题4

正方向: $\mu g\left(\Phi\right)$ 乘后为全微分. 逆定理: $d\Psi=\frac{\mu_1}{\mu}d\Phi$, 故 $\Psi$ 只是 $\Phi$ 的函数. $\blacksquare$
