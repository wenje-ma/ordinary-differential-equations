# Assignment 22

> **Ordinary and Singular Points**<br>Consider the second-order homogeneous linear differential equation $A\left(x\right)y''+B\left(x\right)y'+C\left(x\right)y=0$. If $A\left(x_0\right)\neq0$, then $A\left(x\right)\neq0$ near $x_0$, and the equation can be written as $y''+p\left(x\right)y'+q\left(x\right)y=0$, where $p\left(x\right)=B\left(x\right)/A\left(x\right),\ q\left(x\right)=C\left(x\right)/A\left(x\right)$ are analytic near $x_0$. Such a point $x_0$ is called an ordinary point of the differential equation. If $A\left(x_0\right)=0$, then at least one of $p\left(x\right)$ and $q\left(x\right)$ is discontinuous at $x_0$, and $x_0$ is called a singular point of the differential equation.

> **Theorem 7.2** (Existence and Recursion of Power Series Solutions in a Neighborhood of an Ordinary Point)<br>Suppose the coefficient functions $p\left(x\right)$ and $q\left(x\right)$ in the differential equation $y''+p\left(x\right)y'+q\left(x\right)y=0$ can be expanded into convergent power series in $\left(x-x_0\right)$ on the interval $\left(x_0-r,x_0+r\right)$. Then the equation has a convergent power series solution $y=\sum_{n=0}^{\infty}C_n\left(x-x_0\right)^n$ on $\left(x_0-r,x_0+r\right)$, where $C_0$ and $C_1$ are two arbitrary constants (they can be determined by the initial conditions at $x_0$, i.e. $C_0=y_0$ and $C_1=y_0'$), and $C_n\ \left(n\ge2\right)$ can be determined successively from $C_0$ and $C_1$ by a recursion formula.

### Problem 1

(Problem 7-2, Problem 3) Solve the Hermite equation $y''-2xy'+\lambda y=0\ \left(-\infty< x< +\infty\right)$, where $\lambda$ is a constant.

### Solution to Problem 1

$x=0$ is an ordinary point of the equation (the coefficients are all polynomials). By **Theorem 7.2** (Existence and Recursion of Power Series Solutions in a Neighborhood of an Ordinary Point), assume the equation has a power series solution

$$
y=\sum_{n=0}^{\infty}a_nx^n.
$$

Differentiating term by term and adjusting the summation index gives

$$
y'=\sum_{n=0}^{\infty}\left(n+1\right)a_{n+1}x^n,\quad y''=\sum_{n=0}^{\infty}\left(n+2\right)\left(n+1\right)a_{n+2}x^n.
$$

Substituting into the equation $y''-2xy'+\lambda y=0$, where $-2xy'=-2\sum_{n=1}^{\infty}na_nx^n$, and comparing coefficients of $x^n$:

For $n=0$: $2a_2+\lambda a_0=0$, i.e. $a_2=-\frac{\lambda}{2}a_0$.

For $n\ge1$: $\left(n+2\right)\left(n+1\right)a_{n+2}-2na_n+\lambda a_n=0$, i.e. the recursion formula

$$
a_{n+2}=\frac{2n-\lambda}{\left(n+2\right)\left(n+1\right)}\,a_n\quad\left(n=0,1,2,\cdots\right).
$$

The recursion formula separates into even and odd terms. Write out the even and odd coefficients separately.

Even terms: $a_2=-\frac{\lambda}{2!}a_0,\ a_4=\frac{\left(-\lambda\right)\left(4-\lambda\right)}{4!}a_0,\ a_6=\frac{\left(-\lambda\right)\left(4-\lambda\right)\left(8-\lambda\right)}{6!}a_0$, and in general

$$
a_{2k}=\frac{\left(-\lambda\right)\left(4-\lambda\right)\left(8-\lambda\right)\cdots\left(4k-4-\lambda\right)}{\left(2k\right)!}\,a_0\quad\left(k\ge1\right).
$$

Odd terms: $a_3=\frac{2-\lambda}{3!}a_1,\ a_5=\frac{\left(2-\lambda\right)\left(6-\lambda\right)}{5!}a_1$, and in general

$$
a_{2k+1}=\frac{\left(2-\lambda\right)\left(6-\lambda\right)\left(10-\lambda\right)\cdots\left(4k-2-\lambda\right)}{\left(2k+1\right)!}\,a_1\quad\left(k\ge1\right).
$$

Therefore the general solution of the equation is

$$
y=a_0\left[1+\sum_{k=1}^{\infty}\frac{\left(-\lambda\right)\left(4-\lambda\right)\cdots\left(4k-4-\lambda\right)}{\left(2k\right)!}x^{2k}\right]+a_1\left[x+\sum_{k=1}^{\infty}\frac{\left(2-\lambda\right)\left(6-\lambda\right)\cdots\left(4k-2-\lambda\right)}{\left(2k+1\right)!}x^{2k+1}\right],
$$

where $a_0,a_1$ are arbitrary constants. By the ratio test, $\left|\frac{a_{n+2}}{a_n}\right|=\frac{\left|2n-\lambda\right|}{\left(n+2\right)\left(n+1\right)}\to0$, so both series converge for all $x$. $\blacksquare$

### Problem 2

(Problem 7-2, Problem 4) Find two linearly independent power series solutions of the differential equation $y''+\left(\sin x\right)y=0$ expanded at $x=0$.

### Solution to Problem 2

$x=0$ is an ordinary point of the equation ($\sin x$ is analytic near $x=0$). By **Theorem 7.2** (Existence and Recursion of Power Series Solutions in a Neighborhood of an Ordinary Point), assume

$$
y=\sum_{n=0}^{\infty}a_nx^n,\quad y''=\sum_{n=0}^{\infty}\left(n+2\right)\left(n+1\right)a_{n+2}x^n.
$$

Since $\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots$, the coefficient of $x^n$ in the product $\left(\sin x\right)y$ is $a_{n-1}-\frac{a_{n-3}}{3!}+\frac{a_{n-5}}{5!}-\cdots$ (where $a_{-1}=a_{-2}=0$). Substituting into the equation and comparing coefficients:

$$
n=0:\quad 2a_2=0,\quad a_2=0;;n=1:\quad 6a_3+a_0=0,\quad a_3=-\frac{a_0}{6};;n=2:\quad 12a_4+a_1=0,\quad a_4=-\frac{a_1}{12};;n=3:\quad 20a_5+a_2-\frac{a_0}{6}=0,\quad a_5=\frac{a_0}{120};;n=4:\quad 30a_6+a_3-\frac{a_1}{6}=0,\quad a_6=\frac{a_0}{180}+\frac{a_1}{180};;n=5:\quad 42a_7+a_4-\frac{a_2}{6}+\frac{a_0}{120}=0,\quad a_7=\frac{a_1}{504}-\frac{a_0}{5040}.
$$

Taking $a_0=1,\ a_1=0$ gives the first solution

$$
y_1=1-\frac{x^3}{6}+\frac{x^5}{120}+\frac{x^6}{180}-\frac{x^7}{5040}+\cdots.
$$

Taking $a_0=0,\ a_1=1$ gives the second solution

$$
y_2=x-\frac{x^4}{12}+\frac{x^6}{180}+\frac{x^7}{504}+\cdots.
$$

The two solutions correspond to the initial values $\left(y_1\left(0\right),y_1'\left(0\right)\right)=\left(1,0\right)$ and $\left(y_2\left(0\right),y_2'\left(0\right)\right)=\left(0,1\right)$ respectively; the Wronskian determinant at $x=0$ is $1$, so they are linearly independent. $\blacksquare$
