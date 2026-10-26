# Assignment 15

> **Standard System of Differential Equations and Vector Form**<br>Taking the number of unknown functions equal to the order of the differential equation, the resulting standard system is $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$ ($i=1,\cdots,n$). Using column vectors $y=\left(y_1,\cdots,y_n\right)^\top$, $f=\left(f_1,\cdots,f_n\right)^\top$, the vector form is $\frac{dy}{dx}=f\left(x,y\right)$, where $f\left(x,y\right)$ is continuous on a region $D\subset R^{n+1}$. Adding the initial condition $y\left(x_0\right)=y_0$ gives the Cauchy problem.

> **Norm of a Vector and Its Basic Properties**<br>In the $n$-dimensional linear space $R^n$, one can define the norm $\left|y\right|$ of a vector, e.g. the Euclidean norm $\left|y\right|=\sqrt{y_1^2+\cdots+y_n^2}$. Basic properties of the norm: for any $y,z\in R^n$, the triangle inequality $\left|y+z\right|\le\left|y\right|+\left|z\right|$ holds. After introducing a norm, $R^n$ becomes an $n$-dimensional normed linear space, in which the corresponding calculus and uniform convergence can be developed.

> **Lipschitz Condition**<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$. If there exists a constant $L\ge0$ such that for all $\left(x,y_1\right),\left(x,y_2\right)\in R$, $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, then $f$ is said to satisfy a Lipschitz condition with respect to $y$ on $R$.

> **Picard Existence and Uniqueness Theorem ($n$-dimensional Vector Form)**<br>Suppose $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Let $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has a unique solution on the interval $\left|x-x_0\right|\le h$.

> **Peano Existence Theorem ($n$-dimensional Vector Form)**<br>Suppose $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$. Let $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has at least one solution on the interval $\left|x-x_0\right|\le h$ (uniqueness is not guaranteed).

> **Picard Sequence and Its Uniform Convergence Estimate**<br>The integral equation equivalent to the Cauchy problem is $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. Construct the Picard sequence $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. By induction one can prove $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$, which implies that the Picard sequence converges uniformly on $\left|x-x_0\right|\le h$.

> **Ascoli's Lemma and the Gronwall Inequality**<br>Ascoli's Lemma: a uniformly bounded and equicontinuous sequence of functions on a bounded closed interval always has a uniformly convergent subsequence. Gronwall's inequality: if a nonnegative continuous function $u\left(x\right)$ satisfies $u\left(x\right)\le A+L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$, then $u\left(x\right)\le Ae^{L\left|x-x_0\right|}$.

> **Weierstrass M-test (Uniform Convergence)**<br>If the general term of a series of functions $\displaystyle\sum_{k=0}^{\infty}u_k\left(x\right)$ satisfies $\left|u_k\left(x\right)\right|\le M_k$ for all $x$, and the numerical series $\displaystyle\sum_{k=0}^{\infty}M_k$ converges, then the series of functions converges uniformly on the corresponding interval.

### Problem 1

(Problem 5-2, Problem 2) For the $n$-dimensional vector form of a differential equation, state the corresponding Picard existence and uniqueness theorem and Peano existence theorem, and write out the main steps of the proof.

### Solution to Problem 1

(1) **Picard Existence and Uniqueness Theorem**. Suppose $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$: $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$. Let $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has a unique solution on the interval $\left|x-x_0\right|\le h$.

The main steps of the proof are as follows.

Step 1: by the **Standard System of Differential Equations and Vector Form** and the equivalence between the integral equation and the differential equation, the Cauchy problem is equivalent to the integral equation

$$
y\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt.
$$

Step 2: by the **Picard Sequence and Its Uniform Convergence Estimate**, construct the Picard sequence $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. By induction one can prove $\left|y_k\left(x\right)-y_0\right|\le M\left|x-x_0\right|\le Mh\le b$, so all approximate solutions stay inside the region $R$.

Step 3: by induction prove the estimate $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$ ($k=0,1,2,\cdots$). It follows from the **Lipschitz Condition** and the integral recursion: the base step $k=0$ gives $\left|y_1-y_0\right|\le M\left|x-x_0\right|$; the inductive step follows from $\left|y_{k+1}-y_k\right|\le L\displaystyle\int_{x_0}^{x}\left|y_k-y_{k-1}\right|dt$. Since the numerical series $\displaystyle\sum_{k=0}^{\infty}\frac{ML^kh^{k+1}}{\left(k+1\right)!}$ converges, by the **Weierstrass M-test (Uniform Convergence)**, the Picard sequence converges uniformly on $\left|x-x_0\right|\le h$ to a continuous function $y\left(x\right)$.

Step 4: by the continuity of $f$ and the uniform convergence of the Picard sequence, taking the limit under the integral sign gives $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$, i.e. $y\left(x\right)$ is a solution of the Cauchy problem.

Step 5: prove uniqueness. Suppose $y\left(x\right),\ z\left(x\right)$ are both solutions; let $u\left(x\right)=\left|y\left(x\right)-z\left(x\right)\right|$, then $u\left(x\right)\le L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$. By the **Gronwall inequality**, $u\left(x\right)\equiv0$, so $y\left(x\right)\equiv z\left(x\right)$.

