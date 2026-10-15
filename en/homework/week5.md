# Assignment 5

> **Homogeneous Equation**<br>If in the first-order differential equation $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0$$ the functions $P\left(x,y\right)$ and $Q\left(x,y\right)$ are homogeneous of the same degree, i.e. $P\left(tx,ty\right)=t^mP\left(x,y\right),\ Q\left(tx,ty\right)=t^mQ\left(x,y\right)$, then it is called a homogeneous equation. Making the substitution $y=ux$ (where $u$ is the new unknown function), the equation is transformed into a separable equation in $u$ and $x$.

> **Equation Reducible to Homogeneous Form**<br>For the equation $$\frac{dy}{dx}=\frac{ax+by+c}{mx+ny+l},$$ when $c,l$ are not both zero and $\Delta=an-bm\neq0$, one can determine $\alpha,\beta$ from the linear system $a\alpha+b\beta+c=0,\ m\alpha+n\beta+l=0$, and make the translation $x=\xi+\alpha,\ y=\eta+\beta$; the equation becomes the homogeneous equation $\frac{d\eta}{d\xi}=\frac{a\xi+b\eta}{m\xi+n\eta}$; then setting $\eta=u\xi$ reduces it to a separable equation.

> **Bernoulli Equation**<br>An equation of the form $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)y^n$$ is called a Bernoulli equation, where the constant $n\neq0,1$. Multiplying both sides by $\left(1-n\right)y^{-n}$ and then setting $z=y^{1-n}$ reduces the equation to a first-order linear equation in $z$: $$\frac{dz}{dx}+\left(1-n\right)p\left(x\right)z=\left(1-n\right)q\left(x\right).$$

> **Riccati Equation**<br>If the right-hand side of the first-order equation $\frac{dy}{dx}=f\left(x,y\right)$ is a quadratic polynomial in $y$, written as $$\frac{dy}{dx}=p\left(x\right)y^2+q\left(x\right)y+r\left(x\right),$$ then it is called a Riccati equation, where $p\left(x\right),q\left(x\right),r\left(x\right)$ are continuous on the interval and $p\left(x\right)$ is not identically zero.

### Problem 1

(Problem 2-4, Problem 1(2)) Solve the differential equation $y'=\frac{2y-x+5}{2x-y-4}$.

### Solution to Problem 1

This is an **Equation Reducible to Homogeneous Form**. Solving the system $2y-x+5=0,\ 2x-y-4=0$ gives $x=1,\ y=-2$. Make the translation $x=\xi+1,\ y=\eta-2$, then
$$
2y-x+5=2\eta-\xi,\quad2x-y-4=2\xi-\eta.
$$

The equation becomes the homogeneous equation $\frac{d\eta}{d\xi}=\frac{2\eta-\xi}{2\xi-\eta}$. Setting $\eta=u\xi$, by the **Homogeneous Equation**, we get
$$
u+\xi\frac{du}{d\xi}=\frac{2u-1}{2-u}.
$$

Rearranging gives $\xi\frac{du}{d\xi}=\frac{u^2-1}{2-u}$, and separating variables:
$$
\frac{2-u}{u^2-1}du=\frac{d\xi}{\xi}.
$$

Decomposing the left-hand side $\frac{2-u}{u^2-1}=\frac{1/2}{u-1}-\frac{3/2}{u+1}$ and integrating gives
$$
\frac{1}{2}\ln\left|u-1\right|-\frac{3}{2}\ln\left|u+1\right|=\ln\left|\xi\right|+C.
$$

i.e. $\frac{u-1}{\left(u+1\right)^3}=C\xi^2$. Substituting back $u=\frac{\eta}{\xi}$ and simplifying gives $\frac{\eta-\xi}{\left(\eta+\xi\right)^3}=C$. Substituting back $\xi=x-1,\ \eta=y+2$, the general integral is
$$
y-x+3=C\left(x+y+1\right)^3.
$$

$\blacksquare$

### Problem 2

(Problem 2-4, Problem 1(4)) Solve the differential equation $y'=x^3y^3-xy$.

### Solution to Problem 2

The equation is $\frac{dy}{dx}+xy=x^3y^3$, which is a **Bernoulli equation** with $n=3$. Multiplying both sides by $\left(1-n\right)y^{-n}=-2y^{-3}$ and setting $z=y^{-2}$, then $z'=-2y^{-3}y'$, the equation becomes the first-order linear equation
$$
z'-2xz=-2x^3.
$$

By the integrating factor method for first-order linear equations, the integrating factor is $e^{\int-2x\,dx}=e^{-x^2}$. Thus
$$
\frac{d}{dx}\left(ze^{-x^2}\right)=-2x^3e^{-x^2}.
$$

Integrating the right-hand side $\int-2x^3e^{-x^2}dx=\left(x^2+1\right)e^{-x^2}$, we get
$$
ze^{-x^2}=\left(x^2+1\right)e^{-x^2}+C.
$$

i.e. $z=x^2+1+Ce^{x^2}$. Substituting back $z=y^{-2}$, the general integral is
$$
\frac{1}{y^2}=x^2+1+Ce^{x^2},
$$

