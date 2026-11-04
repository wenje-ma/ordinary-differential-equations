# week12

> **定理 8.5 (初等奇点类型的判定)**
> 
> 由 $p=-\mathrm{tr}\,A$, $q=\det A$ 判断.

> **定理 8.6 (非线性系统与线性化系统的定性结构相同)**
> 
> 小扰动不改变奇点类型.

> **定理 10.1 (首次积分的充要条件)**
> 
> $\frac{\partial\Phi}{\partial x}+\sum\frac{\partial\Phi}{\partial y_j}f_j\equiv0$.

> **定理 10.2 (已知一个首次积分可降低一阶)**
> 
> 用隐函数定理解出一个未知函数.

> **定理 10.7 (大范围首次积分与保守系统)**
> 
> $n-1$ 个独立首次积分蕴含保守性.

> **定理 11.1 (齐次线性偏微分方程的通解)**
> 
> 特征方程首次积分.

> **定理 11.2 (拟线性偏微分方程的隐式通解)**
> 
> $\Phi\left(u,v\right)=0$.

> **定理 11.2 (拟线性偏微分方程的隐式通解与特征线)**
> 
> 特征曲线编织积分曲面.

## 8-3 题2(2)

判断 $x'=2x+y+xy^2$, $y'=x+2y+x^2+y^2$ 的奇点类型.

### 解答 8-3 题2(2)

$p=-4$, $q=3$, $p^2> 4q$. 不稳定两向结点. $\blacksquare$

## 8-3 题2(4)

判断 $x'=x+2y$, $y'=-2x+5y+x^3$.

### 解答 8-3 题2(4)

$p=-6$, $q=9$, $p^2=4q$. 不稳定单向结点. $\blacksquare$

## 8-3 题2(5)

判断 $x'=x\left(1-y\right)$, $y'=y\left(1-x\right)$.

### 解答 8-3 题2(5)

$A=I$, 不稳定星形结点. $\blacksquare$

## 10-2 题1

证明 $k$ 个独立首次积分可降 $k$ 阶.

### 解答 10-2 题1

由隐函数定理解出 $y_1,\cdots,y_k$. $\blacksquare$

## 10-2 题2

证明 $H\left(V_1,\cdots,V_k\right)$ 是首次积分.

### 解答 10-2 题2

由**定理 10.1 (首次积分的充要条件)**, 链式法则每项为零. $\blacksquare$

## 10-4 题1

推广**定理 10.7 (大范围首次积分与保守系统)** 到 $n$ 维, 并说明 $n=2$ 即积分因子理论.

### 解答 10-4 题1

$n-1$ 个独立首次积分的梯度正交补给出广义叉乘 $L_i=\mu f_i$, 散度恒等式 $\sum\partial L_i/\partial x_i=0$. $n=2$ 时 $\mu$ 即积分因子. $\blacksquare$

## 11-1 题1(1)

求解 $\sum x_i\partial y/\partial x_i=0$.

### 解答 11-1 题1(1)

特征方程 $dx_1/x_1=\cdots=dx_n/x_n$. 首次积分 $x_i/x_n$. 通解 $y=\psi\left(x_1/x_n,\cdots,x_{n-1}/x_n\right)$. $\blacksquare$

## 11-1 题1(3)

求解 $a\left(b^2+c^2\right)h_a+b\left(c^2+a^2\right)h_b+c\left(b^2-a^2\right)h_c=0$.

### 解答 11-1 题1(3)

首次积分 $a^2-b^2+c^2$ 与 $a^2/\left(b^2c^2\right)$. $\blacksquare$

## 11-1 题2(2)

求解 $\left(x-y^2\right)z_x+yz_y=0$, $z\left(1,y\right)=f_0\left(y\right)$.

### 解答 11-1 题2(2)

首次积分 $x/y+y=C$. $\blacksquare$

## 11-2 题1(2)

求解 $\left(xy^3-2x^4\right)z_x+\left(2y^4-x^3y\right)z_y=9z\left(x^3-y^3\right)$.

### 解答 11-2 题1(2)

首次积分 $x^2y^2/\left(x^3+y^3\right)$ 与 $\left(x^3+y^3\right)^3z^2$. $\blacksquare$

## 11-2 题2

求解 $\sqrt{x}f_x+\sqrt{y}f_y+\sqrt{z}f_z=f$, $f\left(x,1,z\right)=xz$.

### 解答 11-2 题2

$f=e^{2\sqrt{y}-2}\left(\sqrt{x}-\sqrt{y}+1\right)^2\left(1-\sqrt{y}+\sqrt{z}\right)^2$. $\blacksquare$

## 11-3 题1

求解 $\sqrt{x}z_x+\sqrt{y}z_y=\sqrt{z}$, 通过 $x=y=z$.

### 解答 11-3 题1

初始曲线即特征曲线, 解不唯一. $\blacksquare$
