# Assignment 29

> **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation)<br>Consider the first-order quasilinear partial differential equation $X\left(x,y,z\right)\frac{\partial z}{\partial x}+Y\left(x,y,z\right)\frac{\partial z}{\partial y}=Z\left(x,y,z\right)$, where $X,Y,Z$ are continuously differentiable and $X,Y$ are not both zero. Its corresponding characteristic equation is $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$. Suppose $u\left(x,y,z\right)=C_1,\ v\left(x,y,z\right)=C_2$ are two independent first integrals of this characteristic equation. Then the implicit general solution of the original quasilinear partial differential equation is $\Phi\left[u\left(x,y,z\right),v\left(x,y,z\right)\right]=0$, where $\Phi$ is an arbitrary continuously differentiable function, and we require $\frac{\partial\Phi}{\partial z}\neq0$ so that $z=z\left(x,y\right)$ can be solved implicitly.

> **Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation)<br>The $n-1$ independent first integrals $\varphi_i=C_i$ of the characteristic equation $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$ give the general solution $u=\psi\left(\varphi_1,\cdots,\varphi_{n-1}\right)$ of the homogeneous linear equation $\sum_{i=1}^nA_i\frac{\partial u}{\partial x_i}=0$. The method for finding first integrals of the characteristic equation also applies to the case $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$ in Theorem 11.2.

### Problem 1

(Problem 11-2, Problem 1(2)) Find the general solution of the partial differential equation $\left(xy^3-2x^4\right)\frac{\partial z}{\partial x}+\left(2y^4-x^3y\right)\frac{\partial z}{\partial y}=9z\left(x^3-y^3\right)$.

### Solution to Problem 1

By **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation), first write the characteristic equation

$$
\frac{dx}{xy^3-2x^4}=\frac{dy}{2y^4-x^3y}=\frac{dz}{9z\left(x^3-y^3\right)}.
$$

Let $u=x^3,\ v=y^3$; then the denominators of the first two terms are $x\left(v-2u\right),\ y\left(2v-u\right)$. Eliminating $x,y$ from the first two equations gives

$$
\frac{du}{dv}=\frac{u\left(v-2u\right)}{v\left(2v-u\right)}.
$$

Let $w=\frac{u}{v}$, i.e. $u=wv$; then $w+v\frac{dw}{dv}=\frac{w\left(1-2w\right)}{2-w}$, which simplifies to

$$
v\frac{dw}{dv}=-\frac{w\left(1+w\right)}{2-w}.
$$

Separating variables and integrating $\frac{2-w}{w\left(1+w\right)}dw=-\frac{dv}{v}$, i.e. $\left(\frac{2}{w}-\frac{3}{1+w}\right)dw=-\frac{dv}{v}$, gives

$$
\frac{u^2v^2}{\left(u+v\right)^3}=C_1.
$$

Substituting back $u=x^3,\ v=y^3$ and taking the cube root gives the first first integral

$$
\varphi_1=\frac{x^2y^2}{x^3+y^3}=C_1.
$$

Next find the first integral involving $z$. Denote the common ratio as $\lambda$; then $du=3\lambda u\left(v-2u\right),\ dv=3\lambda v\left(2v-u\right),\ \frac{dz}{z}=9\lambda\left(u-v\right)$. Compute

$$
d\left(u+v\right)=3\lambda\left[u\left(v-2u\right)+v\left(2v-u\right)\right]=6\lambda\left(v^2-u^2\right)=-6\lambda\left(u-v\right)\left(u+v\right).
$$

Thus $\frac{d\left(u+v\right)}{u+v}=-6\lambda\left(u-v\right)$, while $\frac{dz}{z}=9\lambda\left(u-v\right)$; taking the ratio gives $\frac{d\ln\left(u+v\right)}{d\ln z}=-\frac{2}{3}$, i.e.

$$
\left(u+v\right)^3z^2=C_2.
$$

Substituting back $u+v=x^3+y^3$ gives the second first integral

$$
\varphi_2=\left(x^3+y^3\right)^3z^2=C_2.
$$

By **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation), the implicit general solution is

$$
\Phi\left(\frac{x^2y^2}{x^3+y^3},\ \left(x^3+y^3\right)^3z^2\right)=0,
$$

where $\Phi$ is an arbitrary continuously differentiable function. Solving for $z$, it can be written as

$$
z^2\left(x^3+y^3\right)^3=\psi\left(\frac{x^2y^2}{x^3+y^3}\right),
$$

where $\psi$ is an arbitrary continuously differentiable function. $\blacksquare$

### Problem 2

(Problem 11-2, Problem 2) Solve the initial value problem $\begin{cases}\sqrt{x}\frac{\partial f}{\partial x}+\sqrt{y}\frac{\partial f}{\partial y}+\sqrt{z}\frac{\partial f}{\partial z}=f,\\ \text{当 }y=1\text{ 时}, f\left(x,y,z\right)=xz.\end{cases}$

### Solution to Problem 2

By **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation), the characteristic equation is

$$
\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}=\frac{df}{f}.
$$

From $\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}$ we integrate to get $\sqrt{x}-\sqrt{y}=C_1$; from $\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}$ we get $\sqrt{y}-\sqrt{z}=C_2$; from $\frac{df}{f}=\frac{dy}{\sqrt{y}}$ we get $\ln f=2\sqrt{y}+C$, i.e. $fe^{-2\sqrt{y}}=C_3$. Hence the general solution is

$$
f=e^{2\sqrt{y}}\psi\left(\sqrt{x}-\sqrt{y},\ \sqrt{y}-\sqrt{z}\right),
$$

where $\psi$ is an arbitrary continuously differentiable function of two variables. Substituting the initial condition, when $y=1$, $f=xz$, gives

$$
e^{2}\psi\left(\sqrt{x}-1,\ 1-\sqrt{z}\right)=xz.
$$

Let $\xi=\sqrt{x}-1,\ \eta=1-\sqrt{z}$; then $x=\left(\xi+1\right)^2,\ z=\left(1-\eta\right)^2$, so $\psi\left(\xi,\eta\right)=e^{-2}\left(\xi+1\right)^2\left(1-\eta\right)^2$. Substituting back into the general solution, the desired solution is

$$
f\left(x,y,z\right)=e^{2\sqrt{y}-2}\left(\sqrt{x}-\sqrt{y}+1\right)^2\left(1-\sqrt{y}+\sqrt{z}\right)^2.
$$

Substituting $y=1$ to verify, we get $f=\left(\sqrt{x}\right)^2\left(\sqrt{z}\right)^2=xz$, which is consistent with the initial condition. $\blacksquare$
