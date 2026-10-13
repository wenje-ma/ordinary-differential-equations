# 作业 26

> **定理 10.1**(首次积分的充要条件)<br>设微分方程组 $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$($i=1,\cdots,n$) 的右端 $f_1,\cdots,f_n$ 在区域 $G_1$ 内对 $\left(x,y_1,\cdots,y_n\right)$ 连续, 且对 $\left(y_1,\cdots,y_n\right)$ 连续可微. 设函数 $\Phi\left(x,y_1,\cdots,y_n\right)$ 在 $G_1$ 内连续可微, 则 $\Phi\left(x,y_1,\cdots,y_n\right)=C$ 是该方程组在 $G_1$ 内的首次积分的充要条件为恒等式 $$\frac{\partial\Phi}{\partial x}+\frac{\partial\Phi}{\partial y_1}f_1+\cdots+\frac{\partial\Phi}{\partial y_n}f_n\equiv0$$ 在 $G_1$ 内成立.

> **定理 10.2**(已知一个首次积分可降低一阶)<br>若已知微分方程组 (10.17) 的一个首次积分 $\Phi\left(x,y_1,\cdots,y_n\right)=C$, 则可把该微分方程组降低一阶. 其依据是 $\frac{\partial\Phi}{\partial y_1},\cdots,\frac{\partial\Phi}{\partial y_n}$ 不能全为零, 不妨设 $\frac{\partial\Phi}{\partial y_n}\neq0$, 再用隐函数定理由首次积分解出 $y_n=g\left(x,y_1,\cdots,y_{n-1},C\right)$, 代回原方程组前 $n-1$ 式消去 $y_n$.

> **互相独立的首次积分**(雅可比行列式非零)<br>设微分方程组 (10.17) 有 $k$ 个首次积分 $V_i\left(x,y_1,\cdots,y_n\right)=C_i$($i=1,\cdots,k$). 若在某区域内它们的矩阵 $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ 的秩等于 $k$, 亦即不妨设雅可比行列式 $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$, 则称它们在该区域内是互相独立的.

> **隐函数定理**<br>若函数 $F\left(x,y_1,\cdots,y_k\right)$ 连续可微且 $\frac{\partial F}{\partial y_k}\neq0$, 则由方程 $F\left(x,y_1,\cdots,y_k\right)=0$ 可在局部解出 $y_k$ 为其余变元的连续可微函数.

### 习题一

(习题 10-2 题1)设已知微分方程组 (10.17) 的 $k$($1\le k\le n$) 个互相独立的首次积分 $V_i\left(x,y_1,y_2,\cdots,y_n\right)=C_i$($i=1,2,\cdots,k$). 这里所谓 $k$ 个互相独立的首次积分, 其含意是矩阵 $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ 的秩等于 $k$, 或不妨设雅可比行列式 $\frac{D\left(V_1,V_2,\cdots,V_k\right)}{D\left(y_1,y_2,\cdots,y_k\right)}\neq0$, 则利用这 $k$ 个互相独立的首次积分可以把微分方程组 (10.17) 降低 $k$ 阶.

### 解答 习题一

由**互相独立的首次积分**(雅可比行列式非零), 不妨设在所论区域内 $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$. 把前 $k$ 个未知函数 $y_1,\cdots,y_k$ 看作待解出的变元, 而把 $x,y_{k+1},\cdots,y_n$ 看作自变量. 由**隐函数定理**, 可从方程组

$$
V_i\left(x,y_1,\cdots,y_k,y_{k+1},\cdots,y_n\right)=C_i\qquad(i=1,\cdots,k)
$$

局部解出

$$
y_i=g_i\left(x,y_{k+1},\cdots,y_n,C_1,\cdots,C_k\right)\qquad(i=1,\cdots,k).
$$

将它们代入原微分方程组 (10.17) 的后 $n-k$ 个等式

$$
\frac{dy_{k+1}}{dx}=f_{k+1},\qquad\cdots,\qquad\frac{dy_n}{dx}=f_n,
$$

就消去了 $y_1,\cdots,y_k$, 得到一个以 $y_{k+1},\cdots,y_n$ 为未知函数的 $n-k$ 阶微分方程组. 这正是**定理 10.2**(已知一个首次积分可降低一阶) 的推广: 每用一个独立首次积分消去一个未知函数, 阶数便降低一阶, 故用 $k$ 个独立首次积分即把原方程组降低 $k$ 阶. $\blacksquare$

### 习题二

(习题 10-2 题2)设给定首次积分如题 1 中的 $V_i\left(x,y_1,\cdots,y_n\right)=C_i$($i=1,\cdots,k$), 又设 $H\left(z_1,\cdots,z_k\right)$ 是连续可微的函数, 而且它不是常数, 则 $H\left(V_1\left(x,y_1,\cdots,y_n\right),\cdots,V_k\left(x,y_1,\cdots,y_n\right)\right)=C$ 是微分方程组 (10.17) 的一个首次积分.

### 解答 习题二

记 $W\left(x,y_1,\cdots,y_n\right)=H\left(V_1,\cdots,V_k\right)$. 由**定理 10.1**(首次积分的充要条件), 只需验证 $W$ 满足恒等式 $\frac{\partial W}{\partial x}+\sum_{j=1}^n\frac{\partial W}{\partial y_j}f_j\equiv0$. 由复合函数求导法则,

$$
\frac{\partial W}{\partial x}+\sum_{j=1}^n\frac{\partial W}{\partial y_j}f_j
=\sum_{i=1}^k\frac{\partial H}{\partial z_i}\left(\frac{\partial V_i}{\partial x}+\sum_{j=1}^n\frac{\partial V_i}{\partial y_j}f_j\right).
$$

因为每个 $V_i$ 都是首次积分, 再由**定理 10.1**(首次积分的充要条件), 右端括号内每一项都恒等于零, 故左端恒等于零, 从而 $W=C$ 是微分方程组 (10.17) 的首次积分. $\blacksquare$
