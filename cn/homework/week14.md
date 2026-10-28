# week14

> **基础知识: 首次积分**<br>由高阶方程积分一次所得含任意常数的关系式. 对自治方程 $y''=f\left(y,y'\right)$, 以 $y'$ 乘后左端为全微分.

> **基础知识: 单摆方程与线性单摆方程**<br>$\theta''+a^2\sin\theta=0$, 线性化后 $\theta''+a^2\theta=0$, 周期 $T=2\pi\sqrt{\frac lg}$.

---

## 5-1 题1

利用线性单摆方程估计重力加速度 $g$.

### 解答 5-1 题1

由**基础知识: 单摆方程与线性单摆方程**, $g=\frac{4\pi^2l}{T^2}$. 测量摆长 $l$ 与周期 $T$ 即可. $\blacksquare$

---

## 5-1 题2

证明单摆振动不等时且可发生进动.

### 解答 5-1 题2

由**基础知识: 首次积分**, 得 $\frac12v^2+\frac{a^2}2x^2-\frac{a^2}{24}x^4=E$. 周期 $T\left(A\right)=\frac4a\int_0^{\pi/2}\frac{\mathrm d\varphi}{\sqrt{1-\frac{A^2}{12}\left(1+\sin^2\varphi\right)}}>\frac{2\pi}a$, 随振幅增大而增大. $E>\frac32a^2$ 时轨线不封闭, 对应进动. $\blacksquare$
