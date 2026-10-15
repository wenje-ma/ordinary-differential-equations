# 作业 29

> **定理 11.2**(拟线性偏微分方程的隐式通解)<br>设有一阶拟线性偏微分方程 $X\left(x,y,z\right)\frac{\partial z}{\partial x}+Y\left(x,y,z\right)\frac{\partial z}{\partial y}=Z\left(x,y,z\right)$, 其中 $X,Y,Z$ 连续可微且 $X,Y$ 不同时为零. 其相应特征方程为 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$. 设 $u\left(x,y,z\right)=C_1,\ v\left(x,y,z\right)=C_2$ 是该特征方程的两个独立首次积分, 则原拟线性偏微分方程的隐式通解为 $\Phi\left[u\left(x,y,z\right),v\left(x,y,z\right)\right]=0$, 其中 $\Phi$ 是任意连续可微函数, 并要求 $\frac{\partial\Phi}{\partial z}\neq0$ 以便由隐函数解出 $z=z\left(x,y\right)$.

> **定理 11.1**(齐次线性偏微分方程的通解)<br>特征方程 $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$ 的 $n-1$ 个独立首次积分 $\varphi_i=C_i$ 给出齐次线性方程 $\sum_{i=1}^nA_i\frac{\partial u}{\partial x_i}=0$ 的通解 $u=\psi\left(\varphi_1,\cdots,\varphi_{n-1}\right)$. 求特征方程首次积分的方法同样适用于定理 11.2 中 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$ 的情形.

### 习题一

(习题 11-2 题1(2))求偏微分方程 $\left(xy^3-2x^4\right)\frac{\partial z}{\partial x}+\left(2y^4-x^3y\right)\frac{\partial z}{\partial y}=9z\left(x^3-y^3\right)$ 的通解.

### 解答 习题一

由**定理 11.2**(拟线性偏微分方程的隐式通解), 先写特征方程

$$
\frac{dx}{xy^3-2x^4}=\frac{dy}{2y^4-x^3y}=\frac{dz}{9z\left(x^3-y^3\right)}.
$$

令 $u=x^3,\ v=y^3$, 则前两项分母为 $x\left(v-2u\right),\ y\left(2v-u\right)$. 由前两式消去 $x,y$ 得

$$
\frac{du}{dv}=\frac{u\left(v-2u\right)}{v\left(2v-u\right)}.
$$

设 $w=\frac{u}{v}$, 即 $u=wv$, 则 $w+v\frac{dw}{dv}=\frac{w\left(1-2w\right)}{2-w}$, 化简得

$$
v\frac{dw}{dv}=-\frac{w\left(1+w\right)}{2-w}.
$$

分离变量并积分 $\frac{2-w}{w\left(1+w\right)}dw=-\frac{dv}{v}$, 即 $\left(\frac{2}{w}-\frac{3}{1+w}\right)dw=-\frac{dv}{v}$, 得

$$
\frac{u^2v^2}{\left(u+v\right)^3}=C_1.
$$

以 $u=x^3,\ v=y^3$ 代回并开立方, 得第一个首次积分

$$
\varphi_1=\frac{x^2y^2}{x^3+y^3}=C_1.
$$

再求与 $z$ 有关的首次积分. 记公共比值为 $\lambda$, 则 $du=3\lambda u\left(v-2u\right),\ dv=3\lambda v\left(2v-u\right),\ \frac{dz}{z}=9\lambda\left(u-v\right)$. 计算

$$
d\left(u+v\right)=3\lambda\left[u\left(v-2u\right)+v\left(2v-u\right)\right]=6\lambda\left(v^2-u^2\right)=-6\lambda\left(u-v\right)\left(u+v\right).
$$

故 $\frac{d\left(u+v\right)}{u+v}=-6\lambda\left(u-v\right)$, 而 $\frac{dz}{z}=9\lambda\left(u-v\right)$, 两者相比得 $\frac{d\ln\left(u+v\right)}{d\ln z}=-\frac{2}{3}$, 即

$$
\left(u+v\right)^3z^2=C_2.
$$

代回 $u+v=x^3+y^3$, 得第二个首次积分

$$
\varphi_2=\left(x^3+y^3\right)^3z^2=C_2.
$$

由**定理 11.2**(拟线性偏微分方程的隐式通解), 隐式通解为

$$
\Phi\left(\frac{x^2y^2}{x^3+y^3},\ \left(x^3+y^3\right)^3z^2\right)=0,
$$

其中 $\Phi$ 为任意连续可微函数. 若解出 $z$, 可写为

$$
z^2\left(x^3+y^3\right)^3=\psi\left(\frac{x^2y^2}{x^3+y^3}\right),
$$

其中 $\psi$ 为任意连续可微函数. $\blacksquare$

### 习题二

(习题 11-2 题2)求解初值问题 $\begin{cases}\sqrt{x}\frac{\partial f}{\partial x}+\sqrt{y}\frac{\partial f}{\partial y}+\sqrt{z}\frac{\partial f}{\partial z}=f,\\ \text{当 }y=1\text{ 时}, f\left(x,y,z\right)=xz.\end{cases}$

### 解答 习题二

由**定理 11.2**(拟线性偏微分方程的隐式通解), 特征方程为

$$
\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}=\frac{df}{f}.
$$

由 $\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}$ 积分得 $\sqrt{x}-\sqrt{y}=C_1$; 由 $\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}$ 得 $\sqrt{y}-\sqrt{z}=C_2$; 由 $\frac{df}{f}=\frac{dy}{\sqrt{y}}$ 得 $\ln f=2\sqrt{y}+C$, 即 $fe^{-2\sqrt{y}}=C_3$. 故通解为

$$
f=e^{2\sqrt{y}}\psi\left(\sqrt{x}-\sqrt{y},\ \sqrt{y}-\sqrt{z}\right),
$$

其中 $\psi$ 为任意二元连续可微函数. 代入初值条件, 当 $y=1$ 时 $f=xz$, 得

$$
e^{2}\psi\left(\sqrt{x}-1,\ 1-\sqrt{z}\right)=xz.
$$

令 $\xi=\sqrt{x}-1,\ \eta=1-\sqrt{z}$, 则 $x=\left(\xi+1\right)^2,\ z=\left(1-\eta\right)^2$, 故 $\psi\left(\xi,\eta\right)=e^{-2}\left(\xi+1\right)^2\left(1-\eta\right)^2$. 代回通解, 得所求解为

$$
f\left(x,y,z\right)=e^{2\sqrt{y}-2}\left(\sqrt{x}-\sqrt{y}+1\right)^2\left(1-\sqrt{y}+\sqrt{z}\right)^2.
$$

代入 $y=1$ 检验, 得 $f=\left(\sqrt{x}\right)^2\left(\sqrt{z}\right)^2=xz$, 与初值一致. $\blacksquare$
