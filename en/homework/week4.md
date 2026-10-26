# Assignment 4

> **First-Order Linear Equation**<br>An equation of the form $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$$ is called a first-order linear equation, where $p\left(x\right),q\left(x\right)$ are continuous on an interval $I$. When $q\left(x\right)\equiv0$ it is called the corresponding homogeneous linear equation; otherwise it is called a nonhomogeneous linear equation.

> **General Solution of the Homogeneous Linear Equation**<br>For the homogeneous linear equation $$\frac{dy}{dx}+p\left(x\right)y=0,$$ separating variables and integrating gives the general solution $$y=Ce^{-\int p\left(x\right)dx},$$ where the arbitrary constant $C$ may be zero; $C=0$ corresponds to the particular solution $y\equiv0$.

> **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**<br>Multiplying the nonhomogeneous linear equation on both sides by the integrating factor $$\mu\left(x\right)=e^{\int p\left(x\right)dx}$$ transforms the left-hand side into a total differential $$\frac{d}{dx}\left(e^{\int p\left(x\right)dx}y\right)=q\left(x\right)e^{\int p\left(x\right)dx}.$$ Integrating gives the general solution $$y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C\right].$$

### Problem 1

(Problem 2-3, Problem 1(2)) Solve the differential equation $\frac{dy}{dx}+y\tan x=\sin 2x$.

### Solution to Problem 1

This is a first-order linear equation with $p\left(x\right)=\tan x,\ q\left(x\right)=\sin 2x$. By the **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**, the integrating factor is
$$
\mu\left(x\right)=e^{\int\tan x\,dx}=e^{-\ln\left|\cos x\right|}=\sec x.
$$

Multiplying both sides by $\sec x$ gives
$$
\frac{d}{dx}\left(y\sec x\right)=\sin 2x\sec x=2\sin x\cos x\cdot\frac{1}{\cos x}=2\sin x.
$$

Integrating both sides gives $y\sec x=-2\cos x+C$, so the general solution is
$$
y=C\cos x-2\cos^2x.
$$

$\blacksquare$

### Problem 2

(Problem 2-3, Problem 1(4)) Solve the initial value problem $\frac{dy}{dx}-\frac{1}{1-x^2}y=1+x,\ y\left(0\right)=1$.

### Solution to Problem 2

This is a first-order linear equation with $p\left(x\right)=-\frac{1}{1-x^2},\ q\left(x\right)=1+x$. By the **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**, noting that the solution is considered near $x=0$, i.e. on $\left|x\right|< 1$, the integrating factor is
$$
\mu\left(x\right)=e^{\int-\frac{1}{1-x^2}dx}=e^{-\frac{1}{2}\ln\frac{1+x}{1-x}}=\sqrt{\frac{1-x}{1+x}}.
$$

Multiplying both sides by $\mu\left(x\right)$, the left-hand side becomes a total differential, and the right-hand side is
$$
\mu\left(x\right)q\left(x\right)=\sqrt{\frac{1-x}{1+x}}\left(1+x\right)=\sqrt{1-x^2}.
$$

Thus $\frac{d}{dx}\left(\mu y\right)=\sqrt{1-x^2}$, and integrate from $0$ to $x$. By the initial condition $\mu\left(0\right)y\left(0\right)=1$, we get
$$
\mu\left(x\right)y=1+\int_0^x\sqrt{1-t^2}\,dt=1+\frac{1}{2}\left(x\sqrt{1-x^2}+\arcsin x\right).
$$

Hence the desired solution is
$$
y=\sqrt{\frac{1+x}{1-x}}\left[1+\frac{1}{2}\left(x\sqrt{1-x^2}+\arcsin x\right)\right].
$$

$\blacksquare$

### Problem 3

(Problem 2-3, Problem 3) Let $y=\varphi\left(x\right)$ satisfy the differential inequality $y'+a\left(x\right)y\le0$ ($x\ge0$). Prove: $\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^x a\left(s\right)ds}$ ($x\ge0$).

### Solution to Problem 3

