# Assignment 13

> **Definition 4.2** (Envelope)<br>Suppose there is a continuously differentiable curve $\Gamma$ in the plane. If for every point $q\in\Gamma$, there is a curve $K\left(C^*\right)$ in the one-parameter family of curves $K\left(C\right):V\left(x,y,C\right)=0$ passing through $q$ and tangent to $\Gamma$ at that point, and $K\left(C^*\right)$ is different from $\Gamma$ in any neighborhood of $q$, then $\Gamma$ is called an envelope of this family of curves.

> **Theorem 4.3** (An Envelope Is a Singular Solution)<br>Suppose the differential equation $F\left(x,y,\frac{dy}{dx}\right)=0$ has the general integral $U\left(x,y,C\right)=0$, and suppose this family of integral curves has an envelope $\Gamma:y=\varphi\left(x\right)$ ($x\in J$). Then the envelope $y=\varphi\left(x\right)$ is a singular solution of the differential equation. Therefore, finding the singular solution of a differential equation reduces to finding the envelope of its general integral.

> **Theorem 4.4** (The Envelope Satisfies the $C$-discriminant)<br>Suppose $\Gamma$ is an envelope of the family $K\left(C\right):V\left(x,y,C\right)=0$ and can be represented as a smooth curve in the parameter $C$; then it satisfies the $C$-discriminant $$\begin{cases}V\left(x,y,C\right)=0,\\V_C'\left(x,y,C\right)=0,\end{cases}$$ or the relation $\Omega\left(x,y\right)=0$ obtained by eliminating $C$.

> **Theorem 4.5** (The $C$-discriminant Is a Sufficient Condition for an Envelope)<br>Suppose the $C$-discriminant of the family $K\left(C\right):V\left(x,y,C\right)=0$ determines a continuously differentiable curve not contained in the family $$\Lambda:\begin{cases}x=\varphi\left(C\right),\\y=\psi\left(C\right),\end{cases}\quad\left(C\in J\right),$$ which also satisfies the nondegeneracy conditions $$\left(\varphi'\left(C\right),\psi'\left(C\right)\right)\neq\left(0,0\right),\quad\left(V_x',V_y'\right)\neq\left(0,0\right),$$ then $\Lambda$ is an envelope of the family.

### Problem 1

(Problem 4-3, Problem 2) Find a differential equation that has the singular solution $y=\sin x$.

### Solution to Problem 1

By **Theorem 4.3** (An Envelope Is a Singular Solution), it suffices to construct a one-parameter family of curves whose envelope is $y=\sin x$, and then write the differential equation having this family as its general integral.

Take all tangent lines to $y=\sin x$. At the abscissa $x=a$, the tangent line is

$$
y=\sin a+\cos a\cdot\left(x-a\right)=x\cos a+\sin a-a\cos a.
$$

Denote the family as $V\left(x,y,a\right)=y-x\cos a-\sin a+a\cos a=0$. By **Theorem 4.4** (The Envelope Satisfies the $C$-discriminant), find its envelope: differentiating with respect to the parameter $a$ gives

$$
V_a'\left(x,y,a\right)=x\sin a-\cos a+\cos a-a\sin a=\left(x-a\right)\sin a.
$$

Solve $V=0$ and $V_a'=0$ simultaneously. From $\left(x-a\right)\sin a=0$, take $x=a$ (the branch where $\sin a\neq0$), and substituting into $V=0$ gives $y=a\cos a+\sin a-a\cos a=\sin a$. Since $x=a$, the envelope is $y=\sin x$. Moreover, this curve is nondegenerate and satisfies the nondegeneracy conditions; by **Theorem 4.5** (The $C$-discriminant Is a Sufficient Condition for an Envelope), $y=\sin x$ is indeed an envelope of this family.

Now write the differential equation having this family as its general integral. Let $p=\frac{dy}{dx}=\cos a$; then $a=\arccos p$, $\sin a=\sqrt{1-p^2}$. Substituting into the tangent line equation gives

$$
y=xp+\sqrt{1-p^2}-p\arccos p.
$$

i.e. the desired differential equation is

$$
y=x\frac{dy}{dx}+\sqrt{1-\left(\frac{dy}{dx}\right)^2}-\frac{dy}{dx}\arccos\left(\frac{dy}{dx}\right).
$$

Its general integral is $y=Cx+\sqrt{1-C^2}-C\arccos C$, and $y=\sin x$ is its singular solution. Verification: for $y=\sin x$, $p=\cos x$, and substituting into the right-hand side gives

$$
x\cos x+\sqrt{1-\cos^2 x}-\cos x\cdot\arccos\left(\cos x\right)=x\cos x+\sin x-x\cos x=\sin x=y,
$$

so $y=\sin x$ is indeed a solution of this equation, and by **Theorem 4.3** (An Envelope Is a Singular Solution), it is a singular solution. $\blacksquare$
