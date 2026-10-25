# Assignment 18

> **Existence and Uniqueness Theorem** (Initial Value Problem for Linear Systems)<br>The solution $y=y\left(x\right)$ of the linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ satisfying the initial condition $y\left(x_0\right)=y_0$ exists and is unique on the interval $\left(a,b\right)$, where $x_0\in\left(a,b\right)$ and $y_0\in\mathbb{R}^n$ are arbitrary.

> **Lemma 6.1** (Superposition Principle for Solutions of Homogeneous Linear Systems)<br>If $y=y_1\left(x\right)$ and $y=y_2\left(x\right)$ are solutions of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$, then their linear combination $y=C_1y_1\left(x\right)+C_2y_2\left(x\right)$ is also a solution, where $C_1$ and $C_2$ are arbitrary constants.

> **Lemma 6.2** (Dimension of the Solution Space of a Homogeneous Linear System)<br>The linear space $S$ consisting of all solutions of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ on the interval $\left(a,b\right)$ is $n$-dimensional, where $n$ is the order of the system.

> **Theorem 6.1** (Structure of the General Solution of a Homogeneous Linear System)<br>The homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ has $n$ linearly independent solutions $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$ on the interval $\left(a,b\right)$, and its general solution is $y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right)$, where $C_1,C_2,\cdots,C_n$ are arbitrary constants. The $n$ linearly independent solutions of a homogeneous linear system are usually called a fundamental system of solutions.

