# Assignment 2

> **Exact Equation** (Total Differential Equation)<br>Consider a first-order differential equation in symmetric form $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$. If there exists a differentiable function $\Phi\left(x,y\right)$ whose total differential is $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy$, i.e. whose partial derivatives satisfy $\frac{\partial\Phi}{\partial x}=P\left(x,y\right),\ \frac{\partial\Phi}{\partial y}=Q\left(x,y\right)$, then the equation is called an exact equation or total differential equation. When the equation is exact, it can be rewritten in total differential form $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy=0$, so that $\Phi\left(x,y\right)=C$, where $C$ is an arbitrary constant; $\Phi\left(x,y\right)=C$ is called a general integral of the equation.

> **Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula)<br>Let the functions $P\left(x,y\right)$ and $Q\left(x,y\right)$ be continuous on the region $R:\alpha<x<\beta,\ \gamma<y<\delta$, and have continuous first partial derivatives $\frac{\partial P}{\partial y}$ and $\frac{\partial Q}{\partial x}$. Then the differential equation $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ is an exact equation if and only if the identity $$\frac{\partial}{\partial y}P\left(x,y\right)\equiv\frac{\partial}{\partial x}Q\left(x,y\right)$$ holds in $R$. Moreover, when this holds, the general integral of the equation is $$\int_{x_0}^{x}P\left(x,y\right)dx+\int_{y_0}^{y}Q\left(x_0,y\right)dy=C,$$ or $$\int_{x_0}^{x}P\left(x,y_0\right)dx+\int_{y_0}^{y}Q\left(x,y\right)dy=C,$$ where $\left(x_0,y_0\right)$ is any fixed point in $R$.

### Problem 1

(Problem 2-1, Problem 3) Determine whether the following equation is exact, and solve it if it is: $\left(ax+by\right)dx+\left(bx+cy\right)dy=0$ ($a,b,c$ are constants).

### Solution to Problem 1

Set $P\left(x,y\right)=ax+by,\ Q\left(x,y\right)=bx+cy$. By **Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula), it suffices to check whether $\frac{\partial P}{\partial y}$ and $\frac{\partial Q}{\partial x}$ are identical. Computing gives
$$
\frac{\partial P}{\partial y}=b,\quad\frac{\partial Q}{\partial x}=b.
$$

Thus $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, and the equation is exact. Let $\Phi\left(x,y\right)$ satisfy
$$
\frac{\partial\Phi}{\partial x}=ax+by,\quad\frac{\partial\Phi}{\partial y}=bx+cy.
$$

Integrating the first equation with respect to $x$ gives
$$
\Phi\left(x,y\right)=\frac{a}{2}x^2+bxy+\psi\left(y\right).
$$

Substituting into the second equation gives $bx+\psi'\left(y\right)=bx+cy$, i.e. $\psi'\left(y\right)=cy$, hence $\psi\left(y\right)=\frac{c}{2}y^2$ (omitting the integration constant). Therefore the general integral of the equation is
$$
\Phi\left(x,y\right)=\frac{a}{2}x^2+bxy+\frac{c}{2}y^2=C.
$$

$\blacksquare$

### Problem 2

(Problem 2-1, Problem 6) Determine whether the following equation is exact, and solve it if it is: $\left(ye^x+2e^x+y^2\right)dx+\left(e^x+2xy\right)dy=0$.

### Solution to Problem 2

Set $P\left(x,y\right)=ye^x+2e^x+y^2,\ Q\left(x,y\right)=e^x+2xy$. By **Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula), it suffices to check whether $\frac{\partial P}{\partial y}$ and $\frac{\partial Q}{\partial x}$ are identical. Computing gives
$$
\frac{\partial P}{\partial y}=e^x+2y,\quad\frac{\partial Q}{\partial x}=e^x+2y.
$$

Thus $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, and the equation is exact. Let $\Phi\left(x,y\right)$ satisfy
$$
\frac{\partial\Phi}{\partial x}=ye^x+2e^x+y^2,\quad\frac{\partial\Phi}{\partial y}=e^x+2xy.
$$

Integrating the first equation with respect to $x$ gives
$$
\Phi\left(x,y\right)=ye^x+2e^x+xy^2+\psi\left(y\right).
$$

