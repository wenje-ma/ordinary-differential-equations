# Ordinary Differential Equations

## 1.1 Differential Equations and the Definition of Their Solutions

**Definition 1.1** (Ordinary Differential Equation)

Any equation involving the independent variable $x$, the unknown function $y=y\left(x\right)$ of this independent variable, and its derivatives $y'=y'\left(x\right)$ up to the $n$-th derivative $y^{\left(n\right)}=y^{\left(n\right)}\left(x\right)$, i.e. $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$, is called an ordinary differential equation, where the highest order $n$ at which a derivative actually appears is called the order of the ordinary differential equation. If the left-hand function $F$ is linear in the unknown function $y$ and all its derivatives $y',y'',\cdots,y^{\left(n\right)}$ taken together, then it is called a linear ordinary differential equation; otherwise it is called a nonlinear ordinary differential equation.

**Definition 1.2** (Solution)

Let the function $y=\varphi\left(x\right)$ be continuous on the interval $J$ and possess derivatives up to order $n$. If substituting $y=\varphi\left(x\right)$ and the corresponding derivatives into the equation $F\left(x,y,y',\cdots,y^{\left(n\right)}\right)=0$ yields an identity in $x$

$$
F\left(x,\varphi\left(x\right),\varphi'\left(x\right),\cdots,\varphi^{\left(n\right)}\left(x\right)\right)=0
$$

holding for all $x\in J$, then $y=\varphi\left(x\right)$ is called a solution of the differential equation on the interval $J$.

**Definition 1.3** (General Solution and Particular Solution)

Let a solution $y=\varphi\left(x,C_1,C_2,\cdots,C_n\right)$ of an $n$-th order differential equation contain $n$ independent arbitrary constants $C_1,C_2,\cdots,C_n$; then it is called a general solution. Here the $n$ arbitrary constants $C_1,C_2,\cdots,C_n$ are independent, meaning that the Jacobian determinant $\frac{D\left(\varphi,\varphi',\cdots,\varphi^{\left(n-1\right)}\right)}{D\left(C_1,C_2,\cdots,C_n\right)}\neq0$, where

$$
\varphi^{\left(k\right)}=\varphi^{\left(k\right)}\left(x,C_1,C_2,\cdots,C_n\right)\ \left(k=0,1,\cdots,n-1\right).
$$

If a solution $y=\varphi\left(x\right)$ of the differential equation contains no arbitrary constants, then it is called a particular solution.

**Initial Value Problem** (Cauchy Problem)

For an $n$-th order differential equation, the general formulation of the initial conditions is

$$
y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)},
$$

where $x_0$ is some prescribed initial value of the independent variable, and $y_0,\ y_0',\ \cdots,\ y_0^{\left(n-1\right)}$ are the prescribed initial values of the unknown function and its corresponding derivatives. Thus the initial value problem for an $n$-th order differential equation can be formulated as

$$
\begin{cases}y^{\left(n\right)}=F\left(x,y,y',\cdots,y^{\left(n-1\right)}\right),\\y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}.\end{cases}
$$

The initial value problem is also called the Cauchy problem.

**Solving Differential Equations and Integration Operations**

Solving a differential equation is associated with a certain integration operation. Hence the process of solving a differential equation is often called integrating a differential equation, and a solution of a differential equation is called an integral. Since each indefinite integration introduces an arbitrary constant, the general solution of an $n$-th order differential equation should contain $n$ arbitrary constants.

## 2.1 Exact Equations

**Exact Equation** (Total Differential Equation)

Consider a first-order differential equation in symmetric form $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$. If there exists a differentiable function $\Phi\left(x,y\right)$ whose total differential is $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy$, i.e. whose partial derivatives satisfy $\frac{\partial\Phi}{\partial x}=P\left(x,y\right),\ \frac{\partial\Phi}{\partial y}=Q\left(x,y\right)$, then the equation is called an exact equation or total differential equation. When the equation is exact, it can be rewritten in total differential form $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy=0$, so that $\Phi\left(x,y\right)=C$, where $C$ is an arbitrary constant; $\Phi\left(x,y\right)=C$ is called a general integral of the equation.

**Theorem 2.1** (Criterion for Exact Equations and the General Integral Formula)

Let the functions $P\left(x,y\right)$ and $Q\left(x,y\right)$ be continuous in the region $R:\alpha< x< \beta,\ \gamma< y< \delta$, and have continuous first partial derivatives $\frac{\partial P}{\partial y}$ and $\frac{\partial Q}{\partial x}$. Then the differential equation $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ is an exact equation if and only if the identity

$$
\frac{\partial}{\partial y}P\left(x,y\right)\equiv\frac{\partial}{\partial x}Q\left(x,y\right)
$$

holds in $R$. Moreover, when this holds, the general integral of the equation is

$$
\int_{x_0}^{x}P\left(x,y\right)dx+\int_{y_0}^{y}Q\left(x_0,y\right)dy=C,
$$

or

$$
\int_{x_0}^{x}P\left(x,y_0\right)dx+\int_{y_0}^{y}Q\left(x,y\right)dy=C,
$$

where $\left(x_0,y_0\right)$ is any fixed point in $R$.

## 2.2 Separable Equations

**Separable Equation**

Consider a first-order differential equation in symmetric form

$$
P\left(x,y\right)dx+Q\left(x,y\right)dy=0.
$$

If $P\left(x,y\right)=X\left(x\right)Y_1\left(y\right)$ and $Q\left(x,y\right)=X_1\left(x\right)Y\left(y\right)$ can each be factored into a product of a function of $x$ and a function of $y$, then the equation is called a separable equation. When $X_1\left(x\right)Y_1\left(y\right)\neq0$, dividing both sides by $X_1\left(x\right)Y_1\left(y\right)$ gives

$$
\frac{X\left(x\right)}{X_1\left(x\right)}dx+\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=0,
$$

whose general integral is

$$
\int\frac{X\left(x\right)}{X_1\left(x\right)}dx+\int\frac{Y\left(y\right)}{Y_1\left(y\right)}dy=C.
$$

In addition, the particular solutions $x=a_i$ ($a_i$ being a root of $X_1\left(x\right)=0$) and $y=b_j$ ($b_j$ being a root of $Y_1\left(y\right)=0$), which are not contained in the general integral, must be supplied.

## 2.3 First-Order Linear Equations

**First-Order Linear Equation**

An equation of the form

$$
\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)
$$

is called a first-order linear equation, where $p\left(x\right),q\left(x\right)$ are continuous on the interval $I$. When $q\left(x\right)\equiv0$ it is called the corresponding homogeneous linear equation; otherwise it is called a nonhomogeneous linear equation.

**General Solution of a Homogeneous Linear Equation**

For the homogeneous linear equation

$$
\frac{dy}{dx}+p\left(x\right)y=0,
$$

separating variables and integrating gives the general solution

$$
y=Ce^{-\int p\left(x\right)dx},
$$

where the arbitrary constant $C$ may take the value zero, and $C=0$ corresponds to the particular solution $y\equiv0$.

**General Solution of a Nonhomogeneous Linear Equation** (Integrating Factor Method)

Multiplying both sides of the nonhomogeneous linear equation by the integrating factor

$$
\mu\left(x\right)=e^{\int p\left(x\right)dx}
$$

converts the left-hand side into a total differential

$$
\frac{d}{dx}\left(e^{\int p\left(x\right)dx}y\right)=q\left(x\right)e^{\int p\left(x\right)dx}.
$$

Integrating gives the general solution

$$
y=e^{-\int p\left(x\right)dx}\left[\int q\left(x\right)e^{\int p\left(x\right)dx}dx+C\right].
$$

## 2.4 Elementary Transformation Methods

**Homogeneous Equation**

If, in the first-order differential equation

$$
P\left(x,y\right)dx+Q\left(x,y\right)dy=0
$$

$P\left(x,y\right)$ and $Q\left(x,y\right)$ are homogeneous functions of the same degree, i.e.

$$
P\left(tx,ty\right)=t^mP\left(x,y\right),\ Q\left(tx,ty\right)=t^mQ\left(x,y\right),
$$

then the equation is called a homogeneous equation. Making the substitution $y=ux$ (where $u$ is the new unknown function), the equation becomes a separable equation in $u$ and $x$.

**Equations Reducible to Homogeneous Ones**

For the equation

$$
\frac{dy}{dx}=\frac{ax+by+c}{mx+ny+l},
$$

when $c,l$ are not both zero and $\Delta=an-bm\neq0$, one can determine $\alpha,\beta$ from the linear system $a\alpha+b\beta+c=0,\ m\alpha+n\beta+l=0$, and make the translation $x=\xi+\alpha,\ y=\eta+\beta$; the equation becomes the homogeneous equation $\frac{d\eta}{d\xi}=\frac{a\xi+b\eta}{m\xi+n\eta}$. Then setting $\eta=u\xi$ reduces it to a separable equation.

**Bernoulli Equation**

An equation of the form

$$
\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)y^n
$$

is called a Bernoulli equation, where the constant $n\neq0,1$. Multiplying both sides by $\left(1-n\right)y^{-n}$ and then setting $z=y^{1-n}$ converts the equation into a first-order linear equation in $z$

$$
\frac{dz}{dx}+\left(1-n\right)p\left(x\right)z=\left(1-n\right)q\left(x\right).
$$

**Riccati Equation**

If the right-hand side of the first-order equation $\frac{dy}{dx}=f\left(x,y\right)$ is a quadratic polynomial in $y$, i.e. written as

$$
\frac{dy}{dx}=p\left(x\right)y^2+q\left(x\right)y+r\left(x\right),
$$

then it is called a Riccati equation, where $p\left(x\right),q\left(x\right),r\left(x\right)$ are continuous on the interval and $p\left(x\right)$ is not identically zero.

## 2.5 The Integrating Factor Method

**Integrating Factor**

For the equation

$$
P\left(x,y\right)dx+Q\left(x,y\right)dy=0,
$$

if there exists a differentiable nonzero function $\mu\left(x,y\right)$ such that after multiplication the equation

$$
\mu\left(x,y\right)P\left(x,y\right)dx+\mu\left(x,y\right)Q\left(x,y\right)dy=0
$$

becomes exact, i.e. satisfies

$$
\frac{\partial}{\partial y}\left(\mu P\right)=\frac{\partial}{\partial x}\left(\mu Q\right),
$$

then $\mu\left(x,y\right)$ is called an integrating factor of the original equation.

**Theorem 2.4** (Integrating Factor Depending Only on $x$)

The equation has an integrating factor depending only on $x$ if and only if the expression

$$
\frac{\frac{\partial P}{\partial y}-\frac{\partial Q}{\partial x}}{Q}=G\left(x\right)
$$

depends only on $x$ and is independent of $y$; in this case $\mu\left(x\right)=e^{\int G\left(x\right)dx}$ is an integrating factor of the equation.

**Theorem 2.5** (Integrating Factor Depending Only on $y$)

The equation has an integrating factor depending only on $y$ if and only if the expression

$$
\frac{\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y}}{P}=H\left(y\right)
$$

