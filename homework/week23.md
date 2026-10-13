# 作业 23

> **勒让德方程与勒让德多项式**<br>勒让德方程为 $\left(1-x^2\right)y''-2xy'+n\left(n+1\right)y=0$, 其中 $n$ 是常数. 当 $n$ 是非负整数时, 方程的一个解是 $n$ 次多项式, 即勒让德多项式 $P_n\left(x\right)$, 其统一表达式为 $P_n\left(x\right)=\dfrac{1}{2^n}\sum_{k=0}^{\left[n/2\right]}\dfrac{\left(-1\right)^k\left(2n-2k\right)!}{k!\left(n-k\right)!\left(n-2k\right)!}x^{n-2k}$.

> **勒让德多项式的母函数**<br>令函数 $G\left(x,t\right)=\left(1-2xt+t^2\right)^{-1/2}$, 则 $G\left(x,t\right)$ 关于 $t$ 展开的幂级数为 $G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n$, 其中 $P_n\left(x\right)$ 是勒让德多项式. 函数 $G\left(x,t\right)$ 称为勒让德多项式的母函数. 它满足恒等式 $\left(1-2xt+t^2\right)\dfrac{\partial G}{\partial t}=\left(x-t\right)G$.

### 习题一

(习题 7-3 题2)利用上题中的 $G\left(x,t\right)$ 所满足的恒等式 $\left(1-2xt+t^2\right)\dfrac{\partial G}{\partial t}=\left(x-t\right)G$, 证明递推公式 $\left(n+1\right)P_{n+1}\left(x\right)-\left(2n+1\right)xP_n\left(x\right)+nP_{n-1}\left(x\right)=0\ \left(n\ge1\right)$.

### 解答 习题一

由**勒让德多项式的母函数**, 有

$$
G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n,\qquad\frac{\partial G}{\partial t}=\sum_{n=1}^{\infty}nP_n\left(x\right)t^{n-1}.
$$

将它们代入恒等式 $\left(1-2xt+t^2\right)\dfrac{\partial G}{\partial t}=\left(x-t\right)G$, 左端展开为

$$
\left(1-2xt+t^2\right)\sum_{n=1}^{\infty}nP_nt^{n-1}=\sum_{n=1}^{\infty}nP_nt^{n-1}-2x\sum_{n=1}^{\infty}nP_nt^n+\sum_{n=1}^{\infty}nP_nt^{n+1},
$$

右端展开为

$$
\left(x-t\right)\sum_{n=0}^{\infty}P_nt^n=x\sum_{n=0}^{\infty}P_nt^n-\sum_{n=0}^{\infty}P_nt^{n+1}.
$$

比较两端 $t^k$ 的系数.

$k=0$ 时: 左端系数为 $P_1$, 右端系数为 $xP_0$, 故 $P_1=xP_0=x$.

$k\ge1$ 时: 左端系数为 $\left(k+1\right)P_{k+1}-2xkP_k+\left(k-1\right)P_{k-1}$(其中第三项当 $k=1$ 时为零), 右端系数为 $xP_k-P_{k-1}$. 令其相等:

$$
\left(k+1\right)P_{k+1}-2xkP_k+\left(k-1\right)P_{k-1}=xP_k-P_{k-1}.
$$

整理得

$$
\left(k+1\right)P_{k+1}-\left(2k+1\right)xP_k+kP_{k-1}=0.
$$

将 $k$ 换记为 $n$, 即得递推公式

$$
\left(n+1\right)P_{n+1}\left(x\right)-\left(2n+1\right)xP_n\left(x\right)+nP_{n-1}\left(x\right)=0\qquad\left(n\ge1\right).
$$

$\blacksquare$
