# Assignment 24

> **Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability)<br>Consider a solution $\boldsymbol{x} = \boldsymbol{\varphi}\left(t\right)$ of the equation $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}\left(t,\boldsymbol{x}\right)$. If for any given $\varepsilon > 0$, there exists $\delta = \delta\left(\varepsilon, t_0\right) > 0$ such that whenever $\left\|\boldsymbol{x}_0 - \boldsymbol{\varphi}\left(t_0\right)\right\| < \delta$, the solution $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right)$ with initial condition $\boldsymbol{x}\left(t_0\right) = \boldsymbol{x}_0$ is defined for $t \ge t_0$ and satisfies $\left\|\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right)\right\| < \varepsilon$ for all $t \ge t_0$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is said to be stable (in the sense of Lyapunov). If the solution $\boldsymbol{\varphi}\left(t\right)$ is stable, and there exists $\delta_0 > 0$ such that whenever $\left\|\boldsymbol{x}_0 - \boldsymbol{\varphi}\left(t_0\right)\right\| < \delta_0$, we have $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right) \to \boldsymbol{0}\ \left(t \to +\infty\right)$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is said to be asymptotically stable. If the solution $\boldsymbol{\varphi}\left(t\right)$ is not stable, it is said to be unstable. If the basin of attraction is the entire space, i.e. regardless of the size of the initial value, $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right) \to \boldsymbol{0}$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is said to be globally asymptotically stable.

> **Theorem 8.1** (Eigenvalue Criterion for Stability of the Zero Solution of a Constant-Coefficient Linear System)<br>Suppose the matrix $A$ in the linear equation $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$ is a constant matrix. Then (1) the zero solution is asymptotically stable if and only if all eigenvalues of $A$ have negative real part; (2) the zero solution is stable if and only if all eigenvalues of $A$ have non-positive real part, and the Jordan blocks corresponding to eigenvalues with zero real part are all of order one; (3) the zero solution is unstable if and only if at least one eigenvalue of $A$ has positive real part, or at least one eigenvalue has zero real part and the corresponding Jordan block is of order higher than one.

> **Theorem 8.3** (Judging Instability by Linear Approximation)<br>Suppose $A$ in the nonlinear equation $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x} + \boldsymbol{N}\left(t,\boldsymbol{x}\right)$ is a constant matrix, and at least one eigenvalue of $A$ has positive real part. Then the zero solution of the equation is unstable.

> **Theorem 8.4** (Lyapunov's Stability Criterion)<br>Suppose the right-hand side of the autonomous system $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}\left(\boldsymbol{x}\right)$ satisfies the existence and uniqueness conditions for the initial value problem, and there exists a continuously differentiable scalar function $V\left(\boldsymbol{x}\right)$. Denote the total derivative of $V$ along a trajectory with respect to $t$ as $\frac{dV}{dt} = \sum_{i=1}^{n}\frac{\partial V}{\partial x_i}f_i\left(\boldsymbol{x}\right)$. If condition $I$ ($V\left(\boldsymbol{0}\right) = 0,\ V\left(\boldsymbol{x}\right) > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, called a positive definite function $V$) holds, then (1) if condition $II$ ($\frac{dV}{dt} < 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, i.e. the total derivative is a negative definite function) also holds, the zero solution is asymptotically stable; (2) if condition $II^*$ ($\frac{dV}{dt} \le 0$, i.e. the total derivative is a negative semi-definite function) holds, the zero solution is stable; (3) if condition $III$ ($\frac{dV}{dt} > 0,\ \boldsymbol{x} \ne \boldsymbol{0}$, i.e. the total derivative is a positive definite function) holds, the zero solution is unstable.

### Problem 1

(Problem 8-2, Problem 1) Prove: asymptotic stability of the zero solution of a linear equation is equivalent to its global asymptotic stability.

### Solution to Problem 1

Let the linear equation be $\frac{d\boldsymbol{x}}{dt} = A\left(t\right)\boldsymbol{x}$, with fundamental matrix $\Phi\left(t, t_0\right)$; then the solution with initial condition $\boldsymbol{x}\left(t_0\right) = \boldsymbol{x}_0$ is

$$
\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) = \Phi\left(t, t_0\right)\boldsymbol{x}_0.
$$