> **Lemma 6.3** (Liouville's Formula for the Wronskian Determinant)<br>Suppose $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ are $n$ solutions of a homogeneous linear system, and their Wronskian determinant is $W\left(x\right)$. Then $$W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^{x}\mathrm{tr}\left[A\left(s\right)\right]ds},$$ where $x_0\in\left(a,b\right)$, and $\mathrm{tr}\left[A\left(x\right)\right]$ denotes the trace of the matrix $A\left(x\right)$.

> **Theorem 6.2** (Wronskian Criterion)<br>The system of solutions $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ is linearly independent if and only if $W\left(x\right)\neq0\ \left(a< x< b\right)$.

> **Corollary 2** (Properties of a Fundamental Matrix)<br>(1) If $\Phi\left(x\right)$ is a fundamental matrix of a homogeneous linear system, then for any nonsingular $n$-th order constant matrix $C$, the matrix $\Phi\left(x\right)C$ is also a fundamental matrix of the system; (2) if both $\Phi\left(x\right)$ and $\Psi\left(x\right)$ are fundamental matrices of the system, then there exists a nonsingular $n$-th order constant matrix $C$ such that $\Psi\left(x\right)=\Phi\left(x\right)C$.

> **Lemma 6.4** (Structure of Solutions of a Nonhomogeneous Linear System)<br>If $\Phi\left(x\right)$ is a fundamental matrix of the homogeneous system corresponding to the nonhomogeneous linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$, and $y^*\left(x\right)$ is a particular solution of the nonhomogeneous system, then any solution $y=\varphi\left(x\right)$ of the nonhomogeneous system can be expressed as $\varphi\left(x\right)=\Phi\left(x\right)c+y^*\left(x\right)$, where $c$ is a constant column vector depending on $\varphi\left(x\right)$.

> **Theorem 6.3** (Structure of the General Solution of a Nonhomogeneous Linear System)<br>Suppose $\Phi\left(x\right)$ is a fundamental matrix of the corresponding homogeneous system. Then the general solution of the nonhomogeneous linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ on the interval $\left(a,b\right)$ can be expressed as $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^{x}\Phi^{-1}\left(s\right)f\left(s\right)ds$, where $c$ is an arbitrary $n$-dimensional constant column vector.

### Problem 1

(Problem 6-1, Problem 1(1)) Find the general solution of the homogeneous linear system $\frac{dy}{dt}=A\left(t\right)y$, where $A\left(t\right)=\begin{bmatrix}\frac{1}{t}&0\\0&\frac{1}{t}\end{bmatrix},\ t\neq0$.

### Solution to Problem 1

The component form of the system is

$$\frac{dy_1}{dt}=\frac{1}{t}y_1,\quad\frac{dy_2}{dt}=\frac{1}{t}y_2.$$

The two equations are independent and solved separately. For the first equation, separating variables and integrating gives $\ln\left|y_1\right|=\ln\left|t\right|+C_1$, i.e. $y_1=C_1t$. Similarly $y_2=C_2t$. Therefore the general solution is

$$y=C_1\begin{bmatrix}t\\0\end{bmatrix}+C_2\begin{bmatrix}0\\t\end{bmatrix},$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$

### Problem 2

(Problem 6-1, Problem 1(3)) Find the general solution of the homogeneous linear system $\frac{dy}{dt}=A\left(t\right)y$, where $A\left(t\right)=\begin{bmatrix}0&1\\-1&0\end{bmatrix}$.

### Solution to Problem 2

The component form of the system is

$$\frac{dy_1}{dt}=y_2,\quad\frac{dy_2}{dt}=-y_1.$$

From the first equation, $y_2=\frac{dy_1}{dt}$; substituting into the second gives the second-order equation

$$\frac{d^2y_1}{dt^2}+y_1=0.$$

Its characteristic equation is $r^2+1=0$, with roots $r=\pm i$, so $y_1=C_1\cos t+C_2\sin t$. Hence $y_2=\frac{dy_1}{dt}=-C_1\sin t+C_2\cos t$. Therefore the general solution is

$$y=C_1\begin{bmatrix}\cos t\\-\sin t\end{bmatrix}+C_2\begin{bmatrix}\sin t\\\cos t\end{bmatrix},$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$

### Problem 3

(Problem 6-1, Problem 2(2)) Solve the initial value problem for the nonhomogeneous linear system: $\frac{dx}{dt}=\frac{2t}{1+t^2}x,\ \frac{dy}{dt}=-\frac{1}{t}y+x+t\ \left(t> 0\right),\ x\left(1\right)=0,\ y\left(1\right)=\frac{4}{3}$.

### Solution to Problem 3

First solve the equation for $x$: $\frac{dx}{dt}=\frac{2t}{1+t^2}x$. Separating variables and integrating gives $\ln\left|x\right|=\ln\left(1+t^2\right)+C$, i.e. $x=C\left(1+t^2\right)$. Substituting the initial value $x\left(1\right)=0$ gives $C\left(1+1\right)=0$, so $C=0$, and hence $x\left(t\right)\equiv0$.

Substituting $x\equiv0$ into the equation for $y$ gives the first-order linear equation

$$\frac{dy}{dt}+\frac{1}{t}y=t.$$

The integrating factor is $\mu\left(t\right)=e^{\int\frac{1}{t}dt}=t$; multiplying both sides by it gives

$$\frac{d}{dt}\left(ty\right)=t^2.$$

Integrating gives $ty=\frac{t^3}{3}+C$, i.e. $y=\frac{t^2}{3}+\frac{C}{t}$. Substituting the initial value $y\left(1\right)=\frac{4}{3}$ gives $\frac{4}{3}=\frac{1}{3}+C$, so $C=1$. Therefore the desired solution is

$$x\left(t\right)\equiv0,\quad y\left(t\right)=\frac{t^2}{3}+\frac{1}{t}.$$

$\blacksquare$

### Problem 4

(Problem 6-1, Problem 3) Prove that the vector functions $\begin{bmatrix}1\\0\\0\end{bmatrix},\ \begin{bmatrix}x\\0\\0\end{bmatrix},\ \begin{bmatrix}x^2\\0\\0\end{bmatrix}$ are linearly independent on any interval $\left(a,b\right)$.

### Solution to Problem 4

Suppose there exist constants $C_1,C_2,C_3$ such that for all $x\in\left(a,b\right)$,

$$C_1\begin{bmatrix}1\\0\\0\end{bmatrix}+C_2\begin{bmatrix}x\\0\\0\end{bmatrix}+C_3\begin{bmatrix}x^2\\0\\0\end{bmatrix}=\begin{bmatrix}0\\0\\0\end{bmatrix}.$$

Comparing the first component gives the polynomial identity

$$C_1+C_2x+C_3x^2=0\quad\left(a< x< b\right).$$

Since a nonzero polynomial cannot vanish identically on any interval, we must have $C_1=C_2=C_3=0$. By the definition of linear independence of vector functions, this set of vector functions is linearly independent on any interval $\left(a,b\right)$. $\blacksquare$

### Problem 5

(Problem 6-1, Problem 4) Prove that a fundamental matrix completely determines the homogeneous linear system: that is, if the systems $\frac{dy}{dx}=A\left(x\right)y$ and $\frac{dy}{dx}=B\left(x\right)y$ have a common fundamental matrix, then $A\left(x\right)\equiv B\left(x\right)$.

### Solution to Problem 5

Suppose $\Phi\left(x\right)$ is the common fundamental matrix of the two systems. Since $\Phi\left(x\right)$ is a fundamental matrix of $\frac{dy}{dx}=A\left(x\right)y$, we have $\Phi'\left(x\right)=A\left(x\right)\Phi\left(x\right)$. Also, since $\Phi\left(x\right)$ is a fundamental matrix of $\frac{dy}{dx}=B\left(x\right)y$, we have $\Phi'\left(x\right)=B\left(x\right)\Phi\left(x\right)$. Therefore

$$A\left(x\right)\Phi\left(x\right)=B\left(x\right)\Phi\left(x\right),$$

i.e. $\left(A\left(x\right)-B\left(x\right)\right)\Phi\left(x\right)=0$. Since $\Phi\left(x\right)$ is a fundamental matrix, by **Theorem 6.2** (Wronskian Criterion), its Wronskian determinant $\det\left[\Phi\left(x\right)\right]\neq0$, so $\Phi\left(x\right)$ is invertible. Right-multiplying both sides by $\Phi^{-1}\left(x\right)$ gives

$$A\left(x\right)-B\left(x\right)=0,$$

i.e. $A\left(x\right)\equiv B\left(x\right)$. $\blacksquare$

### Problem 6

(Problem 6-1, Problem 6) Suppose that when $a< x< b$, the function $f\left(x\right)$ in the nonhomogeneous linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ is not identically zero. Prove: the system has at most $\left(n+1\right)$ linearly independent solutions.

### Solution to Problem 6

First prove that there are at most $n+1$ linearly independent solutions. Let $y^*\left(x\right)$ be a particular solution of the nonhomogeneous system, and let $y_1^*\left(x\right),y_2^*\left(x\right),\cdots,y_m^*\left(x\right)$ be any $m$ solutions of the system. By **Lemma 6.4** (Structure of Solutions of a Nonhomogeneous Linear System), the difference of two nonhomogeneous solutions is a solution of the corresponding homogeneous system, so $y_i^*\left(x\right)-y^*\left(x\right)\ \left(i=1,2,\cdots,m\right)$ are all solutions of the homogeneous system $\frac{dy}{dx}=A\left(x\right)y$. By **Lemma 6.2** (Dimension of the Solution Space of a Homogeneous Linear System), the homogeneous solution space is $n$-dimensional, so at most $n$ of these $m$ homogeneous solutions are linearly independent. Hence at most $n+1$ of $y_1^*,y_2^*,\cdots,y_m^*$ are linearly independent (including $y^*$ itself).

Next prove that there exist $n+1$ linearly independent solutions. By **Theorem 6.1** (Structure of the General Solution of a Homogeneous Linear System), take a fundamental system of solutions $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$ of the homogeneous system. Then by the **Existence and Uniqueness Theorem** (Initial Value Problem for Linear Systems), take a particular solution $y^*\left(x\right)$ of the nonhomogeneous system. Consider the $n+1$ solutions:

$$y^*\left(x\right),\quad y^*\left(x\right)+\varphi_1\left(x\right),\quad\cdots,\quad y^*\left(x\right)+\varphi_n\left(x\right).$$

Suppose there exist constants $C_0,C_1,\cdots,C_n$ such that

$$C_0y^*\left(x\right)+C_1\left(y^*\left(x\right)+\varphi_1\left(x\right)\right)+\cdots+C_n\left(y^*\left(x\right)+\varphi_n\left(x\right)\right)=0.$$

Rearranging gives

$$\left(C_0+C_1+\cdots+C_n\right)y^*\left(x\right)+C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)=0.$$

Let $k=C_0+C_1+\cdots+C_n$. If $k\neq0$, then $y^*\left(x\right)=-\frac{1}{k}\left(C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)\right)$, i.e. $y^*$ is a solution of the homogeneous system. But $y^*$ is a particular solution of the nonhomogeneous system and $f\left(x\right)\not\equiv0$; if $y^*$ satisfied the homogeneous equation, substituting into the nonhomogeneous equation would give $f\left(x\right)\equiv0$, a contradiction. Hence $k=0$, i.e. $C_0+C_1+\cdots+C_n=0$. Then the equation becomes

$$C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)=0.$$

Since $\varphi_1,\cdots,\varphi_n$ form a fundamental system (linearly independent), we get $C_1=\cdots=C_n=0$. Then from $C_0+C_1+\cdots+C_n=0$, we get $C_0=0$. Therefore these $n+1$ solutions are linearly independent.

In summary, the nonhomogeneous linear system has exactly $n+1$ linearly independent solutions. $\blacksquare$
