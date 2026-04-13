# week7

> **定理 5.1 (解对参数的连续依赖性)**
> 
> $f$ 连续且对 $y$ 满足利普希茨条件时, 解 $y=\varphi\left(x,\lambda\right)$ 连续.

> **定理 5.2 (解对初值的大范围连续依赖性)**
> 
> 局部利普希茨条件下, 解在有界闭区间上对初值连续依赖.

> **定理 5.3 (解对参数的连续可微性)**
> 
> $f$ 对 $y$ 和 $\lambda$ 有连续偏微商时, 解连续可微.

> **引理 6.1 (齐次线性方程组解的叠加原理)**
> 
> 齐次解的线性组合仍是齐次解.

> **定理 6.1 (齐次线性微分方程组的通解结构)**
> 
> 通解为 $n$ 个线性无关解的线性组合.

> **引理 6.2 (齐次线性方程组解空间的维数)**
> 
> 解空间为 $n$ 维.

> **定理 6.2 (朗斯基行列式判别法)**
> 
> 解组线性无关当且仅当 $W\left(x\right)\ne0$.

> **引理 6.3 (朗斯基行列式的刘维尔公式)**
> 
> $W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm{d}s}$.

> **定理 6.3 (非齐次线性微分方程组的通解结构)**
> 
> $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^x\Phi^{-1}\left(s\right)f\left(s\right)\mathrm{d}s$.

> **引理 6.4 (非齐次线性方程组解的结构)**
> 
> 非齐次解 $=$ 齐次通解 $+$ 特解.

## 5-4 题1

证明 $z=\frac{\partial\varphi}{\partial\lambda}$ 满足变分方程.

### 解答 5-4 题1

由**定理 5.3 (解对参数的连续可微性)** 与雅可比矩阵, 对积分方程两端关于 $\lambda$ 求导, 得 $\frac{\mathrm{d}z}{\mathrm{d}x}=Az+B$, $z\left(x_0\right)=0$.

$\blacksquare$

## 5-4 题2

求 $z=\frac{\partial\varphi}{\partial\eta}$ 满足的方程.

### 解答 5-4 题2

由**定理 5.3 的推论 (解对初值的连续可微性)** 与变分方程, 对积分方程 $\varphi=\eta+\int{f}\mathrm{d}t$ 关于 $\eta$ 求导, 得 $\frac{\mathrm{d}z}{\mathrm{d}x}=f_y\left(x,\varphi\right)z$, $z\left(x_0\right)=I_n$.

$\blacksquare$

## 6-1 题1(1)

求 $\frac{\mathrm{d}y}{\mathrm{d}t}=\begin{bmatrix}\frac1t&0\\0&\frac1t\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(1)

分量独立, $y_1=C_1t$, $y_2=C_2t$.

$\blacksquare$

## 6-1 题1(3)

求 $\frac{\mathrm{d}y}{\mathrm{d}t}=\begin{bmatrix}0&1\\-1&0\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(3)

$y_1=C_1\cos{t}+C_2\sin{t}$, $y_2=-C_1\sin{t}+C_2\cos{t}$.

$\blacksquare$

## 6-1 题2(2)

求解初值问题: $x'=\frac{2t}{1+t^2}x$, $y'=-\frac1ty+x+t$, $x\left(1\right)=0$, $y\left(1\right)=\frac43$.

### 解答 6-1 题2(2)

$x\equiv0$. $y=\frac{t^2}3+\frac1t$.

$\blacksquare$

## 6-1 题3

证明向量函数组 $\begin{bmatrix}1\\0\\0\end{bmatrix}$, $\begin{bmatrix}x\\0\\0\end{bmatrix}$, $\begin{bmatrix}x^2\\0\\0\end{bmatrix}$ 线性无关.

### 解答 6-1 题3

多项式恒等 $C_1+C_2x+C_3x^2=0$ 蕴含 $C_1=C_2=C_3=0$.

$\blacksquare$

## 6-1 题4

证明基解矩阵完全决定齐次方程组.

### 解答 6-1 题4

由**定理 6.2 (朗斯基行列式判别法)**, $\Phi$ 可逆, 故 $A\Phi=B\Phi$ 蕴含 $A=B$.

$\blacksquare$

## 6-1 题6

证明非齐次方程组恰有 $n+1$ 个线性无关解.

### 解答 6-1 题6

由**引理 6.4 (非齐次线性方程组解的结构)** 与**引理 6.2 (齐次线性方程组解空间的维数)**, 非齐次解之差为齐次解, 齐次解空间为 $n$ 维, 故非齐次解至多 $n+1$ 个线性无关. 取特解 $y^*$ 加基本解组即得 $n+1$ 个.

$\blacksquare$

## 6-2 题1(2)

求 $y'=\begin{bmatrix}0&a\\-a&0\end{bmatrix}y$ 的通解.

### 解答 6-2 题1(2)

由**引理 6.6 (方程组有指数型非零解的充要条件)**, 特征根 $\lambda=\pm{i}a$. 由附注 2 (从复值解提取实值解的方法), 取实部虚部得 $y=C_1\begin{bmatrix}\cos{a}x\\-\sin{a}x\end{bmatrix}+C_2\begin{bmatrix}\sin{a}x\\\cos{a}x\end{bmatrix}$.

$\blacksquare$
