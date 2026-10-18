# Assignment 3

> **Separable Equation**<br>Consider a first-order differential equation in symmetric form $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0.$$ If $P\left(x,y\right)=X\left(x\right)Y_1\left(y\right)$ and $Q\left(x,y\right)=X_1\left(x\right)Y\left(y\right)$ can each be factored into a product of a function of $x$ and a function of $y$, then the equation is called a separable equation. When $X_1\left(x\right)Y_1\left(y\right)\neq0$, dividing both sides by $X_1\left(x\right)Y_1\left(y\right)$ gives $$\frac{X\left(x\right)}{X_1\left(x\right)}dx+\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=0,$$ whose general integral is $$\int\frac{X\left(x\right)}{X_1\left(x\right)}dx+\int\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=C.$$ In addition, the particular solutions $x=a_i$ ($a_i$ being a root of $X_1\left(x\right)=0$) and $y=b_j$ ($b_j$ being a root of $Y_1\left(y\right)=0$), which are not contained in the general integral, must be supplied.

### Problem 1

(Problem 2-2, Problem 1(3)) Solve the differential equation $\frac{dy}{dx}+y^2\sin x=0$, and indicate the region in the $Oxy$ plane where the equation is meaningful.

### Solution to Problem 1

The equation is $\frac{dy}{dx}=-y^2\sin x$, whose right-hand side is continuous on the entire plane $Oxy$, so the equation is meaningful on the entire plane. By the **Separable Equation**, when $y\neq0$, separating variables gives
$$
\frac{dy}{y^2}=-\sin x\,dx.
$$

Integrating both sides gives $-\frac{1}{y}=\cos x+C$, i.e.
$$
y=-\frac{1}{\cos x+C}.
$$

In addition, separating variables assumed $y\neq0$, and $y\equiv0$ directly satisfies the original equation; it is a particular solution to be supplied beyond the general integral. $\blacksquare$

### Problem 2

(Problem 2-2, Problem 1(5)) Solve the differential equation $\frac{dy}{dx}=\left(\cos x\cos 2y\right)^2$, and indicate the region in the $Oxy$ plane where the equation is meaningful.

### Solution to Problem 2

The right-hand side $\cos^2x\cos^22y$ is continuous on the entire plane, so the equation is meaningful on the entire plane. By the **Separable Equation**, when $\cos 2y\neq0$, separating variables gives
$$
\frac{dy}{\cos^22y}=\cos^2x\,dx.
$$

Integrating both sides, i.e. $\int\sec^22y\,dy=\int\cos^2x\,dx$, gives $\frac{1}{2}\tan 2y=\frac{x}{2}+\frac{\sin 2x}{4}+C$, which simplifies to
$$
\tan 2y=x+\frac{1}{2}\sin 2x+C.
$$

In addition, $\cos 2y=0$ gives the particular solutions to be supplied: $y=\frac{2k+1}{4}\pi$ ($k$ is an integer). $\blacksquare$

### Problem 3

(Problem 2-2, Problem 2(2)) Solve the initial value problem $x\,dx+ye^{-x}dy=0,\ y\left(0\right)=1$.

### Solution to Problem 3

By the **Separable Equation**, multiply both sides by $e^x$ and separate variables, giving
$$
y\,dy=-x e^x\,dx.
$$

Integrate both sides. On the right, integrating by parts, $\int x e^x dx=\left(x-1\right)e^x$, so
$$
\frac{y^2}{2}=-\left(x-1\right)e^x+C=e^x\left(1-x\right)+C.
$$

i.e. $y^2=2e^x\left(1-x\right)+C_1$. Substituting the initial condition $y\left(0\right)=1$ gives $1=2+C_1$, i.e. $C_1=-1$, so the desired solution is
$$
y^2=2e^x\left(1-x\right)-1.
$$

$\blacksquare$

### Problem 4

(Problem 2-2, Problem 2(4)) Solve the initial value problem $\frac{dy}{dx}=\frac{\ln\left|x\right|}{1+y^2},\ y\left(1\right)=0$.

### Solution to Problem 4

By the **Separable Equation**, separating variables gives
$$
\left(1+y^2\right)dy=\ln\left|x\right|\,dx.
$$

Integrating both sides, the left side is $y+\frac{y^3}{3}$, and on the right, integrating by parts, $\int\ln\left|x\right|dx=x\ln\left|x\right|-x$, so
$$
y+\frac{y^3}{3}=x\ln\left|x\right|-x+C.
$$

Substituting the initial condition $y\left(1\right)=0$ gives $0=-1+C$, i.e. $C=1$, so the desired solution is
$$
y+\frac{y^3}{3}=x\ln\left|x\right|-x+1.
$$

$\blacksquare$

### Problem 5

(Problem 2-2, Problem 3(2)) Solve the differential equation $\frac{dy}{dx}=ay$ ($a\neq0$ is a constant), and sketch the family of integral curves.

