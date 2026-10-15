# Assignment 6

> **Integrating Factor**<br>For the equation $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0,$$ if there exists a differentiable nonzero function $\mu\left(x,y\right)$ such that after multiplication the equation $$\mu\left(x,y\right)P\left(x,y\right)dx+\mu\left(x,y\right)Q\left(x,y\right)dy=0$$ becomes exact, i.e. satisfies $$\frac{\partial}{\partial y}\left(\mu P\right)=\frac{\partial}{\partial x}\left(\mu Q\right),$$ then $\mu\left(x,y\right)$ is called an integrating factor of the original equation.

> **Theorem 2.4** (Integrating Factor Depending Only on $x$)<br>The equation has an integrating factor depending only on $x$ if and only if the expression $$\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q}=G\left(x\right)$$ depends only on $x$ and not on $y$; in this case $\mu\left(x\right)=e^{\int G\left(x\right)dx}$ is an integrating factor of the equation.

> **Theorem 2.5** (Integrating Factor Depending Only on $y$)<br>The equation has an integrating factor depending only on $y$ if and only if the expression $$\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=H\left(y\right)$$ depends only on $y$; in this case $\mu\left(y\right)=e^{\int H\left(y\right)dy}$ is an integrating factor of the equation.

> **Theorem 2.6** (Product of an Integrating Factor with an Arbitrary Function of the General Integral)<br>If $\mu=\mu\left(x,y\right)$ is an integrating factor of the equation such that $$\mu P\left(x,y\right)dx+\mu Q\left(x,y\right)dy=d\Phi\left(x,y\right),$$ then $\mu\left(x,y\right)g\left(\Phi\left(x,y\right)\right)$ is also an integrating factor of the equation, where $g\left(\cdot\right)$ is any differentiable nonzero function.

### Problem 1

(Problem 2-5, Problem 1(2)) Solve the differential equation $y\,dx+\left(2xy-e^{-2y}\right)dy=0$.

### Solution to Problem 1

Set $P\left(x,y\right)=y,\ Q\left(x,y\right)=2xy-e^{-2y}$. Computing gives
$$
\frac{\partial P}{\partial y}=1,\quad\frac{\partial Q}{\partial x}=2y.
$$

These are not identical, so the equation is not exact. By **Theorem 2.5** (Integrating Factor Depending Only on $y$), check the expression
$$
\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=\frac{2y-1}{y}=2-\frac{1}{y},
$$

which depends only on $y$, so there exists an integrating factor depending only on $y$: $\mu\left(y\right)=e^{\int\left(2-\frac{1}{y}\right)dy}=e^{2y-\ln\left|y\right|}=\frac{e^{2y}}{y}$. Multiplying the original equation by $\mu\left(y\right)$ gives the exact equation
$$
e^{2y}dx+\left(2xe^{2y}-\frac{1}{y}\right)dy=0.
$$

Let the general integral be $\Phi\left(x,y\right)=C$. From $\frac{\partial\Phi}{\partial x}=e^{2y}$, integrating with respect to $x$ gives $\Phi\left(x,y\right)=xe^{2y}+\psi\left(y\right)$. Then from $\frac{\partial\Phi}{\partial y}=2xe^{2y}+\psi'\left(y\right)=2xe^{2y}-\frac{1}{y}$, we get $\psi'\left(y\right)=-\frac{1}{y}$, i.e. $\psi\left(y\right)=-\ln\left|y\right|$. Hence the general integral is
$$
xe^{2y}-\ln\left|y\right|=C.
$$

In addition, multiplying by the integrating factor divided by $y$, the lost particular solution $y\equiv0$ must be supplied. $\blacksquare$

### Problem 2

(Problem 2-5, Problem 1(4)) Solve the differential equation $y\,dx-\left(x^2+y^2+x\right)dy=0$.

### Solution to Problem 2

Regroup the left-hand side:
$$
\left(y\,dx-x\,dy\right)-\left(x^2+y^2\right)dy=0.
$$

Noting that $d\left(\arctan\frac{x}{y}\right)=\frac{y\,dx-x\,dy}{x^2+y^2}$, take the integrating factor $\mu\left(x,y\right)=\frac{1}{x^2+y^2}$. Following the regrouping idea of **Theorem 2.6** (Product of an Integrating Factor with an Arbitrary Function of the General Integral), multiplying both sides by $\mu$ gives
$$
\frac{y\,dx-x\,dy}{x^2+y^2}-dy=0.
$$

The first term is the total differential $d\left(\arctan\frac{x}{y}\right)$, so
$$
d\left(\arctan\frac{x}{y}\right)-dy=0.
$$

Integrating both sides gives the general integral
$$
\arctan\frac{x}{y}=y+C.
$$

$\blacksquare$

### Problem 3

(Problem 2-5, Problem 2) Prove: the equation $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ has an integrating factor of the form $\mu=\mu\left(\varphi\left(x,y\right)\right)$ if and only if $\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q\frac{\partial\varphi}{\partial x}-P\frac{\partial\varphi}{\partial y}}=f\left(\varphi\left(x,y\right)\right)$, and write out this integrating factor. Then apply the result to each of the following cases to obtain the necessary and sufficient condition for the existence of each type of integrating factor: (1) $\mu=\mu\left(x\pm y\right)$; (2) $\mu=\mu\left(x^2+y^2\right)$; (3) $\mu=\mu\left(xy\right)$; (4) $\mu=\mu\left(\frac{y}{x}\right)$; (5) $\mu=\mu\left(x^a y^b\right)$.