In addition, the particular solution $y\equiv0$, lost during separation, must be supplied. $\blacksquare$

### Problem 3

(Problem 2-4, Problem 2(2)) Using an appropriate substitution, solve the equation $\left(3uv+v^2\right)du+\left(u^2+uv\right)dv=0$.

### Solution to Problem 3

Set $P\left(u,v\right)=3uv+v^2,\ Q\left(u,v\right)=u^2+uv$; both are homogeneous functions of degree two, so this is a **Homogeneous Equation**. Let $v=wu$ (where $w$ is the new unknown function), then $\frac{dv}{du}=w+u\frac{dw}{du}$, and the original equation becomes
$$
\frac{dv}{du}=-\frac{3uv+v^2}{u^2+uv}=-\frac{3w+w^2}{1+w}.
$$

Hence
$$
u\frac{dw}{du}=-\frac{3w+w^2}{1+w}-w=-\frac{2w\left(2+w\right)}{1+w}.
$$

Separating variables:
$$
\frac{1+w}{w\left(2+w\right)}dw=-\frac{2\,du}{u}.
$$

Decomposing the left-hand side $\frac{1+w}{w\left(2+w\right)}=\frac{1/2}{w}+\frac{1/2}{w+2}$ and integrating gives
$$
\frac{1}{2}\ln\left|w\right|+\frac{1}{2}\ln\left|w+2\right|=-2\ln\left|u\right|+C.
$$

i.e. $w\left(w+2\right)=Cu^{-4}$. Substituting back $w=\frac{v}{u}$ and rearranging, the general integral is
$$
u^2v\left(v+2u\right)=C.
$$

where $C=0$ already includes the particular solutions $v=0$ and $v=-2u$. $\blacksquare$

### Problem 4

(Problem 2-4, Problem 2(4)) Using an appropriate substitution, solve the equation $\frac{dy}{dx}=\frac{2x^3+3xy^2-7x}{3x^2y+2y^3-8y}$.

### Solution to Problem 4

The right-hand side can be written as $\frac{x\left(2x^2+3y^2-7\right)}{y\left(3x^2+2y^2-8\right)}$. Make the substitution $u=x^2,\ v=y^2$, then $\frac{dv}{du}=\frac{2y\,dy/dx}{2x}=\frac{y}{x}\frac{dy}{dx}$, and substituting gives
$$
\frac{dv}{du}=\frac{2u+3v-7}{3u+2v-8}.
$$

This is an **Equation Reducible to Homogeneous Form**. Solving the system $2u+3v-7=0,\ 3u+2v-8=0$ gives $u=2,\ v=1$. Make the translation $u=\xi+2,\ v=\eta+1$, then
$$
2u+3v-7=2\xi+3\eta,\quad3u+2v-8=3\xi+2\eta.
$$

The equation becomes $\frac{d\eta}{d\xi}=\frac{2\xi+3\eta}{3\xi+2\eta}$. Setting $\eta=w\xi$, by the **Homogeneous Equation**, we get
$$
\xi\frac{dw}{d\xi}=\frac{2+3w}{3+2w}-w=\frac{2\left(1-w^2\right)}{3+2w}.
$$

Separating variables:
$$
\frac{3+2w}{1-w^2}dw=\frac{2\,d\xi}{\xi}.
$$

Decomposing the left-hand side $\frac{3+2w}{1-w^2}=\frac{5/2}{1-w}+\frac{1/2}{1+w}$ and integrating gives
$$
-\frac{5}{2}\ln\left|1-w\right|+\frac{1}{2}\ln\left|1+w\right|=2\ln\left|\xi\right|+C.
$$

i.e. $\frac{1+w}{\left(1-w\right)^5}=C\xi^4$. Substituting back $w=\frac{\eta}{\xi}$ and simplifying gives $\frac{\xi+\eta}{\left(\xi-\eta\right)^5}=C$. Substituting back $\xi=x^2-2,\ \eta=y^2-1$, the general integral is
$$
x^2+y^2-3=C\left(x^2-y^2-1\right)^5.
$$

$\blacksquare$

### Problem 5

(Problem 2-4, Problem 4) Transform the second-order differential equation $y''+p\left(x\right)y'+q\left(x\right)y=0$ into a Riccati equation.

### Solution to Problem 5

Make the logarithmic derivative substitution $y'=yz$, i.e. $z=\frac{y'}{y}$ (when $y\neq0$), where $z$ is the new unknown function. Differentiating $y'=yz$ again gives
$$
y''=y'z+yz'=yz^2+yz'.
$$

Substituting into the original second-order equation gives
$$
yz^2+yz'+p\left(x\right)yz+q\left(x\right)y=0.
$$

Canceling the nonzero factor $y$ and rearranging gives
$$
z'=-z^2-p\left(x\right)z-q\left(x\right).
$$

This is exactly the form of a **Riccati equation** $\frac{dz}{dx}=P\left(x\right)z^2+Q\left(x\right)z+R\left(x\right)$, where $P\left(x\right)=-1,\ Q\left(x\right)=-p\left(x\right),\ R\left(x\right)=-q\left(x\right)$. $\blacksquare$
