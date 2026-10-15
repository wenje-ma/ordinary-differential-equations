# Assignment 9

> **Theorem 3.4** (Extension Theorem for Solutions)<br>Suppose in the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ the function $f\left(x,y\right)$ is continuous in an open region $G$, and $P_0\left(x_0,y_0\right)$ is any point in $G$. Then any integral curve through $P_0$ extends to the boundary within $G$: that is, for any bounded closed region $G_1$ ($P_0\in G_1\subset G$), the integral curve extends outside $G_1$. In other words, if the maximal interval of existence of a solution $y=y\left(x\right)$ is $\left(\alpha,\beta\right)$, then when $\beta<+\infty$, $\left(x,y\left(x\right)\right)$ approaches the boundary of $G$ (when $G=\mathbb{R}^2$, this means $\left|y\right|\to+\infty$).

> **Corollary** (Existence, Uniqueness, and Extension Under a Local Lipschitz Condition)<br>Suppose $f\left(x,y\right)$ is continuous in a region $G$ and satisfies a local Lipschitz condition with respect to $y$ (i.e. every point in $G$ has a neighborhood contained in $G$ in which $f$ satisfies a Lipschitz condition with respect to $y$). Then through any point $P_0$ in $G$ there exists a unique integral curve of the differential equation, and it extends to the boundary within $G$.

> **Theorem 3.5** (Global Existence of Solutions on a Strip)<br>Suppose the right-hand side function of the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ is continuous in the strip $S:\ \alpha<x<\beta,\ -\infty<y<+\infty$ and satisfies the inequality $\left|f\left(x,y\right)\right|\le A\left(x\right)\left|y\right|+B\left(x\right)$, where $A\left(x\right)\ge0$ and $B\left(x\right)\ge0$ are continuous on $\left(\alpha,\beta\right)$. Then every solution of the differential equation has $\left(\alpha,\beta\right)$ as its maximal interval of existence.

### Problem 1

(Problem 3-3, Problem 1) Using **Theorem 3.5** (Global Existence of Solutions on a Strip), prove: every solution $y=y\left(x\right)$ of the linear differential equation $\frac{dy}{dx}=a\left(x\right)y+b\left(x\right)$ ($x\in I$) has maximal interval of existence $I$, where $a\left(x\right)$ and $b\left(x\right)$ are assumed continuous on the interval $I$.

### Solution to Problem 1

The right-hand side function of this equation is $f\left(x,y\right)=a\left(x\right)y+b\left(x\right)$, which is continuous in the strip $S:\ x\in I,\ -\infty<y<+\infty$. We estimate

$$
\left|f\left(x,y\right)\right|=\left|a\left(x\right)y+b\left(x\right)\right|\le \left|a\left(x\right)\right|\,\left|y\right|+\left|b\left(x\right)\right|.
$$

Take $A\left(x\right)=\left|a\left(x\right)\right|$, $B\left(x\right)=\left|b\left(x\right)\right|$. Since $a\left(x\right),b\left(x\right)$ are continuous on $I$, $A\left(x\right)\ge0$ and $B\left(x\right)\ge0$ are both continuous on $I$. Thus $\left|f\left(x,y\right)\right|\le A\left(x\right)\left|y\right|+B\left(x\right)$ satisfies the conditions of **Theorem 3.5** (Global Existence of Solutions on a Strip), so every solution of this linear equation has the interval $I$ as its maximal interval of existence. $\blacksquare$

### Problem 2

(Problem 3-3, Problem 2(2)) Discuss the interval of existence of solutions of the differential equation $\frac{dy}{dx}=y\left(y-1\right)$.

### Solution to Problem 2

The right-hand side function $f\left(x,y\right)=y\left(y-1\right)$ is continuous on the entire plane and has continuous partial derivatives with respect to $y$; by the **Corollary** (Existence, Uniqueness, and Extension Under a Local Lipschitz Condition), the solution through any point exists uniquely. Separating variables, from $\frac{dy}{y\left(y-1\right)}=dx$ and $\frac{1}{y\left(y-1\right)}=\frac{1}{y-1}-\frac{1}{y}$, integrating gives

$$
\ln\left|\frac{y-1}{y}\right|=x+C,\quad\text{即}\quad y=\frac{1}{1-Ce^x}.
$$

The interval of existence is determined by the initial point $\left(x_0,y_0\right)$:

(1) The equilibrium solutions $y\equiv0$ and $y\equiv1$ exist on the entire $\left(-\infty,+\infty\right)$.

(2) If $0<y_0<1$, then $C=\frac{y_0-1}{y_0}<0$, the denominator $1-Ce^x>0$ always holds, and the solution exists on the entire $\left(-\infty,+\infty\right)$.

(3) If $y_0<0$ or $y_0>1$, then $C>0$, the denominator $1-Ce^x=0$ at the finite point $x=\ln\frac{1}{C}$, and the solution blows up there; hence the maximal interval of existence is a finite interval. $\blacksquare$

### Problem 3

(Problem 3-3, Problem 2(4)) Discuss the interval of existence of solutions of the differential equation $\frac{dy}{dx}=1+y^2$.

### Solution to Problem 3