### Solution to Problem 5

By the **Separable Equation**, when $y\neq0$, separating variables gives
$$
\frac{dy}{y}=a\,dx.
$$

Integrating both sides gives $\ln\left|y\right|=ax+C$, i.e.
$$
y=C_1 e^{ax}.
$$

When $C_1=0$ we get the particular solution $y\equiv0$, which is already contained in the general solution. The family of integral curves is a family of curves asymptotic to the $x$-axis, rising or falling exponentially; when $a>0$ they grow exponentially as $x$ increases, and when $a<0$ they decay exponentially as $x$ increases. $\blacksquare$

### Problem 6

(Problem 2-2, Problem 3(4)) Solve the differential equation $\frac{dy}{dx}=y^n$ ($n=\frac{1}{3},1,2$), and sketch the family of integral curves.

### Solution to Problem 6

By the **Separable Equation**, we discuss the three values of $n$ separately.

When $n=\frac{1}{3}$, $y\neq0$, separating variables gives $y^{-1/3}dy=dx$, and integrating gives $\frac{3}{2}y^{2/3}=x+C$, i.e.
$$
y=\pm\left[\frac{2}{3}\left(x+C\right)\right]^{3/2},
$$

together with the particular solution $y\equiv0$ to be supplied. The integral curves are semicubical parabolas, meeting $y=0$ on the $x$-axis.

When $n=1$, $y\neq0$, separating variables gives $\frac{dy}{y}=dx$, and integrating gives
$$
y=Ce^x,
$$

where $C=0$ corresponds to the particular solution $y\equiv0$, already contained in the general solution. The integral curves are a family of exponential curves.

When $n=2$, $y\neq0$, separating variables gives $\frac{dy}{y^2}=dx$, and integrating gives $-\frac{1}{y}=x+C$, i.e.
$$
y=-\frac{1}{x+C},
$$

together with the particular solution $y\equiv0$ to be supplied. The integral curves are a family of hyperbolas with the line $x=-C$ as vertical asymptote. $\blacksquare$

### Problem 7

(Problem 2-2, Problem 5) Consider the differential equation $\frac{dy}{dx}=f\left(y\right)$, where $f\left(y\right)$ is continuous in some neighborhood of $y=a$ (e.g. the interval $\left[a-\epsilon,a+\epsilon\right]$), and $f\left(y\right)=0$ if and only if $y=a$. Prove: at every point on the line $y=a$, the solution of the equation is locally unique if and only if the improper integral $\left|\int_a^{a\pm\epsilon}\frac{dy}{f\left(y\right)}\right|=+\infty$ (diverges).

### Solution to Problem 7

Since $f\left(y\right)$ is continuous on $\left[a-\epsilon,a+\epsilon\right]$ and vanishes only at $y=a$, $f\left(y\right)$ keeps a fixed sign on both $\left(a,a+\epsilon\right)$ and $\left(a-\epsilon,a\right)$. The line $y\equiv a$ itself is always a solution of the equation. The question is whether there can be another nonconstant solution reaching the line $y=a$ at some point $\left(x_0,a\right)$.

First, prove sufficiency. Suppose both one-sided improper integrals diverge. Take any solution $y=y\left(x\right)$ through $\left(x_0,a\right)$, and suppose it is nonconstant; then near $x_0$, $y\left(x\right)\neq a$. By the **Separable Equation**, after separating variables, for a nonconstant solution we have
$$
x-x_0=\int_a^{y\left(x\right)}\frac{ds}{f\left(s\right)}.
$$

When $y\left(x\right)\to a$, the right-hand side diverges to $+\infty$ by assumption, i.e. $x-x_0\to+\infty$, contradicting the fact that $x-x_0$ is finite. Hence there can be no nonconstant solution through $\left(x_0,a\right)$; the unique solution is $y\equiv a$, and local uniqueness holds.

Next, prove necessity. Suppose one side's improper integral converges, e.g. $\int_a^{a+\epsilon}\frac{dy}{f\left(y\right)}=I$ is finite. Without loss of generality suppose $f\left(y\right)>0$ on $\left(a,a+\epsilon\right)$. Fix $x_1$; by the **Separable Equation**, the solution through $\left(x_1,a+\epsilon\right)$ satisfies
$$
x-x_1=\int_{a+\epsilon}^{y}\frac{ds}{f\left(s\right)}.
$$

Letting $y\to a^{+}$, the right-hand side tends to $\int_{a+\epsilon}^{a}\frac{ds}{f\left(s\right)}=-I$, which is finite. Thus this solution reaches $y=a$ at the finite abscissa $x_1-I$. Patching this solution with the line $y=a$ when $x\le x_1-I$ gives another solution through $\left(x_1-I,a\right)$ different from $y\equiv a$, and local uniqueness is destroyed. Hence the improper integral must diverge. $\blacksquare$