By **Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability), it is obvious that global asymptotic stability implies asymptotic stability; it suffices to prove the converse. Suppose the zero solution is asymptotically stable. By definition, the zero solution is stable, so there exists a constant $M > 0$ such that $\left\|\Phi\left(t, t_0\right)\right\| \le M\ \left(t \ge t_0\right)$; and there exists $\delta_0 > 0$ such that whenever $\left\|\boldsymbol{x}_0\right\| < \delta_0$, we have $\Phi\left(t, t_0\right)\boldsymbol{x}_0 \to \boldsymbol{0}\ \left(t \to +\infty\right)$.

Now take any initial value $\boldsymbol{x}_0^*$ (its norm may be arbitrarily large). If $\boldsymbol{x}_0^* \ne \boldsymbol{0}$, let

$$
\boldsymbol{y}_0 = \frac{\delta_0}{2\left\|\boldsymbol{x}_0^*\right\|}\boldsymbol{x}_0^*.
$$

Then $\left\|\boldsymbol{y}_0\right\| = \delta_0/2 < \delta_0$, and by asymptotic stability $\Phi\left(t, t_0\right)\boldsymbol{y}_0 \to \boldsymbol{0}$. By linearity of the solution with respect to the initial value,

$$
\Phi\left(t, t_0\right)\boldsymbol{y}_0 = \frac{\delta_0}{2\left\|\boldsymbol{x}_0^*\right\|}\Phi\left(t, t_0\right)\boldsymbol{x}_0^*.
$$

Since the coefficient $\frac{\delta_0}{2\left\|\boldsymbol{x}_0^*\right\|}$ is a positive constant, $\Phi\left(t, t_0\right)\boldsymbol{x}_0^* \to \boldsymbol{0}$. This shows that the solution corresponding to any initial value (regardless of its magnitude) tends to the zero vector, i.e. the basin of attraction is the entire space. Combined with the already-proved stability (the solution is bounded for any initial value), the zero solution is globally asymptotically stable. $\blacksquare$

### Problem 2

(Problem 8-2, Problem 2) Let $x$ and $t$ both be scalars. Find the necessary and sufficient conditions for the zero solution of the equation $\frac{dx}{dt} = a\left(t\right)x$ to be stable or asymptotically stable.

### Solution to Problem 2

The equation is separable; the solution with initial condition $x\left(t_0\right) = x_0$ is

$$
x\left(t\right) = x_0\exp\!\left(\int_{t_0}^{t}a\left(s\right)\,ds\right).
$$

Denote $A\left(t\right) = \int_{t_0}^{t}a\left(s\right)\,ds$; then $\left|x\left(t\right)\right| = \left|x_0\right|\,e^{A\left(t\right)}$.

First discuss asymptotic stability. By **Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability), asymptotic stability of the zero solution requires that for all initial values $x_0$, $x\left(t\right) \to 0\ \left(t \to +\infty\right)$, i.e. $e^{A\left(t\right)} \to 0$, which is equivalent to

$$
\lim_{t \to +\infty}A\left(t\right) = -\infty.
$$

Hence the necessary and sufficient condition for asymptotic stability of the zero solution is $\int_{t_0}^{t}a\left(s\right)\,ds \to -\infty\ \left(t \to +\infty\right)$.

Next discuss stability. Stability of the zero solution requires: for any $\varepsilon > 0$, there exists $\delta > 0$ such that when $\left|x_0\right| < \delta$, $\left|x\left(t\right)\right| < \varepsilon$ for all $t \ge t_0$, i.e. $e^{A\left(t\right)}$ is bounded above for $t \ge t_0$. This is equivalent to $A\left(t\right)$ being bounded above for $t \ge t_0$:

$$
\sup_{t \ge t_0}\int_{t_0}^{t}a\left(s\right)\,ds < +\infty.
$$

Hence the necessary and sufficient condition for stability of the zero solution is that $\int_{t_0}^{t}a\left(s\right)\,ds$ remains bounded above as $t \to +\infty$. $\blacksquare$

### Problem 3

(Problem 8-2, Problem 3) For the equation in polar coordinates $\frac{d\theta}{dt} = 1,\ \frac{dr}{dt} = \begin{cases} r^2\sin\frac{1}{r}, & r > 0, \\ 0, & r = 0, \end{cases}$ sketch the phase portrait near the origin and study the stability of the equilibrium point $r = 0$.

### Solution to Problem 3

