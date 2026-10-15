# 作业 15

> **标准微分方程组与向量形式**<br>把未知函数的个数取成等于微分方程的阶数, 所得标准方程组为 $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$($i=1,\cdots,n$). 采用列向量 $y=\left(y_1,\cdots,y_n\right)^T$, $f=\left(f_1,\cdots,f_n\right)^T$, 则向量形式为 $\frac{dy}{dx}=f\left(x,y\right)$, 其中 $f\left(x,y\right)$ 在区域 $D\subset R^{n+1}$ 上连续. 附加初值条件 $y\left(x_0\right)=y_0$ 即得柯西问题.

> **向量的模(范数)及其基本性质**<br>在 $n$ 维线性空间 $R^n$ 中可定义向量的模 $\left|y\right|$, 例如欧几里得模 $\left|y\right|=\sqrt{y_1^2+\cdots+y_n^2}$. 模的基本性质: 对任何 $y,z\in R^n$, 有三角不等式 $\left|y+z\right|\le\left|y\right|+\left|z\right|$. 在引进模以后, $R^n$ 成为 $n$ 维赋范线性空间, 其中可建立相应的微积分学与一致收敛等概念.

> **利普希茨条件**<br>设 $n$ 维向量值函数 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 如果存在常数 $L\ge0$, 使对一切 $\left(x,y_1\right),\left(x,y_2\right)\in R$ 都有 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, 则称 $f$ 在 $R$ 上对 $y$ 满足利普希茨条件.

> **皮卡存在唯一性定理($n$ 维向量形式)**<br>设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 且对 $y$ 满足利普希茨条件. 令 $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$, 则柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left|x-x_0\right|\le h$ 上存在唯一解.

> **佩亚诺存在定理($n$ 维向量形式)**<br>设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 令 $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$, 则柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left|x-x_0\right|\le h$ 上至少存在一个解(不保证唯一性).

> **皮卡序列及其一致收敛估计**<br>与柯西问题等价的积分方程为 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. 作皮卡序列 $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. 归纳可证 $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$, 它蕴涵皮卡序列在 $\left|x-x_0\right|\le h$ 上一致收敛.

> **阿斯科利引理与格朗沃尔不等式**<br>阿斯科利引理: 有界闭区间上一致有界且等度连续的函数列必有一致收敛的子列. 格朗沃尔不等式: 若非负连续函数 $u\left(x\right)$ 满足 $u\left(x\right)\le A+L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$, 则 $u\left(x\right)\le Ae^{L\left|x-x_0\right|}$.

> **魏尔斯特拉斯判别法(一致收敛)**<br>若函数项级数 $\displaystyle\sum_{k=0}^{\infty}u_k\left(x\right)$ 的通项满足 $\left|u_k\left(x\right)\right|\le M_k$ 对一切 $x$ 成立, 且数项级数 $\displaystyle\sum_{k=0}^{\infty}M_k$ 收敛, 则函数项级数在相应区间上一致收敛.

### 习题一

(习题 5-2 题2)对 $n$ 维向量形式的微分方程, 叙述相应的皮卡存在和唯一性定理以及佩亚诺存在定理, 并写出证明的主要步骤.

### 解答 习题一

(1) **皮卡存在唯一性定理**. 设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续, 且对 $y$ 满足利普希茨条件 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$. 令 $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. 则柯西问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在区间 $\left|x-x_0\right|\le h$ 上存在唯一解.

证明主要步骤如下.

第一步, 由**标准微分方程组与向量形式**及积分方程与微分方程的等价性, 柯西问题等价于积分方程

$$
y\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt.
$$

第二步, 由**皮卡序列及其一致收敛估计**, 作皮卡序列 $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. 归纳可证 $\left|y_k\left(x\right)-y_0\right|\le M\left|x-x_0\right|\le Mh\le b$, 故所有近似解都停留在区域 $R$ 内.

第三步, 再用归纳法证明估计式 $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$($k=0,1,2,\cdots$). 它由**利普希茨条件**与积分递推得到: 基步 $k=0$ 时 $\left|y_1-y_0\right|\le M\left|x-x_0\right|$; 归纳步由 $\left|y_{k+1}-y_k\right|\le L\displaystyle\int_{x_0}^{x}\left|y_k-y_{k-1}\right|dt$ 得到. 由于数项级数 $\displaystyle\sum_{k=0}^{\infty}\frac{ML^kh^{k+1}}{\left(k+1\right)!}$ 收敛, 由**魏尔斯特拉斯判别法(一致收敛)**, 皮卡序列在 $\left|x-x_0\right|\le h$ 上一致收敛于连续函数 $y\left(x\right)$.

第四步, 由 $f$ 连续与皮卡序列一致收敛, 在积分号下取极限, 得 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$, 即 $y\left(x\right)$ 是柯西问题的解.

第五步, 证唯一性. 设 $y\left(x\right),\ z\left(x\right)$ 都是解, 令 $u\left(x\right)=\left|y\left(x\right)-z\left(x\right)\right|$, 则 $u\left(x\right)\le L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$. 由**格朗沃尔不等式**, $u\left(x\right)\equiv0$, 故 $y\left(x\right)\equiv z\left(x\right)$.

