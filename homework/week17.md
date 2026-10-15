# 作业 17

> **定理 5.3**(解对参数的连续可微性)<br>设 $n$ 维向量值函数 $f\left(x,y,\lambda\right)$ 在区域 $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ 上连续, 而且对 $y$ 和 $\lambda$ 有连续的偏微商, 则初值问题 $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ 的解 $y=\varphi\left(x,\lambda\right)$ 在区域 $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$ 上是连续可微的, 其中 $h=\min\left\{a,\frac{b}{M}\right\}$, $M$ 为 $\left|f\left(x,y,\lambda\right)\right|$ 在 $G$ 上的一个上界.

> **定理 5.3 的推论**(解对初值的连续可微性)<br>设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 而且对 $y$ 有连续的偏微商 $f_y\left(x,y\right)$, 则初值问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ 的解 $y=\varphi\left(x,\eta\right)$ 在区域 $D:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$ 上是连续可微的.

> **变分方程**<br>设 $y=\varphi\left(x;x_0,y_0,\lambda\right)$ 是 $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(x_0\right)=y_0$ 的解. 与柯西问题等价的积分方程为 $\varphi\left(x;x_0,y_0,\lambda\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(s,\varphi\left(s;x_0,y_0,\lambda\right),\lambda\right)ds$. 记 $A\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial y}\left(x,\varphi,\lambda\right)$, $B\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial\lambda}\left(x,\varphi,\lambda\right)$. 则 $z=\frac{\partial\varphi}{\partial\lambda}$ 满足 $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z+B\left(x,x_0,y_0,\lambda\right)$, $z\left(x_0\right)=0$; $z=\frac{\partial\varphi}{\partial y_0}$ 满足 $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=1$; $z=\frac{\partial\varphi}{\partial x_0}$ 满足 $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=-f\left(x_0,y_0,\lambda\right)$. 这些方程统称为原方程关于初值和参数的变分方程.

> **雅可比矩阵**<br>向量值函数 $f\left(x,y,\lambda\right)=\left(f_1,\cdots,f_n\right)^T$ 对 $y=\left(y_1,\cdots,y_n\right)^T$ 的雅可比矩阵为 $f_y=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$, 对参数 $\lambda=\left(\lambda_1,\cdots,\lambda_m\right)^T$ 的雅可比矩阵为 $f_\lambda=\left(\frac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. 复合函数求导按矩阵乘法进行: $\frac{\partial f\left(x,\varphi,\lambda\right)}{\partial\lambda_k}=\displaystyle\sum_{j=1}^{n}\frac{\partial f}{\partial y_j}\frac{\partial\varphi_j}{\partial\lambda_k}+\frac{\partial f}{\partial\lambda_k}$.

### 习题一

(习题 5-4 题1)利用**定理 5.3**(解对参数的连续可微性)(在 $y$ 为列向量的情况)证明 $z=\frac{\partial\varphi}{\partial\lambda}\left(x,\lambda\right)=\left(\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)\right)_{n\times m}$ 满足线性(变分)方程 $\frac{dz}{dx}=A\left(x,\lambda\right)z+B\left(x,\lambda\right)$ 和初值条件 $z\left(x_0,\lambda\right)=0$, 其中 $A\left(x,\lambda\right)=f_y'\left(x,\varphi\left(x,\lambda\right),\lambda\right)=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$, $B\left(x,\lambda\right)=f_\lambda'\left(x,\varphi\left(x,\lambda\right),\lambda\right)=\left(\frac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. 试在 $y$ 为行向量的情况考虑相应的变分方程.

### 解答 习题一

考虑柯西问题

$$
\frac{dy}{dx}=f\left(x,y,\lambda\right),\qquad y\left(x_0\right)=y_0,
$$

其中初值 $y_0$ 固定(不依赖于 $\lambda$), $\lambda\in K\subset R^m$. 由**定理 5.3**(解对参数的连续可微性), 其解 $y=\varphi\left(x,\lambda\right)$ 连续可微, 故偏导数 $z=\frac{\partial\varphi}{\partial\lambda}$ 存在且连续.

由**变分方程**中的积分方程等价形式, 有

$$
\varphi\left(x,\lambda\right)=y_0+\int_{x_0}^{x}f\left(s,\varphi\left(s,\lambda\right),\lambda\right)ds.
$$

两端对 $\lambda_k$ 求偏导. 左端为 $\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)=z_{ik}$. 由**雅可比矩阵**的复合求导法则, 右端为

