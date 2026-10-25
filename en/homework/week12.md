# Assignment 12

> **Definition 4.1** (Singular Solution)<br>Suppose the first-order differential equation $$F\left(x,y,\frac{dy}{dx}\right)=0$$ has a particular solution $\Gamma:y=\varphi\left(x\right)$ ($x\in J$). If at every point $Q\in\Gamma$, in any neighborhood of $Q$, the equation has another solution different from $\Gamma$ that is tangent to $\Gamma$ at $Q$, then $\Gamma$ is called a singular solution of the differential equation.

> **Theorem 4.1** (Necessary Condition for a Singular Solution, i.e. the $p$-discriminant)<br>Suppose the function $F\left(x,y,p\right)$ is continuous for $\left(x,y,p\right)\in G$, and has continuous partial derivatives $F_y'$ and $F_p'$ with respect to $y$ and $p$. If the function $y=\varphi\left(x\right)$ ($x\in J$) is a singular solution of the differential equation and $\left(x,\varphi\left(x\right),\varphi'\left(x\right)\right)\in G$, then the singular solution $y=\varphi\left(x\right)$ satisfies the $p$-discriminant $$\begin{cases}F\left(x,y,p\right)=0,\\F_p'\left(x,y,p\right)=0,\end{cases}\quad\left(p=\frac{dy}{dx}\right).$$ The curve determined by eliminating $p$ from the $p$-discriminant is called the $p$-discriminant curve. A singular solution must be a $p$-discriminant curve. Note, however, that a function determined by the $p$-discriminant is not necessarily a solution, and even if it is a solution it is not necessarily a singular solution; it must still be verified by **Definition 4.1** (Singular Solution).

> **Theorem 4.2** (Sufficient Condition for a Singular Solution)<br>Suppose the function $F\left(x,y,p\right)$ is twice continuously differentiable for $\left(x,y,p\right)\in G$. Suppose further that the function $y=\psi\left(x\right)$ ($x\in J$) obtained by eliminating $p$ from the $p$-discriminant is a solution of the differential equation, and the conditions $$F_y'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0,\quad F_{pp}''\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0$$ and $$F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$$ hold for $x\in J$; then $y=\psi\left(x\right)$ is a singular solution of the differential equation.

### Problem 1

(Problem 4-2, Problem 1(3)) Use the $p$-discriminant to find the singular solution of the differential equation $\left(y-1\right)^2\left(\frac{dy}{dx}\right)^2=\frac{4}{9}y$.

### Solution to Problem 1

Set $p=\frac{dy}{dx}$; then $F\left(x,y,p\right)=\left(y-1\right)^2p^2-\frac{4}{9}y=0$. By **Theorem 4.1** (Necessary Condition for a Singular Solution, i.e. the $p$-discriminant), first write the $p$-discriminant

$$
\begin{cases}
\left(y-1\right)^2p^2-\frac{4}{9}y=0,\\
F_p'\left(x,y,p\right)=2p\left(y-1\right)^2=0.
\end{cases}
$$

From the second equation, $p=0$ (the other possibility, $y=1$, substituted into the first gives $-\frac{4}{9}=0$, which fails). Substituting $p=0$ into the first equation gives $-\frac{4}{9}y=0$, i.e. $y=0$.

Verify that $y=0$ is indeed a solution: then $p=y'=0$, and $F\left(x,0,0\right)=\left(0-1\right)^2\cdot0-\frac{4}{9}\cdot0=0$. Then by **Theorem 4.2** (Sufficient Condition for a Singular Solution), check the conditions: at $\left(x,0,0\right)$, $F_y'=2\left(y-1\right)p^2-\frac{4}{9}=-\frac{4}{9}\neq0$, $F_{pp}''=2\left(y-1\right)^2=2\neq0$, $F_p'=2p\left(y-1\right)^2=0$; all three conditions are satisfied. Hence $y=0$ is a singular solution of this differential equation. $\blacksquare$

### Problem 2

(Problem 4-2, Problem 3) Study the following example to show that the condition $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ in **Theorem 4.2** (Sufficient Condition for a Singular Solution) is indispensable: $y=2x+\frac{dy}{dx}-\frac{1}{3}\left(\frac{dy}{dx}\right)^3$.

### Solution to Problem 2

Set $p=\frac{dy}{dx}$; then $F\left(x,y,p\right)=y-2x-p+\frac{1}{3}p^3=0$. By **Theorem 4.1** (Necessary Condition for a Singular Solution, i.e. the $p$-discriminant), the $p$-discriminant is

$$
\begin{cases}
y-2x-p+\frac{1}{3}p^3=0,\\
F_p'\left(x,y,p\right)=-1+p^2=0.
\end{cases}
$$

From the second equation, $p=\pm1$. Substituting back into the first equation: when $p=1$, $y=2x+\frac{2}{3}$; when $p=-1$, $y=2x-\frac{2}{3}$.

First verify whether these two $p$-discriminant curves are solutions. The line $y=2x-\frac{2}{3}$ has slope $y'=2$; substituting into the left-hand side $F\left(x,2x-\frac{2}{3},2\right)=\left(2x-\frac{2}{3}\right)-2x-2+\frac{8}{3}=0$, so it is a solution. The line $y=2x+\frac{2}{3}$ also has slope $2$; substituting gives $F\left(x,2x+\frac{2}{3},2\right)=\frac{2}{3}-2+\frac{8}{3}=\frac{4}{3}\neq0$, so it is not a solution.

For the solution $y=2x-\frac{2}{3}$, check the conditions of **Theorem 4.2** (Sufficient Condition for a Singular Solution): $F_y'=1\neq0$, $F_{pp}''=2p=4\neq0$, so these two inequality conditions hold; but the third condition requires $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$, whereas here $\psi'\left(x\right)=2$, so

$$
F_p'\left(x,2x-\frac{2}{3},2\right)=-1+2^2=3\neq0,
$$

i.e. the condition $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ does not hold.

Finally, by **Definition 4.1** (Singular Solution), verify whether $y=2x-\frac{2}{3}$ is a singular solution. Take any point on this line; other integral curves through that point satisfy $F=0$, i.e. $y_0-2x_0-p+\frac{1}{3}p^3=0$. Substituting $y_0=2x_0-\frac{2}{3}$ gives $-\frac{2}{3}-p+\frac{1}{3}p^3=0$, i.e. $p^3-3p-2=0=\left(p-2\right)\left(p+1\right)^2$. Hence the slope of other integral curves at that point is $p=-1$, which is not equal to the line's slope $2$; i.e. they merely intersect at that point rather than being tangent. Therefore $y=2x-\frac{2}{3}$ is not a singular solution. This shows that having $y=\psi\left(x\right)$ be a solution and the two inequality conditions is not enough; the condition $F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0$ is indispensable. $\blacksquare$

### Problem 3

(Problem 4-2, Problem 4) Suppose the continuous function $E\left(y\right)$ satisfies $E\left(0\right)=0$, and $E\left(y\right)\neq0$ when $0< y\le1$. Then $y=0$ is a singular solution of the differential equation $\frac{dy}{dx}=E\left(y\right)$ if and only if the improper integral $\int_0^1\frac{dy}{E\left(y\right)}$ converges.

### Solution to Problem 3

Set $p=\frac{dy}{dx}$; then $F\left(x,y,p\right)=p-E\left(y\right)=0$. Since $E\left(0\right)=0$, $y=0$ is a solution of the equation.

First find the general solution. Separating variables gives $\frac{dy}{E\left(y\right)}=dx$, and integrating gives

$$
x=\int\frac{dy}{E\left(y\right)}+C.
$$

By **Definition 4.1** (Singular Solution), $y=0$ is a singular solution if and only if in any neighborhood of every point on $y=0$, there is another integral curve tangent to $y=0$ at that point.

If the improper integral $\int_0^1\frac{dy}{E\left(y\right)}$ converges, then a nontrivial integral curve starting from some $y_0> 0$ reaches $y=0$ after traversing a finite abscissa $\int_0^{y_0}\frac{dy}{E\left(y\right)}$. That is, the nontrivial integral curve meets $y=0$ at a finite abscissa; at the meeting point its slope $p=E\left(y\right)\to E\left(0\right)=0$, which equals the slope $0$ of $y=0$, so the two are tangent there. Hence near every point on $y=0$ there are other integral curves tangent to $y=0$, and $y=0$ is a singular solution.

If the improper integral $\int_0^1\frac{dy}{E\left(y\right)}$ diverges, then a nontrivial integral curve starting from $y_0> 0$ must traverse an infinite abscissa for $y\to0$; i.e. they only approach $y=0$ asymptotically as the abscissa tends to infinity, and do not meet $y=0$ at any finite point. Hence near every point on $y=0$ there are no other integral curves tangent to it, and $y=0$ is not a singular solution.

In summary, $y=0$ is a singular solution if and only if $\int_0^1\frac{dy}{E\left(y\right)}$ converges. $\blacksquare$