depends only on $y$; in this case $\mu\left(y\right)=e^{\int H\left(y\right)dy}$ is an integrating factor of the equation.

**Theorem 2.6** (Product of an Integrating Factor with an Arbitrary Function of the General Integral)

If $\mu=\mu\left(x,y\right)$ is an integrating factor of the equation such that

$$
\mu P\left(x,y\right)dx+\mu Q\left(x,y\right)dy=d\Phi\left(x,y\right),
$$

then $\mu\left(x,y\right)g\left(\Phi\left(x,y\right)\right)$ is also an integrating factor of the equation, where $g\left(\cdot\right)$ is any differentiable nonzero function.

## 3.1 Picard's Existence and Uniqueness Theorem

**Lipschitz Condition**

Let the function $f\left(x,y\right)$ satisfy in the region $D$ the inequality $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, where the constant $L> 0$; then the function $f\left(x,y\right)$ is said to satisfy a Lipschitz condition with respect to $y$ in the region $D$. If $f\left(x,y\right)$ has a continuous partial derivative with respect to $y$ in a convex region $D$, then it satisfies a Lipschitz condition with respect to $y$ in $D$.

**Theorem 3.1** (Picard's Existence and Uniqueness Theorem)

Consider the initial value problem $\left(E\right)$:

$$
\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0,
$$

where $f\left(x,y\right)$ is continuous in the rectangular region $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Then $\left(E\right)$ has exactly one solution on the interval $I=\left[x_0-h,x_0+h\right]$, where the constant $h=\min\left\{a,\frac{b}{M}\right\}$ and $M=\max_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

**Theorem 3.2** (Uniqueness of Solutions Under the Osgood Condition)

Let the function $f\left(x,y\right)$ be continuous in the region $G$ and satisfy the inequality

$$
\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le F\left(\left|y_1-y_2\right|\right),
$$

where $F\left(r\right)> 0$ is a continuous function of $r> 0$, and the improper integral $\int_0^{r_1}\frac{dr}{F\left(r\right)}=+\infty$ ($r_1> 0$ a constant). Then $f\left(x,y\right)$ is said to satisfy the Osgood condition with respect to $y$ in $G$; in this case the solution of the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ through every point in $G$ is unique.

**Equivalence Between the Integral Equation and the Initial Value Problem**

The initial value problem $\left(E\right)$:

$$
\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0
$$

has a solution $y=\varphi\left(x\right)$ if and only if the integral equation $y=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$ has a solution. Its Picard sequence is

$$
y_{n+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt,
$$

where one takes $y_0\left(x\right)=y_0$.

## 3.2 Peano's Existence Theorem

**Euler Broken Line**

Let the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ be continuous in the rectangular region $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$, let $M$ be an upper bound of $\left|f\left(x,y\right)\right|$ on $R$, and set $h=\min\left\{a,\frac{b}{M}\right\}$. Divide the interval $\left[x_0-h,x_0+h\right]$ into $2n$ equal parts. Starting from the initial point $P_0\left(x_0,y_0\right)$, draw at each node a line segment along the direction of the line element at that point, obtaining a continuous broken line $y=\rho_n\left(x\right)$ that stays within the angular region $\left|y-y_0\right|\le M\left|x-x_0\right|$; this is called the Euler broken line of the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$.

**Theorem 3.1** (Picard's Existence and Uniqueness Theorem)

Consider the initial value problem $\left(E\right)$:

$$
\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0,
$$

where $f\left(x,y\right)$ is continuous in the rectangular region $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Then $\left(E\right)$ has exactly one solution on the interval $I=\left[x_0-h,x_0+h\right]$, where $h=\min\left\{a,\frac{b}{M}\right\}$ and $M=\max_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

**Equivalence Between the Integral Equation and the Initial Value Problem**

The initial value problem $\left(E\right)$ has a solution if and only if the integral equation $y=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$ has a solution.

**Uniform Boundedness and Equicontinuity**

Suppose a sequence of functions $f_1\left(x\right),f_2\left(x\right),\cdots$ is given on the interval $I$. If there exists a constant $K> 0$ such that $\left|f_n\left(x\right)\right|< K$ for all $n$, then the sequence is called uniformly bounded on $I$; if for every positive number $\varepsilon$ there exists $\delta=\delta\left(\varepsilon\right)$ such that whenever $\left|x_1-x_2\right|< \delta$ one has $\left|f_n\left(x_1\right)-f_n\left(x_2\right)\right|< \varepsilon$ for all $n$, then the sequence is called equicontinuous on $I$.

**Ascoli's Lemma**

If a sequence of functions is uniformly bounded and equicontinuous on a finite closed interval $I$, then one can select a subsequence that converges uniformly on $I$.

**Lemma 3.1** (Convergent Subsequence of the Euler Sequence)

The sequence of Euler broken lines $\left\{\rho_n\left(x\right)\right\}$ is uniformly bounded and equicontinuous on the interval $\left[x_0-h,x_0+h\right]$, and hence contains at least one uniformly convergent subsequence.

**Lemma 3.2** (Integral Relation for the Euler Broken Line)

The Euler broken line $y=\rho_n\left(x\right)$ satisfies on the interval $\left[x_0-h,x_0+h\right]$

$$
\rho_n\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,\rho_n\left(t\right)\right)\,dt+\delta_n\left(x\right),
$$

where $\lim_{n\to\infty}\delta_n\left(x\right)=0$ uniformly for $\left|x-x_0\right|\le h$.

**Theorem 3.3** (Peano's Existence Theorem)

Let the function $f\left(x,y\right)$ be continuous in the rectangular region $R$. Then the initial value problem

$$
\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0
$$

has at least one solution on the interval $\left[x_0-h,x_0+h\right]$, where the rectangular region $R$ and the positive number $h$ are defined as in **Theorem 3.1** (Picard's Existence and Uniqueness Theorem).

## 3.3 Continuation of Solutions

**Theorem 3.4** (Continuation Theorem for Solutions)

In the differential equation $\frac{dy}{dx}=f\left(x,y\right)$, let the function $f\left(x,y\right)$ be continuous in the open region $G$, and let $P_0\left(x_0,y_0\right)$ be any point in $G$. Then every integral curve through $P_0$ can be continued to the boundary of $G$: that is, for any bounded closed region $G_1$ ($P_0\in G_1\subset G$), the integral curve extends beyond $G_1$. In other words, if the maximal interval of existence of the solution $y=y\left(x\right)$ is $\left(\alpha,\beta\right)$, then when $\beta< +\infty$ the point $\left(x,y\left(x\right)\right)$ approaches the boundary of $G$ (when $G=\mathbb{R}^2$, this means $\left|y\right|\to+\infty$).

**Corollary** (Existence, Uniqueness and Continuation of Solutions Under a Local Lipschitz Condition)

Let $f\left(x,y\right)$ be continuous in the region $G$ and satisfy a local Lipschitz condition with respect to $y$ (i.e. every point of $G$ has a neighborhood contained in $G$ in which $f$ satisfies a Lipschitz condition with respect to $y$). Then through every point $P_0$ in $G$ there exists a unique integral curve of the differential equation, and it can be continued to the boundary of $G$.

**Theorem 3.5** (Global Existence of Solutions on a Strip)

Let the right-hand function of the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ be continuous in the strip

$$
S:\ \alpha< x< \beta,\ -\infty< y< +\infty
$$

and satisfy the inequality $\left|f\left(x,y\right)\right|\le A\left(x\right)\left|y\right|+B\left(x\right)$, where $A\left(x\right)\ge0$ and $B\left(x\right)\ge0$ are continuous on $\left(\alpha,\beta\right)$. Then every solution of the differential equation has $\left(\alpha,\beta\right)$ as its maximal interval of existence.

## 3.4 Comparison Theorems and Their Applications

**Theorem 3.1** (Picard's Existence and Uniqueness Theorem)

Consider the initial value problem $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, where $f\left(x,y\right)$ is continuous in the rectangular region

$$
R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b
$$

Then $h=\min\left\{a,\frac{b}{M}\right\}$, $M=\max_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

**Theorem 3.6** (First Comparison Theorem)

Let the functions $f\left(x,y\right)$ and $F\left(x,y\right)$ both be continuous in the plane region $G$ and satisfy $f\left(x,y\right)< F\left(x,y\right)$ ($\left(x,y\right)\in G$). Let $y=\varphi\left(x\right)$ and $y=\Phi\left(x\right)$ be, on the interval $\left(a,b\right)$, solutions of the initial value problems $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ and $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$, respectively, where $\left(x_0,y_0\right)\in G$. Then $\varphi\left(x\right)< \Phi\left(x\right)$ on $\left(x_0,b\right)$, while $\varphi\left(x\right)> \Phi\left(x\right)$ on $\left(a,x_0\right)$. Geometrically, a curve with smaller slope cannot cross from below to above a curve with larger slope as one moves to the right.

**Minimal Solution and Maximal Solution**

Let the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ be continuous in the rectangular region $R$. If on the interval $\left[x_0-h,x_0+h\right]$ there are two solutions $y=W\left(x\right)$ and $y=Z\left(x\right)$ such that every solution $y=y\left(x\right)$ of $\left(E\right)$ satisfies $W\left(x\right)\le y\left(x\right)\le Z\left(x\right)$, then $y=W\left(x\right)$ and $y=Z\left(x\right)$ are called the minimal solution and the maximal solution of $\left(E\right)$, respectively.

**Theorem 3.7** (Existence of the Minimal and Maximal Solutions)

There exists a positive number $\delta< h$ such that the initial value problem $\left(E\right)$ has a minimal solution and a maximal solution on the interval $\left[x_0-\delta,x_0+\delta\right]$. Construction method: for $\varepsilon> 0$, consider $\left(E_\varepsilon\right):\ \frac{dy}{dx}=f\left(x,y\right)\pm\varepsilon$, take its solutions by **Theorem 3.3** (Peano's Existence Theorem), and take the limit using **Ascoli's Lemma** to obtain the minimal and maximal solutions.

**Theorem 3.8** (Second Comparison Theorem)

Let the functions $f\left(x,y\right)$ and $F\left(x,y\right)$ both be continuous in the plane region $G$ and satisfy $f\left(x,y\right)\le F\left(x,y\right)$. Let $y=\varphi\left(x\right)$ and $y=\Phi\left(x\right)$ be, on $\left(a,b\right)$, solutions of $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ and $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$, respectively, where $y=\varphi\left(x\right)$ is the right-going minimal solution and left-going maximal solution of $\left(E_1\right)$, and $y=\Phi\left(x\right)$ is the right-going maximal solution and left-going minimal solution of $\left(E_2\right)$. Then $\varphi\left(x\right)\le\Phi\left(x\right)$ on $\left[x_0,b\right)$, while $\varphi\left(x\right)\ge\Phi\left(x\right)$ on $\left(a,x_0\right]$.

**Theorem 3.3** (Peano's Existence Theorem)

Let the function $f\left(x,y\right)$ be continuous in the rectangular region $R$. Then the initial value problem

$$
\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0
$$

has at least one solution on the interval $\left[x_0-h,x_0+h\right]$.

**Theorem 3.4** (Continuation Theorem for Solutions)

Let $f\left(x,y\right)$ be continuous in the open region $G$. Then the integral curve through every point in $G$ can be continued to the boundary of $G$.

## 4.1 First-Order Implicit Differential Equations

**First-Order Implicit Differential Equation**

As a supplement to the elementary integration methods in Chapter 2, this section discusses several special solution methods for the first-order implicit equation

$$
F\left(x,y,\frac{dy}{dx}\right)=0
$$

Here "implicit" means that the derivative $\frac{dy}{dx}$ of the unknown function is not expressed in advance as an explicit function of $x,y$.

**Differentiation Method**

Suppose the unknown function can be solved explicitly from the first-order implicit equation

$$
y=f\left(x,p\right),
$$

where $p=\frac{dy}{dx}$. Let the function $f\left(x,p\right)$ be continuously differentiable in $\left(x,p\right)$. Differentiating the above with respect to $x$ gives

$$
\left[f_x\left(x,p\right)-p\right]dx+f_p\left(x,p\right)dp=0.
$$

This is a first-order explicit differential equation in the variables $x$ and $p$. If its general solution $p=u\left(x,C\right)$ can be found, then the general solution of the original equation is $y=f\left(x,u\left(x,C\right)\right)$; if its general solution is easily written in the form $x=v\left(p,C\right)$, then the general solution of the original equation can be written as

$$
\begin{cases}x=v\left(p,C\right),\\y=f\left(v\left(p,C\right),p\right),\end{cases}
$$

where $p$ is regarded as a parameter.

**Parametric Method**

Suppose the differential equation does not explicitly contain the independent variable, i.e.

$$
F\left(y,p\right)=0.
$$

As a relation between $y$ and $p$, it generally represents several curves in the $Oyp$ plane. Let

$$
y=g\left(t\right),\quad p=h\left(t\right)
$$

be a parametric representation of one of them, with $h\left(t\right)\neq0$. From $dy=p\,dx$ one obtains $dx=\frac{g'\left(t\right)}{h\left(t\right)}dt$, and integrating gives the general solution of the original equation

$$
x=\int\frac{g'\left(t\right)}{h\left(t\right)}dt+C,\quad y=g\left(t\right).
$$

Similarly, for an equation not explicitly containing the unknown function $F\left(x,p\right)=0$, one may take the parametric representation $x=f\left(t\right),\ p=h\left(t\right)$; then from $dy=p\,dx$ one obtains $dy=h\left(t\right)f'\left(t\right)dt$, and the general solution is

$$
y=\int h\left(t\right)f'\left(t\right)dt+C,\quad x=f\left(t\right).
$$

## 4.2 Singular Solutions

**Definition 4.1** (Singular Solution)

Let the first-order differential equation

$$
F\left(x,y,\frac{dy}{dx}\right)=0
$$

have a particular solution $\Gamma:y=\varphi\left(x\right)$ ($x\in J$). If for every point $Q\in\Gamma$, in any neighborhood of $Q$ the equation has a solution different from $\Gamma$ that is tangent to $\Gamma$ at $Q$, then $\Gamma$ is called a singular solution of the differential equation.

**Theorem 4.1** (Necessary Condition for a Singular Solution, i.e. the $p$-Discriminant)

Let the function $F\left(x,y,p\right)$ be continuous for $\left(x,y,p\right)\in G$ and have continuous partial derivatives $F_y'$ and $F_p'$ with respect to $y$ and $p$. If the function $y=\varphi\left(x\right)$ ($x\in J$) is a singular solution of the differential equation and $\left(x,\varphi\left(x\right),\varphi'\left(x\right)\right)\in G$, then the singular solution $y=\varphi\left(x\right)$ satisfies the $p$-discriminant

$$
\begin{cases}F\left(x,y,p\right)=0,\\F_p'\left(x,y,p\right)=0,\end{cases}\quad\left(p=\frac{dy}{dx}\right).
$$

The curve determined by the equation obtained by eliminating $p$ from the $p$-discriminant is called a $p$-discriminant curve. A singular solution must be a $p$-discriminant curve. However, note that a function determined by the $p$-discriminant is not necessarily a solution, and even if it is a solution it is not necessarily a singular solution; it must still be verified according to **Definition 4.1** (Singular Solution).

**Theorem 4.2** (Sufficient Condition for a Singular Solution)

Let the function $F\left(x,y,p\right)$ be twice continuously differentiable for $\left(x,y,p\right)\in G$. Suppose the function $y=\psi\left(x\right)$ ($x\in J$) obtained by eliminating $p$ from the $p$-discriminant is a solution of the differential equation, and the conditions

$$
F_y'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0,\quad F_{pp}''\left(x,\psi\left(x\right),\psi'\left(x\right)\right)\neq0
$$

and

$$
F_p'\left(x,\psi\left(x\right),\psi'\left(x\right)\right)=0
$$

hold for $x\in J$. Then $y=\psi\left(x\right)$ is a singular solution of the differential equation.

## 4.3 Envelopes

**Definition 4.2** (Envelope)

Let there be a continuously differentiable curve $\Gamma$ in the plane. If for every point $q\in\Gamma$, in the one-parameter family of curves $K\left(C\right):V\left(x,y,C\right)=0$ there is a curve $K\left(C^*\right)$ passing through $q$ and tangent to $\Gamma$ at that point, and $K\left(C^*\right)$ is different from $\Gamma$ in any neighborhood of $q$, then the curve $\Gamma$ is called an envelope of this family of curves.

**Theorem 4.3** (An Envelope Is a Singular Solution)

Let the differential equation $F\left(x,y,\frac{dy}{dx}\right)=0$ have the general integral $U\left(x,y,C\right)=0$, and suppose this family of integral curves has an envelope $\Gamma:y=\varphi\left(x\right)$ ($x\in J$). Then the envelope $y=\varphi\left(x\right)$ is a singular solution of the differential equation. Hence finding the singular solution of a differential equation reduces to finding the envelope of its general integral.

**Theorem 4.4** (The Envelope Satisfies the $C$-Discriminant)

Let $\Gamma$ be an envelope of the family of curves $K\left(C\right):V\left(x,y,C\right)=0$, and suppose it can be represented as a smooth curve in the parameter $C$. Then it satisfies the $C$-discriminant

$$
\begin{cases}V\left(x,y,C\right)=0,\\V_C'\left(x,y,C\right)=0,\end{cases}
$$

or the relation $\Omega\left(x,y\right)=0$ obtained after eliminating $C$.

**Theorem 4.5** (The $C$-Discriminant Is a Sufficient Condition for an Envelope)

Suppose that from the $C$-discriminant of the family of curves $K\left(C\right):V\left(x,y,C\right)=0$ there is determined a continuously differentiable curve not contained in the family

$$
\Lambda:\begin{cases}x=\varphi\left(C\right),\\y=\psi\left(C\right),\end{cases}\quad\left(C\in J\right),
$$

and that it satisfies the nondegeneracy conditions

$$
\left(\varphi'\left(C\right),\psi'\left(C\right)\right)\neq\left(0,0\right),\quad\left(V_x',V_y'\right)\neq\left(0,0\right),
$$

then $\Lambda$ is an envelope of this family of curves.

## 5.1 Several Examples

**Autonomous (Stationary) Differential Equation**

There is a class of differential equations that do not explicitly contain the independent variable; these are called autonomous (or stationary) differential equations. They can be reduced in order. For example, for the second-order autonomous equation $y''=f\left(y,y'\right)$, set $z=\frac{dy}{dx}$; then $y''=\frac{dz}{dx}=\frac{dz}{dy}\cdot\frac{dy}{dx}=z\frac{dz}{dy}$, reducing it to the first-order equation in $z=z\left(y\right)$: $z\frac{dz}{dy}=f\left(y,z\right)$.

**First Integral**

The relation obtained by integrating a higher-order differential equation once (hence containing one arbitrary constant) is called a first integral. For example, for the autonomous equation $y''=f\left(y,y'\right)$, multiplying the equation by $y'$ makes the left-hand side exactly the total differential $\frac{d}{dx}\left[\frac{1}{2}\left(y'\right)^2-F\left(y\right)\right]$, where $F'\left(y\right)=-f\left(y,0\right)$ is the corresponding antiderivative; integrating directly gives a first integral.

**Phase Plane, Orbits and Phase Portrait**

For the second-order autonomous equation $\frac{d^2x}{dt^2}=f\left(x,\frac{dx}{dt}\right)$, on the phase plane $O\left(x,v\right)$ ($v=\frac{dx}{dt}$), the curve determined by the first integral $\frac{1}{2}v^2+V\left(x\right)=E$ is called an orbit; the distribution of orbits in the phase plane is called a phase portrait. Equilibrium points correspond to the zero solution (trivial solution) of the equation, and closed orbits represent periodic motion.

**The Simple Pendulum Equation and the Linear Simple Pendulum Equation**

The equation of motion of a simple pendulum is $\frac{d^2\theta}{dt^2}+a^2\sin\theta=0$, where the constant $a=\sqrt{\frac{g}{l}}$, $g$ is the magnitude of gravitational acceleration, and $l$ is the pendulum length. Taking the first-order approximation $\sin\theta\approx\theta$ of $\sin\theta$ gives the linear simple pendulum equation $\frac{d^2\theta}{dt^2}+a^2\theta=0$, whose general solution is $\theta=A\sin\left(at+D\right)$, where $A,D$ are arbitrary constants, and the period of oscillation is $T=\frac{2\pi}{a}=2\pi\sqrt{\frac{l}{g}}$.

## 5.2 Differential Equations in n-Dimensional Linear Space

**Standard System of Differential Equations and Vector Form**

Taking the number of unknown functions equal to the order of the differential equation, the resulting standard system is $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$ ($i=1,\cdots,n$). Using column vectors $y=\left(y_1,\cdots,y_n\right)^\top$, $f=\left(f_1,\cdots,f_n\right)^\top$, the vector form is $\frac{dy}{dx}=f\left(x,y\right)$, where $f\left(x,y\right)$ is continuous on the region $D\subset R^{n+1}$. Adding the initial condition $y\left(x_0\right)=y_0$ gives the Cauchy problem.

**The Norm of a Vector and Its Basic Properties**

In the $n$-dimensional linear space $R^n$ one can define the norm $\left|y\right|$ of a vector, for example the Euclidean norm $\left|y\right|=\sqrt{y_1^2+\cdots+y_n^2}$. Basic properties of the norm: for any $y,z\in R^n$, there is the triangle inequality $\left|y+z\right|\le\left|y\right|+\left|z\right|$. After introducing a norm, $R^n$ becomes an $n$-dimensional normed linear space, in which one can develop the corresponding calculus and notions such as uniform convergence.

**Lipschitz Condition**

Let the $n$-dimensional vector-valued function $f\left(x,y\right)$ be continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$. If there exists a constant $L\ge0$ such that for all $\left(x,y_1\right),\left(x,y_2\right)\in R$ one has $\left|f\left(x,y_1\right)-f\left(x,y_2\right)\right|\le L\left|y_1-y_2\right|$, then $f$ is said to satisfy a Lipschitz condition with respect to $y$ on $R$.

**Picard's Existence and Uniqueness Theorem** ($n$-Dimensional Vector Form)

Let $f\left(x,y\right)$ be continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfy a Lipschitz condition with respect to $y$. Set $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has a unique solution on the interval $\left|x-x_0\right|\le h$.

**Peano's Existence Theorem** ($n$-Dimensional Vector Form)

Let $f\left(x,y\right)$ be continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$. Set $M=\max_R\left|f\left(x,y\right)\right|$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has at least one solution on the interval $\left|x-x_0\right|\le h$ (uniqueness is not guaranteed).

**The Picard Sequence and Its Uniform Convergence Estimate**

The integral equation equivalent to the Cauchy problem is $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. Construct the Picard sequence $y_{k+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y_k\left(t\right)\right)dt$, $y_0\left(x\right)\equiv y_0$. By induction one proves $\left|y_{k+1}\left(x\right)-y_k\left(x\right)\right|\le\frac{ML^k\left|x-x_0\right|^{k+1}}{\left(k+1\right)!}$, which implies that the Picard sequence converges uniformly on $\left|x-x_0\right|\le h$.

**Ascoli's Lemma and Gronwall's Inequality**

Ascoli's lemma: a uniformly bounded and equicontinuous sequence of functions on a bounded closed interval always has a uniformly convergent subsequence. Gronwall's inequality: if the nonnegative continuous function $u\left(x\right)$ satisfies $u\left(x\right)\le A+L\displaystyle\int_{x_0}^{x}u\left(t\right)dt$, then $u\left(x\right)\le Ae^{L\left|x-x_0\right|}$.

**Weierstrass Test** (Uniform Convergence)

If the general term of the function series $\displaystyle\sum_{k=0}^{\infty}u_k\left(x\right)$ satisfies $\left|u_k\left(x\right)\right|\le M_k$ for all $x$, and the number series $\displaystyle\sum_{k=0}^{\infty}M_k$ converges, then the function series converges uniformly on the corresponding interval.

## 5.3 Continuous Dependence of Solutions on Initial Values and Parameters

**Theorem 5.1** (Continuous Dependence of Solutions on Parameters)

Let the $n$-dimensional vector-valued function $f\left(x,y,\lambda\right)$ be continuous on the region $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ and satisfy a Lipschitz condition with respect to $y$: $\left|f\left(x,y_1,\lambda\right)-f\left(x,y_2,\lambda\right)\right|\le L\left|y_1-y_2\right|$. Let $M$ be an upper bound of $\left|f\left(x,y,\lambda\right)\right|$ on $G$, and $h=\min\left\{a,\frac{b}{M}\right\}$. Then the solution $y=\varphi\left(x,\lambda\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ is continuous on the region $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$.

**Corollary of Theorem 5.1** (Continuous Dependence of Solutions on Initial Values)

Let the $n$-dimensional vector-valued function $f\left(x,y\right)$ be continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfy a Lipschitz condition with respect to $y$. Then the solution $y=\varphi\left(x,\eta\right)$ of the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ is continuous on the region $Q:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$, where $h=\min\left\{a,\frac{b}{M}\right\}$ and $M$ is an upper bound of $\left|f\left(x,y\right)\right|$ on $R$.

**Theorem 5.2** (Global Continuous Dependence of Solutions on Initial Values)

Let the $n$-dimensional vector-valued function $f\left(x,y\right)$ be continuous on the open region $G$ and satisfy a local Lipschitz condition with respect to $y$. Suppose $y=\xi\left(x\right)$ is a solution of $\frac{dy}{dx}=f\left(x,y\right)$, with interval of existence $J$. Take any bounded closed interval $\left[a,b\right]\subset J$. Then there exists a constant $\delta> 0$ such that for any initial value $\left(x_0,y_0\right)$ satisfying $a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$, the solution $y=\varphi\left(x;x_0,y_0\right)$ of the Cauchy problem exists at least on $\left[a,b\right]$ and on the closed region

$$
D_\delta:a\le x\le b,\ a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta
$$

is continuous.

**Equivalence Between the Integral Equation and the Cauchy Problem**

The Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ is equivalent to the integral equation $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. When a sequence of approximate solutions converges uniformly and $f$ is continuous, one may take the limit under the integral sign.

**Ascoli's Lemma**

A uniformly bounded and equicontinuous sequence of functions on a bounded closed interval always has a uniformly convergent subsequence.

## 5.4 Continuous Differentiability of Solutions with Respect to Initial Values and Parameters

**Theorem 5.3** (Continuous Differentiability of Solutions with Respect to Parameters)

Let the $n$-dimensional vector-valued function $f\left(x,y,\lambda\right)$ be continuous on the region $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ and have continuous partial derivatives with respect to $y$ and $\lambda$. Then the solution $y=\varphi\left(x,\lambda\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ is continuously differentiable on the region $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$, where $h=\min\left\{a,\frac{b}{M}\right\}$ and $M$ is an upper bound of $\left|f\left(x,y,\lambda\right)\right|$ on $G$.

**Corollary of Theorem 5.3** (Continuous Differentiability of Solutions with Respect to Initial Values)

Let the $n$-dimensional vector-valued function $f\left(x,y\right)$ be continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and have a continuous partial derivative $f_y\left(x,y\right)$ with respect to $y$. Then the solution $y=\varphi\left(x,\eta\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ is continuously differentiable on the region $D:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$.

**Variational Equation**

Let $y=\varphi\left(x;x_0,y_0,\lambda\right)$ be the solution of $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(x_0\right)=y_0$. The integral equation equivalent to the Cauchy problem is

$$
\varphi\left(x;x_0,y_0,\lambda\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(s,\varphi\left(s;x_0,y_0,\lambda\right),\lambda\right)ds.
$$

Set $A\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial y}\left(x,\varphi,\lambda\right)$, $B\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial\lambda}\left(x,\varphi,\lambda\right)$. Then $z=\frac{\partial\varphi}{\partial\lambda}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z+B\left(x,x_0,y_0,\lambda\right)$, $z\left(x_0\right)=0$; $z=\frac{\partial\varphi}{\partial y_0}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=1$; $z=\frac{\partial\varphi}{\partial x_0}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=-f\left(x_0,y_0,\lambda\right)$. These equations are collectively called the variational equations of the original equation with respect to the initial values and parameters.

**Jacobian Matrix**

The Jacobian matrix of the vector-valued function $f\left(x,y,\lambda\right)=\left(f_1,\cdots,f_n\right)^\top$ with respect to $y=\left(y_1,\cdots,y_n\right)^\top$ is $f_y=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$, and with respect to the parameter $\lambda=\left(\lambda_1,\cdots,\lambda_m\right)^\top$ is $f_\lambda=\left(\frac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. Differentiation of composite functions proceeds by matrix multiplication: $\frac{\partial f\left(x,\varphi,\lambda\right)}{\partial\lambda_k}=\displaystyle\sum_{j=1}^{n}\frac{\partial f}{\partial y_j}\frac{\partial\varphi_j}{\partial\lambda_k}+\frac{\partial f}{\partial\lambda_k}$.

## 6.1 General Theory

**Existence and Uniqueness Theorem** (Initial Value Problem for Linear Systems of Differential Equations)

The solution $y=y\left(x\right)$ of the linear system of differential equations $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ satisfying the initial condition $y\left(x_0\right)=y_0$ exists and is unique on the interval $\left(a,b\right)$, where $x_0\in\left(a,b\right)$ and $y_0\in\mathbb{R}^n$ are arbitrary prescribed values.

**Lemma 6.1** (Superposition Principle for Solutions of a Homogeneous Linear System)

Let $y=y_1\left(x\right)$ and $y=y_2\left(x\right)$ be solutions of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$. Then their linear combination $y=C_1y_1\left(x\right)+C_2y_2\left(x\right)$ is also a solution of the system, where $C_1$ and $C_2$ are arbitrary constants.

**Lemma 6.2** (Dimension of the Solution Space of a Homogeneous Linear System)

The linear space $S$ consisting of all solutions of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ on the interval $\left(a,b\right)$ is $n$-dimensional, where $n$ is the order of the system.

**Theorem 6.1** (Structure of the General Solution of a Homogeneous Linear System)

The homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ has $n$ linearly independent solutions $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$ on the interval $\left(a,b\right)$, and its general solution is

$$
y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right),
$$

where $C_1,C_2,\cdots,C_n$ are arbitrary constants. The $n$ linearly independent solutions of a homogeneous linear system are usually called a fundamental system of solutions.

**Lemma 6.3** (Liouville's Formula for the Wronskian Determinant)

Let $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ be $n$ solutions of a homogeneous linear system, with Wronskian determinant $W\left(x\right)$. Then

$$
W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^{x}\mathrm{tr}\left[A\left(s\right)\right]ds},
$$

where $x_0\in\left(a,b\right)$, and $\mathrm{tr}\left[A\left(x\right)\right]$ denotes the trace of the matrix $A\left(x\right)$.

**Theorem 6.2** (Wronskian Determinant Criterion)

The system of solutions $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ of the homogeneous linear system $\frac{dy}{dx}=A\left(x\right)y$ is linearly independent if and only if $W\left(x\right)\neq0\ \left(a< x< b\right)$.

**Corollary 2** (Properties of a Fundamental Matrix)

(1) Let $\Phi\left(x\right)$ be a fundamental matrix of the homogeneous linear system. Then for any nonsingular $n$-th order constant matrix $C$, the matrix $\Phi\left(x\right)C$ is also a fundamental matrix of the system. (2) Let $\Phi\left(x\right)$ and $\Psi\left(x\right)$ both be fundamental matrices of the system. Then there necessarily exists a nonsingular $n$-th order constant matrix $C$ such that $\Psi\left(x\right)=\Phi\left(x\right)C$.

**Lemma 6.4** (Structure of Solutions of a Nonhomogeneous Linear System)

If $\Phi\left(x\right)$ is a fundamental matrix of the homogeneous linear system corresponding to the nonhomogeneous linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$, and $y^*\left(x\right)$ is a particular solution of the nonhomogeneous system, then any solution $y=\varphi\left(x\right)$ of the nonhomogeneous system can be written as $\varphi\left(x\right)=\Phi\left(x\right)c+y^*\left(x\right)$, where $c$ is a constant column vector depending on $\varphi\left(x\right)$.

**Theorem 6.3** (Structure of the General Solution of a Nonhomogeneous Linear System)

Let $\Phi\left(x\right)$ be a fundamental matrix of the corresponding homogeneous linear system. Then the general solution of the nonhomogeneous linear system $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ on the interval $\left(a,b\right)$ can be written as $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^{x}\Phi^{-1}\left(s\right)f\left(s\right)ds$, where $c$ is an arbitrary $n$-dimensional constant column vector.

## 6.2 Linear Systems with Constant Coefficients

**Proposition 1** (Absolute Convergence of Matrix Power Series and the Definition of the Matrix Exponential)

For an $n$-th order real constant matrix $A$, the matrix power series

$$
E+A+\frac{1}{2!}A^2+\cdots+\frac{1}{k!}A^k+\cdots
$$

is absolutely convergent, and its sum is denoted by

$$
e^A=\sum_{k=0}^{\infty}\frac{1}{k!}A^k,
$$

and is called the exponential function of the matrix $A$, where $E$ is the $n$-th order identity matrix.

**Proposition 2** (Properties of the Matrix Exponential)

The matrix exponential has the following properties: (1) if the matrices $A$ and $B$ commute (i.e. $AB=BA$), then

$$
e^{A+B}=e^A e^B;
$$

(2) for any matrix $A$, the exponential $e^A$ is invertible, and

$$
\left(e^A\right)^{-1}=e^{-A};
$$

(3) if $P$ is a nonsingular $n$-th order matrix, then

$$
e^{PAP^{-1}}=Pe^AP^{-1}.
$$

**Theorem 6.4** (The Matrix Exponential Is the Standard Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System)

The matrix exponential

$$
\Phi\left(x\right)=e^{xA}
$$

is a standard fundamental matrix of the constant-coefficient homogeneous linear system

$$
\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}
$$

(i.e. the fundamental matrix $\Phi\left(x\right)$ satisfies $\Phi\left(0\right)=E$).

**Corollary 3** (General Solution and Initial Value Solution of a Constant-Coefficient Nonhomogeneous Linear System)

The general solution of the constant-coefficient nonhomogeneous linear system

$$
\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)
$$

on the interval $\left(a,b\right)$ is

$$
\boldsymbol{y}=e^{xA}\boldsymbol{c}+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,
$$

where $c$ is an arbitrary constant column vector; and the solution of the system satisfying the initial condition $y\left(x_0\right)=y_0$ is

$$
\boldsymbol{y}=e^{\left(x-x_0\right)A}\boldsymbol{y}_0+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,
$$

where $x_0\in\left(a,b\right)$.

**Lemma 6.6** (Necessary and Sufficient Condition for the System to Have an Exponential Nonzero Solution)

The constant-coefficient homogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ has a nonzero solution $y=e^{\lambda x}r$ if and only if $\lambda$ is an eigenvalue of the matrix $A$ and $\boldsymbol{r}$ is the eigenvector corresponding to $\lambda$, i.e. $\boldsymbol{r}$ satisfies the homogeneous linear algebraic system $\left(A-\lambda E\right)\boldsymbol{r}=\boldsymbol{0}$.

**Theorem 6.5** (Fundamental Matrix When There Are $n$ Distinct Eigenvalues)

Let the $n$-th order matrix $A$ have $n$ distinct eigenvalues $\lambda_1,\lambda_2,\cdots,\lambda_n$. Then the matrix function

$$
\Phi\left(x\right)=\left(e^{\lambda_1 x}\boldsymbol{r}_1,e^{\lambda_2 x}\boldsymbol{r}_2,\cdots,e^{\lambda_n x}\boldsymbol{r}_n\right)
$$

is a fundamental matrix of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$, where $r_i$ is the eigenvector of $A$ corresponding to $\lambda_i$.

**Lemma 6.7** (Method for Determining the Coefficients of the Vector Polynomial in the Case of Multiple Eigenvalues)

Let $\lambda_i$ be an eigenvalue of multiplicity $n_i$ of the matrix $A$. Then the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ has a nonzero solution of the form

$$
e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)
$$

if and only if $r_0$ is a nonzero solution of the homogeneous linear algebraic system $\left(A-\lambda_i E\right)^{n_i}\boldsymbol{r}=\boldsymbol{0}$, and $r_1,r_2,\cdots,r_{n_i-1}$ are determined successively by the relations

$$
\boldsymbol{r}_1=\left(A-\lambda_i E\right)\boldsymbol{r}_0,\ \boldsymbol{r}_2=\left(A-\lambda_i E\right)\boldsymbol{r}_1,\ \cdots,\ \boldsymbol{r}_{n_i-1}=\left(A-\lambda_i E\right)\boldsymbol{r}_{n_i-2}.
$$

**Theorem 6.6** (Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System in the Case of Multiple Eigenvalues)

Let the $n$-th order real constant matrix $A$ have, in the complex domain, distinct eigenvalues $\lambda_1,\lambda_2,\cdots,\lambda_s$ with corresponding multiplicities $n_1,n_2,\cdots,n_s$. Then every solution of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ is a linear combination of vector functions of the form

$$
e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)
$$

where $i=1,2,\cdots,s$.

**Remark 2** (Method for Extracting Real-Valued Solutions from Complex-Valued Solutions)

Let the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ have a complex-valued solution $\boldsymbol{y}_1=\boldsymbol{u}\left(x\right)+i\boldsymbol{v}\left(x\right)$, where $A$ is a real matrix. Then the conjugate $\boldsymbol{y}_2=\boldsymbol{u}\left(x\right)-i\boldsymbol{v}\left(x\right)$ of $\boldsymbol{y}_1$ is also a complex-valued solution of the system, and hence both the real part $\boldsymbol{u}\left(x\right)$ and the imaginary part $\boldsymbol{v}\left(x\right)$ of $\boldsymbol{y}_1$ are real-valued solutions of the system; that is, from a pair of conjugate complex-valued solutions one obtains two real-valued solutions.

## 6.3 Higher-Order Linear Differential Equations

**Theorem 6.1*** (Structure of Solutions of a Homogeneous Linear Differential Equation)

The homogeneous linear differential equation (6.47) has $n$ linearly independent solutions on the interval $\left(a,b\right)$. If these $n$ linearly independent solutions are $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$, then the general solution of equation (6.47) is

$$
y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right),
$$

where $C_1,C_2,\cdots,C_n$ are arbitrary constants. These $n$ linearly independent solutions are called a fundamental system of solutions.

**Theorem 6.2*** (Wronskian Criterion for Linear Independence of a Solution Set)

The solution set $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ of equation (6.47) is linearly independent if and only if its Wronskian determinant

$$
W\left(x\right)=\left|\begin{matrix}\varphi_1\left(x\right)&\cdots&\varphi_n\left(x\right)\\\varphi_1'\left(x\right)&\cdots&\varphi_n'\left(x\right)\\\vdots&&\vdots\\\varphi_1^{\left(n-1\right)}\left(x\right)&\cdots&\varphi_n^{\left(n-1\right)}\left(x\right)\end{matrix}\right|
$$

never vanishes on the interval $\left(a,b\right)$.

**Liouville's Formula** (Evolution Formula for the Wronskian Determinant (6.54))

If $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ is a solution set of equation (6.47), with Wronskian determinant $W\left(x\right)$, then

$$
W\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}a_1\left(s\right)ds}\quad\left(a< x< b\right),
$$

where $x_0\in\left(a,b\right)$, and $a_1\left(x\right)$ is the coefficient of the $y^{\left(n-1\right)}$ term in equation (6.47). In particular, for the second-order equation $y''+p\left(x\right)y'+q\left(x\right)y=0$ one has $a_1\left(x\right)=p\left(x\right)$.

**Example 1** (Formula for Constructing the General Solution from a Nonzero Solution (6.56))

Let $y=\varphi\left(x\right)$ be a nonzero solution of the second-order homogeneous linear differential equation $y''+p\left(x\right)y'+q\left(x\right)y=0$, where $p\left(x\right)$ and $q\left(x\right)$ are continuous functions on the interval $\left(a,b\right)$. Then on the subinterval where $\varphi\left(x\right)\neq0$, the general solution of the equation is

$$
y=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2\left(s\right)}e^{-\int_{x_0}^{s}p\left(t\right)dt}ds\right],
$$

where $C_1$ and $C_2$ are arbitrary constants.

**Theorem 6.3*** (General Solution Structure of a Nonhomogeneous Linear Differential Equation and the Method of Variation of Constants (6.57)(6.58))

Let $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ be a fundamental system of solutions of the homogeneous linear differential equation (6.47) on the interval $\left(a,b\right)$. Then the general solution of the nonhomogeneous linear differential equation (6.46) is

$$
y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)+\varphi^*\left(x\right),
$$

where

$$
\varphi^*\left(x\right)=\sum_{k=1}^{n}\varphi_k\left(x\right)\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds
$$

is a particular solution of equation (6.46), $W\left(x\right)$ is the Wronskian determinant of the fundamental system, and $W_k\left(x\right)$ is the cofactor of the element in the $n$-th row and $k$-th column of $W\left(x\right)$.

**Theorem 6.6*** (Characteristic Root Method for Constant-Coefficient Homogeneous Linear Differential Equations)

The characteristic equation of the constant-coefficient homogeneous linear differential equation $y^{\left(n\right)}+a_1y^{\left(n-1\right)}+\cdots+a_ny=0$ is

$$
\lambda^n+a_1\lambda^{n-1}+\cdots+a_{n-1}\lambda+a_n=0.
$$

Let the characteristic equation have, in the complex domain, a total of $s$ distinct roots $\lambda_1,\cdots,\lambda_s$ with corresponding multiplicities $n_1,\cdots,n_s$. Then the set of functions

$$
e^{\lambda_kx},\ xe^{\lambda_kx},\ \cdots,\ x^{n_k-1}e^{\lambda_kx}\ \left(k=1,\cdots,s\right)
$$

is a fundamental system of solutions. Complex roots occur in conjugate pairs; taking the real and imaginary parts of the complex-valued solutions gives the corresponding real-valued solutions.

**Method of Undetermined Coefficients** (Presetting the Form of the Particular Solution for Special Nonhomogeneous Terms)

When the nonhomogeneous term is $f\left(x\right)=P_m\left(x\right)e^{\mu x}$ (where $P_m\left(x\right)$ is a polynomial of degree $m$), if $\mu$ is not a characteristic root, set the particular solution $\varphi^*\left(x\right)=Q_m\left(x\right)e^{\mu x}$; if $\mu$ is a characteristic root of multiplicity $k$, then set

$$
\varphi^*\left(x\right)=x^kQ_m\left(x\right)e^{\mu x},
$$

where $Q_m\left(x\right)$ is a polynomial of degree $m$ with undetermined coefficients. When the nonhomogeneous term is

$$
f\left(x\right)=\left[A_m\left(x\right)\cos\beta x+B_l\left(x\right)\sin\beta x\right]e^{\alpha x}
$$

set

$$
\varphi^*\left(x\right)=x^k\left[C_n\left(x\right)\cos\beta x+D_n\left(x\right)\sin\beta x\right]e^{\alpha x},
$$

where $k$ is the multiplicity of $\alpha\pm i\beta$ as a characteristic root (take $k=0$ when it is not a characteristic root), $n=\max\left\{m,l\right\}$, and the coefficients of the polynomials $C_n\left(x\right),D_n\left(x\right)$ are undetermined.

**Existence and Uniqueness of the Solution to the Initial Value Problem**

The solution of an $n$-th order linear differential equation satisfying the initial conditions

$$
y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}
$$

exists and is unique on the common interval of continuity of the coefficients and the nonhomogeneous term. In particular, the initial value problem with all initial conditions taken to be zero has only the zero solution.

## 7.1 Cauchy's Theorem

**Majorant Series and Majorant Function**

Suppose there are two power series $\sum_{i,j=0}^{\infty}a_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j$ and $\sum_{i,j=0}^{\infty}A_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j\ \left(A_{ij}\ge0\right)$, where the coefficients $a_{ij}$ and $A_{ij}$ satisfy $\left|a_{ij}\right|\le A_{ij}\ \left(i,j=0,1,2,\cdots\right)$. Then the second power series is called a majorant series (or dominant series) of the first. If this majorant series is also convergent in the region $D:\left|x-x_0\right|< \alpha,\ \left|y-y_0\right|< \beta$, then its sum function $F\left(x,y\right)$ is called a majorant function (or dominant function) of the original power series in $D$.

**Theorem 7.1** (Cauchy's Theorem)

If the function $f\left(x,y\right)$ can be expanded, on the rectangular region $R:\left|x-x_0\right|< \alpha,\ \left|y-y_0\right|< \beta$, into a convergent power series in $\left(x-x_0\right)$ and $\left(y-y_0\right)$, then the initial value problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has an analytic solution $y=y\left(x\right)$ in the neighborhood $\left(x_0-\rho,x_0+\rho\right)$ of $x_0$, and it is unique. Here the coefficients of the formal solution are

$$
C_n=\frac{1}{n!}y^{\left(n\right)}\left(x_0\right)=P_n\left(a_{00},a_{01},a_{10},\cdots,a_{n-1,0}\right),
$$

where $P_n$ is a polynomial with positive coefficients in the various coefficients, depending only on the index $n$ and not on the function $f$.

**Remark 3** (Application of the Majorant Series Method to Systems of Differential Equations)

The majorant series method can be applied to systems of differential equations. Consider the initial value problem for a system

$$
\frac{dy_k}{dx}=f_k\left(x,y_1,\cdots,y_n\right),\ y_k\left(0\right)=0\ \left(k=1,2,\cdots,n\right).
$$

Suppose the right-hand functions can be expanded into convergent power series in the region $\left|x\right|\le\alpha,\ \left|y_1\right|\le\beta,\ \cdots,\ \left|y_n\right|\le\beta$. Then, analogously to Lemma 7.1, one proves the existence of a majorant function; using the same reasoning as in Theorem 7.1, it follows that the initial value problem has a convergent power series solution in some neighborhood of $x=0$.

## 7.2 Power Series Solution Method

**Ordinary Point and Singular Point**

Consider the second-order homogeneous linear differential equation $A\left(x\right)y''+B\left(x\right)y'+C\left(x\right)y=0$. If $A\left(x_0\right)\neq0$, then near $x_0$ one has $A\left(x\right)\neq0$, and the equation can be written as $y''+p\left(x\right)y'+q\left(x\right)y=0$, where

$$
p\left(x\right)=B\left(x\right)/A\left(x\right),\ q\left(x\right)=C\left(x\right)/A\left(x\right)
$$

are analytic near $x_0$. Such a point $x_0$ is called an ordinary point of the differential equation. If $A\left(x_0\right)=0$, then at least one of $p\left(x\right)$ and $q\left(x\right)$ is discontinuous at $x_0$, and $x_0$ is called a singular point of the differential equation.

**Theorem 7.2** (Existence and Recursion of Power Series Solutions in a Neighborhood of an Ordinary Point)

Let the coefficient functions $p\left(x\right)$ and $q\left(x\right)$ in the differential equation $y''+p\left(x\right)y'+q\left(x\right)y=0$ be expandable into a convergent power series in $\left(x-x_0\right)$ on the interval $\left(x_0-r,x_0+r\right)$. Then the equation has a convergent power series solution $y=\sum_{n=0}^{\infty}C_n\left(x-x_0\right)^n$ on the interval $\left(x_0-r,x_0+r\right)$, where $C_0$ and $C_1$ are two arbitrary constants (they may be determined by the initial conditions at $x_0$, i.e. $C_0=y_0$ and $C_1=y_0'$), and $C_n\ \left(n\ge2\right)$ can be determined successively from $C_0$ and $C_1$ by a recurrence formula.

## 7.3 Legendre Polynomials

**Legendre's Equation and Legendre Polynomials**

Legendre's equation is $\left(1-x^2\right)y''-2xy'+n\left(n+1\right)y=0$, where $n$ is a constant. When $n$ is a nonnegative integer, one solution of the equation is a polynomial of degree $n$, namely the Legendre polynomial $P_n\left(x\right)$, whose unified expression is $P_n\left(x\right)=\frac{1}{2^n}\sum_{k=0}^{\left[n/2\right]}\frac{\left(-1\right)^k\left(2n-2k\right)!}{k!\left(n-k\right)!\left(n-2k\right)!}x^{n-2k}$.

**Generating Function of Legendre Polynomials**

Let the function $G\left(x,t\right)=\left(1-2xt+t^2\right)^{-1/2}$. Then the power series expansion of $G\left(x,t\right)$ in $t$ is $G\left(x,t\right)=\sum_{n=0}^{\infty}P_n\left(x\right)t^n$, where $P_n\left(x\right)$ are Legendre polynomials. The function $G\left(x,t\right)$ is called the generating function of the Legendre polynomials. It satisfies the identity $\left(1-2xt+t^2\right)\frac{\partial G}{\partial t}=\left(x-t\right)G$.

## 8.2 Stability of Solutions

**Stability of Solutions** (Stability in the Sense of Lyapunov, Asymptotic Stability, Instability, and Global Asymptotic Stability)

Consider a solution $\boldsymbol{x} = \boldsymbol{\varphi}\left(t\right)$ of the equation $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}\left(t,\boldsymbol{x}\right)$. If for every given $\varepsilon >  0$ there exists $\delta = \delta\left(\varepsilon, t_0\right) >  0$ such that whenever $\left\|\boldsymbol{x}_0 - \boldsymbol{\varphi}\left(t_0\right)\right\| <  \delta$, the solution $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right)$ of the equation with initial value $\boldsymbol{x}\left(t_0\right) = \boldsymbol{x}_0$ is defined for $t \ge t_0$ and satisfies $\left\|\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right)\right\| <  \varepsilon$ for all $t \ge t_0$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is called stable (in the sense of Lyapunov). If the solution $\boldsymbol{\varphi}\left(t\right)$ is stable and there exists $\delta_0 >  0$ such that whenever $\left\|\boldsymbol{x}_0 - \boldsymbol{\varphi}\left(t_0\right)\right\| <  \delta_0$ one has $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right) \to \boldsymbol{0}\ \left(t \to +\infty\right)$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is called asymptotically stable. If the solution $\boldsymbol{\varphi}\left(t\right)$ is not stable, it is called unstable. If the basin of attraction is the whole space, i.e. regardless of the size of the initial value one has $\boldsymbol{x}\left(t, t_0, \boldsymbol{x}_0\right) - \boldsymbol{\varphi}\left(t\right) \to \boldsymbol{0}$, then the solution $\boldsymbol{\varphi}\left(t\right)$ is called globally asymptotically stable.