From $\frac{d\theta}{dt} = 1$, the trajectories rotate counterclockwise around the origin with constant angular velocity $1$. The radial equation $\frac{dr}{dt} = r^2\sin\frac{1}{r}$ has right-hand side zero when $\sin\frac{1}{r} = 0$ for $r > 0$, i.e.

$$
r = r_n = \frac{1}{n\pi}\quad\left(n = 1, 2, 3, \cdots\right)
$$

Thus each circle $r = r_n$ is an equilibrium circle of the radial equation, i.e. a closed orbit (periodic trajectory) of the original system.

Between two adjacent circles, $\sin\frac{1}{r}$ has a constant sign: when $r \in \left(\frac{1}{\left(2k+1\right)\pi}, \frac{1}{2k\pi}\right)$, $\sin\frac{1}{r} > 0$, and the trajectory monotonically approaches the outer boundary $r = \frac{1}{2k\pi}$; when $r \in \left(\frac{1}{\left(2k+2\right)\pi}, \frac{1}{\left(2k+1\right)\pi}\right)$, $\sin\frac{1}{r} < 0$, and the trajectory monotonically approaches the inner boundary $r = \frac{1}{\left(2k+2\right)\pi}$. Hence the phase portrait is as follows: near the origin there are infinitely many concentric circular closed orbits, and in the annular region between adjacent closed orbits, the trajectories rotate counterclockwise while monotonically spiraling toward one of the boundary closed orbits.

Now study the stability of the equilibrium point $r = 0$. By **Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability), for any $\varepsilon > 0$, take a sufficiently large positive integer $N$ such that $r_N = \frac{1}{N\pi} < \varepsilon$, and set $\delta = r_N$. When the initial value $r_0 < \delta$, since each circle $r = r_n$ is an invariant closed orbit, the trajectories cannot cross them, so the annular interval $\left(r_{k+1}, r_k\right)$ (where $k \ge N$) containing the initial value is positively invariant, and hence

$$
r\left(t\right) < r_k \le r_N = \delta < \varepsilon\quad\left(t \ge 0\right).
$$

Thus $r = 0$ is stable. But it is not asymptotically stable: any closed orbit $r = r_n$ is itself a periodic trajectory, and trajectories on it never approach the origin; any trajectory starting from an annular region also remains in that region forever and does not approach the origin. Hence the equilibrium point $r = 0$ is stable but not asymptotically stable. $\blacksquare$

### Problem 4

(Problem 8-2, Problem 4) Consider the second-order constant-coefficient linear equation $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$, where $A$ is a $2 \times 2$ constant matrix. Denote $p = -\text{tr}\left[A\right]$ (the negative of the trace of $A$) and $q = \det\left[A\right]$, and assume $p^2 + q^2 \ne 0$. Prove: (1) when $p > 0$ and $q > 0$, the zero solution is asymptotically stable; (2) when $p > 0$ and $q = 0$, or $p = 0$ and $q > 0$, the zero solution is stable but not asymptotically stable; (3) in all other cases, the zero solution is unstable.

### Solution to Problem 4

The characteristic equation of the matrix $A$ is

$$
\det\left(\lambda I - A\right) = \lambda^2 - \text{tr}\left[A\right]\,\lambda + \det\left[A\right] = \lambda^2 + p\lambda + q = 0.
$$

Thus the two eigenvalues $\lambda_1, \lambda_2$ satisfy $\lambda_1 + \lambda_2 = -p,\ \lambda_1\lambda_2 = q$. By **Theorem 8.1** (Eigenvalue Criterion for Stability of the Zero Solution of a Constant-Coefficient Linear System), we discuss three cases.

(1) When $p > 0$ and $q > 0$, $\lambda_1\lambda_2 > 0$ means the two eigenvalues have the same sign (either real roots of the same sign or conjugate complex roots); and $\lambda_1 + \lambda_2 = -p < 0$ means the sum of their real parts is negative, so the real parts of both eigenvalues are negative. By Theorem 8.1(1), the zero solution is asymptotically stable.

(2) When $p > 0$ and $q = 0$, the characteristic equation is $\lambda\left(\lambda + p\right) = 0$, with eigenvalues $\lambda = 0$ and $\lambda = -p < 0$. The Jordan block corresponding to the zero eigenvalue is of order one (the two eigenvalues are distinct), and the other eigenvalue has negative real part. By Theorem 8.1(2), the zero solution is stable; but since there is an eigenvalue with zero real part, by Theorem 8.1(1) it is not asymptotically stable.