Substituting into the second equation gives $e^x+2xy+\psi'\left(y\right)=e^x+2xy$, i.e. $\psi'\left(y\right)=0$, so take $\psi\left(y\right)=0$. Therefore the general integral of the equation is
$$
\Phi\left(x,y\right)=e^x\left(y+2\right)+xy^2=C.
$$

$\blacksquare$

### Problem 3

(Problem 2-1, Problem 9) Determine whether the following equation is exact, and solve it if it is: $\frac{2s-1}{t}ds+\frac{s-s^2}{t^2}dt=0$.

### Solution to Problem 3

Set $P\left(s,t\right)=\frac{2s-1}{t},\ Q\left(s,t\right)=\frac{s-s^2}{t^2}$. By **Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula), it suffices to check whether $\frac{\partial P}{\partial t}$ and $\frac{\partial Q}{\partial s}$ are identical. Computing gives
$$
\frac{\partial P}{\partial t}=-\frac{2s-1}{t^2},\quad\frac{\partial Q}{\partial s}=\frac{1-2s}{t^2}=-\frac{2s-1}{t^2}.
$$

Thus $\frac{\partial P}{\partial t}\equiv\frac{\partial Q}{\partial s}$, and the equation is exact. Let $\Phi\left(s,t\right)$ satisfy
$$
\frac{\partial\Phi}{\partial s}=\frac{2s-1}{t},\quad\frac{\partial\Phi}{\partial t}=\frac{s-s^2}{t^2}.
$$

Integrating the first equation with respect to $s$ gives
$$
\Phi\left(s,t\right)=\frac{s^2-s}{t}+\psi\left(t\right).
$$

Substituting into the second equation gives $-\frac{s^2-s}{t^2}+\psi'\left(t\right)=\frac{s-s^2}{t^2}$. Since $-\left(s^2-s\right)=s-s^2$, we have $\psi'\left(t\right)=0$, so take $\psi\left(t\right)=0$. Therefore the general integral of the equation is
$$
\Phi\left(s,t\right)=\frac{s^2-s}{t}=C.
$$

$\blacksquare$

### Problem 4

(Problem 2-1, Problem 10) Determine whether the following equation is exact, and solve it if it is: $xf\left(x^2+y^2\right)dx+yf\left(x^2+y^2\right)dy=0$, where $f\left(\cdot\right)$ is continuously differentiable.

### Solution to Problem 4

Set $P\left(x,y\right)=xf\left(x^2+y^2\right),\ Q\left(x,y\right)=yf\left(x^2+y^2\right)$. By **Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula), it suffices to check whether $\frac{\partial P}{\partial y}$ and $\frac{\partial Q}{\partial x}$ are identical. Since $f$ is continuously differentiable, computing gives
$$
\frac{\partial P}{\partial y}=2xyf'\left(x^2+y^2\right),\quad\frac{\partial Q}{\partial x}=2xyf'\left(x^2+y^2\right).
$$

Thus $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, and the equation is exact. Let $F\left(u\right)$ be an antiderivative of $f\left(u\right)$, i.e. $F'\left(u\right)=f\left(u\right)$. Let $\Phi\left(x,y\right)$ satisfy
$$
\frac{\partial\Phi}{\partial x}=xf\left(x^2+y^2\right),\quad\frac{\partial\Phi}{\partial y}=yf\left(x^2+y^2\right).
$$

Integrating the first equation with respect to $x$, using $\int xf\left(x^2+y^2\right)dx=\frac{1}{2}F\left(x^2+y^2\right)$, gives
$$
\Phi\left(x,y\right)=\frac{1}{2}F\left(x^2+y^2\right)+\psi\left(y\right).
$$

Substituting into the second equation gives $yf\left(x^2+y^2\right)+\psi'\left(y\right)=yf\left(x^2+y^2\right)$, i.e. $\psi'\left(y\right)=0$, so take $\psi\left(y\right)=0$. Therefore the general integral of the equation is
$$
\Phi\left(x,y\right)=\frac{1}{2}F\left(x^2+y^2\right)=C,
$$

i.e. $F\left(x^2+y^2\right)=C$, where $F$ is an antiderivative of $f$. $\blacksquare$
