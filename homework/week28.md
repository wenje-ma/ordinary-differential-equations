# 作业 28

> **定理 11.1**(齐次线性偏微分方程的通解)<br>设有一阶齐次线性偏微分方程 $\sum_{i=1}^nA_i\left(x_1,\cdots,x_n\right)\frac{\partial u}{\partial x_i}=0$, 其中系数 $A_1,\cdots,A_n$ 连续可微且不同时为零. 其特征方程为对称形式的常微分方程组 $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$, 它是一个 $n-1$ 阶方程组, 有 $n-1$ 个独立的首次积分 $\varphi_i\left(x_1,\cdots,x_n\right)=C_i$($i=1,\cdots,n-1$). 则原偏微分方程的通解为 $u=\psi\left[\varphi_1,\cdots,\varphi_{n-1}\right]$, 其中 $\psi$ 是任意的 $n-1$ 元连续可微函数. 换言之, 函数 $\varphi$ 为特征方程首次积分的充要条件是恒等式 $\sum_{i=1}^nA_i\frac{\partial\varphi}{\partial x_i}\equiv0$ 成立.

### 习题一

(习题 11-1 题1(1))求解偏微分方程 $x_1\frac{\partial y}{\partial x_1}+x_2\frac{\partial y}{\partial x_2}+\cdots+x_n\frac{\partial y}{\partial x_n}=0$($n\ge2$).

### 解答 习题一

由**定理 11.1**(齐次线性偏微分方程的通解), 先写出特征方程

$$
\frac{dx_1}{x_1}=\frac{dx_2}{x_2}=\cdots=\frac{dx_n}{x_n}.
$$

由 $\frac{dx_1}{x_1}=\frac{dx_n}{x_n}$ 得 $\ln\left|x_1\right|-\ln\left|x_n\right|=C$, 即 $\frac{x_1}{x_n}=C_1$; 同理 $\frac{x_2}{x_n}=C_2,\ \cdots,\ \frac{x_{n-1}}{x_n}=C_{n-1}$. 这是 $n-1$ 个独立的首次积分. 故通解为

$$
y=\psi\left(\frac{x_1}{x_n},\frac{x_2}{x_n},\cdots,\frac{x_{n-1}}{x_n}\right),
$$

其中 $\psi$ 是任意的 $n-1$ 元连续可微函数. $\blacksquare$

### 习题二

(习题 11-1 题1(3))求解偏微分方程 $a\left(b^2+c^2\right)\frac{\partial h}{\partial a}+b\left(c^2+a^2\right)\frac{\partial h}{\partial b}+c\left(b^2-a^2\right)\frac{\partial h}{\partial c}=0$.

### 解答 习题二

由**定理 11.1**(齐次线性偏微分方程的通解), 特征方程为

$$
\frac{da}{a\left(b^2+c^2\right)}=\frac{db}{b\left(c^2+a^2\right)}=\frac{dc}{c\left(b^2-a^2\right)}.
$$

设公共比值为 $\lambda$, 则 $da=\lambda a\left(b^2+c^2\right),\ db=\lambda b\left(c^2+a^2\right),\ dc=\lambda c\left(b^2-a^2\right)$. 计算微分

$$
d\left(a^2-b^2+c^2\right)=2a\,da-2b\,db+2c\,dc
=2\lambda\left[a^2\left(b^2+c^2\right)-b^2\left(c^2+a^2\right)+c^2\left(b^2-a^2\right)\right].
$$

括号内化简为 $a^2b^2+a^2c^2-b^2c^2-a^2b^2+b^2c^2-a^2c^2=0$, 故

$$
d\left(a^2-b^2+c^2\right)=0,
$$

即 $\varphi_1=a^2-b^2+c^2=C_1$ 是一个首次积分.

再由 $d\left(a^2\right)=2\lambda a^2\left(b^2+c^2\right)$ 得 $\frac{d\left(a^2\right)}{a^2}=2\lambda\left(b^2+c^2\right)$; 同理 $\frac{d\left(b^2\right)}{b^2}=2\lambda\left(c^2+a^2\right),\ \frac{d\left(c^2\right)}{c^2}=2\lambda\left(b^2-a^2\right)$. 于是

$$
\frac{d\left(a^2\right)}{a^2}-\frac{d\left(b^2\right)}{b^2}=2\lambda\left(b^2-a^2\right)=\frac{d\left(c^2\right)}{c^2},
$$

即 $d\ln\frac{a^2}{b^2}=d\ln c^2$, 故 $\frac{a^2}{b^2c^2}=C_2$ 是另一个独立的首次积分. 因此原偏微分方程的通解为

$$
h=\psi\left(a^2-b^2+c^2,\frac{a^2}{b^2c^2}\right),
$$

其中 $\psi$ 是任意的二元连续可微函数. $\blacksquare$

### 习题三

(习题 11-1 题2(2))求解初值问题 $\begin{cases}\left(x-y^2\right)\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}=0,\\ \text{当 }x=1\text{ 时}, z=f_0(y).\end{cases}$

### 解答 习题三

由**定理 11.1**(齐次线性偏微分方程的通解), 特征方程为

$$
\frac{dx}{x-y^2}=\frac{dy}{y}.
$$

由 $y\,dx=\left(x-y^2\right)dy$ 得 $y\,dx-x\,dy=-y^2\,dy$. 两端除以 $y^2$, 注意到 $\frac{y\,dx-x\,dy}{y^2}=d\left(\frac{x}{y}\right)$, 有

$$
d\left(\frac{x}{y}\right)=-dy,
$$

故 $\frac{x}{y}+y=C$ 是首次积分. 通解为 $z=\psi\left(\frac{x}{y}+y\right)$, 其中 $\psi$ 是任意连续可微函数. 代入初值条件, 当 $x=1$ 时 $z=f_0(y)$, 得

$$
\psi\left(\frac{1}{y}+y\right)=f_0(y).
$$

此式确定函数 $\psi$: 对任意变元 $s$, 取 $y$ 满足 $y+\frac{1}{y}=s$, 则 $\psi(s)=f_0(y)$. 故所求解为

$$
z=\psi\left(\frac{x}{y}+y\right),
$$

其中函数 $\psi$ 由 $\psi\left(y+\frac{1}{y}\right)=f_0(y)$ 确定. $\blacksquare$