**Theorem 8.1** (Eigenvalue Criterion for the Stability of the Zero Solution of a Constant-Coefficient Linear System)

Let the matrix $A$ in the linear equation $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x}$ be constant. Then: (1) the zero solution is asymptotically stable if and only if all eigenvalues of $A$ have negative real part; (2) the zero solution is stable if and only if the real parts of all eigenvalues of $A$ are nonpositive, and the Jordan blocks corresponding to those eigenvalues with zero real part are all of order one; (3) the zero solution is unstable if and only if at least one eigenvalue of $A$ has positive real part, or at least one has zero real part and the corresponding Jordan block is of order higher than one.

**Theorem 8.3** (Determining Instability by Linear Approximation)

Let $A$ in the nonlinear equation $\frac{d\boldsymbol{x}}{dt} = A\boldsymbol{x} + \boldsymbol{N}\left(t,\boldsymbol{x}\right)$ be a constant matrix, and suppose at least one eigenvalue of $A$ has positive real part. Then the zero solution of the equation is unstable.

**Theorem 8.4** (Lyapunov's Stability Criterion)

Let the right-hand side of the autonomous system $\frac{d\boldsymbol{x}}{dt} = \boldsymbol{f}\left(\boldsymbol{x}\right)$ satisfy the existence and uniqueness conditions for solutions of the initial value problem, and suppose there exists a continuously differentiable scalar function $V\left(\boldsymbol{x}\right)$. Denote the total derivative of $V$ along an orbit with respect to $t$ by $\frac{dV}{dt} = \sum_{i=1}^{n}\frac{\partial V}{\partial x_i}f_i\left(\boldsymbol{x}\right)$. If condition $I$ holds ($V\left(\boldsymbol{0}\right) = 0,\ V\left(\boldsymbol{x}\right) >  0,\ \boldsymbol{x} \ne \boldsymbol{0}$; $V$ is called a positive definite function), then: (1) if in addition condition $II$ holds ($\frac{dV}{dt} <  0,\ \boldsymbol{x} \ne \boldsymbol{0}$, i.e. the total derivative is a negative definite function), the zero solution is asymptotically stable; (2) if in addition condition $II^*$ holds ($\frac{dV}{dt} \le 0$, i.e. the total derivative is a negative semidefinite function), the zero solution is stable; (3) if in addition condition $III$ holds ($\frac{dV}{dt} >  0,\ \boldsymbol{x} \ne \boldsymbol{0}$, i.e. the total derivative is a positive definite function), the zero solution is unstable.

## 8.3 Dynamical Systems in the Plane, Singular Points and Limit Cycles

**Elementary Singular Point** (and Higher-Order Singular Points)

Consider the linear system $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$ with singular point at $\left(0,0\right)$. When the matrix $A$ is nondegenerate (i.e. $A$ does not have zero as an eigenvalue), the point $\left(0,0\right)$ is called an elementary singular point of the system; otherwise it is called a higher-order singular point. Elementary singular points are all isolated, while linear higher-order singular points are all non-isolated.

**Special Direction**

As $t \to +\infty$ (or $-\infty$), some orbits may approach the singular point $\left(0,0\right)$ along a fixed line $y = kx$ (or $x = ky$); the direction of this line is called a special direction. A star node has infinitely many special directions, a two-way node and a saddle point have two special directions, a one-way node has one special direction, and a focus and a center have no special direction; moreover, when the line $y = kx$ gives a special direction of the linear system, the two rays into which the singular point divides this line are both orbits of the system.

**Theorem 8.5** (Classification of Elementary Singular Points)

For the linear system $\frac{d\boldsymbol{u}}{dt} = A\boldsymbol{u}$, set $p = -\text{tr}\left[A\right]$ (the negative of the trace of $A$) and $q = \det\left[A\right]$. Then: (1) when $q <  0$, $\left(0,0\right)$ is a saddle point; (2) when $q >  0$ and $p^2 >  4q$, $\left(0,0\right)$ is a two-way node; (3) when $q >  0$ and $p^2 = 4q$, $\left(0,0\right)$ is a one-way node or a star node; (4) when $q >  0$ and $0 <  p^2 <  4q$, $\left(0,0\right)$ is a focus; (5) when $q >  0$ and $p = 0$, $\left(0,0\right)$ is a center. Moreover, in cases (2) through (4), when $p >  0$ the singular point $\left(0,0\right)$ is stable, and when $p <  0$ it is unstable.

**Theorem 8.6** (A Nonlinear System Near an Elementary Singular Point Has the Same Qualitative Structure as the Linearized System)

Consider the nonlinear system

$$
\frac{dx}{dt} = ax + by + \varphi\left(x,y\right),\ \frac{dy}{dt} = cx + dy + \psi\left(x,y\right)
$$

with $\left(0,0\right)$ as an isolated singular point, whose linearized system $\frac{dx}{dt} = ax + by,\ \frac{dy}{dt} = cx + dy$ has $\left(0,0\right)$ as an elementary singular point, where $r = \sqrt{x^2 + y^2}$. Then: (1) if the linearized system has $\left(0,0\right)$ as a focus and condition $A$ holds ($\varphi\left(x,y\right) = o\left(r\right),\ \psi\left(x,y\right) = o\left(r\right),\ r \to 0$), then $\left(0,0\right)$ is also a focus of the original system, with the same stability; (2) if the linearized system has $\left(0,0\right)$ as a saddle point or two-way node and conditions $A$ and $B$ hold ($\varphi, \psi$ are continuously differentiable in $x, y$ in a small neighborhood of the origin), then $\left(0,0\right)$ is respectively a saddle point or two-way node of the original system, with the same stability; (3) if the linearized system has $\left(0,0\right)$ as a one-way node and condition $A^*$ holds ($\left|\varphi\right|/r$ and $\left|\psi\right|/r$ tend uniformly to zero as $r \to 0$), then $\left(0,0\right)$ is also a one-way node of the original system, with the same stability; (4) if the linearized system has $\left(0,0\right)$ as a star node and conditions $A^*$ and $B$ hold, then $\left(0,0\right)$ is also a star node of the original system, with the same stability.

## 10.2 Properties of First Integrals

**Theorem 10.1** (Necessary and Sufficient Condition for a First Integral)

Let the right-hand sides $f_1,\cdots,f_n$ of the system of differential equations $\frac{dy_i}{dx}=f_i\left(x,y_1,\cdots,y_n\right)$ ($i=1,\cdots,n$) be continuous in the region $G_1$ in $\left(x,y_1,\cdots,y_n\right)$ and continuously differentiable in $\left(y_1,\cdots,y_n\right)$. Let the function $\Phi\left(x,y_1,\cdots,y_n\right)$ be continuously differentiable in $G_1$. Then $\Phi\left(x,y_1,\cdots,y_n\right)=C$ is a first integral of the system in $G_1$ if and only if the identity

$$
\frac{\partial\Phi}{\partial x}+\frac{\partial\Phi}{\partial y_1}f_1+\cdots+\frac{\partial\Phi}{\partial y_n}f_n\equiv0
$$

holds in $G_1$.

**Theorem 10.2** (Knowing One First Integral Reduces the Order by One)

If one knows a first integral $\Phi\left(x,y_1,\cdots,y_n\right)=C$ of the system (10.17), then the order of the system can be reduced by one. The reason is that $\frac{\partial\Phi}{\partial y_1},\cdots,\frac{\partial\Phi}{\partial y_n}$ cannot all be zero; without loss of generality suppose $\frac{\partial\Phi}{\partial y_n}\neq0$, and then use the implicit function theorem to solve $y_n=g\left(x,y_1,\cdots,y_{n-1},C\right)$ from the first integral, and substitute back into the first $n-1$ equations of the original system to eliminate $y_n$.

**Mutually Independent First Integrals** (Nonzero Jacobian Determinant)

Let the system (10.17) have $k$ first integrals $V_i\left(x,y_1,\cdots,y_n\right)=C_i$ ($i=1,\cdots,k$). If in some region the matrix $\left(\frac{\partial V_i}{\partial y_j}\right)_{k\times n}$ has rank equal to $k$, i.e. without loss of generality the Jacobian determinant $\frac{D\left(V_1,\cdots,V_k\right)}{D\left(y_1,\cdots,y_k\right)}\neq0$, then they are called mutually independent in that region.

**Implicit Function Theorem**

If the function $F\left(x,y_1,\cdots,y_k\right)$ is continuously differentiable and $\frac{\partial F}{\partial y_k}\neq0$, then from the equation $F\left(x,y_1,\cdots,y_k\right)=0$ one can locally solve $y_k$ as a continuously differentiable function of the remaining variables.

## 10.4 Global First Integrals

**Theorem 10.7** (Global First Integrals and Conservative Systems)

For the three-dimensional autonomous system $\frac{dx}{dt}=E,\ \frac{dy}{dt}=F,\ \frac{dz}{dt}=G$, if it has two mutually independent stationary first integrals $\Phi_1=C_1,\ \Phi_2=C_2$ in the global region $\Omega$, then the system is a conservative system in $\Omega$ or equivalent to one. Derivation: from the necessary and sufficient condition for a first integral, $\frac{\partial\Phi_i}{\partial x}E+\frac{\partial\Phi_i}{\partial y}F+\frac{\partial\Phi_i}{\partial z}G\equiv0$, solve that $\left(E,F,G\right)$ is proportional to the Jacobian quantities

$$
L=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(y,z\right)},\ M=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(z,x\right)},\ N=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(x,y\right)}
$$