When $p = 0$ and $q > 0$, the eigenvalues are $\lambda = \pm i\sqrt{q}$, a pair of purely imaginary roots, and the corresponding Jordan blocks are all of order one. By Theorem 8.1(2), the zero solution is stable; but since both eigenvalues have zero rather than negative real part, by Theorem 8.1(1) it is not asymptotically stable.

(3) All other cases. If $q < 0$, then $\lambda_1\lambda_2 < 0$, so the two eigenvalues are real roots of opposite sign, and at least one has positive real part; by Theorem 8.1(3), the zero solution is unstable. If $q > 0$ and $p < 0$, then the sum of the real parts is $-p > 0$, so both have positive real part (real roots or conjugate complex roots); by Theorem 8.1(3), the zero solution is unstable. If $q = 0$ and $p < 0$, then the eigenvalues are $\lambda = 0$ and $\lambda = -p > 0$, and the latter has positive real part; by Theorem 8.1(3), the zero solution is unstable. The case $p = q = 0$ is excluded by $p^2 + q^2 \ne 0$. Hence in all other cases the zero solution is unstable. $\blacksquare$

### Problem 5

(Problem 8-2, Problem 5) Discuss the stability of the zero solution of the two-dimensional system $\begin{cases}\frac{dx}{dt} = y - xf\left(x,y\right), \\ \frac{dy}{dt} = -x - yf\left(x,y\right)\end{cases}$, where the function $f\left(x,y\right)$ is continuously differentiable near $\left(0,0\right)$.

### Solution to Problem 5

Take the Lyapunov function $V\left(x,y\right) = x^2 + y^2$. It satisfies $V\left(0,0\right) = 0$, and $V\left(x,y\right) > 0$ when $\left(x,y\right) \ne \left(0,0\right)$, i.e. $V$ is a positive definite function. Compute the total derivative of $V$ along trajectories:

$$
\frac{dV}{dt} = 2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 2x\bigl(y - xf\bigr) + 2y\bigl(-x - yf\bigr) = -2f\left(x,y\right)\bigl(x^2 + y^2\bigr).
$$

