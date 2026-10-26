# Assignment 16

> **Theorem 5.1** (Continuous Dependence of Solutions on a Parameter)<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y,\lambda\right)$ is continuous on the region $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ and satisfies a Lipschitz condition with respect to $y$: $\left|f\left(x,y_1,\lambda\right)-f\left(x,y_2,\lambda\right)\right|\le L\left|y_1-y_2\right|$. Let $M$ be an upper bound of $\left|f\left(x,y,\lambda\right)\right|$ on $G$, $h=\min\left\{a,\frac{b}{M}\right\}$. Then the solution $y=\varphi\left(x,\lambda\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ is continuous on the region $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$.

> **Corollary to Theorem 5.1** (Continuous Dependence of Solutions on Initial Values)<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Then the solution $y=\varphi\left(x,\eta\right)$ of the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ is continuous on the region $Q:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$, where $h=\min\left\{a,\frac{b}{M}\right\}$, and $M$ is an upper bound of $\left|f\left(x,y\right)\right|$ on $R$.

> **Theorem 5.2** (Global Continuous Dependence of Solutions on Initial Values)<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y\right)$ is continuous on an open region $G$ and satisfies a local Lipschitz condition with respect to $y$. Suppose $y=\xi\left(x\right)$ is a solution of $\frac{dy}{dx}=f\left(x,y\right)$, with interval of existence $J$. Take any bounded closed interval $\left[a,b\right]\subset J$. Then there exists a constant $\delta> 0$ such that for any initial value $\left(x_0,y_0\right)$ satisfying $a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$, the solution $y=\varphi\left(x;x_0,y_0\right)$ of the Cauchy problem exists at least on $\left[a,b\right]$ and is continuous on the closed region $D_\delta:a\le x\le b,\ a\le x_0\le b,\ \left|y_0-\xi\left(x_0\right)\right|\le\delta$.

