# week8

> **Proposition 1 (Matrix Exponential)**
> 
> $e^A=\sum_{k=0}^\infty\frac1{k!}A^k$.

> **Proposition 2 (Properties of Matrix Exponential)**
> 
> $e^{A+B}=e^Ae^B$; $\left(e^A\right)^{-1}=e^{-A}$.

> **Note 2 (Extracting Real Solutions)**
> 
> Real and imaginary parts of complex solutions are real solutions.

> **Corollary 3 (Nonhomogeneous Constant Coefficient Systems)**
> 
> $y=e^{xA}c+\int_{x_0}^x e^{\left(x-s\right)A}f\left(s\right)\mathrm ds$.

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
> $W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm ds}$.

> **Theorem 6.3 (General Solution of Nonhomogeneous Systems)**
> 
> $y=\Phi\left(x\right)c+\Phi\left(x\right)\int\Phi^{-1}f$.

> **Lemma 6.4 (Structure of Nonhomogeneous Solutions)**
> 
> Nonhomogeneous = homogeneous general + particular.

> **Theorem 6.4 ($e^{xA}$ is a Fundamental Matrix)**
> 
> $\Phi\left(x\right)=e^{xA}$ with $\Phi\left(0\right)=E$.

> **Theorem 6.5 (Distinct Eigenvalues)**
> 
> $\Phi\left(x\right)=\left(e^{\lambda_1 x}r_1,\cdots,e^{\lambda_n x}r_n\right)$.

> **Lemma 6.6 (Exponential Solutions)**
> 
> $y=e^{\lambda x}r$ is a solution iff $\lambda$ is an eigenvalue.

> **Theorem 6.6 (Repeated Eigenvalue Case)**
> 
> Linear combinations of $e^{\lambda_i x}\left(r_0+xr_1+\cdots\right)$.

> **Lemma 6.7 (Repeated Eigenvalues)**
> 
> Solutions are $e^{\lambda x}\left(r_0+xr_1+\cdots\right)$.

## 6-1 Problem 4

Prove a fundamental matrix determines the system.

### Solution to 6-1 Problem 4

By Theorem 6.2, $\Phi$ is invertible. $\blacksquare$

## 6-1 Problem 6

Prove exactly $n+1$ linearly independent nonhomogeneous solutions.

### Solution to 6-1 Problem 6

By Lemma 6.4 and Lemma 6.2. $\blacksquare$

## 6-2 Problem 1(2)

Solve $y'=\begin{bmatrix}0&a\\-a&0\end{bmatrix}y$.

### Solution to 6-2 Problem 1(2)

$C_1\left(\cos ax,-\sin ax\right)^\top+C_2\left(\sin ax,\cos ax\right)^\top$. $\blacksquare$

## 6-2 Problem 1(4)

Solve the 3x3 system with triple eigenvalue.

### Solution to 6-2 Problem 1(4)

$C_1e^x\left(1,0,0\right)^\top+C_2e^x\left(0,1,1\right)^\top+C_3e^x\left[\left(0,1,0\right)^\top+x\left(\frac23,-\frac13,-\frac13\right)^\top\right]$. $\blacksquare$

## 6-2 Problem 2(2)

Solve the nonhomogeneous system.

### Solution to 6-2 Problem 2(2)

Homogeneous + particular trigonometric solution. $\blacksquare$

## 6-2 Problem 2(4)

Solve the nonhomogeneous 3x3 system.

### Solution to 6-2 Problem 2(4)

Homogeneous with eigenvalues $1,\pm i$ + particular $\left(-1,x,0\right)^\top$. $\blacksquare$

## 6-2 Problem 3(2)

Solve the IVP.

### Solution to 6-2 Problem 3(2)

$y=\frac{13}4\left(\cos2x,\sin2x\right)^\top-3\left(\sin2x,-\cos2x\right)^\top+\left(-\frac54,\frac32x\right)^\top$. $\blacksquare$
