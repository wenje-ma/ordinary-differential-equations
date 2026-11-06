# week9

> **Proposition 1 (Matrix Exponential)**
> 
> $e^A=\sum_{k=0}^\infty\frac1{k!}A^k$.

> **Example 1 (Reduction of Order)**
> 
> $y=\varphi\left(x\right)\left[C_1+C_2\int\frac1{\varphi^2}e^{-\int{p}}\mathrm{d}s\right]$.

> **Proposition 2 (Properties of Matrix Exponential)**
> 
> $e^{A+B}=e^Ae^B$; $\left(e^A\right)^{-1}=e^{-A}$.

> **Note 2 (Extracting Real Solutions)**
> 
> Real and imaginary parts of complex solutions are real solutions.

> **Corollary 3 (Nonhomogeneous Constant Coefficient Systems)**
> 
> $y=e^{xA}c+\int_{x_0}^xe^{\left(x-s\right)A}f\left(s\right)\mathrm{d}s$.

> **Theorem 6.4 ($e^{xA}$ is a Fundamental Matrix)**
> 
> $\Phi\left(x\right)=e^{xA}$ with $\Phi\left(0\right)=E$.

> **Theorem 6.5 (Distinct Eigenvalues)**
> 
> $\Phi\left(x\right)=\left(e^{\lambda_1x}r_1,\cdots,e^{\lambda_nx}r_n\right)$.

> **Lemma 6.6 (Exponential Solutions)**
> 
> $y=e^{\lambda{x}}r$ is a solution iff $\lambda$ is an eigenvalue.

> **Theorem 6.6 (Repeated Eigenvalue Case)**
> 
> Linear combinations of $e^{\lambda_ix}\left(r_0+xr_1+\cdots\right)$.

> **Lemma 6.7 (Repeated Eigenvalues)**
> 
> Solutions are $e^{\lambda{x}}\left(r_0+xr_1+\cdots\right)$.

## 6-2 Problem 3(4)

Solve the resonant IVP.

### Solution to 6-2 Problem 3(4)

$y=xe^{-x}\left(-2,-3,2\right)^{\top}$. $\blacksquare$

## 6-2 Problem 4

Solve the rotation system.

### Solution to 6-2 Problem 4

$C_1e^{at}\left(\cos{b}t,\sin{b}t\right)^{\top}+C_2e^{at}\left(\sin{b}t,-\cos{b}t\right)^{\top}$. $\blacksquare$

## 6-2 Problem 5

Prove solutions tend to zero iff all eigenvalues have negative real part.

### Solution to 6-2 Problem 5

By Theorem 6.6 and Lemma 6.6. $\blacksquare$

## 6-3 Problem 3

(1) Prove Wronskian is constant for $y''+qy=0$. (2) Find solution given $y=e^x$.

### Solution to 6-3 Problem 3

(1) By Liouville's formula. (2) $q=-1$, $y=C_1e^x+C_2e^{-x}$. $\blacksquare$

## 6-3 Problem 4

Prove zeros are simple and finite on compact intervals.

### Solution to 6-3 Problem 4

By uniqueness of IVP. $\blacksquare$

## 6-3 Problem 5

Prove coefficients are uniquely determined by a fundamental set.

### Solution to 6-3 Problem 5

By Wronskian criterion and Cramer's rule. $\blacksquare$

## 6-3 Problem 6

Prove Theorem 6.3* by variation of constants.

### Solution to 6-3 Problem 6

Set $y=\sum{C}_k\left(x\right)\varphi_k\left(x\right)$. $\blacksquare$