(2) **佩亚诺存在定理**. 设 $f\left(x,y\right)$ 在区域 $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ 上连续(不要求利普希茨条件), $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. 则柯西问题在 $\left|x-x_0\right|\le h$ 上至少存在一个解.

证明主要步骤如下.

第一步, 在 $\left|x-x_0\right|\le h$ 上作欧拉折线近似解序列 $y_n\left(x\right)$: 以 $y_n\left(x_0\right)=y_0$ 为初值, 在每个小区间上取右端点处的斜率 $f\left(x_k,y_n\left(x_k\right)\right)$ 作直线段.

第二步, 一致有界与等度连续. 由 $\left|\frac{dy_n}{dx}\right|\le M$ 得 $\left|y_n\left(x\right)-y_0\right|\le M\left|x-x_0\right|\le b$, 故序列一致有界; 且 $\left|y_n\left(x\right)-y_n\left(x'\right)\right|\le M\left|x-x'\right|$, 故序列等度连续.

第三步, 由**阿斯科利引理**, 存在一致收敛的子列 $y_{n_k}\left(x\right)\to y\left(x\right)$, $y$ 连续.

第四步, 由 $f$ 在有界闭区域 $R$ 上一致连续, $f\left(t,y_{n_k}\left(t\right)\right)\to f\left(t,y\left(t\right)\right)$ 一致成立; 在欧拉折线的积分等式 $y_{n_k}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_{n_k}\left(t\right)\right)dt$ 两端取极限, 得 $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$, 故 $y\left(x\right)$ 是柯西问题的解. 存在性得证(不保证唯一).

$\blacksquare$

### 习题二

(习题 5-2 题3)对 $n$ 阶线性微分方程组的初值问题, 试叙述并证明解的存在和唯一性定理.

### 解答 习题二

**定理叙述**. 设矩阵函数 $A\left(x\right)=\left(a_{ij}\left(x\right)\right)_{n\times n}$ 和向量函数 $e\left(x\right)$ 都在区间 $\left(\alpha,\beta\right)$ 上连续, 则线性微分方程组柯西问题

$$
\frac{dy}{dx}=A\left(x\right)y+e\left(x\right),\quad y\left(x_0\right)=y_0
$$

(其中 $\alpha<x_0<\beta$, $y_0\in R^n$)的解在整个区间 $\left(\alpha,\beta\right)$ 上存在且唯一.

**证明**. 令 $f\left(x,y\right)=A\left(x\right)y+e\left(x\right)$.

第一步, 连续性. 由 $A\left(x\right),e\left(x\right)$ 连续, 知 $f\left(x,y\right)$ 对 $\left(x,y\right)$ 连续.

第二步, 局部满足**利普希茨条件**. 对任意 $y_1,y_2$, 有

$$
\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|=\left|A\left(x\right)\left(y_1-y_2\right)\right|\le\left\|A\left(x\right)\right\|\cdot\left|y_1-y_2\right|.
$$

在任一有界闭子区间 $\left[c,d\right]\subset\left(\alpha,\beta\right)$ 上, $\left\|A\left(x\right)\right\|$ 连续故有上界 $L$, 从而 $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$. 由**皮卡存在唯一性定理($n$ 维向量形式)**, 解局部存在且唯一.

第三步, 延拓到整个 $\left(\alpha,\beta\right)$. 设解 $y=y\left(x\right)$ 的最大存在区间为 $\left(\omega_1,\omega_2\right)$. 假设 $\omega_2<\beta$. 在 $\left[x_0,\omega_2\right)$ 上, $\left\|A\left(x\right)\right\|$ 与 $\left|e\left(x\right)\right|$ 都有界, 分别记为 $M_1,M_2$, 则

$$
\left|y'\left(x\right)\right|\le\left\|A\left(x\right)\right\|\left|y\left(x\right)\right|+\left|e\left(x\right)\right|\le M_1\left|y\left(x\right)\right|+M_2.
$$

由**格朗沃尔不等式**, $\left|y\left(x\right)\right|\le\left(\left|y_0\right|+M_2\left(\omega_2-x_0\right)\right)e^{M_1\left(\omega_2-x_0\right)}$ 在 $\left[x_0,\omega_2\right)$ 上有界. 因而 $\left|y'\left(x\right)\right|\le M_1\left|y\left(x\right)\right|+M_2$ 也有界, 故当 $x\to\omega_2^{-}$ 时 $y\left(x\right)$ 收敛于某极限 $y_*$(有界导数的函数为柯西列). 以 $y\left(\omega_2\right)=y_*$ 作为新初值, 由皮卡存在唯一性定理, 解可向右延拓过 $\omega_2$, 与 $\omega_2$ 为最大右端点矛盾. 故 $\omega_2=\beta$. 同理 $\omega_1=\alpha$.

第四步, 唯一性由皮卡存在唯一性定理局部保证, 延拓过程中不产生分歧, 故整体唯一. 定理得证.

$\blacksquare$
