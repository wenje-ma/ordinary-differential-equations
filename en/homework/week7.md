# Assignment 7

> **Lipschitz Condition**<br>If the function $f\left(x,y\right)$ satisfies the inequality $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$ in a region $D$, where the constant $L> 0$, then $f\left(x,y\right)$ is said to satisfy a Lipschitz condition with respect to $y$ in $D$. If $f\left(x,y\right)$ has a continuous partial derivative with respect to $y$ in a convex region $D$, then it satisfies a Lipschitz condition with respect to $y$ in $D$.

> **Theorem 3.1** (Picard Existence and Uniqueness Theorem)<br>Consider the initial value problem $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, where $f\left(x,y\right)$ is continuous in the rectangle $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Then $\left(E\right)$ has one and only one solution on the interval $I=\left[x_0-h,x_0+h\right]$, where the constant $h=\min\left\{a,\frac{b}{M}\right\}$, $M=\max\limits_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

> **Theorem 3.2** (Uniqueness of Solutions Under the Osgood Condition)<br>If the function $f\left(x,y\right)$ is continuous in a region $G$ and satisfies the inequality $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le F\left(\left|y_1-y_2\right|\right)$, where $F\left(r\right)> 0$ is a continuous function of $r> 0$, and the improper integral $\int_0^{r_1}\frac{dr}{F\left(r\right)}=+\infty$ ($r_1> 0$ is a constant), then $f\left(x,y\right)$ is said to satisfy the Osgood condition with respect to $y$ in $G$; in this case, the solution of the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ through every point in $G$ is unique.