Following the idea of the **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**, take the integrating factor $A\left(x\right)=e^{\int_0^x a\left(s\right)ds}> 0$. Multiplying both sides of the inequality $y'+a\left(x\right)y\le0$ by $A\left(x\right)$ gives
$$
A\left(x\right)\left[y'+a\left(x\right)y\right]=\frac{d}{dx}\left(A\left(x\right)y\right)\le0.
$$

Thus $A\left(x\right)y\left(x\right)$ is nonincreasing on $x\ge0$, and therefore
$$
A\left(x\right)y\left(x\right)\le A\left(0\right)y\left(0\right)=y\left(0\right).
$$

Substituting $A\left(x\right)=e^{\int_0^x a\left(s\right)ds}$ and rearranging gives
$$
\varphi\left(x\right)\le\varphi\left(0\right)e^{-\int_0^x a\left(s\right)ds}\quad\left(x\ge0\right).
$$

$\blacksquare$

### Problem 4

(Problem 2-3, Problem 4) Use the method of variation of constants to solve the nonhomogeneous linear equation $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$: assume it has the form of the homogeneous general solution, but vary the arbitrary constant $C$ into an undetermined function $C\left(x\right)$ of $x$, then substitute into the equation to determine $C\left(x\right)$.

### Solution to Problem 4

By the **General Solution of the Homogeneous Linear Equation**, the general solution of the corresponding homogeneous equation is $y=Ce^{-\int p\left(x\right)dx}$. Regarding $C$ as a function of $x$, suppose the nonhomogeneous equation has a solution of the form
$$
y=C\left(x\right)e^{-\int p\left(x\right)dx}
$$

Differentiating with respect to $x$ gives
$$
y'=C'\left(x\right)e^{-\int p\left(x\right)dx}-C\left(x\right)p\left(x\right)e^{-\int p\left(x\right)dx}.
$$

Substituting into $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$, the two terms containing $C\left(x\right)$ cancel, giving
$$
C'\left(x\right)e^{-\int p\left(x\right)dx}=q\left(x\right),
$$

i.e. $C'\left(x\right)=q\left(x\right)e^{\int p\left(x\right)dx}$. Integrating gives
$$
C\left(x\right)=\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C_1.
$$

Substituting back gives the general solution, consistent with the **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**:
$$
y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C_1\right].
$$

$\blacksquare$

### Problem 5

(Problem 2-3, Problem 5) Consider the equation $\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)$, where $p\left(x\right),q\left(x\right)$ are both continuous functions with period $\omega> 0$. Prove: (1) if $q\left(x\right)\equiv0$, then any nonzero solution of the equation has period $\omega$ if and only if the mean value of the function $p\left(x\right)$ $\overline p\equiv\frac{1}{\omega}\int_0^\omega p\left(x\right)dx=0$; (2) if $q\left(x\right)$ is not identically zero, then the equation has a unique $\omega$-periodic solution if and only if $\overline p\neq0$, and find this solution.

### Solution to Problem 5

By the **General Solution of the Homogeneous Linear Equation**, when $q\left(x\right)\equiv0$, any solution is $y\left(x\right)=Ce^{-\int_0^x p\left(t\right)dt}$. Since $p\left(x\right)$ has period $\omega$, $\int_x^{x+\omega}p\left(t\right)dt=\int_0^\omega p\left(t\right)dt$. Hence
$$
y\left(x+\omega\right)=Ce^{-\int_0^{x+\omega}p}=Ce^{-\int_0^x p}\cdot e^{-\int_0^\omega p}=y\left(x\right)e^{-\int_0^\omega p}.
$$

A nonzero solution has period $\omega$ means $y\left(x+\omega\right)=y\left(x\right)$, which holds if and only if $e^{-\int_0^\omega p}=1$, i.e. $\int_0^\omega p\left(t\right)dt=0$, equivalent to $\overline p=0$. This proves (1).

By the **General Solution of the Nonhomogeneous Linear Equation (Integrating Factor Method)**, when $q\left(x\right)$ is not identically zero, the general solution is
$$
y\left(x\right)=e^{-\int_0^x p}\left[C+\int_0^x q\left(s\right)e^{\int_0^s p}ds\right].
$$

Let $P_\omega=\int_0^\omega p\left(t\right)dt,\ I=\int_0^\omega q\left(s\right)e^{\int_0^s p}ds$. A solution has period $\omega$ is equivalent to $y\left(\omega\right)=y\left(0\right)=C$. Substituting into the general solution gives
$$
e^{-P_\omega}\left(C+I\right)=C.
$$

When $P_\omega\neq0$, i.e. $\overline p\neq0$, $e^{-P_\omega}\neq1$, and one can uniquely solve
$$
C=\frac{e^{-P_\omega}I}{1-e^{-P_\omega}}=\frac{I}{e^{P_\omega}-1},
$$

so there exists a unique $\omega$-periodic solution. When $P_\omega=0$, i.e. $\overline p=0$, the equation becomes $C+I=C$, i.e. $I=0$; but when $q\left(x\right)$ is not identically zero, generally $I\neq0$, in which case there is no solution; even if $I=0$, there are infinitely many $C$ giving periodic solutions, and uniqueness fails. Hence there is a unique periodic solution if and only if $\overline p\neq0$, and this unique periodic solution is
$$
y\left(x\right)=e^{-\int_0^x p\left(t\right)dt}\left[\frac{\int_0^\omega q\left(s\right)e^{\int_0^s p\left(t\right)dt}ds}{e^{\int_0^\omega p\left(t\right)dt}-1}+\int_0^x q\left(s\right)e^{\int_0^s p\left(t\right)dt}ds\right].
$$

$\blacksquare$
