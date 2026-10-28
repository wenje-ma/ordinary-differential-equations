# week4

> **基础知识: 一阶线性方程**<br>形如 $\frac{\mathrm dy}{\mathrm dx}+p\left(x\right)y=q\left(x\right)$ 的方程. $q\equiv0$ 时为齐次, 否则为非齐次.

> **基础知识: 齐次线性方程的通解**<br>$y=Ce^{-\int p\left(x\right)\mathrm dx}$.

> **基础知识: 非齐次线性方程的通解 (积分因子法)**<br>积分因子 $\mu\left(x\right)=e^{\int p\left(x\right)\mathrm dx}$, 通解为 $y=e^{-\int p\left(x\right)\mathrm dx}\left[\int q\left(x\right)e^{\int p\left(x\right)\mathrm dx}\mathrm dx+C\right]$.

---

## 2-3 题1(2)

求解 $\frac{\mathrm dy}{\mathrm dx}+y\tan x=\sin2x$.

### 解答 2-3 题1(2)

由**基础知识: 非齐次线性方程的通解 (积分因子法)**, 积分因子 $\mu=\sec x$. 积分得 $y\sec x=-2\cos x+C$, 故 $y=C\cos x-2\cos^2x$. $\blacksquare$

---

## 2-3 题1(4)

求解初值问题 $\frac{\mathrm dy}{\mathrm dx}-\frac1{1-x^2}y=1+x$, $y\left(0\right)=1$.

### 解答 2-3 题1(4)

积分因子 $\mu=\sqrt{\frac{1-x}{1+x}}$. 积分得 $\mu y=1+\frac12\left(x\sqrt{1-x^2}+\arcsin x\right)$. 故 $y=\sqrt{\frac{1+x}{1-x}}\left[1+\frac12\left(x\sqrt{1-x^2}+\arcsin x\right)\right]$. $\blacksquare$

---

## 2-3 题3

证明: 若 $y'+a\left(x\right)y\le0$, 则 $\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^x a\left(s\right)\mathrm ds}$.

### 解答 2-3 题3

取积分因子 $A\left(x\right)=e^{\int_0^x a\left(s\right)\mathrm ds}$, 则 $\frac{\mathrm d}{\mathrm dx}\left(Ay\right)\le0$, 故 $Ay$ 单调不增. $\blacksquare$

---

## 2-3 题4

用常数变易法推导非齐次线性方程的通解.

### 解答 2-3 题4

设 $y=C\left(x\right)e^{-\int p\mathrm dx}$, 代入方程得 $C'\left(x\right)=q\left(x\right)e^{\int p\mathrm dx}$. 积分后即得与积分因子法一致的结果. $\blacksquare$

---

## 2-3 题5

证明: 若 $p,q$ 均以 $\omega$ 为周期, 则方程有唯一 $\omega$ 周期解当且仅当 $\bar p\ne0$.

### 解答 2-3 题5

由**基础知识: 齐次线性方程的通解** 与**基础知识: 非齐次线性方程的通解 (积分因子法)**, $y\left(x+\omega\right)=y\left(x\right)$ 等价于 $e^{-\int_0^\omega p}=1$, 即 $\bar p=0$. 非齐次时唯一周期解当且仅当 $\bar p\ne0$. $\blacksquare$
