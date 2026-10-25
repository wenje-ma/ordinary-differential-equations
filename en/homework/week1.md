# Assignment 1

> **Definition 1.1** (Ordinary Differential Equation)<br>Any equation involving the independent variable $x$, the unknown function $y=y\left(x\right)$ of this independent variable, and its derivatives $y'=y'\left(x\right)$ up to the $n$-th derivative $y^{\left(n\right)}=y^{\left(n\right)}\left(x\right)$, i.e. $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$, is called an ordinary differential equation, where the highest order $n$ at which a derivative actually appears is called the order of the ordinary differential equation. If the left-hand function $F$ is linear in the unknown function $y$ and all its derivatives $y',y'',\cdots,y^{\left(n\right)}$ taken together, then it is called a linear ordinary differential equation; otherwise it is called a nonlinear ordinary differential equation.

> **Definition 1.2** (Solution)<br>Let the function $y=\varphi\left(x\right)$ be continuous on the interval $J$ and possess derivatives up to order $n$. If substituting $y=\varphi\left(x\right)$ and the corresponding derivatives into the equation $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$ yields an identity $F\left(x,\varphi\left(x\right),\varphi'\left(x\right),\cdots,\varphi^{\left(n\right)}\left(x\right)\right)=0$ in $x$ holding for all $x\in J$, then $y=\varphi\left(x\right)$ is called a solution of the differential equation on the interval $J$.

> **Definition 1.3** (General Solution and Particular Solution)<br>Let a solution $y=\varphi\left(x,C_1,C_2,\cdots,C_n\right)$ of an $n$-th order differential equation contain $n$ independent arbitrary constants $C_1,C_2,\cdots,C_n$; then it is called a general solution. Here the $n$ arbitrary constants $C_1,C_2,\cdots,C_n$ are independent, meaning that the Jacobian determinant $\frac{D\left(\varphi,\varphi',\cdots,\varphi^{\left(n-1\right)}\right)}{D\left(C_1,C_2,\cdots,C_n\right)}\neq0$, where $\varphi^{\left(k\right)}=\varphi^{\left(k\right)}\left(x,C_1,C_2,\cdots,C_n\right)\ \left(k=0,1,\cdots,n-1\right)$. If a solution $y=\varphi\left(x\right)$ of the differential equation contains no arbitrary constants, then it is called a particular solution.

> **Initial Value Problem** (Cauchy Problem)<br>For an $n$-th order differential equation, the general formulation of the initial conditions is $y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$, where $x_0$ is some prescribed initial value of the independent variable, and $y_0,\ y_0',\ \cdots,\ y_0^{\left(n-1\right)}$ are the prescribed initial values of the unknown function and its corresponding derivatives. Thus the initial value problem for an $n$-th order differential equation can be formulated as: $$\begin{cases}y^{\left(n\right)}=F\left(x,y,y',\cdots,y^{\left(n-1\right)}\right),\\y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}.\end{cases}$$ The initial value problem is also called the Cauchy problem.

> **Solving Differential Equations and Integration Operations**<br>Solving a differential equation is associated with a certain integration operation. Hence the process of solving a differential equation is often called integrating a differential equation, and a solution of a differential equation is called an integral. Since each indefinite integration introduces an arbitrary constant, the general solution of an $n$-th order differential equation should contain $n$ arbitrary constants.

### Problem 1

(Problem 1-1, Problem 1(4)) Verify that the function $y=\begin{cases}-\frac{1}{4}\left(x-C_1\right)^2,&-\infty< x< C_1,\\0,&C_1\le x\le C_2,\\\frac{1}{4}\left(x-C_2\right)^2,&C_2< x< +\infty\end{cases}$ is a solution of the corresponding differential equation $y'=\sqrt{\left|y\right|}$.

### Solution to Problem 1

By **Definition 1.2** (Solution), it suffices to verify that $y=y\left(x\right)$ satisfies $y'=\sqrt{\left|y\right|}$. We verify $y=y\left(x\right)$ in three segments.

(1) When $-\infty< x< C_1$, $y=-\frac{1}{4}\left(x-C_1\right)^2< 0$, so $y'=-\frac{1}{2}\left(x-C_1\right)$, and $\left|y\right|=\frac{1}{4}\left(x-C_1\right)^2$. Since $x< C_1$, $\left|x-C_1\right|=C_1-x$, hence
$$
\sqrt{\left|y\right|}=\frac{1}{2}\left|x-C_1\right|=\frac{1}{2}\left(C_1-x\right)=-\frac{1}{2}\left(x-C_1\right)=y'.
$$

(2) When $C_1\le x\le C_2$, $y=0$, so $y'=0$, and $\sqrt{\left|y\right|}=0$, hence $y'=\sqrt{\left|y\right|}$.

(3) When $C_2< x< +\infty$, $y=\frac{1}{4}\left(x-C_2\right)^2> 0$, so $y'=\frac{1}{2}\left(x-C_2\right)$, and $\left|y\right|=\frac{1}{4}\left(x-C_2\right)^2$. Since $x> C_2$, $\left|x-C_2\right|=x-C_2$, hence
$$
\sqrt{\left|y\right|}=\frac{1}{2}\left|x-C_2\right|=\frac{1}{2}\left(x-C_2\right)=y'.
$$

In summary, on all three intervals $y'=\sqrt{\left|y\right|}$, so $y$ is a solution of the differential equation $y'=\sqrt{\left|y\right|}$. $\blacksquare$

### Problem 2

(Problem 1-2, Problem 2(3)) Find the solution of the initial value problem $\frac{dR}{dt}=-aR,\ R\left(0\right)=1$ (where $a> 0$ is a constant).

### Solution to Problem 2

By the **Initial Value Problem** (Cauchy Problem), its solution must satisfy the initial condition $R\left(0\right)=1$. Since solving a differential equation is associated with integration, we separate variables and integrate both sides. When $R\neq0$, separating variables gives
$$
\frac{dR}{R}=-a\,dt.
$$

Integrating both sides gives $\ln\left|R\right|=-at+C$, i.e. $R=Ce^{-at}$ ($C\neq0$ is an arbitrary constant; $C=0$ corresponds to the zero solution $R\equiv0$, which also satisfies the equation). Substituting the initial condition $R\left(0\right)=1$ gives $C=1$, so the desired solution is
$$
R\left(t\right)=e^{-at}.
$$

$\blacksquare$

### Problem 3

(Problem 1-2, Problem 2(4)) Find the solution of the initial value problem $\frac{dy}{dx}=1+y^2,\ y\left(x_0\right)=y_0$.

### Solution to Problem 3

Since solving a differential equation is associated with integration, we separate variables and integrate both sides. Since $1+y^2\neq0$ always holds, separating variables gives
$$
\frac{dy}{1+y^2}=dx.
$$

Integrating both sides gives $\arctan y=x+C$, i.e. $y=\tan\left(x+C\right)$. Substituting the initial condition $y\left(x_0\right)=y_0$ gives $\arctan y_0=x_0+C$, i.e. $C=\arctan y_0-x_0$, so the desired solution is
$$
y=\tan\left(x+\arctan y_0-x_0\right).
$$

$\blacksquare$
