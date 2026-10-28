# week18

> **Basic Knowledge: Existence and Uniqueness for Linear Systems**<br>Solution exists and is unique on the whole interval.

> **Lemma 6.1 (Superposition Principle)**<br>Linear combinations of homogeneous solutions are solutions.

> **Theorem 6.1 (General Solution of Homogeneous Systems)**<br>Linear combination of $n$ linearly independent solutions.

> **Lemma 6.2 (Dimension of Solution Space)**<br>The solution space is $n$-dimensional.

> **Theorem 6.2 (Wronskian Criterion)**<br>Linearly independent iff $W\ne0$.

> **Lemma 6.3 (Liouville's Formula for Wronskian)**<br>$W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^x\mathrm{tr}A\left(s\right)\mathrm ds}$.

> **Theorem 6.3 (General Solution of Nonhomogeneous Systems)**<br>$y=\Phi\left(x\right)c+\Phi\left(x\right)\int\Phi^{-1}f$.

> **Lemma 6.4 (Structure of Nonhomogeneous Solutions)**<br>Nonhomogeneous = homogeneous general + particular.
---

## 6-1 Problem 1(1)

Solve $y'=\begin{bmatrix}\frac1t&0\\0&\frac1t\end{bmatrix}y$.

### Solution 6-1 Problem 1(1)

$y_1=C_1t$, $y_2=C_2t$. $\blacksquare$

---

## 6-1 Problem 1(3)

Solve $y'=\begin{bmatrix}0&1\\-1&0\end{bmatrix}y$.

### Solution 6-1 Problem 1(3)

$y_1=C_1\cos t+C_2\sin t$, $y_2=-C_1\sin t+C_2\cos t$. $\blacksquare$

---

## 6-1 Problem 2(2)

Solve $x'=\frac{2t}{1+t^2}x$, $y'=-\frac1t y+x+t$, $x\left(1\right)=0$, $y\left(1\right)=\frac43$.

### Solution 6-1 Problem 2(2)

$x\equiv0$, $y=\frac{t^2}3+\frac1t$. $\blacksquare$

---

## 6-1 Problem 3

Prove the vector functions are linearly independent.

### Solution 6-1 Problem 3

Polynomial identity implies all coefficients zero. $\blacksquare$

---

## 6-1 Problem 4

Prove a fundamental matrix determines the system.

### Solution 6-1 Problem 4

By Theorem 6.2, $\Phi$ is invertible. $\blacksquare$

---

## 6-1 Problem 6

Prove exactly $n+1$ linearly independent nonhomogeneous solutions.

### Solution 6-1 Problem 6

By Lemma 6.4 and Lemma 6.2. $\blacksquare$
