# Assignment 28

> **Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation)<br>Consider the first-order homogeneous linear partial differential equation $\sum_{i=1}^nA_i\left(x_1,\cdots,x_n\right)\frac{\partial u}{\partial x_i}=0$, where the coefficients $A_1,\cdots,A_n$ are continuously differentiable and not all zero. Its characteristic equation is the system of ordinary differential equations in symmetric form $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$, which is an $n-1$-th order system with $n-1$ independent first integrals $\varphi_i\left(x_1,\cdots,x_n\right)=C_i$ ($i=1,\cdots,n-1$). Then the general solution of the original partial differential equation is $u=\psi\left[\varphi_1,\cdots,\varphi_{n-1}\right]$, where $\psi$ is an arbitrary continuously differentiable function of $n-1$ variables. In other words, a function $\varphi$ is a first integral of the characteristic equation if and only if the identity $\sum_{i=1}^nA_i\frac{\partial\varphi}{\partial x_i}\equiv0$ holds.

### Problem 1

(Problem 11-1, Problem 1(1)) Solve the partial differential equation $x_1\frac{\partial y}{\partial x_1}+x_2\frac{\partial y}{\partial x_2}+\cdots+x_n\frac{\partial y}{\partial x_n}=0$ ($n\ge2$).

### Solution to Problem 1

By **Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation), first write the characteristic equation

$$
\frac{dx_1}{x_1}=\frac{dx_2}{x_2}=\cdots=\frac{dx_n}{x_n}.
$$

From $\frac{dx_1}{x_1}=\frac{dx_n}{x_n}$ we get $\ln\left|x_1\right|-\ln\left|x_n\right|=C$, i.e. $\frac{x_1}{x_n}=C_1$; similarly $\frac{x_2}{x_n}=C_2,\ \cdots,\ \frac{x_{n-1}}{x_n}=C_{n-1}$. These are $n-1$ independent first integrals. Hence the general solution is

$$
y=\psi\left(\frac{x_1}{x_n},\frac{x_2}{x_n},\cdots,\frac{x_{n-1}}{x_n}\right),
$$

where $\psi$ is an arbitrary continuously differentiable function of $n-1$ variables. $\blacksquare$

### Problem 2

(Problem 11-1, Problem 1(3)) Solve the partial differential equation $a\left(b^2+c^2\right)\frac{\partial h}{\partial a}+b\left(c^2+a^2\right)\frac{\partial h}{\partial b}+c\left(b^2-a^2\right)\frac{\partial h}{\partial c}=0$.

### Solution to Problem 2

By **Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation), the characteristic equation is

$$
\frac{da}{a\left(b^2+c^2\right)}=\frac{db}{b\left(c^2+a^2\right)}=\frac{dc}{c\left(b^2-a^2\right)}.
$$

Let the common ratio be $\lambda$; then $da=\lambda a\left(b^2+c^2\right),\ db=\lambda b\left(c^2+a^2\right),\ dc=\lambda c\left(b^2-a^2\right)$. Compute the differential

$$
d\left(a^2-b^2+c^2\right)=2a\,da-2b\,db+2c\,dc
=2\lambda\left[a^2\left(b^2+c^2\right)-b^2\left(c^2+a^2\right)+c^2\left(b^2-a^2\right)\right].
$$

Simplifying inside the brackets gives $a^2b^2+a^2c^2-b^2c^2-a^2b^2+b^2c^2-a^2c^2=0$, so

$$
d\left(a^2-b^2+c^2\right)=0,
$$

i.e. $\varphi_1=a^2-b^2+c^2=C_1$ is a first integral.

Next, from $d\left(a^2\right)=2\lambda a^2\left(b^2+c^2\right)$ we get $\frac{d\left(a^2\right)}{a^2}=2\lambda\left(b^2+c^2\right)$; similarly $\frac{d\left(b^2\right)}{b^2}=2\lambda\left(c^2+a^2\right),\ \frac{d\left(c^2\right)}{c^2}=2\lambda\left(b^2-a^2\right)$. Thus

$$
\frac{d\left(a^2\right)}{a^2}-\frac{d\left(b^2\right)}{b^2}=2\lambda\left(b^2-a^2\right)=\frac{d\left(c^2\right)}{c^2},
$$

i.e. $d\ln\frac{a^2}{b^2}=d\ln c^2$, so $\frac{a^2}{b^2c^2}=C_2$ is another independent first integral. Therefore the general solution of the original partial differential equation is

$$
h=\psi\left(a^2-b^2+c^2,\frac{a^2}{b^2c^2}\right),
$$

where $\psi$ is an arbitrary continuously differentiable function of two variables. $\blacksquare$

### Problem 3

(Problem 11-1, Problem 2(2)) Solve the initial value problem $\begin{cases}\left(x-y^2\right)\frac{\partial z}{\partial x}+y\frac{\partial z}{\partial y}=0,\\ \text{当 }x=1\text{ 时}, z=f_0\left(y\right).\end{cases}$

### Solution to Problem 3

By **Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation), the characteristic equation is

$$
\frac{dx}{x-y^2}=\frac{dy}{y}.
$$

From $y\,dx=\left(x-y^2\right)dy$ we get $y\,dx-x\,dy=-y^2\,dy$. Dividing both sides by $y^2$ and noting that $\frac{y\,dx-x\,dy}{y^2}=d\left(\frac{x}{y}\right)$, we have

$$
d\left(\frac{x}{y}\right)=-dy,
$$

so $\frac{x}{y}+y=C$ is a first integral. The general solution is $z=\psi\left(\frac{x}{y}+y\right)$, where $\psi$ is an arbitrary continuously differentiable function. Substituting the initial condition, when $x=1$, $z=f_0\left(y\right)$, gives

$$
\psi\left(\frac{1}{y}+y\right)=f_0\left(y\right).
$$

This determines the function $\psi$: for any argument $s$, take $y$ satisfying $y+\frac{1}{y}=s$, then $\psi\left(s\right)=f_0\left(y\right)$. Hence the desired solution is

$$
z=\psi\left(\frac{x}{y}+y\right),
$$

where the function $\psi$ is determined by $\psi\left(y+\frac{1}{y}\right)=f_0\left(y\right)$. $\blacksquare$