### Solution to Problem 3

Let $\mu=\mu\left(\varphi\left(x,y\right)\right)$. By the necessary and sufficient condition for an **Integrating Factor** $\frac{\partial\left(\mu P\right)}{\partial y}=\frac{\partial\left(\mu Q\right)}{\partial x}$, expanding gives
$$
\mu'\left(\varphi\right)\varphi_y P+\mu\frac{\partial P}{\partial y}=\mu'\left(\varphi\right)\varphi_x Q+\mu\frac{\partial Q}{\partial x}.
$$

Collecting $\mu'/\mu$:
$$
\frac{\mu'\left(\varphi\right)}{\mu\left(\varphi\right)}=\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q\varphi_x-P\varphi_y}.
$$

The left-hand side is a function of $\varphi$ alone, so the right-hand side must also depend only on $\varphi\left(x,y\right)$. Conversely, if the right-hand side equals some function $f\left(\varphi\right)$ of $\varphi$, then $\frac{d\mu}{\mu}=f\left(\varphi\right)d\varphi$, and integrating gives $\mu=e^{\int f\left(\varphi\right)d\varphi}$. The necessary and sufficient condition is proved, and the integrating factor is
$$
\mu=e^{\int f\left(\varphi\left(x,y\right)\right)d\varphi}.
$$

Substituting each $\varphi$:

(1) $\varphi=x\pm y$, then $\varphi_x=1,\ \varphi_y=\pm1$, the condition is
$$
\frac{P_y-Q_x}{Q\mp P}=f\left(x\pm y\right).
$$

(2) $\varphi=x^2+y^2$, then $\varphi_x=2x,\ \varphi_y=2y$, the condition is
$$
\frac{P_y-Q_x}{2\left(xQ-yP\right)}=f\left(x^2+y^2\right).
$$

(3) $\varphi=xy$, then $\varphi_x=y,\ \varphi_y=x$, the condition is
$$
\frac{P_y-Q_x}{yQ-xP}=f\left(xy\right).
$$

(4) $\varphi=\frac{y}{x}$, then $\varphi_x=-\frac{y}{x^2},\ \varphi_y=\frac{1}{x}$, the condition is
$$
\frac{x^2\left(P_y-Q_x\right)}{-\left(yQ+xP\right)}=f\left(\frac{y}{x}\right).
$$

(5) $\varphi=x^a y^b$, then $\varphi_x=ax^{a-1}y^b,\ \varphi_y=bx^ay^{b-1}$, the condition is
$$
\frac{P_y-Q_x}{x^{a-1}y^{b-1}\left(axQ-byP\right)}=f\left(x^ay^b\right).
$$

$\blacksquare$

### Problem 4

(Problem 2-5, Problem 4) Prove Theorem 2.6 and its converse: under the assumptions of Theorem 2.6, if $\mu_1$ is another integrating factor of the differential equation, then $\mu_1$ must be expressible in the form $\mu_1=\mu g\left(\Phi\right)$, where the functions $g$ and $\Phi$ have the same meaning as in Theorem 2.6.

### Solution to Problem 4

First prove the forward direction, i.e. **Theorem 2.6** (Product of an Integrating Factor with an Arbitrary Function of the General Integral) itself. Given $\mu P dx+\mu Q dy=d\Phi$. Multiplying both sides by any differentiable nonzero function $g\left(\Phi\right)$ gives
$$
g\left(\Phi\right)\left(\mu P dx+\mu Q dy\right)=g\left(\Phi\right)d\Phi=d\left(\int g\left(\Phi\right)d\Phi\right),
$$

the right-hand side is the total differential of some function, so $\mu g\left(\Phi\right)$ is still an integrating factor.

Next prove the converse. Let $\mu_1$ be another integrating factor; then there exists a function $\Psi\left(x,y\right)$ such that $\mu_1 P dx+\mu_1 Q dy=d\Psi$. Also $d\Phi=\mu P dx+\mu Q dy$, so
$$
d\Psi=\mu_1P dx+\mu_1Q dy=\frac{\mu_1}{\mu}\left(\mu P dx+\mu Q dy\right)=\frac{\mu_1}{\mu}d\Phi.
$$

Let $r=\frac{\mu_1}{\mu}$, then $d\Psi=r\,d\Phi$. On any level line of $\Phi$, $d\Phi=0$, hence $d\Psi=0$, i.e. $\Psi$ is constant on level lines of $\Phi$, so $\Psi$ is a function of $\Phi$ alone, $\Psi=\Psi\left(\Phi\right)$. Thus $d\Psi=\Psi'\left(\Phi\right)d\Phi$, and comparing with $d\Psi=r\,d\Phi$ gives
$$
r=\Psi'\left(\Phi\right)=g\left(\Phi\right).
$$

i.e. $\frac{\mu_1}{\mu}=g\left(\Phi\right)$, i.e. $\mu_1=\mu g\left(\Phi\right)$. The converse is proved. $\blacksquare$