> **Equivalence Between the Integral Equation and the Initial Value Problem**<br>The initial value problem $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has a solution $y=\varphi\left(x\right)$ if and only if the integral equation $y=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$ has a solution. Its Picard sequence is $y_{n+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt$, where $y_0\left(x\right)=y_0$.

### Problem 1

(Problem 3-1, Problem 1) Using the properties of the right-hand side function, discuss the uniqueness of solutions of the following differential equations satisfying the initial condition $y\left(0\right)=0$: (1) $\frac{dy}{dx}=\left|y\right|^{\alpha}$, constant $\alpha> 0$; (2) $\frac{dy}{dx}=\begin{cases}0,&y=0,\\ y\ln\left|y\right|,&y\ne0.\end{cases}$

### Solution to Problem 1

(1) The right-hand side function $f\left(x,y\right)=\left|y\right|^{\alpha}$ is independent of $x$; we discuss two cases.

When $\alpha\ge1$, $f\left(x,y\right)$ satisfies a Lipschitz condition with respect to $y$: if $\alpha=1$, then $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|=\left|\right|y_1\left|-\right|y_2\left|\right|\le\left|y_1-y_2\right|$; if $\alpha> 1$, then $f\left(x,y\right)=\left|y\right|^{\alpha}$ has a continuous and bounded derivative $f_y=\alpha\left|y\right|^{\alpha-1}\operatorname{sign}\left(y\right)$ near $y=0$, which by the criterion for the Lipschitz condition (a continuous partial derivative in a convex region implies the Lipschitz condition) gives the result. By **Theorem 3.1** (Picard Existence and Uniqueness Theorem), the solution through $\left(0,0\right)$ is unique, namely the zero solution $y\equiv0$.

When $0< \alpha< 1$, $f\left(x,y\right)=\left|y\right|^{\alpha}$ is not Lipschitz near $y=0$ (the derivative $\alpha\left|y\right|^{\alpha-1}$ is unbounded as $y\to0$), so **Theorem 3.1** (Picard Existence and Uniqueness Theorem) cannot guarantee uniqueness. In fact, $y\equiv0$ is one solution; take another function

$$
y\left(x\right)=\begin{cases}0,&x\le0,\\ \big[\left(1-\alpha\right)x\big]^{\frac{1}{1-\alpha}},&x\ge0.\end{cases}
$$

It is continuously differentiable and $y\left(0\right)=0$. For $x> 0$, direct differentiation gives $y'=\big[\left(1-\alpha\right)x\big]^{\frac{\alpha}{1-\alpha}}=y^{\alpha}=\left|y\right|^{\alpha}$, so it is also a solution. The two solutions are different, hence the solution is not unique.

(2) The right-hand side function $f\left(x,y\right)=\begin{cases}0,&y=0,\\ y\ln\left|y\right|,&y\ne0\end{cases}$ is independent of $x$, and since $\lim\limits_{y\to0}y\ln\left|y\right|=0$, it is continuous. It does not satisfy a Lipschitz condition with respect to $y$ (at $y\ne0$, $f_y=\ln\left|y\right|+1$, which is unbounded as $y\to0$), so **Theorem 3.1** (Picard Existence and Uniqueness Theorem) cannot be used. Below, by an argument analogous to the proof of **Theorem 3.2** (Uniqueness of Solutions Under the Osgood Condition), we prove the uniqueness of the zero solution by contradiction.

Let $y=y\left(x\right)$ be a solution satisfying $y\left(0\right)=0$. Suppose for contradiction there is an $x_1> 0$ such that $y\left(x_1\right)> 0$ (the case of a negative value is analogous). Let $x_0=\inf\left\{x\ge0:\ y\left(x\right)> 0\ \text{于}\ \left(x,x_1\right]\right\}$, then $y\left(x_0\right)=0$, and on $\left(x_0,x_1\right]$, $y> 0$. On this interval set $u=\ln y$, then

$$
\frac{du}{dx}=\frac{y'}{y}=\ln y=u.
$$

The solution of this equation is $u=Ce^x$, i.e. on $\left(x_0,x_1\right]$, $y=e^{Ce^x}$. But from $y\left(x_0\right)=0$ we should have $u\left(x_0\right)=-\infty$, whereas $Ce^{x_0}$ is a finite number, a contradiction. Hence there is no point at which $y\left(x_1\right)\ne0$, i.e. $y\equiv0$ is the unique solution. This shows that failing to satisfy the Lipschitz condition does not necessarily imply non-uniqueness. $\blacksquare$

### Problem 2

(Problem 3-1, Problem 2) Find the Picard sequence for the initial value problem $\frac{dy}{dx}=x+y+1,\ y\left(0\right)=0$, and solve by taking the limit.

### Solution to Problem 2

By the equivalence between the integral equation and the initial value problem, this initial value problem is equivalent to the integral equation $y\left(x\right)=\displaystyle\int_0^x\big[t+y\left(t\right)+1\big]\,dt$; the Picard sequence is

$$
y_{n+1}\left(x\right)=\int_0^x\big[t+y_n\left(t\right)+1\big]\,dt,\quad y_0\left(x\right)=0.
$$

Computing the first few terms:

$$
y_1\left(x\right)=\int_0^x\left(t+1\right)\,dt=x+\frac{x^2}{2},
$$

$$
y_2\left(x\right)=\int_0^x\left[t+\left(t+\frac{t^2}{2}\right)+1\right]dt=\int_0^x\left(\frac{t^2}{2}+2t+1\right)dt=x+x^2+\frac{x^3}{6},
$$

$$
y_3\left(x\right)=\int_0^x\left[t+\left(t+t^2+\frac{t^3}{6}\right)+1\right]dt=x+x^2+\frac{x^3}{3}+\frac{x^4}{24}.
$$

If the Picard sequence converges to the solution $y=y\left(x\right)$, then the limit function satisfies the integral equation $y\left(x\right)=\displaystyle\int_0^x\big[t+y\left(t\right)+1\big]\,dt$, i.e. the differential equation $y'=x+y+1$ and the initial condition $y\left(0\right)=0$. This is the first-order linear equation $y'-y=x+1$; multiplying both sides by the integrating factor $e^{-x}$ gives

$$
\big(ye^{-x}\big)'=\left(x+1\right)e^{-x}.
$$

Integrating gives $ye^{-x}=-\left(x+2\right)e^{-x}+C$; substituting $y\left(0\right)=0$ gives $C=2$, hence

$$
y\left(x\right)=2e^x-x-2.
$$

$\blacksquare$
