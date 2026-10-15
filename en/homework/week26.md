# Assignment 26

> **Theorem 10.1** (Necessary and Sufficient Condition for a First Integral)<br>Suppose the right-hand sides $f_1,\cdots,f_n$ of the system $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$ ($i=1,\cdots,n$) are continuous in $\left(x,y_1,\cdots,y_n\right)$ in a region $G_1$ and continuously differentiable in $\left(y_1,\cdots,y_n\right)$. Suppose the function $\Phi\left(x,y_1,\cdots,y_n\right)$ is continuously differentiable in $G_1$. Then $\Phi\left(x,y_1,\cdots,y_n\right)=C$ is a first integral of the system in $G_1$ if and only if the identity $$\frac{\partial\Phi}{\partial x}+\frac{\partial\Phi}{\partial y_1}f_1+\cdots+\frac{\partial\Phi}{\partial y_n}f_n\equiv0$$ holds in $G_1$.

> **Theorem 10.2** (Knowing One First Integral Lowers the Order by One)<br>If a first integral $\Phi\left(x,y_1,\cdots,y_n\right)=C$ of the system (10.17) is known, then the system can be lowered by one order. The basis is that $\frac{\partial\Phi}{\partial y_1},\cdots,\frac{\partial\Phi}{\partial y_n}$ cannot all be zero; without loss of generality suppose $\frac{\partial\Phi}{\partial y_n}\neq0$, then by the implicit function theorem solve the first integral for $y_n=g\left(x,y_1,\cdots,y_{n-1},C\right)$, and substitute back into the first $n-1$ equations of the original system to eliminate $y_n$.

> **Mutually Independent First Integrals** (Nonvanishing Jacobian)<br>Suppose the system (10.17) has $k$ first integrals $V_i\left(x,y_1,\cdots,y_n\right)=C_i$ ($i=1,\cdots,k$). If in some region the matrix $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ has rank equal to $k$, i.e. without loss of generality the Jacobian determinant $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$, then they are said to be mutually independent in that region.

> **Implicit Function Theorem**<br>If the function $F\left(x,y_1,\cdots,y_k\right)$ is continuously differentiable and $\frac{\partial F}{\partial y_k}\neq0$, then the equation $F\left(x,y_1,\cdots,y_k\right)=0$ can be locally solved for $y_k$ as a continuously differentiable function of the remaining variables.

### Problem 1

(Problem 10-2, Problem 1) Suppose $k$ ($1\le k\le n$) mutually independent first integrals $V_i\left(x,y_1,y_2,\cdots,y_n\right)=C_i$ ($i=1,2,\cdots,k$) of the system (10.17) are known. Here, by $k$ mutually independent first integrals, we mean that the matrix $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ has rank equal to $k$, or without loss of generality the Jacobian determinant $\frac{D\left(V_1,V_2,\cdots,V_k\right)}{D\left(y_1,y_2,\cdots,y_k\right)}\neq0$. Then using these $k$ mutually independent first integrals, the system (10.17) can be lowered by $k$ orders.

### Solution to Problem 1

By **Mutually Independent First Integrals** (Nonvanishing Jacobian), without loss of generality suppose $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$ in the region under consideration. Treat the first $k$ unknown functions $y_1,\cdots,y_k$ as the variables to be solved for, and treat $x,y_{k+1},\cdots,y_n$ as independent variables. By the **Implicit Function Theorem**, from the system

$$
V_i\left(x,y_1,\cdots,y_k,y_{k+1},\cdots,y_n\right)=C_i\quad\left(i=1,\cdots,k\right)
$$

we can locally solve

$$
y_i=g_i\left(x,y_{k+1},\cdots,y_n,C_1,\cdots,C_k\right)\quad\left(i=1,\cdots,k\right).
$$

Substituting them into the last $n-k$ equations of the original system (10.17)

$$
\frac{dy_{k+1}}{dx}=f_{k+1},\quad\cdots,\quad\frac{dy_n}{dx}=f_n,
$$

eliminates $y_1,\cdots,y_k$, yielding an $n-k$-th order system with $y_{k+1},\cdots,y_n$ as unknown functions. This is exactly the generalization of **Theorem 10.2** (Knowing One First Integral Lowers the Order by One): each independent first integral used to eliminate one unknown function lowers the order by one, so using $k$ independent first integrals lowers the original system by $k$ orders. $\blacksquare$

### Problem 2

(Problem 10-2, Problem 2) Given the first integrals $V_i\left(x,y_1,\cdots,y_n\right)=C_i$ ($i=1,\cdots,k$) as in Problem 1, and suppose $H\left(z_1,\cdots,z_k\right)$ is a continuously differentiable function that is not a constant. Then $H\left(V_1\left(x,y_1,\cdots,y_n\right),\cdots,V_k\left(x,y_1,\cdots,y_n\right)\right)=C$ is a first integral of the system (10.17).

### Solution to Problem 2

Denote $W\left(x,y_1,\cdots,y_n\right)=H\left(V_1,\cdots,V_k\right)$. By **Theorem 10.1** (Necessary and Sufficient Condition for a First Integral), it suffices to verify that $W$ satisfies the identity $\frac{\partial W}{\partial x}+\sum_{j=1}^n\frac{\partial W}{\partial y_j}f_j\equiv0$. By the chain rule for composite functions,

$$
\frac{\partial W}{\partial x}+\sum_{j=1}^n\frac{\partial W}{\partial y_j}f_j
=\sum_{i=1}^k\frac{\partial H}{\partial z_i}\left(\frac{\partial V_i}{\partial x}+\sum_{j=1}^n\frac{\partial V_i}{\partial y_j}f_j\right).
$$

Since each $V_i$ is a first integral, by **Theorem 10.1** (Necessary and Sufficient Condition for a First Integral), each term in parentheses on the right-hand side is identically zero; hence the left-hand side is identically zero, and therefore $W=C$ is a first integral of the system (10.17). $\blacksquare$
