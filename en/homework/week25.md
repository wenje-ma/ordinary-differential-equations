# Assignment 25

> **Elementary Singular Points** (and Higher-Order Singular Points)<br>Consider a linear system $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$ with singular point at $\left(0,0\right)$. When the matrix $A$ is nondegenerate (i.e. $A$ does not have zero as an eigenvalue), the point $\left(0,0\right)$ is called an elementary singular point of the system; otherwise it is called a higher-order singular point. Elementary singular points are always isolated, while linear higher-order singular points are always non-isolated.

> **Characteristic Directions**<br>When $t \to +\infty$ (or $-\infty$), some trajectories may approach the singular point $\left(0,0\right)$ along a fixed line $y = kx$ (or $x = ky$); the direction of this line is called a characteristic direction. A star node has infinitely many characteristic directions, a two-way node and a saddle point have two, a one-way node has one, and a focus and a center have none; moreover, when the line $y = kx$ gives a characteristic direction of the linear system, both rays of this line divided by the singular point are trajectories of the system.

> **Theorem 8.5** (Classification of Elementary Singular Points)<br>For the linear system $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$, denote $p = -\text{tr}\left[A\right]$ (the negative of the trace of $A$) and $q = \det\left[A\right]$. Then: (1) when $q < 0$, $\left(0,0\right)$ is a saddle point; (2) when $q > 0$ and $p^2 > 4q$, $\left(0,0\right)$ is a two-way node; (3) when $q > 0$ and $p^2 = 4q$, $\left(0,0\right)$ is a one-way node or a star node; (4) when $q > 0$ and $0 < p^2 < 4q$, $\left(0,0\right)$ is a focus; (5) when $q > 0$ and $p = 0$, $\left(0,0\right)$ is a center. Furthermore, in cases (2) through (4), when $p > 0$ the singular point $\left(0,0\right)$ is stable, and when $p < 0$ it is unstable.

> **Theorem 8.6** (Nonlinear Systems Have the Same Qualitative Structure Near Elementary Singular Points as Their Linearized Systems)<br>Suppose the nonlinear system $\frac{dx}{dt} = ax + by + \varphi\left(x,y\right),\ \frac{dy}{dt} = cx + dy + \psi\left(x,y\right)$ has an isolated singular point at $\left(0,0\right)$, and its linearized system $\frac{dx}{dt} = ax + by,\ \frac{dy}{dt} = cx + dy$ has an elementary singular point at $\left(0,0\right)$, where $r = \sqrt{x^2 + y^2}$. Then: (1) if the linearized system has a focus at $\left(0,0\right)$ and condition $A$ ($\varphi\left(x,y\right) = o\left(r\right),\ \psi\left(x,y\right) = o\left(r\right),\ r \to 0$) holds, then $\left(0,0\right)$ is also a focus of the original system with the same stability; (2) if the linearized system has a saddle point or two-way node at $\left(0,0\right)$ and conditions $A$ and $B$ ($\varphi, \psi$ are continuously differentiable in $x, y$ in a small neighborhood of the origin) hold, then $\left(0,0\right)$ is respectively a saddle point or two-way node of the original system with the same stability; (3) if the linearized system has a one-way node at $\left(0,0\right)$ and condition $A^*$ ($\left|\varphi\right|/r$ and $\left|\psi\right|/r$ tend uniformly to zero as $r \to 0$) holds, then $\left(0,0\right)$ is also a one-way node of the original system with the same stability; (4) if the linearized system has a star node at $\left(0,0\right)$ and conditions $A^*$ and $B$ hold, then $\left(0,0\right)$ is also a star node of the original system with the same stability.

### Problem 1

(Problem 8-3, Problem 1) Suppose the linear system $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$ has a higher-order singular point at $\left(0,0\right)$. Sketch its phase portrait.

### Solution to Problem 1

By **Elementary Singular Points** (and Higher-Order Singular Points), $\left(0,0\right)$ being a higher-order singular point means that the matrix $A$ has zero as an eigenvalue, i.e. $\det\left[A\right] = 0$. We discuss three cases.

(1) The rank of $A$ is $1$, i.e. $A$ has one nonzero real eigenvalue $\lambda \ne 0$ and one zero eigenvalue. Then $A$ is similar to the diagonal form $\begin{bmatrix}\lambda & 0 \\ 0 & 0\end{bmatrix}$, and the system is

$$
\frac{dx}{dt} = \lambda x,\quad\frac{dy}{dt} = 0.
$$

Phase portrait: each horizontal line $y = c$ is a line containing trajectories; points on it move along the $x$-axis toward the $y$-axis ($\lambda < 0$) or away from the $y$-axis ($\lambda > 0$); the entire $y$-axis consists of infinitely many equilibrium points (the singular point is non-isolated).

(2) $A$ is a nonzero nilpotent matrix, i.e. $A$ is similar to $\begin{bmatrix}0 & 1 \\ 0 & 0\end{bmatrix}$, and the system is

$$
\frac{dx}{dt} = y,\quad\frac{dy}{dt} = 0.
$$

Phase portrait: each horizontal line $y = c \ne 0$ is a trajectory, moving in the direction of increasing $x$ when $c > 0$ and in the direction of decreasing $x$ when $c < 0$; the entire $x$-axis consists of infinitely many equilibrium points.

(3) $A = 0$, then every point in the plane is an equilibrium point, and all points remain stationary.

In summary, the higher-order singular point of a linear system is non-isolated; its set of equilibrium points is either a line (the entire line consists of equilibrium points) or the entire plane, and there are no isolated equilibrium points. $\blacksquare$

### Problem 2