By **Theorem 8.4** (Lyapunov's Stability Criterion), discuss cases.

If $f\left(x,y\right) > 0$ near the origin (in particular, when $f\left(0,0\right) > 0$, by continuity it is positive near the origin), then $\frac{dV}{dt} < 0$ when $\left(x,y\right) \ne \left(0,0\right)$, i.e. the total derivative is a negative definite function; by Theorem 8.4(1), the zero solution is asymptotically stable.

If $f\left(x,y\right) < 0$ near the origin (in particular, when $f\left(0,0\right) < 0$), then $\frac{dV}{dt} > 0$ when $\left(x,y\right) \ne \left(0,0\right)$, i.e. the total derivative is a positive definite function; by Theorem 8.4(3), the zero solution is unstable.

If $f\left(0,0\right) = 0$, the sign of the total derivative depends on the higher-order behavior of $f\left(x,y\right)$ near the origin: when $f\left(x,y\right)$ remains positive near the origin, the zero solution is asymptotically stable; when it remains negative, the zero solution is unstable; when $f\left(x,y\right)$ changes sign near the origin, this Lyapunov function alone cannot determine stability, and higher-order analysis is needed. $\blacksquare$

### Problem 6

(Problem 8-2, Problem 6) Let $x \in \mathbb{R}^1$, the function $g\left(x\right)$ be continuous, and $xg\left(x\right) > 0$ when $x \ne 0$. Prove that the zero solution of the equation $\ddot{x} + g\left(x\right) = 0$ is stable but not asymptotically stable.

### Solution to Problem 6

Convert the second-order equation into the first-order system $\frac{dx}{dt} = y,\ \frac{dy}{dt} = -g\left(x\right)$. Take the Lyapunov function

$$
V\left(x,y\right) = \frac{1}{2}y^2 + \int_{0}^{x}g\left(s\right)\,ds.
$$

From the condition $xg\left(x\right) > 0$ when $x \ne 0$, we know: when $x > 0$, $g\left(x\right) > 0$; when $x < 0$, $g\left(x\right) < 0$. Hence when $x \ne 0$, $\int_{0}^{x}g\left(s\right)\,ds > 0$, and together with $\frac{1}{2}y^2 \ge 0$, we have $V\left(0,0\right) = 0$ and $V\left(x,y\right) > 0$ when $\left(x,y\right) \ne \left(0,0\right)$, i.e. $V$ is a positive definite function. Compute the total derivative:

$$
\frac{dV}{dt} = y\frac{dy}{dt} + g\left(x\right)\frac{dx}{dt} = y\bigl(-g\left(x\right)\bigr) + g\left(x\right)y = 0.
$$

The total derivative is identically zero, which certainly satisfies the negative semi-definite condition. By conclusion (2) of **Theorem 8.4** (Lyapunov's Stability Criterion), the zero solution is stable.

It is not asymptotically stable: since $\frac{dV}{dt} \equiv 0$, the trajectories always remain on the level curve $V\left(x,y\right) = C$. Taking $C > 0$, the level curve $V = C$ is a closed curve around the origin (or at least does not contain the origin), and trajectories on it do not approach the origin at $V = 0$. Hence the zero solution is stable but not asymptotically stable. $\blacksquare$

### Problem 7

(Problem 8-2, Problem 7) Study the stability of the two equilibrium points of the two-dimensional system $\begin{cases}\frac{dx}{dt} = y, \\ \frac{dy}{dt} = -1 + x^2\end{cases}$.

### Solution to Problem 7

The equilibrium points satisfy $y = 0,\ -1 + x^2 = 0$, so the two equilibrium points are $\left(1,0\right)$ and $\left(-1,0\right)$.

First study the equilibrium point $\left(1,0\right)$. The Jacobian matrix of the right-hand side functions $\left(y,\ x^2 - 1\right)$ at $\left(1,0\right)$ is

$$
J = \begin{bmatrix}0 & 1 \\ 2x & 0\end{bmatrix}\bigg|_{x = 1} = \begin{bmatrix}0 & 1 \\ 2 & 0\end{bmatrix}.
$$

Its characteristic equation is $\lambda^2 - 2 = 0$, with eigenvalues $\lambda = \pm\sqrt{2}$, where $\sqrt{2} > 0$ has positive real part. By **Theorem 8.3** (Judging Instability by Linear Approximation), the equilibrium point $\left(1,0\right)$ is unstable.

Next study the equilibrium point $\left(-1,0\right)$. Its Jacobian matrix is

$$
J = \begin{bmatrix}0 & 1 \\ 2x & 0\end{bmatrix}\bigg|_{x = -1} = \begin{bmatrix}0 & 1 \\ -2 & 0\end{bmatrix}.
$$

The characteristic equation is $\lambda^2 + 2 = 0$, with eigenvalues $\lambda = \pm i\sqrt{2}$, purely imaginary roots; linear approximation cannot determine stability, so we use Lyapunov's second method. Take the function

$$
V\left(x,y\right) = \frac{1}{2}y^2 + x - \frac{1}{3}x^3 + \frac{2}{3}.
$$

Compute the total derivative:

$$
\frac{dV}{dt} = y\frac{dy}{dt} + \left(1 - x^2\right)\frac{dx}{dt} = y\left(x^2 - 1\right) + \left(1 - x^2\right)y = 0.
$$

Let $u = x + 1$ and expand near $\left(-1,0\right)$:

$$
V = \frac{1}{2}y^2 + u^2 - \frac{1}{3}u^3.
$$

Its quadratic part $\frac{1}{2}y^2 + u^2$ is positive definite, and the cubic term $-\frac{1}{3}u^3$ is a higher-order infinitesimal, so in a small neighborhood of $\left(-1,0\right)$, $V$ is a positive definite function, and the total derivative is identically zero (negative semi-definite). By conclusion (2) of **Theorem 8.4** (Lyapunov's Stability Criterion), the equilibrium point $\left(-1,0\right)$ is stable; and since the total derivative is identically zero, nearby trajectories move along level curves $V = C$ and do not approach the point, so it is not asymptotically stable. $\blacksquare$

### Problem 8

(Problem 8-2, Problem 8(2)) Discuss the stability of the zero solution of the system $\begin{cases}\frac{dx}{dt} = -y^3 - x^5, \\ \frac{dy}{dt} = x^3 - y^5\end{cases}$.

### Solution to Problem 8

Take the Lyapunov function $V\left(x,y\right) = x^4 + y^4$. Clearly $V\left(0,0\right) = 0$, and $V\left(x,y\right) > 0$ when $\left(x,y\right) \ne \left(0,0\right)$, i.e. $V$ is a positive definite function. Compute the total derivative:

$$
\frac{dV}{dt} = 4x^3\frac{dx}{dt} + 4y^3\frac{dy}{dt} = 4x^3\bigl(-y^3 - x^5\bigr) + 4y^3\bigl(x^3 - y^5\bigr).
$$

After expansion, the cross terms $-4x^3y^3$ and $+4x^3y^3$ cancel, giving

$$
\frac{dV}{dt} = -4x^8 - 4y^8 < 0\quad\left(\left(x,y\right) \ne \left(0,0\right)\right).
$$

That is, the total derivative is a negative definite function. By conclusion (1) of **Theorem 8.4** (Lyapunov's Stability Criterion), the zero solution is asymptotically stable. $\blacksquare$

### Problem 9

(Problem 8-2, Problem 8(4)) Discuss the stability of the zero solution of the system $\begin{cases}\frac{dx}{dt} = 2x^2y + y^3, \\ \frac{dy}{dt} = -xy^2 + 2x^5\end{cases}$.

### Solution to Problem 9

First try the Lyapunov function $V\left(x,y\right) = x^2 + y^2$, which is positive definite. Compute the total derivative:

$$
\frac{dV}{dt} = 2x\frac{dx}{dt} + 2y\frac{dy}{dt} = 2x\left(2x^2y + y^3\right) + 2y\left(-xy^2 + 2x^5\right) = 4x^3y\left(1 + x^2\right).
$$

Its sign changes as $xy$ changes sign, so it is not a definite function; this function cannot directly determine stability. Below we analyze directly from the definition of instability.

Consider the wedge-shaped region $R = \left\{\left(x,y\right): x > 0,\ 0 < y < x^2\right\}$ above the positive $x$-axis. Inside $R$, since $y < x^2$, we have $y^2 < x^4$, and thus

$$
\frac{dy}{dt} = -xy^2 + 2x^5 > -x\cdot x^4 + 2x^5 = x^5 > 0,
$$

and $\frac{dx}{dt} = y\left(2x^2 + y^2\right) > 0$.

Next verify that $R$ is a positively invariant region. On the boundary $y = 0$, $\frac{dy}{dt} = 2x^5 > 0$, so trajectories cannot exit from the $y > 0$ side; on the boundary $y = x^2$, compute

$$
\frac{d}{dt}\left(y - x^2\right) = \frac{dy}{dt} - 2x\frac{dx}{dt} = -xy^2 + 2x^5 - 4x^3y - 2xy^3.
$$

Substituting $y = x^2$, we get

$$
\frac{d}{dt}\left(y - x^2\right)\bigg|_{y = x^2} = -x^5 + 2x^5 - 4x^5 - 2x^7 = -3x^5 - 2x^7 < 0\quad\left(x > 0\right),
$$

i.e. on this boundary the trajectories are pressed toward the $y < x^2$ side. Hence the wedge-shaped region $R$ is positively invariant.

Now take any sufficiently small positive number $\rho > 0$; a trajectory starting from a point $\left(x_0, 0\right)$ on the positive $x$-axis ($x_0 > 0$ arbitrarily small) immediately enters $R$ because $\frac{dy}{dt} = 2x_0^5 > 0$, and evolves monotonically inside $R$. If it always remained in the disk $x^2 + y^2 < \rho^2$, then $\frac{dx}{dt} > 0$ would force $x\left(t\right)$ to increase monotonically and approach a finite limit $x^*$, and thus $\frac{dx}{dt} \to 0$, i.e. $y\left(2x^2 + y^2\right) \to 0$. Since $x \to x^* > 0$, we must have $y\left(t\right) \to 0$, but then $\frac{dy}{dt} \to 2x^{*5} > 0$, contradicting $y\left(t\right) \to 0$. Hence this trajectory must exit the disk $x^2 + y^2 < \rho^2$ in finite time.

By **Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability), no matter how small a neighborhood of the origin, there always exists a trajectory starting from within it that exits a given $\varepsilon$-neighborhood; hence the zero solution is unstable. $\blacksquare$
