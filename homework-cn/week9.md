# week9

> **命题 1 (矩阵幂级数的绝对收敛性与矩阵指数函数的定义)**
> 
> $e^A=\sum_{k=0}^\infty\frac1{k!}A^k$.

> **例 1 (由一个非零解构造通解的公式)**
> 
> $y=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^x\frac1{\varphi^2\left(s\right)}e^{-\int_{x_0}^sp\left(t\right)\mathrm{d}t}\mathrm{d}s\right]$.

> **命题 2 (矩阵指数函数的性质)**
> 
> $e^{A+B}=e^Ae^B$ ($AB=BA$); $\left(e^A\right)^{-1}=e^{-A}$; $e^{PAP^{-1}}=Pe^AP^{-1}$.

> **推论 3 (常系数非齐次线性微分方程组的通解与初值问题解)**
> 
> $y=e^{xA}c+\int_{x_0}^xe^{\left(x-s\right)A}f\left(s\right)\mathrm{d}s$.

> **定理 6.4 (矩阵指数函数是常系数齐次线性微分方程组的标准基解矩阵)**
> 
> $\Phi\left(x\right)=e^{xA}$ 是标准基解矩阵 ($\Phi\left(0\right)=E$).

> **定理 6.5 ($n$ 个互不相同特征根时的基解矩阵)**
> 
> $\Phi\left(x\right)=\left(e^{\lambda_1x}r_1,\cdots,e^{\lambda_nx}r_n\right)$.

> **引理 6.6 (方程组有指数型非零解的充要条件)**
> 
> $y=e^{\lambda{x}}r$ 是解当且仅当 $\lambda$ 是 $A$ 的特征根, $r$ 为对应特征向量.

> **定理 6.6 (有重特征根时常系数齐次线性微分方程组的基解矩阵)**
> 
> 解为形如 $e^{\lambda_ix}\left(r_0+xr_1+\cdots\right)$ 的线性组合.

> **引理 6.7 (重特征根时确定向量多项式系数的方法)**
> 
> $\lambda_i$ 为 $n_i$ 重根时, 解形如 $e^{\lambda_ix}\left(r_0+xr_1+\cdots\right)$, 其中 $\left(A-\lambda_iE\right)^{n_i}r_0=0$.

## 6-2 题3(4)

求解初值问题 $y'=\begin{bmatrix}16&14&38\\-9&-7&-18\\-4&-4&-11\end{bmatrix}y+\begin{bmatrix}-2e^{-x}\\-3e^{-x}\\2e^{-x}\end{bmatrix}$, $y\left(0\right)=0$.

### 解答 6-2 题3(4)

非齐次项共振于特征根 $\lambda=-1$. 由**推论 3 (常系数非齐次线性微分方程组的通解与初值问题解)**, $y=xe^{-x}\left(-2,-3,2\right)^{\top}$. $\blacksquare$

## 6-2 题4

求解 $\frac{\mathrm{d}}{\mathrm{d}t}\begin{bmatrix}x\\y\end{bmatrix}=\begin{bmatrix}a&-b\\b&a\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}$.

### 解答 6-2 题4

由附注 2 (从复值解提取实值解的方法), 通解为 $C_1e^{at}\left(\cos{b}t,\sin{b}t\right)^{\top}+C_2e^{at}\left(\sin{b}t,-\cos{b}t\right)^{\top}$. $\blacksquare$

## 6-2 题5

证明: 解趋于零当且仅当 $A$ 的所有特征根实部为负.

### 解答 6-2 题5

由**定理 6.6 (有重特征根时常系数齐次线性微分方程组的基解矩阵)**, 解为 $e^{\lambda{x}}$ 乘多项式. 充分性: $\mathrm{Re}\,\lambda<0$ 时多项式增长慢于指数衰减. 必要性: 由**引理 6.6 (方程组有指数型非零解的充要条件)**, 若有 $\mathrm{Re}\,\lambda\ge0$ 的特征根, 对应解不趋于零. $\blacksquare$

## 6-3 题3

(1) 证明 $y''+q\left(x\right)y=0$ 的两解朗斯基行列式为常数. (2) 已知 $y=e^x$ 为解, 求通解与 $q\left(x\right)$.

### 解答 6-3 题3

(1) 由刘维尔公式 (朗斯基行列式的演化公式), $a_1\left(x\right)=0$, 故 $W\left(x\right)\equiv{W}\left(x_0\right)$. (2) $q\left(x\right)=-1$, 通解 $y=C_1e^x+C_2e^{-x}$. $\blacksquare$

## 6-3 题4

证明非零解只有简单零点, 且有限闭区间上零点有限.

### 解答 6-3 题4

由初值问题解的存在唯一性, 若 $\varphi\left(x_0\right)=0$ 且 $\varphi'\left(x_0\right)=0$ 则 $\varphi\equiv0$, 矛盾. 零点孤立, 故有限. $\blacksquare$

## 6-3 题5

证明基本解组唯一确定系数 $p\left(x\right),q\left(x\right)$, 且两解无共同零点.

### 解答 6-3 题5

由**定理 6.2* (解组线性无关的朗斯基行列式判据)**, $W\ne0$, 线性方程组有唯一解. 共同零点蕴含 $W\left(x_0\right)=0$, 矛盾. $\blacksquare$

## 6-3 题6

用常数变易法证明**定理 6.3* (非齐次线性微分方程的通解结构与常数变易公式)**.

### 解答 6-3 题6

设 $y=\sum{C}_k\left(x\right)\varphi_k\left(x\right)$, 令 $\sum{C}_k'\varphi_k^{\left(j\right)}=0$ ($j=0,\cdots,n-2$), 得 $C_k'=\frac{W_k}{W}f$. $\blacksquare$