(Problem 8-3, Problem 2(2)) Determine the type of the singular point $\left(0,0\right)$ of the system $\begin{cases}\frac{dx}{dt} = 2x + y + xy^2, \\ \frac{dy}{dt} = x + 2y + x^2 + y^2\end{cases}$, and sketch the phase portrait near this singular point.

### Solution to Problem 2

The linear part matrix is $A = \begin{bmatrix}2 & 1 \\ 1 & 2\end{bmatrix}$. Computing:

$$
p = -\text{tr}\left[A\right] = -4,\quad q = \det\left[A\right] = 3,\quad p^2 - 4q = 16 - 12 = 4 > 0.
$$

By **Theorem 8.5** (Classification of Elementary Singular Points), $q > 0$ and $p^2 > 4q$, so the linearized system has a two-way node at $\left(0,0\right)$; also $p = -4 < 0$, so this node is unstable.

The nonlinear terms $xy^2,\ x^2 + y^2$ are all $o\left(r\right)$ ($r \to 0$) and are continuously differentiable near the origin, so conditions $A$ and $B$ hold. By conclusion (2) of **Theorem 8.6** (Nonlinear Systems Have the Same Qualitative Structure Near Elementary Singular Points as Their Linearized Systems), $\left(0,0\right)$ of the original system is also an unstable two-way node.

Next find the characteristic directions. The characteristic equation is $\lambda^2 - 4\lambda + 3 = 0$, with eigenvalues $\lambda = 1,\ 3$. The eigenvector for $\lambda = 1$ satisfies $\left(A - I\right)\boldsymbol{v} = 0$, i.e. $\boldsymbol{v}$ lies along the line $y = -x$; the eigenvector for $\lambda = 3$ lies along the line $y = x$. By **Characteristic Directions**, a two-way node has two characteristic directions, namely the lines $y = x$ and $y = -x$.

Phase portrait description: near the singular point, except for trajectories lying on the line $y = x$, all other trajectories are tangent to the slower characteristic direction $y = -x$ as they approach (or leave) the singular point; all trajectories move away from the singular point as $t \to +\infty$. $\blacksquare$

### Problem 3

(Problem 8-3, Problem 2(4)) Determine the type of the singular point $\left(0,0\right)$ of the system $\begin{cases}\frac{dx}{dt} = x + 2y, \\ \frac{dy}{dt} = 5y - 2x + x^3\end{cases}$, and sketch the phase portrait near this singular point.

### Solution to Problem 3

The linear part matrix is $A = \begin{bmatrix}1 & 2 \\ -2 & 5\end{bmatrix}$. Computing:

$$
p = -\text{tr}\left[A\right] = -6,\quad q = \det\left[A\right] = 9,\quad p^2 - 4q = 36 - 36 = 0.
$$

By **Theorem 8.5** (Classification of Elementary Singular Points), $q > 0$ and $p^2 = 4q$, so the linearized system has a one-way node or star node at $\left(0,0\right)$. The characteristic equation is $\left(\lambda - 3\right)^2 = 0$, with double eigenvalue $\lambda = 3$. Solving $\left(A - 3I\right)\boldsymbol{v} = \begin{bmatrix}-2 & 2 \\ -2 & 2\end{bmatrix}\boldsymbol{v} = 0$, we get a unique characteristic direction $y = x$, i.e. only one linearly independent eigenvector, so the singular point is a one-way node. Also $p = -6 < 0$, so this one-way node is unstable.

The nonlinear term $x^3 = o\left(r\right)$ ($r \to 0$) and is continuously differentiable near the origin, so condition $A^*$ holds. By conclusion (3) of **Theorem 8.6** (Nonlinear Systems Have the Same Qualitative Structure Near Elementary Singular Points as Their Linearized Systems), $\left(0,0\right)$ of the original system is also an unstable one-way node.

Phase portrait description: by **Characteristic Directions**, a one-way node has only one characteristic direction, namely the line $y = x$; near the singular point, all trajectories are tangent to this line and move away from the singular point as $t \to +\infty$. $\blacksquare$

### Problem 4

(Problem 8-3, Problem 2(5)) Determine the type of the singular point $\left(0,0\right)$ of the system $\begin{cases}\frac{dx}{dt} = x\left(1 - y\right), \\ \frac{dy}{dt} = y\left(1 - x\right)\end{cases}$, and sketch the phase portrait near this singular point.

### Solution to Problem 4

Near $\left(0,0\right)$, the right-hand side functions expand to $\frac{dx}{dt} = x - xy,\ \frac{dy}{dt} = y - xy$, and the linear part matrix is $A = \begin{bmatrix}1 & 0 \\ 0 & 1\end{bmatrix}$. Computing:

$$
p = -\text{tr}\left[A\right] = -2,\quad q = \det\left[A\right] = 1,\quad p^2 - 4q = 4 - 4 = 0.
$$

By **Theorem 8.5** (Classification of Elementary Singular Points), $q > 0$ and $p^2 = 4q$, so the linearized system has a one-way node or star node at $\left(0,0\right)$. The characteristic equation is $\left(\lambda - 1\right)^2 = 0$, with double eigenvalue $\lambda = 1$; but $A = I$, so every nonzero vector is an eigenvector, i.e. both Jordan blocks are of order one, so the singular point is a star node. Also $p = -2 < 0$, so this star node is unstable.

The nonlinear term $-xy$ is $o\left(r\right)$ ($r \to 0$) and is continuously differentiable near the origin, so conditions $A^*$ and $B$ hold. By conclusion (4) of **Theorem 8.6** (Nonlinear Systems Have the Same Qualitative Structure Near Elementary Singular Points as Their Linearized Systems), $\left(0,0\right)$ of the original system is also an unstable star node.

Phase portrait description: by **Characteristic Directions**, a star node has infinitely many characteristic directions; near the singular point, trajectories approximately move outward along every ray emanating from the origin. $\blacksquare$
