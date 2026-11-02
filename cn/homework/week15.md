# week15

> **基础知识: 标准微分方程组与向量形式**
> 
> $\frac{\mathrm dy_i}{\mathrm dx}=f_i\left(x,y_1,\cdots,y_n\right)$, 向量形式 $\frac{\mathrm dy}{\mathrm dx}=f\left(x,y\right)$.

> **基础知识: 向量的模及其基本性质**
> 
> 欧几里得模 $\left|y\right|=\sqrt{y_1^2+\cdots+y_n^2}$, 满足三角不等式.

> **基础知识: 利普希茨条件**
> 
> $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$.

> **基础知识: 皮卡存在唯一性定理 ($n$ 维向量形式)**
> 
> $f$ 连续且满足利普希茨条件时, 柯西问题在 $\left|x-x_0\right|\le h$ 上存在唯一解.

> **基础知识: 佩亚诺存在定理 ($n$ 维向量形式)**
> 
> $f$ 连续时, 柯西问题至少有一个解.

> **基础知识: 皮卡序列及其一致收敛估计**
> 
> $y_{k+1}=y_0+\int_{x_0}^x f\left(t,y_k\left(t\right)\right)\mathrm dt$, 估计 $\left|y_{k+1}-y_k\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$.

> **基础知识: 阿斯科利引理与格朗沃尔不等式**
> 
> 阿斯科利引理: 一致有界且等度连续函数列有一致收敛子列. 格朗沃尔不等式: $u\le A+L\int u$ 蕴含 $u\le Ae^{L\left|x-x_0\right|}$.

> **基础知识: 魏尔斯特拉斯判别法 (一致收敛)**
> 
> $\left|u_k\left(x\right)\right|\le M_k$ 且 $\sum M_k$ 收敛, 则函数项级数一致收敛.

---

## 5-2 题2

叙述并证明 $n$ 维向量形式的皮卡存在唯一性定理与佩亚诺存在定理.

### 解答 5-2 题2

由**基础知识: 标准微分方程组与向量形式** 及积分方程等价性, 柯西问题等价于积分方程. 由**基础知识: 皮卡序列及其一致收敛估计** 与**基础知识: 魏尔斯特拉斯判别法 (一致收敛)**, 皮卡序列一致收敛, 取极限得解. 唯一性由**基础知识: 阿斯科利引理与格朗沃尔不等式** 中的格朗沃尔不等式给出. 佩亚诺定理由欧拉折线与**基础知识: 阿斯科利引理与格朗沃尔不等式** 中的阿斯科利引理证明. $\blacksquare$

---

## 5-2 题3

叙述并证明线性微分方程组初值问题解的存在唯一性定理.

### 解答 5-2 题3

$f\left(x,y\right)=A\left(x\right)y+e\left(x\right)$ 连续. 由**基础知识: 利普希茨条件**, $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le\left\|A\left(x\right)\right\|\left|y_1-y_2\right|$, 局部利普希茨. 由**基础知识: 皮卡存在唯一性定理 ($n$ 维向量形式)** 局部存在唯一. 由格朗沃尔不等式, 解在有界区间上有界, 故可延拓到整个区间. $\blacksquare$