The right-hand side function $f\left(x,y\right)=1+y^2$ is continuous on the entire plane and has continuous partial derivatives with respect to $y$; by the **Corollary** (Existence, Uniqueness, and Extension Under a Local Lipschitz Condition), the solution exists uniquely and extends to the entire plane. Separating variables $\frac{dy}{1+y^2}=dx$ and integrating gives $\arctan y=x+C$, i.e. $y=\tan\left(x+C\right)$. The domain of the tangent function requires $x+C\in\left(-\frac{\pi}{2},\frac{\pi}{2}\right)$, so the maximal interval of existence of each solution is the finite interval $\left(-\frac{\pi}{2}-C,\ \frac{\pi}{2}-C\right)$, with endpoints determined by the initial value.

$\blacksquare$

### Problem 4

(Problem 3-3, Problem 3) Consider the differential equation in symmetric form $x\,dx+y\,dy=0$, with domain $G=\left\{\left(x,y\right)\mid x^2+y^2>0\right\}$. The unit circle $\left(x^2+y^2=1\right)$ is an integral curve lying in the interior of $G$ and does not extend to the boundary of $G$. Does this contradict the extension theorem for solutions above? Why?

### Solution to Problem 4

No contradiction.

**Theorem 3.4** (Extension Theorem for Solutions) and its corollary apply to the normal form $\frac{dy}{dx}=f\left(x,y\right)$, which requires the right-hand side function $f\left(x,y\right)$ to be continuous on the entire open region $G$. In this problem, if we write the symmetric form $x\,dx+y\,dy=0$ in normal form $\frac{dy}{dx}=-\frac{x}{y}$, the right-hand side function is undefined on the line $y=0$ (the $x$-axis), and hence is not continuous on all of $G$ (the plane with the origin removed). The points on the $x$-axis lie entirely inside $G$, so the hypothesis of **Theorem 3.4** (Extension Theorem for Solutions) on all of $G$ does not hold.

The integral curve $x^2+y^2=C$ cannot traverse the full circle as a single-valued function $y=\varphi\left(x\right)$. It splits into upper and lower branches $y=\pm\sqrt{C-x^2}$, each with maximal $x$-interval of existence $\left(-\sqrt{C},\sqrt{C}\right)$. As $x\to\pm\sqrt{C}$, the curve reaches the points $\left(\pm\sqrt{C},0\right)$, i.e. the line $y=0$, which is exactly where the right-hand side in normal form loses continuity and is the effective boundary of its domain. Hence each branch of the integral curve extends to the boundary of its own domain, consistent with the extension theorem; there is no contradiction. $\blacksquare$

### Problem 5

(Problem 3-3, Problem 4) Let the maximal interval of existence of a solution of the initial value problem $\left(E\right)$: $\frac{dy}{dx}=\left(y^2-2y-3\right)e^{\left(x+y\right)^2},\ y\left(x_0\right)=y_0$ be $\left(a,b\right)$, where $\left(x_0,y_0\right)$ is any point in the plane. Then at least one of $a=-\infty$ and $b=+\infty$ holds.

### Solution to Problem 5

The right-hand side function $f\left(x,y\right)=\left(y^2-2y-3\right)e^{\left(x+y\right)^2}$ is continuous on the entire plane and has continuous partial derivatives with respect to $y$; by the **Corollary** (Existence, Uniqueness, and Extension Under a Local Lipschitz Condition), the solution through $\left(x_0,y_0\right)$ exists uniquely and, by **Theorem 3.4** (Extension Theorem for Solutions), extends to the boundary of the whole plane; but the whole plane has no finite boundary point, so if one endpoint is finite, then at that end $\left|y\right|\to+\infty$.

Note that $y^2-2y-3=\left(y-3\right)\left(y+1\right)$, and $e^{\left(x+y\right)^2}>0$, so the sign of $y'$ is determined by $\left(y-3\right)\left(y+1\right)$: when $y>3$ or $y<-1$, $y'>0$; when $-1<y<3$, $y'<0$.

First consider the right endpoint $b$. If $b<+\infty$, then necessarily $y\to+\infty$. In fact, when $y<-1$, $y'>0$ and the function is monotonically increasing, so it cannot tend to $-\infty$ as $x\to b^{-}$; hence blow-up at the right end can only be $y\to+\infty$, and the solution eventually enters the region $y>3$ and rises monotonically.

Next consider the left endpoint $a$. If $a>-\infty$, by the same argument the solution eventually enters the region $y<-1$, where $y'>0$, and as $x\to a^{+}$ one can only have $y\to-\infty$.

Suppose for contradiction that both $a>-\infty$ and $b<+\infty$ hold. Then the solution must grow monotonically from $y\to-\infty$ as $x\to a^{+}$ to $y\to+\infty$ as $x\to b^{-}$, and therefore must cross the interval $\left(-1,3\right)$. But inside $\left(-1,3\right)$, $y'<0$ and the function is monotonically decreasing, contradicting its monotonic rise from $-\infty$ to $+\infty$. More precisely: once the solution rises in the region $y<-1$ (where $y'>0$) and approaches $y=-1$, at $y=-1$, $y'=0$; upon just entering $\left(-1,3\right)$, $y'<0$, which pushes it back below $y=-1$. Hence the solution cannot cross $y=-1$ into $\left(-1,3\right)$, let alone reach $y>3$ and blow up to $+\infty$.

Therefore $a>-\infty$ and $b<+\infty$ cannot both hold; i.e. at least one of $a=-\infty$ and $b=+\infty$ holds. $\blacksquare$
