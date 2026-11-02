# week22

> **基础知识: 常点与奇点**
> 
> $A\left(x_0\right)\ne0$ 时常点, $A\left(x_0\right)=0$ 时奇点.

> **定理 7.2 (常点邻域内幂级数解的存在与递推)**
> 
> $p,q$ 解析时, 方程在常点邻域内有收敛幂级数解 $y=\sum C_n\left(x-x_0\right)^n$.

---

## 7-2 题3

求解埃尔米特方程 $y''-2xy'+\lambda y=0$.

### 解答 7-2 题3

由**定理 7.2 (常点邻域内幂级数解的存在与递推)**, 递推公式 $a_{n+2}=\frac{2n-\lambda}{\left(n+2\right)\left(n+1\right)}a_n$. $\blacksquare$

---

## 7-2 题4

求 $y''+\left(\sin x\right)y=0$ 在 $x=0$ 处的两个幂级数解.

### 解答 7-2 题4

由**定理 7.2 (常点邻域内幂级数解的存在与递推)**, $y_1=1-\frac{x^3}6+\frac{x^5}{120}+\cdots$, $y_2=x-\frac{x^4}{12}+\frac{x^6}{180}+\cdots$. $\blacksquare$