(2) **Peano Existence Theorem**. Suppose $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ (without requiring a Lipschitz condition), $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem has at least one solution on $\left|x-x_0\right|\le h$.

The main steps of the proof are as follows.

Step 1: on $\left|x-x_0\right|\le h$, construct the Euler broken-line approximate solution sequence $y_n\left(x\right)$: with initial value $y_n\left(x_0\right)=y_0$, on each small interval take the slope at the right endpoint $f\left(x_k,y_n\left(x_k\right)\right)$ to draw a line segment.

Step 2: uniform boundedness and equicontinuity. From $\left|\frac{dy_n}{dx}\right|\le M$ we get $\left|y_n\left(x\right)-y_0\right|\le M\left|x-x_0\right|\le b$, so the sequence is uniformly bounded; and $\left|y_n\left(x\right)-y_n\left(x'\right)\right|\le M\left|x-x'\right|$, so the sequence is equicontinuous.

Step 3: by **Ascoli's Lemma**, there exists a uniformly convergent subsequence $y_{n_k}\left(x\right)\to y\left(x\right)$, with $y$ continuous.

Step 4: by the uniform continuity of $f$ on the bounded closed region $R$, $f\left(t,y_{n_k}\left(t\right)\right)\to f\left(t,y\left(t\right)\right)$ uniformly; taking the limit on both sides of the integral identity for the Euler broken line $y_{n_k}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_{n_k}\left(t\right)\right)dt$ gives $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$, so $y\left(x\right)$ is a solution of the Cauchy problem. Existence is proved (uniqueness is not guaranteed).

$\blacksquare$

### Problem 2

(Problem 5-2, Problem 3) For the initial value problem of an $n$-th order linear system of differential equations, state and prove the existence and uniqueness theorem for solutions.

### Solution to Problem 2

**Statement of the theorem**. Suppose the matrix function $A\left(x\right)=\left(a_{ij}\left(x\right)\right)_{n\times n}$ and the vector function $e\left(x\right)$ are both continuous on the interval $\left(\alpha,\beta\right)$. Then the Cauchy problem for the linear system

$$
\frac{dy}{dx}=A\left(x\right)y+e\left(x\right),\quad y\left(x_0\right)=y_0
$$

(where $\alpha< x_0< \beta$, $y_0\in R^n$) has a solution that exists and is unique on the entire interval $\left(\alpha,\beta\right)$.

**Proof**. Let $f\left(x,y\right)=A\left(x\right)y+e\left(x\right)$.

Step 1: continuity. Since $A\left(x\right),e\left(x\right)$ are continuous, $f\left(x,y\right)$ is continuous in $\left(x,y\right)$.

Step 2: locally satisfies the **Lipschitz Condition**. For any $y_1,y_2$,

$$
\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|=\left|A\left(x\right)\left(y_1-y_2\right)\right|\le\left\|A\left(x\right)\right\|\cdot\left|y_1-y_2\right|.
$$

On any bounded closed subinterval $\left[c,d\right]\subset\left(\alpha,\beta\right)$, $\left\|A\left(x\right)\right\|$ is continuous and hence has an upper bound $L$, so $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$. By the **Picard Existence and Uniqueness Theorem ($n$-dimensional Vector Form)**, the solution exists and is unique locally.

Step 3: extend to the entire $\left(\alpha,\beta\right)$. Suppose the maximal interval of existence of the solution $y=y\left(x\right)$ is $\left(\omega_1,\omega_2\right)$. Assume $\omega_2< \beta$. On $\left[x_0,\omega_2\right)$, both $\left\|A\left(x\right)\right\|$ and $\left|e\left(x\right)\right|$ are bounded, denote them by $M_1,M_2$; then

$$
\left|y'\left(x\right)\right|\le\left\|A\left(x\right)\right\|\left|y\left(x\right)\right|+\left|e\left(x\right)\right|\le M_1\left|y\left(x\right)\right|+M_2.
$$

By the **Gronwall inequality**, $\left|y\left(x\right)\right|\le\left(\left|y_0\right|+M_2\left(\omega_2-x_0\right)\right)e^{M_1\left(\omega_2-x_0\right)}$ is bounded on $\left[x_0,\omega_2\right)$. Hence $\left|y'\left(x\right)\right|\le M_1\left|y\left(x\right)\right|+M_2$ is also bounded, so as $x\to\omega_2^{-}$, $y\left(x\right)$ converges to some limit $y_*$ (a function with bounded derivative is a Cauchy sequence). Taking $y\left(\omega_2\right)=y_*$ as a new initial value, by the Picard existence and uniqueness theorem the solution can be extended to the right past $\omega_2$, contradicting that $\omega_2$ is the maximal right endpoint. Hence $\omega_2=\beta$. Similarly $\omega_1=\alpha$.

Step 4: uniqueness is guaranteed locally by the Picard existence and uniqueness theorem, and no branching occurs during extension, so it is unique globally. The theorem is proved.

$\blacksquare$