> **Equivalence Between the Integral Equation and the Cauchy Problem**<br>The Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ is equivalent to the integral equation $y\left(x\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(t,y\left(t\right)\right)dt$. When the sequence of approximate solutions converges uniformly and $f$ is continuous, one may take the limit under the integral sign.

> **Ascoli's Lemma**<br>A uniformly bounded and equicontinuous sequence of functions on a bounded closed interval always has a uniformly convergent subsequence.

### Problem 1

(Problem 5-3, Problem 2) Suppose $f\left(x,y\right)$ is continuous on the region $R$, and the integral curve of the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ through any interior point of $R$ is (in existence) unique. Then the solutions of the above differential equation depend continuously on the initial values. Here the region $R$ is defined as in **Corollary to Theorem 5.1** (Continuous Dependence of Solutions on Initial Values).

### Solution to Problem 1

Fix any interior point $\left(\overline{x}_0,\overline{y}_0\right)$ in $R$. We prove: as $\left(x_0,y_0\right)\to\left(\overline{x}_0,\overline{y}_0\right)$, the solution $y=\varphi\left(x;x_0,y_0\right)$ of the Cauchy problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ converges uniformly on some common interval to the solution $\overline{\varphi}\left(x\right)=\varphi\left(x;\overline{x}_0,\overline{y}_0\right)$.

Step 1: shrink the region so that $f$ is bounded. Since $\left(\overline{x}_0,\overline{y}_0\right)$ is an interior point of $R$, we may take a small bounded closed rectangle $R':\left|x-\overline{x}_0\right|\le a',\ \left|y-\overline{y}_0\right|\le b'$ contained in the interior of $R$. $f$ is continuous on the bounded closed region $R'$, hence bounded; denote $\left|f\left(x,y\right)\right|\le M$.

Step 2: take a sequence of initial values $\left(x_0^{\left(k\right)},y_0^{\left(k\right)}\right)\to\left(\overline{x}_0,\overline{y}_0\right)$. The solution sequence $\varphi_k\left(x\right)=\varphi\left(x;x_0^{\left(k\right)},y_0^{\left(k\right)}\right)$ satisfies the integral equation

$$
\varphi_k\left(x\right)=y_0^{\left(k\right)}+\int_{x_0^{\left(k\right)}}^{x}f\left(t,\varphi_k\left(t\right)\right)dt.
$$

By the **Equivalence Between the Integral Equation and the Cauchy Problem**, from $\left|f\right|\le M$ we get $\left|\varphi_k\left(x\right)-\overline{y}_0\right|\le\left|y_0^{\left(k\right)}-\overline{y}_0\right|+M\left|x-\overline{x}_0\right|$. Take $h> 0$ sufficiently small so that $Mh< \frac{b'}{2}$, and take $k$ sufficiently large so that $\left|y_0^{\left(k\right)}-\overline{y}_0\right|< \frac{b'}{2}$; then $\left|\varphi_k\left(x\right)-\overline{y}_0\right|< b'$, i.e. all $\varphi_k$ stay inside $R'$, and hence are defined on $\left[\overline{x}_0-h,\overline{x}_0+h\right]$.

Step 3: uniform boundedness and equicontinuity. Uniform boundedness follows from Step 2. Equicontinuity: for any $x,x'$ on this interval,

$$
\left|\varphi_k\left(x\right)-\varphi_k\left(x'\right)\right|=\left|\int_{x'}^{x}f\left(t,\varphi_k\left(t\right)\right)dt\right|\le M\left|x-x'\right|,
$$

which is independent of $k$, so the sequence is equicontinuous.

Step 4: by **Ascoli's Lemma**, there exists a subsequence $\varphi_{k_j}\left(x\right)$ converging uniformly on $\left[\overline{x}_0-h,\overline{x}_0+h\right]$ to some continuous function $\psi\left(x\right)$.

Step 5: prove that the limit $\psi$ satisfies the integral equation. In $\varphi_{k_j}\left(x\right)=y_0^{\left(k_j\right)}+\displaystyle\int_{x_0^{\left(k_j\right)}}^{x}f\left(t,\varphi_{k_j}\left(t\right)\right)dt$, let $j\to\infty$ on both sides. Since $f$ is uniformly continuous on $R'$ and $\varphi_{k_j}\rightrightarrows\psi$, we have $f\left(t,\varphi_{k_j}\left(t\right)\right)\rightrightarrows f\left(t,\psi\left(t\right)\right)$; also $x_0^{\left(k_j\right)}\to\overline{x}_0$, $y_0^{\left(k_j\right)}\to\overline{y}_0$, so

$$
\psi\left(x\right)=\overline{y}_0+\int_{\overline{x}_0}^{x}f\left(t,\psi\left(t\right)\right)dt.
$$

By the **Equivalence Between the Integral Equation and the Cauchy Problem**, $\psi\left(x\right)$ is the solution through $\left(\overline{x}_0,\overline{y}_0\right)$.

Step 6: use the uniqueness condition in the problem. The problem guarantees that the integral curve through $\left(\overline{x}_0,\overline{y}_0\right)$ is unique, so $\psi\left(x\right)=\overline{\varphi}\left(x\right)$. Hence every convergent subsequence of $\left\{\varphi_k\right\}$ converges uniformly to the same limit $\overline{\varphi}$; if the whole sequence did not converge uniformly to $\overline{\varphi}$, there would exist some $\varepsilon> 0$ and a subsequence with $\left|\varphi_{k_j}\left(x_j\right)-\overline{\varphi}\left(x_j\right)\right|\ge\varepsilon$, which by Ascoli's Lemma contains a convergent subsequence, a contradiction. Therefore $\varphi_k\rightrightarrows\overline{\varphi}$. By the arbitrariness of the sequence, the solutions depend continuously on the initial values.

$\blacksquare$

### Problem 2

(Problem 5-3, Problem 3) Give an example to show that if a differential equation does not satisfy the uniqueness condition for solutions, then its family of integral curves cannot be regarded as a family of parallel straight lines even locally.

### Solution to Problem 2

Counterexample: take the differential equation

$$
\frac{dy}{dx}=3y^{\frac{2}{3}},
$$

and discuss near the origin $\left(0,0\right)$.

First, its solutions are not unique. $y\equiv0$ is clearly a solution. Second, $y=\left(x-c\right)^3$ is also a solution: direct verification gives $y'=3\left(x-c\right)^2$, and $3y^{\frac{2}{3}}=3\left[\left(x-c\right)^3\right]^{\frac{2}{3}}=3\left(x-c\right)^2$, so $y'=3y^{\frac{2}{3}}$. Furthermore, for any constant $c\le0$, the piecewise function

$$
y\left(x\right)=\begin{cases}0,&x\le c,\\\left(x-c\right)^3,&x> c\end{cases}
$$

is continuous and continuously differentiable at $x=c$ (both the function values and derivatives on the left and right are $0$), and is still a solution of the equation. Letting $c$ range over all values in $\left(-\infty,0\right]$ gives infinitely many integral curves through $\left(0,0\right)$.

Second, see how solutions starting from nearby initial values collect. For the initial value $y\left(0\right)=\eta> 0$, the solution through $\left(0,\eta\right)$ is $\varphi\left(x;\eta\right)=\left(x+\eta^{\frac{1}{3}}\right)^3$. Letting $\eta\to0^{+}$, at a fixed $x> 0$, $\varphi\left(x;\eta\right)\to x^3$. That is: for the family of integral curves starting from initial values near the origin on the right side, the limit is the curve $y=x^3$ (a solution through and leaving the origin); whereas the solution starting from the origin itself may be $y\equiv0$. In other words, which curve is the limit depends on the direction and manner of approaching the origin; there is no uniquely determined limiting curve of nearby solutions.

Finally, explain why it cannot be locally regarded as a family of parallel straight lines. In **Corollary to Theorem 5.1** (Continuous Dependence of Solutions on Initial Values), the transformation $T:\left(x,\eta\right)\mapsto\left(x,\varphi\left(x,\eta\right)\right)$ that locally "straightens" the family of integral curves is a one-to-one topological map precisely because of the uniqueness of solutions: when $\eta_1\ne\eta_2$, $\varphi\left(x,\eta_1\right)\ne\varphi\left(x,\eta_2\right)$. In this counterexample, uniqueness fails: for any $x< 0$, the curve $\varphi\left(x;\eta\right)=\left(x+\eta^{\frac{1}{3}}\right)^3$ crosses the zero line $y=0$ when $\eta=\left(-x\right)^3< 0$, i.e. integral curves starting from different initial values $\eta$ cross each other near the origin; meanwhile, infinitely many curves crowd near the same starting point $\left(0,0\right)$. Hence $T$ is no longer a one-to-one map, and the family of integral curves fans out near the origin, so it cannot be locally regarded as a family of parallel straight lines.

$\blacksquare$
