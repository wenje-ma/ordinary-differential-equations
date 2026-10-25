# 作业 30

> **定理 11.2**(拟线性偏微分方程的隐式通解与特征线)<br>一阶拟线性方程 $X\frac{\partial z}{\partial x}+Y\frac{\partial z}{\partial y}=Z$ 的特征方程为 $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$, 其积分曲线称特征曲线, 它在每点以特征向量 $\left(X,Y,Z\right)$ 为切向量. 偏微分方程的解 $z=z\left(x,y\right)$ 所确定的积分曲面 $S$ 由特征曲线编织而成: 通过 $S$ 上每点的特征曲线整个落在 $S$ 上.

> **特征线法**(初值问题的解法)<br>给定初始曲线 $\Lambda:\ x=\alpha\left(\sigma\right),\ y=\beta\left(\sigma\right),\ z=\gamma\left(\sigma\right)$. 设特征方程有两个独立首次积分 $\varphi=C_1,\ \psi=C_2$. 在 $\Lambda$ 上取点 $M$, 过 $M$ 的特征曲线为 $\varphi=\overline{C}_1,\ \psi=\overline{C}_2$, 其中 $\overline{C}_1=\varphi\left(\alpha,\beta,\gamma\right),\ \overline{C}_2=\psi\left(\alpha,\beta,\gamma\right)$. 消去参数 $\sigma$ 得 $\overline{C}_1,\overline{C}_2$ 间的关系式 $E\left(\overline{C}_1,\overline{C}_2\right)=0$, 则 $E\left(\varphi\left(x,y,z\right),\psi\left(x,y,z\right)\right)=0$ 即为所求积分曲面.

> **特征线法附注**(初始曲线为特征曲线时解不唯一)<br>若过初始曲线 $\Lambda$ 的每点所作特征曲线与 $\Lambda$ 在交点处横截相交, 则这些特征曲线组成唯一的光滑积分曲面 $z=z\left(x,y\right)$; 但若初始曲线 $\Lambda$ 本身就是一条特征曲线, 则过 $\Lambda$ 的特征曲线只是 $\Lambda$ 自己, 不能张成曲面, 此时任何包含 $\Lambda$ 的积分曲面都是初值问题的解, 即解存在但不唯一.

### 习题一

(习题 11-3 题1)求解初值问题 $\begin{cases}\sqrt{x}\frac{\partial z}{\partial x}+\sqrt{y}\frac{\partial z}{\partial y}=\sqrt{z},\\ \text{通过初始曲线 }\Lambda:\ x=y=z.\end{cases}$

### 解答 习题一

由**定理 11.2**(拟线性偏微分方程的隐式通解与特征线), 先求特征方程

$$
\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}.
$$

由 $\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}$ 积分得 $\sqrt{x}-\sqrt{y}=C_1$; 由 $\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}$ 得 $\sqrt{y}-\sqrt{z}=C_2$. 这是两个独立的首次积分.

现在考察初始曲线 $\Lambda:\ x=y=z$. 把它参数化为 $x=y=z=\sigma$($\sigma> 0$). 代入两个首次积分, 得

$$
\overline{C}_1=\sqrt{\sigma}-\sqrt{\sigma}=0,\quad\overline{C}_2=\sqrt{\sigma}-\sqrt{\sigma}=0.
$$

无论参数 $\sigma$ 取何值, 都有 $\overline{C}_1=\overline{C}_2=0$, 即初始曲线 $\Lambda$ 恰好是特征曲线 $\sqrt{x}-\sqrt{y}=0,\ \sqrt{y}-\sqrt{z}=0$(亦即 $\sqrt{x}=\sqrt{y}=\sqrt{z}$) 本身. 由**特征线法附注**(初始曲线为特征曲线时解不唯一), 当初始曲线本身是一条特征曲线时, 过 $\Lambda$ 的特征曲线只是 $\Lambda$ 自己, 不能张成曲面, 此时初值问题的解存在但不唯一.

具体地, 原方程的积分曲面可写为 $\Phi\left(\sqrt{x}-\sqrt{y},\ \sqrt{y}-\sqrt{z}\right)=0$, 要让它包含 $\Lambda$, 只须 $\Phi\left(0,0\right)=0$. 这样的 $\Phi$ 有无穷多个, 它们都给出过 $\Lambda$ 的积分曲面. 故该初值问题有无穷多个解, 不唯一. $\blacksquare$
