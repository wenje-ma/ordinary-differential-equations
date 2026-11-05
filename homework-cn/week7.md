# week7

> **定理 5.1 (解对参数的连续依赖性)**
> 
> $f$ 连续且对 $y$ 满足利普希茨条件时, 解 $y=\varphi\left(x,\lambda\right)$ 连续.

> **定理 5.1 的推论 (解对初值的连续依赖性)**
> 
> 解 $y=\varphi\left(x,\eta\right)$ 在初值附近连续.

> **定理 5.2 (解对初值的大范围连续依赖性)**
> 
> 局部利普希茨条件下, 解在有界闭区间上对初值连续依赖.

> **定理 5.3 (解对参数的连续可微性)**
> 
> $f$ 对 $y$ 和 $\lambda$ 有连续偏微商时, 解连续可微.

> **定理 5.3 的推论 (解对初值的连续可微性)**
> 
> $f_y$ 连续时, 解对初值连续可微.

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

## 5-2 题3

叙述并证明线性微分方程组初值问题解的存在唯一性定理.

### 解答 5-2 题3

$f\left(x,y\right)=A\left(x\right)y+e\left(x\right)$ 连续. 由利普希茨条件, $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le\left\|A\left(x\right)\right\|\left|y_1-y_2\right|$, 局部利普希茨. 由皮卡存在唯一性定理 ($n$ 维向量形式) 局部存在唯一. 由格朗沃尔不等式, 解在有界区间上有界, 故可延拓到整个区间. $\blacksquare$

## 5-3 题2

证明: 若解存在唯一, 则解对初值连续依赖.

### 解答 5-3 题2

由积分方程与柯西问题的等价性 与阿斯科利引理, 任一收敛子列的极限满足积分方程. 由唯一性, 所有子列收敛到同一极限, 故整体一致收敛. $\blacksquare$

## 5-3 题3

举例说明: 不满足唯一性时, 积分曲线族不能局部视作平行直线族.

### 解答 5-3 题3

反例: $y'=3y^{2/3}$. $y\equiv0$ 与 $y=\left(x-c\right)^3$ 均为解, 无穷多条解过原点. 由**定理 5.1 的推论 (解对初值的连续依赖性)**, 一一映射依赖唯一性, 唯一性失效时映射不再一一. $\blacksquare$

## 5-4 题1

证明 $z=\frac{\partial\varphi}{\partial\lambda}$ 满足变分方程.

### 解答 5-4 题1

由**定理 5.3 (解对参数的连续可微性)** 与雅可比矩阵, 对积分方程两端关于 $\lambda$ 求导, 得 $\frac{\mathrm{d}z}{\mathrm{d}x}=Az+B$, $z\left(x_0\right)=0$. $\blacksquare$

## 5-4 题2

求 $z=\frac{\partial\varphi}{\partial\eta}$ 满足的方程.

### 解答 5-4 题2

由**定理 5.3 的推论 (解对初值的连续可微性)** 与变分方程, 对积分方程 $\varphi=\eta+\int{f}\mathrm{d}t$ 关于 $\eta$ 求导, 得 $\frac{\mathrm{d}z}{\mathrm{d}x}=f_y\left(x,\varphi\right)z$, $z\left(x_0\right)=I_n$. $\blacksquare$

## 6-1 题1(1)

求 $\frac{\mathrm{d}y}{\mathrm{d}t}=\begin{bmatrix}\frac1t&0\\0&\frac1t\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(1)

分量独立, $y_1=C_1t$, $y_2=C_2t$. $\blacksquare$

## 6-1 题1(3)

求 $\frac{\mathrm{d}y}{\mathrm{d}t}=\begin{bmatrix}0&1\\-1&0\end{bmatrix}y$ 的通解.

### 解答 6-1 题1(3)

$y_1=C_1\cos{t}+C_2\sin{t}$, $y_2=-C_1\sin{t}+C_2\cos{t}$. $\blacksquare$

## 6-1 题2(2)

求解初值问题: $x'=\frac{2t}{1+t^2}x$, $y'=-\frac1ty+x+t$, $x\left(1\right)=0$, $y\left(1\right)=\frac43$.

### 解答 6-1 题2(2)

$x\equiv0$. $y=\frac{t^2}3+\frac1t$. $\blacksquare$

## 6-1 题3

证明向量函数组 $\begin{bmatrix}1\\0\\0\end{bmatrix}$, $\begin{bmatrix}x\\0\\0\end{bmatrix}$, $\begin{bmatrix}x^2\\0\\0\end{bmatrix}$ 线性无关.

### 解答 6-1 题3

多项式恒等 $C_1+C_2x+C_3x^2=0$ 蕴含 $C_1=C_2=C_3=0$. $\blacksquare$