i.e. $L=\mu E,\ M=\mu F,\ N=\mu G$; then from the identity $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$ one obtains $\frac{\partial\left(\mu E\right)}{\partial x}+\frac{\partial\left(\mu F\right)}{\partial y}+\frac{\partial\left(\mu G\right)}{\partial z}\equiv0$.

**Divergence and Conservative Systems**

The divergence of the vector field $\left(E,F,G\right)$ is $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}$. When $\mu$ is constant, the above becomes $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}=0$, i.e. the divergence is zero, and the system is called a conservative system. When $\mu$ is not constant, $\mu\left(x,y,z\right)$ is called a quasi-integrating factor; in this case the original system, under the parameter transformation $d\tau=\frac{dt}{\mu}$, becomes the equivalent conservative system $\frac{dx}{d\tau}=\mu E,\ \frac{dy}{d\tau}=\mu F,\ \frac{dz}{d\tau}=\mu G$.

**The Exact Equation and Integrating Factor Theory of Chapter 2**

For the first-order equation in symmetric form $Pdx+Qdy=0$, it is an exact equation (i.e. there exists $\Phi$ such that $d\Phi=Pdx+Qdy$) if and only if $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$; when it is not exact, if there is a factor $\mu\left(x,y\right)$ such that $\mu Pdx+\mu Qdy=0$ becomes exact, then $\mu$ is called an integrating factor of the equation.

