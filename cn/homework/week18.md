# week18

> **基础知识: 存在和唯一性定理 (线性微分方程组)**<br>$\frac{\mathrm dy}{\mathrm dx}=A\left(x\right)y+f\left(x\right)$ 的解在整个区间上存在唯一.

> **引理 6.1 (齐次线性方程组解的叠加原理)**<br>齐次解的线性组合仍是齐次解.

> **定理 6.1 (齐次线性微分方程组的通解结构)**<br>通解为 $n$ 个线性无关解的线性组合.

> **引理 6.2 (齐次线性方程组解空间的维数)**<br>解空间为 $n$ 维.

> **定理 6.2 (朗斯基行列式判别法)**<br>解组线性无关当且仅当 $W\left(x\right)\ne0$.

> **引理 6.3 (朗斯基行列式的刘维尔公式)**<br>$W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm ds}$.

> **定理 6.3 (非齐次线性微分方程组的通解结构)**<br>$y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^x\Phi^{-1}\left(s\right)f\left(s\right)\mathrm ds$.

> **引理 6.4 (非齐次线性方程组解的结构)**<br>非齐次解 $=$ 齐次通解 $+$ 特解.
---

## 6-1 题1(1)

求 $\frac{\mathrm dy}{\mathrm dt}=\begin{bmatrix}\frac1t&0\\0&\frac1t\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(1)

分量独立, $y_1=C_1t$, $y_2=C_2t$. $\blacksquare$

---

## 6-1 题1(3)

求 $\frac{\mathrm dy}{\mathrm dt}=\begin{bmatrix}0&1\\-1&0\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(3)

$y_1=C_1\cos t+C_2\sin t$, $y_2=-C_1\sin t+C_2\cos t$. $\blacksquare$

---

## 6-1 题2(2)

求解初值问题: $x'=\frac{2t}{1+t^2}x$, $y'=-\frac1t y+x+t$, $x\left(1\right)=0$, $y\left(1\right)=\frac43$.

### 解答 6-1 题2(2)

$x\equiv0$. $y=\frac{t^2}3+\frac1t$. $\blacksquare$

---

## 6-1 题3

证明向量函数组 $\begin{bmatrix}1\\0\\0\end{bmatrix}$, $\begin{bmatrix}x\\0\\0\end{bmatrix}$, $\begin{bmatrix}x^2\\0\\0\end{bmatrix}$ 线性无关.

### 解答 6-1 题3

多项式恒等 $C_1+C_2x+C_3x^2=0$ 蕴含 $C_1=C_2=C_3=0$. $\blacksquare$

---

## 6-1 题4

证明基解矩阵完全决定齐次方程组.

### 解答 6-1 题4

由**定理 6.2 (朗斯基行列式判别法)**, $\Phi$ 可逆, 故 $A\Phi=B\Phi$ 蕴含 $A=B$. $\blacksquare$

---

## 6-1 题6

证明非齐次方程组恰有 $n+1$ 个线性无关解.

### 解答 6-1 题6

由**引理 6.4 (非齐次线性方程组解的结构)** 与**引理 6.2 (齐次线性方程组解空间的维数)**, 非齐次解之差为齐次解, 齐次解空间为 $n$ 维, 故非齐次解至多 $n+1$ 个线性无关. 取特解 $y^*$ 加基本解组即得 $n+1$ 个. $\blacksquare$
