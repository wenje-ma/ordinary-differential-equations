# week8

> **命题 1 (矩阵幂级数的绝对收敛性与矩阵指数函数的定义)**
> 
> $e^A=\sum_{k=0}^\infty\frac1{k!}A^k$.

> **命题 2 (矩阵指数函数的性质)**
> 
> $e^{A+B}=e^Ae^B$ ($AB=BA$); $\left(e^A\right)^{-1}=e^{-A}$; $e^{PAP^{-1}}=Pe^AP^{-1}$.

> **推论 3 (常系数非齐次线性微分方程组的通解与初值问题解)**
> 
> $y=e^{xA}c+\int_{x_0}^x e^{\left(x-s\right)A}f\left(s\right)\mathrm ds$.

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
> $W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm ds}$.

> **定理 6.3 (非齐次线性微分方程组的通解结构)**
> 
> $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^x\Phi^{-1}\left(s\right)f\left(s\right)\mathrm ds$.

> **引理 6.4 (非齐次线性方程组解的结构)**
> 
> 非齐次解 $=$ 齐次通解 $+$ 特解.

> **定理 6.4 (矩阵指数函数是常系数齐次线性微分方程组的标准基解矩阵)**
> 
> $\Phi\left(x\right)=e^{xA}$ 是标准基解矩阵 ($\Phi\left(0\right)=E$).

> **定理 6.5 ($n$ 个互不相同特征根时的基解矩阵)**
> 
> $\Phi\left(x\right)=\left(e^{\lambda_1 x}r_1,\cdots,e^{\lambda_n x}r_n\right)$.

> **引理 6.6 (方程组有指数型非零解的充要条件)**
> 
> $y=e^{\lambda x}r$ 是解当且仅当 $\lambda$ 是 $A$ 的特征根, $r$ 为对应特征向量.

> **定理 6.6 (有重特征根时常系数齐次线性微分方程组的基解矩阵)**
> 
> 解为形如 $e^{\lambda_i x}\left(r_0+xr_1+\cdots\right)$ 的线性组合.

> **引理 6.7 (重特征根时确定向量多项式系数的方法)**
> 
> $\lambda_i$ 为 $n_i$ 重根时, 解形如 $e^{\lambda_i x}\left(r_0+xr_1+\cdots\right)$, 其中 $\left(A-\lambda_iE\right)^{n_i}r_0=0$.

## 6-1 题4

证明基解矩阵完全决定齐次方程组.

### 解答 6-1 题4

由**定理 6.2 (朗斯基行列式判别法)**, $\Phi$ 可逆, 故 $A\Phi=B\Phi$ 蕴含 $A=B$. $\blacksquare$

## 6-1 题6

证明非齐次方程组恰有 $n+1$ 个线性无关解.

### 解答 6-1 题6

由**引理 6.4 (非齐次线性方程组解的结构)** 与**引理 6.2 (齐次线性方程组解空间的维数)**, 非齐次解之差为齐次解, 齐次解空间为 $n$ 维, 故非齐次解至多 $n+1$ 个线性无关. 取特解 $y^*$ 加基本解组即得 $n+1$ 个. $\blacksquare$

## 6-2 题1(2)

求 $y'=\begin{bmatrix}0&a\\-a&0\end{bmatrix}y$ 的通解.

### 解答 6-2 题1(2)

由**引理 6.6 (方程组有指数型非零解的充要条件)**, 特征根 $\lambda=\pm ia$. 由**附注 2 (从复值解提取实值解的方法)**, 取实部虚部得 $y=C_1\begin{bmatrix}\cos ax\\-\sin ax\end{bmatrix}+C_2\begin{bmatrix}\sin ax\\\cos ax\end{bmatrix}$. $\blacksquare$

## 6-2 题1(4)

求 $y'=\begin{bmatrix}1&\frac23&-\frac23\\0&\frac23&\frac13\\0&-\frac13&\frac43\end{bmatrix}y$ 的通解.

### 解答 6-2 题1(4)

由**引理 6.7 (重特征根时确定向量多项式系数的方法)**, $\lambda=1$ 为三重根. 通解为 $C_1e^x\left(1,0,0\right)^\top+C_2e^x\left(0,1,1\right)^\top+C_3e^x\left[\left(0,1,0\right)^\top+x\left(\frac23,-\frac13,-\frac13\right)^\top\right]$. $\blacksquare$

## 6-2 题2(2)

求 $y'=\begin{bmatrix}0&-n^2\\-n^2&0\end{bmatrix}y+\begin{bmatrix}\cos nx\\\sin nx\end{bmatrix}$ 的通解.

### 解答 6-2 题2(2)

齐次通解由**定理 6.5 ($n$ 个互不相同特征根时的基解矩阵)** 给出. 特解设为三角函数形式. 由**推论 3 (常系数非齐次线性微分方程组的通解与初值问题解)**, 通解为齐次通解加特解. $\blacksquare$

## 6-2 题2(4)

求 $y'=\begin{bmatrix}2&1&-2\\-1&0&0\\1&1&-1\end{bmatrix}y+\begin{bmatrix}2-x\\0\\1-x\end{bmatrix}$ 的通解.

### 解答 6-2 题2(4)

特征根 $\lambda=1,\pm i$. 由**附注 2 (从复值解提取实值解的方法)** 取实部虚部. 特解设为一次式 $\left(-1,x,0\right)^\top$. $\blacksquare$

## 6-2 题3(2)

求解初值问题 $y'=\begin{bmatrix}0&-2\\2&0\end{bmatrix}y+\begin{bmatrix}3x\\4\end{bmatrix}$, $y\left(0\right)=\left(2,3\right)^\top$.

### 解答 6-2 题3(2)

由**推论 3 (常系数非齐次线性微分方程组的通解与初值问题解)**, $y=\frac{13}4\begin{bmatrix}\cos2x\\\sin2x\end{bmatrix}-3\begin{bmatrix}\sin2x\\-\cos2x\end{bmatrix}+\begin{bmatrix}-\frac54\\\frac32x\end{bmatrix}$. $\blacksquare$