## 11.1 First-Order Homogeneous Linear Partial Differential Equations

**Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation)

Consider the first-order homogeneous linear partial differential equation $\sum_{i=1}^nA_i\left(x_1,\cdots,x_n\right)\frac{\partial u}{\partial x_i}=0$, where the coefficients $A_1,\cdots,A_n$ are continuously differentiable and not all zero. Its characteristic equations are the system of ordinary differential equations in symmetric form $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$, which is an $n-1$-th order system with $n-1$ independent first integrals $\varphi_i\left(x_1,\cdots,x_n\right)=C_i$ ($i=1,\cdots,n-1$). Then the general solution of the original partial differential equation is $u=\psi\left[\varphi_1,\cdots,\varphi_{n-1}\right]$, where $\psi$ is an arbitrary continuously differentiable function of $n-1$ variables. In other words, a function $\varphi$ is a first integral of the characteristic equations if and only if the identity $\sum_{i=1}^nA_i\frac{\partial\varphi}{\partial x_i}\equiv0$ holds.

## 11.2 First-Order Quasilinear Partial Differential Equations

**Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation)

Consider the first-order quasilinear partial differential equation

$$
X\left(x,y,z\right)\frac{\partial z}{\partial x}+Y\left(x,y,z\right)\frac{\partial z}{\partial y}=Z\left(x,y,z\right),
$$

