# week4

> **Theorem 2.5 (Integrating Factor depending only on $y$)**
> 
> $\frac{Q_x-P_y}{P}=H\left(y\right)$ iff $\mu\left(y\right)=e^{\int H\mathrm dy}$.

> **Theorem 2.6 (Product of Integrating Factor and Function of $\Phi$)**
> 
> If $\mu$ is an IF, then $\mu g\left(\Phi\right)$ is also an IF.

> **Theorem 3.1 (Picard Existence and Uniqueness)**
> 
> Unique solution when Lipschitz.

> **Theorem 3.2 (Osgood Uniqueness)**
> 
> If $\int_0^{r_1}\frac{\mathrm dr}{F\left(r\right)}=\infty$, then uniqueness holds.

> **Lemma 3.2 (Euler Polygonal Integral Relation)**
> 
> $\rho_n=y_0+\int f\left(t,\rho_n\right)\mathrm dt+\delta_n$, $\delta_n\to0$.

> **Theorem 3.3 (Peano Existence Theorem)**
> 
> At least one solution.

## 2-4 Problem 4

Reduce $y''+py'+qy=0$ to a Riccati equation.

### Solution to 2-4 Problem 4

Set $z=\frac{y'}y$, then $z'=-z^2-pz-q$. $\blacksquare$

## 2-5 Problem 1(2)

Solve $y\mathrm dx+\left(2xy-e^{-2y}\right)\mathrm dy=0$.

### Solution to 2-5 Problem 1(2)

$xe^{2y}-\ln\left|y\right|=C$, plus $y\equiv0$. $\blacksquare$

## 2-5 Problem 1(4)

Solve $y\mathrm dx-\left(x^2+y^2+x\right)\mathrm dy=0$.

### Solution to 2-5 Problem 1(4)

$\arctan\frac xy=y+C$. $\blacksquare$

## 2-5 Problem 2

Prove the necessary and sufficient condition for $\mu=\mu\left(\varphi\right)$.

### Solution to 2-5 Problem 2

$\mu=e^{\int f\left(\varphi\right)\mathrm d\varphi}$. $\blacksquare$

## 2-5 Problem 4

Prove Theorem 2.6 and its converse.

### Solution to 2-5 Problem 4

By $d\Psi=\frac{\mu_1}{\mu}d\Phi$. $\blacksquare$

## 3-1 Problem 1

Discuss uniqueness for $y\left(0\right)=0$.

### Solution to 3-1 Problem 1

(1) $\alpha\ge1$ unique, $0< \alpha< 1$ not unique. (2) Zero solution is unique. $\blacksquare$

## 3-1 Problem 2

Compute Picard iterates for $y'=x+y+1$, $y\left(0\right)=0$.

### Solution to 3-1 Problem 2

$y=2e^x-x-2$. $\blacksquare$

## 3-2 Problem 3

Can Picard iterates prove Peano's theorem?

### Solution to 3-2 Problem 3

No. Because the error in Euler polygons vanishes uniformly, while Picard iterates may converge to different limits. $\blacksquare$

## 3-2 Problem 4

Prove Peano's theorem using Tonelli sequence.

### Solution to 3-2 Problem 4

By Ascoli's lemma and passing to the limit in the integral equation. $\blacksquare$
