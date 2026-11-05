# week7

> **Theorem 5.1 (Continuous Dependence on Parameters)**
> 
> The solution depends continuously on parameters.

> **Corollary of 5.1 (Continuous Dependence on Initial Values)**
> 
> The solution depends continuously on initial values.

> **Theorem 5.2 (Global Continuous Dependence)**
> 
> On bounded intervals under local Lipschitz.

> **Theorem 5.3 (Differentiability with Respect to Parameters)**
> 
> The solution is differentiable.

> **Corollary of 5.3 (Differentiability with Respect to Initial Values)**
> 
> Differentiable in initial values.

> **Lemma 6.1 (Superposition Principle)**
> 
> Linear combinations of homogeneous solutions are solutions.

> **Theorem 6.1 (General Solution of Homogeneous Systems)**
> 
> Linear combination of $n$ linearly independent solutions.

> **Lemma 6.2 (Dimension of Solution Space)**
> 
> The solution space is $n$-dimensional.

> **Theorem 6.2 (Wronskian Criterion)**
> 
> Linearly independent iff $W\ne0$.

> **Lemma 6.3 (Liouville's Formula for Wronskian)**
> 
> $W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm{d}s}$.

> **Theorem 6.3 (General Solution of Nonhomogeneous Systems)**
> 
> $y=\Phi\left(x\right)c+\Phi\left(x\right)\int\Phi^{-1}f$.

> **Lemma 6.4 (Structure of Nonhomogeneous Solutions)**
> 
> Nonhomogeneous = homogeneous general + particular.

## 5-2 Problem 3

State and prove existence and uniqueness for linear systems.

### Solution to 5-2 Problem 3

$f=A\left(x\right)y+e\left(x\right)$ is locally Lipschitz; extend by Gronwall. $\blacksquare$

## 5-3 Problem 2

Prove: uniqueness implies continuous dependence on initial values.

### Solution to 5-3 Problem 2

By Ascoli lemma and uniqueness. $\blacksquare$

## 5-3 Problem 3

Show non-uniqueness breaks the parallel-lines analogy.

### Solution to 5-3 Problem 3

Counterexample: $y'=3y^{2/3}$. $\blacksquare$

## 5-4 Problem 1

Prove $z=\frac{\partial\varphi}{\partial\lambda}$ satisfies the variational equation.

### Solution to 5-4 Problem 1

By Theorem 5.3 and Jacobian differentiation. $\blacksquare$

## 5-4 Problem 2

Find the equation for $z=\frac{\partial\varphi}{\partial\eta}$.

### Solution to 5-4 Problem 2

$\frac{\mathrm{d}z}{\mathrm{d}x}=f_y\left(x,\varphi\right)z$, $z\left(x_0\right)=I_n$. $\blacksquare$

## 6-1 Problem 1(1)

Solve $y'=\begin{bmatrix}\frac1t&0\\0&\frac1t\end{bmatrix}y$.

### Solution to 6-1 Problem 1(1)

$y_1=C_1t$, $y_2=C_2t$. $\blacksquare$

## 6-1 Problem 1(3)

Solve $y'=\begin{bmatrix}0&1\\-1&0\end{bmatrix}y$.

### Solution to 6-1 Problem 1(3)

$y_1=C_1\cos{t}+C_2\sin{t}$, $y_2=-C_1\sin{t}+C_2\cos{t}$. $\blacksquare$

## 6-1 Problem 2(2)

Solve $x'=\frac{2t}{1+t^2}x$, $y'=-\frac1ty+x+t$, $x\left(1\right)=0$, $y\left(1\right)=\frac43$.

### Solution to 6-1 Problem 2(2)

$x\equiv0$, $y=\frac{t^2}3+\frac1t$. $\blacksquare$

## 6-1 Problem 3

Prove the vector functions are linearly independent.

### Solution to 6-1 Problem 3

Polynomial identity implies all coefficients zero. $\blacksquare$
