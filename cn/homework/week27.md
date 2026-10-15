# 作业 27

> **定理 10.7**(大范围首次积分与保守系统)<br>对于三维自治系统 $\frac{dx}{dt}=E,\ \frac{dy}{dt}=F,\ \frac{dz}{dt}=G$, 若它在大范围区域 $\Omega$ 内有两个互相独立的驻定首次积分 $\Phi_1=C_1,\ \Phi_2=C_2$, 则该系统在 $\Omega$ 内是一个保守系统或等价于一个保守系统. 其推导为: 由首次积分充要条件 $\frac{\partial\Phi_i}{\partial x}E+\frac{\partial\Phi_i}{\partial y}F+\frac{\partial\Phi_i}{\partial z}G\equiv0$ 解出 $\left(E,F,G\right)$ 与雅可比量 $L=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(y,z\right)},\ M=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(z,x\right)},\ N=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(x,y\right)}$ 成比例, 即 $L=\mu E,\ M=\mu F,\ N=\mu G$; 再由恒等式 $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$ 得 $\frac{\partial\left(\mu E\right)}{\partial x}+\frac{\partial\left(\mu F\right)}{\partial y}+\frac{\partial\left(\mu G\right)}{\partial z}\equiv0$.

> **散度与保守系统**<br>向量场 $\left(E,F,G\right)$ 的散度为 $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}$. 当 $\mu$ 为常数时, 上式成为 $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}=0$, 即散度等于零, 称该系统为保守系统. 当 $\mu$ 不是常数时, 称 $\mu\left(x,y,z\right)$ 为拟积分因子, 此时原系统经参数变换 $d\tau=\frac{dt}{\mu}$ 化为等价的保守系统 $\frac{dx}{d\tau}=\mu E,\ \frac{dy}{d\tau}=\mu F,\ \frac{dz}{d\tau}=\mu G$.

> **第二章的恰当方程与积分因子理论**<br>对于对称形式的一阶方程 $Pdx+Qdy=0$, 它是恰当方程(即存在 $\Phi$ 使 $d\Phi=Pdx+Qdy$)的充要条件为 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$; 当它不是恰当方程时, 若有因子 $\mu\left(x,y\right)$ 使 $\mu Pdx+\mu Qdy=0$ 成为恰当方程, 则称 $\mu$ 为该方程的积分因子.

### 习题一

(习题 10-4 题1)对一般的自治系统 $\frac{dx_i}{dt}=f_i\left(x_1,\cdots,x_n\right)$($i=1,2,\cdots,n,\ n\ge2$) 建立类似于定理 10.7 的理论; 并且当 $n=2$ 时说明上述分析就是在第二章中大范围的恰当方程或积分因子的理论.

### 解答 习题一

第一步, 把**定理 10.7**(大范围首次积分与保守系统) 推广到 $n$ 维. 设 $n$ 维自治系统 $\frac{dx_i}{dt}=f_i$($i=1,\cdots,n$) 在区域 $\Omega$ 内有 $n-1$ 个互相独立的驻定首次积分 $\Phi_1,\cdots,\Phi_{n-1}$. 由首次积分的充要条件, 有恒等式

$$
\sum_{i=1}^n f_i\frac{\partial\Phi_k}{\partial x_i}\equiv0\quad\left(k=1,\cdots,n-1\right).
$$

因为 $\Phi_1,\cdots,\Phi_{n-1}$ 互相独立, 这 $n-1$ 个梯度 $\nabla\Phi_k$ 线性无关, 而向量 $f=\left(f_1,\cdots,f_n\right)$ 与它们都垂直, 故 $f$ 落在一维正交补空间中. 定义广义叉乘向量

$$
L_i=\left(-1\right)^{i-1}\frac{D\left(\Phi_1,\cdots,\Phi_{n-1}\right)}{D\left(x_1,\cdots,\widehat{x_i},\cdots,x_n\right)}\quad\left(i=1,\cdots,n\right),
$$

其中 $\widehat{x_i}$ 表示去掉变元 $x_i$. 按行列式的拉普拉斯展开, 有 $\sum_{i=1}^nL_i\frac{\partial\Phi_k}{\partial x_i}\equiv0$, 故 $L$ 与 $f$ 成比例:

$$
L_i=\mu f_i\quad\left(i=1,\cdots,n\right).
$$

另一方面, 与三维时 $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$ 同理(要求各 $\Phi_k$ 二次连续可微), 有

$$
\sum_{i=1}^n\frac{\partial L_i}{\partial x_i}\equiv0.
$$

代入 $L_i=\mu f_i$, 得

$$
\sum_{i=1}^n\frac{\partial\left(\mu f_i\right)}{\partial x_i}\equiv0.
$$

当 $\mu$ 为常数时, 此即 $\sum_{i=1}^n\frac{\partial f_i}{\partial x_i}=0$, 系统散度为零, 是保守系统; 当 $\mu$ 不是常数时, $\mu$ 为拟积分因子, 经参数变换 $d\tau=\frac{dt}{\mu}$ 后系统化为保守系统. 于是得到推广结论: 若 $n$ 维自治系统在大范围区域内有 $n-1$ 个互相独立的驻定首次积分, 则它是保守系统或等价于一个保守系统.

第二步, 取 $n=2$. 此时系统为 $\frac{dx}{dt}=f_1,\ \frac{dy}{dt}=f_2$, 沿轨线有 $\frac{dy}{dx}=\frac{f_2}{f_1}$. 它只有 $n-1=1$ 个首次积分 $\Phi\left(x,y\right)=C$. 按上述广义叉乘, 取 $i=1,2$:

$$
L_1=\frac{D\left(\Phi\right)}{D\left(y\right)}=\frac{\partial\Phi}{\partial y},\quad L_2=-\frac{D\left(\Phi\right)}{D\left(x\right)}=-\frac{\partial\Phi}{\partial x},
$$

于是 $L_i=\mu f_i$ 即 $\frac{\partial\Phi}{\partial y}=\mu f_1,\ -\frac{\partial\Phi}{\partial x}=\mu f_2$. 推广后的散度恒等式成为

$$
\frac{\partial L_1}{\partial x}+\frac{\partial L_2}{\partial y}
=\frac{\partial\left(\mu f_1\right)}{\partial x}+\frac{\partial\left(\mu f_2\right)}{\partial y}\equiv0.
$$

而沿首次积分解有 $d\Phi=\frac{\partial\Phi}{\partial x}dx+\frac{\partial\Phi}{\partial y}dy=-\mu f_2\,dx+\mu f_1\,dy=0$, 即对称形式 $Pdx+Qdy=0$ 其中 $P=-\mu f_2,\ Q=\mu f_1$. 由**定理 2.1**(恰当方程的判别与通积分公式), 其恰当性条件 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$ 正是

$$
-\frac{\partial\left(\mu f_2\right)}{\partial y}=\frac{\partial\left(\mu f_1\right)}{\partial x},
$$

它与上面的散度恒等式完全一致. 因此 $n=2$ 时这里的 $\mu$ 恰是第二章中的积分因子: 当 $\mu$ 为常数时原方程本身已是恰当方程, 当 $\mu$ 不是常数时它是把原方程化为恰当方程的积分因子. 故上述大范围分析就是第二章中大范围的恰当方程与积分因子理论. $\blacksquare$
