# Assignment 21

> **Majorant Series and Majorant Function**<br>Suppose there are two power series $\sum_{i,j=0}^{\infty}a_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j$ and $\sum_{i,j=0}^{\infty}A_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j\ \left(A_{ij}\ge0\right)$, where the coefficients $a_{ij}$ and $A_{ij}$ satisfy the inequality $\left|a_{ij}\right|\le A_{ij}\ \left(i,j=0,1,2,\cdots\right)$. Then the second power series is called a majorant series (or dominating series) of the first. If this majorant series is also convergent in the region $D:\left|x-x_0\right|< \alpha,\ \left|y-y_0\right|< \beta$, then its sum function $F\left(x,y\right)$ is called a majorant function (or dominating function) of the original power series in $D$.

> **Theorem 7.1** (Cauchy's Theorem)<br>If the function $f\left(x,y\right)$ can be expanded into a convergent power series in $\left(x-x_0\right)$ and $\left(y-y_0\right)$ on the rectangular region $R:\left|x-x_0\right|< \alpha,\ \left|y-y_0\right|< \beta$, then the initial value problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has an analytic solution $y=y\left(x\right)$ in a neighborhood $\left(x_0-\rho,x_0+\rho\right)$ of $x_0$, and it is unique. Here the coefficients of the formal solution are $C_n=\frac{1}{n!}y^{\left(n\right)}\left(x_0\right)=P_n\left(a_{00},a_{01},a_{10},\cdots,a_{n-1,0}\right)$, where $P_n$ is a polynomial with positive coefficients in the various coefficients, depending only on the index $n$ and not on the function $f$.

> **Remark 3** (Application of the Majorant Series Method to Systems of Differential Equations)<br>The majorant series method can be applied to the case of systems of differential equations. Consider the initial value problem for a system $\frac{dy_k}{dx}=f_k\left(x,y_1,\cdots,y_n\right),\ y_k\left(0\right)=0\ \left(k=1,2,\cdots,n\right)$. Suppose the right-hand side functions can be expanded into convergent power series in the region $\left|x\right|\le\alpha,\ \left|y_1\right|\le\beta,\ \cdots,\ \left|y_n\right|\le\beta$. Then, analogous to Lemma 7.1, one can prove the existence of a majorant function; and by the same reasoning as in Theorem 7.1, the initial value problem has a convergent power series solution in some neighborhood of $x=0$.

### Problem 1

(Problem 7-1, Problem 2) Consider the initial value problem $\left(E\right):\ y''+p\left(x\right)y'+q\left(x\right)y=0,\ y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0'$, where $p\left(x\right)$ and $q\left(x\right)$ can be expanded into convergent power series in $\left(x-x_0\right)$ on the interval $\left(x_0-a,x_0+a\right)$. Then the analytic solution $y=y\left(x\right)$ of $\left(E\right)$ exists and is unique on $\left(x_0-a,x_0+a\right)$.

### Solution to Problem 1

Convert the second-order equation into a first-order system. Let $y_1=y,\ y_2=y'$; then the original equation is equivalent to

$$
\begin{cases}\frac{dy_1}{dx}=y_2,\\\frac{dy_2}{dx}=-q\left(x\right)y_1-p\left(x\right)y_2,\end{cases}
$$

with initial conditions $y_1\left(x_0\right)=y_0,\ y_2\left(x_0\right)=y_0'$.

Denote the right-hand side functions $f_1\left(x,y_1,y_2\right)=y_2,\ f_2\left(x,y_1,y_2\right)=-q\left(x\right)y_1-p\left(x\right)y_2$. Since $p\left(x\right)$ and $q\left(x\right)$ can be expanded into convergent power series in $\left(x-x_0\right)$ on $\left(x_0-a,x_0+a\right)$, while $f_1=y_2$ is linear in $y_2$ (naturally analytic), and $f_2$ is a sum of products of $p\left(x\right),q\left(x\right)$ with $y_1,y_2$, it follows that $f_1$ and $f_2$ are analytic in $\left(x,y_1,y_2\right)$ near $x_0$.

By **Remark 3** (Application of the Majorant Series Method to Systems of Differential Equations), this first-order system has a unique convergent power series solution $\left(y_1\left(x\right),y_2\left(x\right)\right)$ in some neighborhood of $x_0$. Therefore $y=y_1\left(x\right)$ can be expanded into a convergent power series in $\left(x-x_0\right)$ near $x_0$, i.e. the analytic solution exists and is unique.

Furthermore, since the power series of $p\left(x\right)$ and $q\left(x\right)$ converge on the entire interval $\left(x_0-a,x_0+a\right)$, take any point $x^*$ in this interval; the already-obtained analytic solution takes finite values $y\left(x^*\right),\ y'\left(x^*\right)$ at $x^*$, and $p,q$ are still analytic near $x^*$, so the above conclusion can be reapplied at $x^*$ to extend the analytic solution. By the connectedness of the interval, the analytic solution exists and is unique on the entire $\left(x_0-a,x_0+a\right)$. $\blacksquare$

### Problem 2

(Problem 7-1, Problem 3) State and prove the theorem on the analyticity of the solution of an analytic differential equation with respect to initial values and parameters.

### Solution to Problem 2

**Theorem (Analyticity of the Solution with Respect to Initial Values and Parameters).** Consider the initial value problem

$$
\frac{dy}{dx}=f\left(x,y,\lambda\right),\quad y\left(x_0\right)=y_0
$$

where $f\left(x,y,\lambda\right)$ is analytic in $\left(x,y,\lambda\right)$ in some neighborhood of $\left(x_0,y_0,\lambda_0\right)$. Then the solution $y=y\left(x,x_0,y_0,\lambda\right)$ is analytic in all variables $\left(x,x_0,y_0,\lambda\right)$ near $\left(x_0,y_0,\lambda_0\right)$.

**Proof.** Translate $x$ by letting $t=x-x_0$; then the equation becomes

$$
\frac{dy}{dt}=f\left(t+x_0,y,\lambda\right),\quad y\left(0\right)=y_0.
$$

Treat $x_0$ and $\lambda$ as additional unknown functions satisfying $\frac{dx_0}{dt}=0$ and $\frac{d\lambda}{dt}=0$; then we obtain the system

$$
\begin{cases}\frac{dy}{dt}=f\left(t+x_0,y,\lambda\right),\\\frac{dx_0}{dt}=0,\\\frac{d\lambda}{dt}=0.\end{cases}
$$

The right-hand side function $f\left(t+x_0,y,\lambda\right)$ is analytic in $\left(t,x_0,y,\lambda\right)$, and the other right-hand sides are identically zero, hence also analytic. By **Remark 3** (Application of the Majorant Series Method to Systems of Differential Equations), this system has a unique convergent power series solution near $t=0$. Since $x_0\left(t\right)\equiv a,\ \lambda\left(t\right)\equiv b$ are constants, $y=y\left(t,a,y_0,b\right)$ is an analytic function of $t$.

To show that $y$ is analytic in $\left(a,y_0,b\right)$, note that the coefficients $c_n$ in the formal power series $y=\sum_{n=0}^{\infty}c_n\left(a,y_0,b\right)t^n$ are polynomials in the various partial derivatives of $f$ at $\left(a,y_0,b\right)$ (as follows from the recursive nature of the formal solution coefficients in the proof of **Theorem 7.1** (Cauchy's Theorem)); hence $c_n$ is analytic in $\left(a,y_0,b\right)$. The majorant series method guarantees that the power series converges uniformly near $\left(a,y_0,b\right)$, so $y$ is also analytic in $\left(a,y_0,b\right)$. $\blacksquare$