$$
\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)=\int_{x_0}^{x}\left[\sum_{j=1}^{n}\frac{\partial f_i}{\partial y_j}\left(s,\varphi,\lambda\right)\frac{\partial\varphi_j}{\partial\lambda_k}\left(s,\lambda\right)+\frac{\partial f_i}{\partial\lambda_k}\left(s,\varphi,\lambda\right)\right]ds.
$$

注意 $\frac{\partial\varphi_j}{\partial\lambda_k}=z_{jk}$. 上式两端再对 $x$ 求导, 得

$$
\frac{\partial z_{ik}}{\partial x}=\sum_{j=1}^{n}A_{ij}\left(x,\lambda\right)z_{jk}\left(x,\lambda\right)+B_{ik}\left(x,\lambda\right),
$$

其中 $A_{ij}=\frac{\partial f_i}{\partial y_j}$, $B_{ik}=\frac{\partial f_i}{\partial\lambda_k}$. 写成矩阵形式, 即

$$
\frac{dz}{dx}=A\left(x,\lambda\right)z+B\left(x,\lambda\right).
$$

初值条件: 由于 $\varphi\left(x_0,\lambda\right)=y_0$ 与 $\lambda$ 无关, $\frac{\partial\varphi}{\partial\lambda}\left(x_0,\lambda\right)=0$, 故

$$
z\left(x_0,\lambda\right)=0.
$$

列向量情形证毕.

行向量情形: 若 $y$ 取行向量(即 $y$ 为 $1\times n$ 行, 方程组写成 $\frac{dy}{dx}=yA_{\text{行}}\left(x,\lambda\right)+e\left(x,\lambda\right)$ 的形式), 则分量求导公式 $\frac{\partial z_{ik}}{\partial x}=\displaystyle\sum_{j=1}^{n}\frac{\partial f_i}{\partial y_j}z_{jk}+\frac{\partial f_i}{\partial\lambda_k}$ 不变, 但雅可比矩阵按行向量约定右乘, 变分方程写成

$$
\frac{dz}{dx}=z\,A\left(x,\lambda\right)+B\left(x,\lambda\right),
$$

其中 $z=\frac{\partial\varphi}{\partial\lambda}$ 与 $B$ 都取相应的转置排列(阶数为 $m\times n$), 初值条件仍为 $z\left(x_0,\lambda\right)=0$.

$\blacksquare$

### 习题二

(习题 5-4 题2)在本节最后的推论(即**定理 5.3 的推论**(解对初值的连续可微性))中, 试求 $z=\frac{\partial\varphi}{\partial\eta}\left(x,\eta\right)$ 所满足的微分方程和初值条件. (只要求作形式的计算. )

### 解答 习题二

在**定理 5.3 的推论**(解对初值的连续可微性)中, 柯西问题为

$$
\frac{dy}{dx}=f\left(x,y\right),\qquad y\left(x_0\right)=\eta,
$$

其中 $f\left(x,y\right)$ 连续且对 $y$ 有连续偏微商 $f_y\left(x,y\right)$, 解 $y=\varphi\left(x,\eta\right)$.

由**变分方程**中的积分方程等价形式, 有

$$
\varphi\left(x,\eta\right)=\eta+\int_{x_0}^{x}f\left(s,\varphi\left(s,\eta\right)\right)ds.
$$

两端对 $\eta$ 求偏导(记 $z=\frac{\partial\varphi}{\partial\eta}$, 为 $n\times n$ 矩阵), 由**雅可比矩阵**的复合求导法则, 得

$$
z\left(x,\eta\right)=I_n+\int_{x_0}^{x}f_y\left(s,\varphi\left(s,\eta\right)\right)z\left(s,\eta\right)ds,
$$

其中 $I_n$ 为 $n$ 阶单位矩阵. 上式两端再对 $x$ 求导, 得微分方程

$$
\frac{dz}{dx}=f_y\left(x,\varphi\left(x,\eta\right)\right)\,z\left(x,\eta\right).
$$

初值条件: 在积分方程中令 $x=x_0$, 得 $\varphi\left(x_0,\eta\right)=\eta$, 对 $\eta$ 求偏导即得

$$
z\left(x_0,\eta\right)=I_n.
$$

一维(标量)情形时退化为 $\frac{dz}{dx}=f_y\left(x,\varphi\left(x,\eta\right)\right)z$, $z\left(x_0,\eta\right)=1$. 这就是推论中解对初值 $\eta$ 的变分方程.

$\blacksquare$
