# Assignment 8

> **Euler Broken Line**<br>Suppose the differential equation $\frac{dy}{dx}=f\left(x,y\right)$ is continuous in the rectangle $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$, let $M$ be an upper bound of $\left|f\left(x,y\right)\right|$ on $R$, and set $h=\min\left\{a,\frac{b}{M}\right\}$. Divide the interval $\left[x_0-h,x_0+h\right]$ into $2n$ equal parts; starting from the initial point $P_0\left(x_0,y_0\right)$, at each node draw a line segment in the direction of the line element there, obtaining a continuous broken line $y=\rho_n\left(x\right)$ staying inside the angular region $\left|y-y_0\right|\le M\left|x-x_0\right|$, called the Euler broken line of the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$.

> **Theorem 3.1** (Picard Existence and Uniqueness Theorem)<br>Consider the initial value problem $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, where $f\left(x,y\right)$ is continuous in the rectangle $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and satisfies a Lipschitz condition with respect to $y$. Then $\left(E\right)$ has one and only one solution on the interval $I=\left[x_0-h,x_0+h\right]$, where $h=\min\left\{a,\frac{b}{M}\right\}$, $M=\max\limits_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

> **Equivalence Between the Integral Equation and the Initial Value Problem**<br>The initial value problem $\left(E\right)$ has a solution if and only if the integral equation $y=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$ has a solution.

> **Uniform Boundedness and Equicontinuity**<br>Suppose a sequence of functions $f_1\left(x\right),f_2\left(x\right),\cdots$ is given on an interval $I$. If there exists a constant $K>0$ such that $\left|f_n\left(x\right)\right|<K$ for all $n$, the sequence is called uniformly bounded on $I$; if for any positive $\epsilon$, there exists $\delta=\delta\left(\epsilon\right)$ such that $\left|f_n\left(x_1\right)-f_n\left(x_2\right)\right|<\epsilon$ for all $n$ whenever $\left|x_1-x_2\right|<\delta$, the sequence is called equicontinuous on $I$.

> **Ascoli's Lemma**<br>If a sequence of functions is uniformly bounded and equicontinuous on a finite closed interval $I$, then one can select a subsequence that converges uniformly on $I$.

> **Lemma 3.1** (Convergent Subsequence of the Euler Sequence)<br>The sequence of Euler broken lines $\left\{\rho_n\left(x\right)\right\}$ is uniformly bounded and equicontinuous on the interval $\left[x_0-h,x_0+h\right]$, and hence contains at least one uniformly convergent subsequence.

> **Lemma 3.2** (Integral Relation for the Euler Broken Line)<br>The Euler broken line $y=\rho_n\left(x\right)$ satisfies $\rho_n\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,\rho_n\left(t\right)\right)\,dt+\delta_n\left(x\right)$ on the interval $\left[x_0-h,x_0+h\right]$, where $\lim\limits_{n\to\infty}\delta_n\left(x\right)=0$ uniformly for $\left|x-x_0\right|\le h$.

> **Theorem 3.3** (Peano Existence Theorem)<br>If the function $f\left(x,y\right)$ is continuous in the rectangle $R$, then the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has at least one solution on the interval $\left[x_0-h,x_0+h\right]$, where the rectangle $R$ and the positive number $h$ are defined as in **Theorem 3.1** (Picard Existence and Uniqueness Theorem).

### Problem 1

(Problem 3-2, Problem 3) We know that the Picard sequence satisfies the conditions of Ascoli's Lemma. Question: can the Picard sequence be used to prove the Peano existence theorem? Explain why.

### Solution to Problem 1

No. The reason is as follows.

The proof of the Peano existence theorem (see **Theorem 3.3** (Peano Existence Theorem)) works crucially because of **Lemma 3.2** (Integral Relation for the Euler Broken Line): the Euler broken lines $\rho_n$ satisfy

$$
\rho_n\left(x\right)=y_0+\int_{x_0}^x f\left(t,\rho_n\left(t\right)\right)\,dt+\delta_n\left(x\right),
$$

where the error term $\delta_n\left(x\right)$ tends uniformly to zero. Thus, taking the uniformly convergent subsequence $\rho_{n_k}\to\varphi$ obtained by **Ascoli's Lemma**, and letting $k\to\infty$ on both sides, the error term disappears, directly yielding $\varphi\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,\varphi\left(t\right)\right)\,dt$, i.e. $\varphi$ is a solution.

The Picard sequence is different. It satisfies the recursion $y_{n+1}\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt$, i.e. the two sides involve adjacent terms $y_{n+1}$ and $y_n$ of the sequence. With only continuity and no Lipschitz condition, even if **Ascoli's Lemma** gives $y_{n_k}\to\varphi$, the shifted subsequence $y_{n_k+1}$ is another subsequence, and the two may converge to different limits, so one cannot take the limit in the recursion simultaneously to obtain a fixed-point equation. The Miller counterexample in this section illustrates exactly this: its Picard sequence is $y_n\left(x\right)=\left(-1\right)^{n+1}x^2$, the even subsequence converges to $-x^2$, and the odd subsequence converges to $x^2$, neither of which is a solution of the initial value problem.

