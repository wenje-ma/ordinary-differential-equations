# week8

> **Basic Knowledge: Integral Equation Equivalence**
> 
> $y=y_0+\int_{x_0}^x f\left(t,y\left(t\right)\right)\mathrm dt$.

> **Basic Knowledge: Ascoli Lemma**
> 
> Uniformly bounded and equicontinuous sequence has uniformly convergent subsequence.

> **Theorem 3.1 (Picard Existence and Uniqueness)**
> 
> Unique solution when Lipschitz.

> **Lemma 3.2 (Euler Polygonal Integral Relation)**
> 
> $\rho_n=y_0+\int f\left(t,\rho_n\right)\mathrm dt+\delta_n$, $\delta_n\to0$.

> **Theorem 3.3 (Peano Existence Theorem)**
> 
> At least one solution when $f$ is continuous.

---

## 3-2 Problem 3

Can Picard iterates prove Peano's theorem?

### Solution 3-2 Problem 3

No. Because the error in Euler polygons vanishes uniformly, while Picard iterates may converge to different limits. $\blacksquare$

---

## 3-2 Problem 4

Prove Peano's theorem using Tonelli sequence.

### Solution 3-2 Problem 4

By Ascoli's lemma and passing to the limit in the integral equation. $\blacksquare$
