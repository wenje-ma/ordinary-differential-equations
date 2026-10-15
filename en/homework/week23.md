# Assignment 23

> **Legendre Equation and Legendre Polynomials**<br>The Legendre equation is $\left(1-x^2\right)y''-2xy'+n\left(n+1\right)y=0$, where $n$ is a constant. When $n$ is a non-negative integer, one solution of the equation is a polynomial of degree $n$, namely the Legendre polynomial $P_n\left(x\right)$, whose unified expression is $P_n\left(x\right)=\frac{1}{2^n}\sum_{k=0}^{\left[n/2\right]}\frac{\left(-1\right)^k\left(2n-2k\right)!}{k!\left(n-k\right)!\left(n-2k\right)!}x^{n-2k}$.

> **Generating Function of Legendre Polynomials**<br>Let the function $G\left(x,t\right)=\left(1-2xt+t^2\right)^{-1/2}$; then the power series expansion of $G\left(x,t\right)$ in $t$ is $G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n$, where $P_n\left(x\right)$ are the Legendre polynomials. The function $G\left(x,t\right)$ is called the generating function of the Legendre polynomials. It satisfies the identity $\left(1-2xt+t^2\right)\frac{\partial G}{\partial t}=\left(x-t\right)G$.

### Problem 1

(Problem 7-3, Problem 2) Using the identity $\left(1-2xt+t^2\right)\frac{\partial G}{\partial t}=\left(x-t\right)G$ satisfied by $G\left(x,t\right)$ from the previous problem, prove the recursion formula $\left(n+1\right)P_{n+1}\left(x\right)-\left(2n+1\right)xP_n\left(x\right)+nP_{n-1}\left(x\right)=0\ \left(n\ge1\right)$.

### Solution to Problem 1

By the **Generating Function of Legendre Polynomials**, we have

$$
G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n,\quad\frac{\partial G}{\partial t}=\sum_{n=1}^{\infty}nP_n\left(x\right)t^{n-1}.
$$

Substituting them into the identity $\left(1-2xt+t^2\right)\frac{\partial G}{\partial t}=\left(x-t\right)G$, the left-hand side expands to

$$
\left(1-2xt+t^2\right)\sum_{n=1}^{\infty}nP_nt^{n-1}=\sum_{n=1}^{\infty}nP_nt^{n-1}-2x\sum_{n=1}^{\infty}nP_nt^n+\sum_{n=1}^{\infty}nP_nt^{n+1},
$$

and the right-hand side expands to

$$
\left(x-t\right)\sum_{n=0}^{\infty}P_nt^n=x\sum_{n=0}^{\infty}P_nt^n-\sum_{n=0}^{\infty}P_nt^{n+1}.
$$

Compare the coefficients of $t^k$ on both sides.

For $k=0$: the left-hand coefficient is $P_1$, and the right-hand coefficient is $xP_0$, so $P_1=xP_0=x$.

For $k\ge1$: the left-hand coefficient is $\left(k+1\right)P_{k+1}-2xkP_k+\left(k-1\right)P_{k-1}$ (where the third term is zero when $k=1$), and the right-hand coefficient is $xP_k-P_{k-1}$. Setting them equal:

$$
\left(k+1\right)P_{k+1}-2xkP_k+\left(k-1\right)P_{k-1}=xP_k-P_{k-1}.
$$

Rearranging gives

$$
\left(k+1\right)P_{k+1}-\left(2k+1\right)xP_k+kP_{k-1}=0.
$$

Renaming $k$ as $n$, we obtain the recursion formula

$$
\left(n+1\right)P_{n+1}\left(x\right)-\left(2n+1\right)xP_n\left(x\right)+nP_{n-1}\left(x\right)=0\quad\left(n\ge1\right).
$$

$\blacksquare$