where $X,Y,Z$ are continuously differentiable and $X,Y$ are not both zero. The corresponding characteristic equations are $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$. Let $u\left(x,y,z\right)=C_1,\ v\left(x,y,z\right)=C_2$ be two independent first integrals of these characteristic equations. Then the implicit general solution of the original quasilinear partial differential equation is $\Phi\left[u\left(x,y,z\right),v\left(x,y,z\right)\right]=0$, where $\Phi$ is an arbitrary continuously differentiable function, with the requirement that $\frac{\partial\Phi}{\partial z}\neq0$ so that $z=z\left(x,y\right)$ can be solved implicitly.

**Theorem 11.1** (General Solution of a Homogeneous Linear Partial Differential Equation)

The $n-1$ independent first integrals $\varphi_i=C_i$ of the characteristic equations $\frac{dx_1}{A_1}=\frac{dx_2}{A_2}=\cdots=\frac{dx_n}{A_n}$ give the general solution $u=\psi\left(\varphi_1,\cdots,\varphi_{n-1}\right)$ of the homogeneous linear equation $\sum_{i=1}^nA_i\frac{\partial u}{\partial x_i}=0$. The method of finding first integrals of the characteristic equations also applies to the case $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$ in Theorem 11.2.

## 11.3 Geometric Interpretation

**Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation and the Characteristic Curves)

The characteristic equations of the first-order quasilinear equation $X\frac{\partial z}{\partial x}+Y\frac{\partial z}{\partial y}=Z$ are $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$, whose integral curves are called characteristic curves; at each point they have the characteristic vector $\left(X,Y,Z\right)$ as their tangent vector. The integral surface $S$ determined by the solution $z=z\left(x,y\right)$ of the partial differential equation is woven from characteristic curves: the characteristic curve through every point of $S$ lies entirely on $S$.

**Method of Characteristics** (Solution Method for the Initial Value Problem)

Given the initial curve $\Lambda:\ x=\alpha\left(\sigma\right),\ y=\beta\left(\sigma\right),\ z=\gamma\left(\sigma\right)$. Suppose the characteristic equations have two independent first integrals $\varphi=C_1,\ \psi=C_2$. Take a point $M$ on $\Lambda$; the characteristic curve through $M$ is $\varphi=\overline{C}_1,\ \psi=\overline{C}_2$, where $\overline{C}_1=\varphi\left(\alpha,\beta,\gamma\right),\ \overline{C}_2=\psi\left(\alpha,\beta,\gamma\right)$. Eliminating the parameter $\sigma$ gives the relation $E\left(\overline{C}_1,\overline{C}_2\right)=0$ between $\overline{C}_1,\overline{C}_2$, and $E\left(\varphi\left(x,y,z\right),\psi\left(x,y,z\right)\right)=0$ is the desired integral surface.

**Remark on the Method of Characteristics** (The Solution Is Not Unique When the Initial Curve Is Itself a Characteristic Curve)

If the characteristic curves drawn through every point of the initial curve $\Lambda$ intersect $\Lambda$ transversely at the intersection points, then these characteristic curves form a unique smooth integral surface $z=z\left(x,y\right)$; but if the initial curve $\Lambda$ is itself a characteristic curve, then the characteristic curves through $\Lambda$ are just $\Lambda$ itself and cannot span a surface. In this case any integral surface containing $\Lambda$ is a solution of the initial value problem, i.e. a solution exists but is not unique.
