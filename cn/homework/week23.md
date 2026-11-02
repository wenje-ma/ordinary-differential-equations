# week23

> **基础知识: 勒让德方程与勒让德多项式**
> 
> $\left(1-x^2\right)y''-2xy'+n\left(n+1\right)y=0$.

> **基础知识: 勒让德多项式的母函数**
> 
> $G\left(x,t\right)=\left(1-2xt+t^2\right)^{-1/2}=\sum P_n\left(x\right)t^n$.

---

## 7-3 题2

证明递推公式 $\left(n+1\right)P_{n+1}-\left(2n+1\right)xP_n+nP_{n-1}=0$.

### 解答 7-3 题2

由**基础知识: 勒让德多项式的母函数**, $G=\sum P_nt^n$, $G_t=\sum nP_nt^{n-1}$. 代入 $\left(1-2xt+t^2\right)G_t=\left(x-t\right)G$, 比较 $t^k$ 系数即得. $\blacksquare$
