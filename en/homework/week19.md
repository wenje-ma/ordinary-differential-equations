# week19

> **Proposition 1 (Matrix Exponential)**<br>$e^A=\sum_{k=0}^\infty\frac1{k!}A^k$.

> **Proposition 2 (Properties of Matrix Exponential)**<br>$e^{A+B}=e^Ae^B$; $(e^A)^{-1}=e^{-A}$.

> **Note 2 (Extracting Real Solutions)**<br>Real and imaginary parts of complex solutions are real solutions.

> **Corollary 3 (Nonhomogeneous Constant Coefficient Systems)**<br>$y=e^{xA}c+\int_{x_0}^x e^{(x-s)A}f(s)\mathrm ds$.

> **Theorem 6.4 ($e^{xA}$ is a Fundamental Matrix)**<br>$\Phi(x)=e^{xA}$ with $\Phi(0)=E$.

> **Theorem 6.5 (Distinct Eigenvalues)**<br>$\Phi(x)=(e^{\lambda_1 x}r_1,\cdots,e^{\lambda_n x}r_n)$.

> **Lemma 6.6 (Exponential Solutions)**<br>$y=e^{\lambda x}r$ is a solution iff $\lambda$ is an eigenvalue.

> **Theorem 6.6 (Repeated Eigenvalue Case)**<br>Linear combinations of $e^{\lambda_i x}(r_0+xr_1+\cdots)$.

> **Lemma 6.7 (Repeated Eigenvalues)**<br>Solutions are $e^{\lambda x}(r_0+xr_1+\cdots)$.
---

## 6-2 Problem 1(2)

Solve $y'=\begin{bmatrix}0&a\\-a&0\end{bmatrix}y$.

### Solution 6-2 Problem 1(2)

$C_1(\cos ax,-\sin ax)^\top+C_2(\sin ax,\cos ax)^\top$. $\blacksquare$

---

## 6-2 Problem 1(4)

Solve the 3x3 system with triple eigenvalue.

### Solution 6-2 Problem 1(4)

$C_1e^x(1,0,0)^\top+C_2e^x(0,1,1)^\top+C_3e^x[(0,1,0)^\top+x(\frac23,-\frac13,-\frac13)^\top]$. $\blacksquare$

---

## 6-2 Problem 2(2)

Solve the nonhomogeneous system.

### Solution 6-2 Problem 2(2)

Homogeneous + particular trigonometric solution. $\blacksquare$

---

## 6-2 Problem 2(4)

Solve the nonhomogeneous 3x3 system.

### Solution 6-2 Problem 2(4)

Homogeneous with eigenvalues $1,\pm i$ + particular $(-1,x,0)^\top$. $\blacksquare$

---

## 6-2 Problem 3(2)

Solve the IVP.

### Solution 6-2 Problem 3(2)

$y=\frac{13}4(\cos2x,\sin2x)^\top-3(\sin2x,-\cos2x)^\top+(-\frac54,\frac32x)^\top$. $\blacksquare$

---

## 6-2 Problem 3(4)

Solve the resonant IVP.

### Solution 6-2 Problem 3(4)

$y=xe^{-x}(-2,-3,2)^\top$. $\blacksquare$

---

## 6-2 Problem 4

Solve the rotation system.

### Solution 6-2 Problem 4

$C_1e^{at}(\cos bt,\sin bt)^\top+C_2e^{at}(\sin bt,-\cos bt)^\top$. $\blacksquare$

---

## 6-2 Problem 5

Prove solutions tend to zero iff all eigenvalues have negative real part.

### Solution 6-2 Problem 5

By Theorem 6.6 and Lemma 6.6. $\blacksquare$