The root cause is that the proof of convergence of the Picard sequence relies on the Lipschitz condition to estimate the difference $\left|y_{n+1}-y_n\right|$ between adjacent terms, and then prove uniform convergence of the corresponding series (see the third step of the proof of **Theorem 3.1** (Picard Existence and Uniqueness Theorem)). The Peano theorem assumes only that $f$ is continuous, without this estimate, and the Picard sequence may fail to converge. Therefore the Picard sequence cannot be used to prove the Peano existence theorem. $\blacksquare$

### Problem 2

(Problem 3-2, Problem 4) For the integral equation equivalent to the initial value problem $\left(E\right)$: $y\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y\left(t\right)\right)\,dt$, construct a Tonelli sequence on the interval $I=\left[x_0,x_0+h\right]$ as follows: for any positive integer $n$, set $d_n=\frac{h}{n}$, $x_k=x_0+kd_n$ ($k=0,1,\cdots,n$); the points $x_0,x_1,\cdots,x_n\left(=x_0+h\right)$ divide $I$ into $n$ equal parts. Define the function $y_n\left(x\right)=\begin{cases}y_0,&x\in\left[x_0,x_1\right],\\ y_0+\displaystyle\int_{x_0}^{x-d_n}f\left(t,y_n\left(t\right)\right)\,dt,&x\in\left[x_1,x_0+h\right].\end{cases}$ Use the Tonelli sequence and Ascoli's Lemma to prove the Peano existence theorem (i.e. **Theorem 3.3** (Peano Existence Theorem)).

### Solution to Problem 2

The proof is in four steps.

Step 1: prove that $\left\{y_n\left(x\right)\right\}$ is uniformly bounded on $I$. On $\left[x_0,x_1\right]$, $y_n\equiv y_0$. On $\left[x_1,x_0+h\right]$, estimate by induction: suppose for $t\le x-d_n$ we already have $\left|y_n\left(t\right)-y_0\right|\le M\left(t-x_0\right)$, then

$$
\left|y_n\left(x\right)-y_0\right|\le\int_{x_0}^{x-d_n}\left|f\left(t,y_n\left(t\right)\right)\right|\,dt\le M\left(x-d_n-x_0\right)\le M\left(x-x_0\right)\le Mh\le b.
$$

Thus $\left|y_n\left(x\right)-y_0\right|\le b$ for all $n$ and $x\in I$, and the sequence is uniformly bounded.

Step 2: prove that $\left\{y_n\left(x\right)\right\}$ is equicontinuous. On $\left[x_1,x_0+h\right]$, almost everywhere $y_n'\left(x\right)=f\left(x-d_n,y_n\left(x-d_n\right)\right)$, so $\left|y_n'\left(x\right)\right|\le M$; on $\left[x_0,x_1\right]$, $y_n$ is constant. Hence for any $s,t\in I$, $\left|y_n\left(s\right)-y_n\left(t\right)\right|\le M\left|s-t\right|$, and the sequence is equicontinuous.

Step 3: by **Ascoli's Lemma**, the set $\left\{y_n\left(x\right)\right\}$ has a uniformly convergent subsequence $y_{n_k}\left(x\right)\to\varphi\left(x\right)$, and the limit function $\varphi$ is continuous on $I$.

Step 4: prove that $\varphi$ satisfies the integral equation. For $x\in\left[x_1,x_0+h\right]$, rewrite the upper limit $x-d_n$ as $x$, obtaining

$$
y_n\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,y_n\left(t\right)\right)\,dt-\int_{x-d_n}^{x}f\left(t,y_n\left(t\right)\right)\,dt.
$$

The second integral on the right has length $d_n$, and $\left|f\right|\le M$, so its absolute value is at most $Md_n$, which tends uniformly to zero as $n\to\infty$. That is, $y_n\left(x\right)=y_0+\displaystyle\int_{x_0}^x f\left(t,y_n\left(t\right)\right)\,dt+\epsilon_n\left(x\right)$, where $\epsilon_n\left(x\right)$ tends uniformly to zero. Along the subsequence, letting $k\to\infty$, by $y_{n_k}\to\varphi$ uniformly and the continuity of $f$, taking the limit under the integral sign gives

$$
\varphi\left(x\right)=y_0+\int_{x_0}^{x}f\left(t,\varphi\left(t\right)\right)\,dt.
$$

By the equivalence between the integral equation and the initial value problem, $y=\varphi\left(x\right)$ is a solution of $\left(E\right)$ on $I=\left[x_0,x_0+h\right]$. The leftward segment is proved analogously. This proves **Theorem 3.3** (Peano Existence Theorem) using the Tonelli sequence. $\blacksquare$
