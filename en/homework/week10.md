# Assignment 10

> **Theorem 3.1** (Picard Existence and Uniqueness Theorem)<br>Consider the initial value problem $\left(E\right)$: $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$, where $f\left(x,y\right)$ is continuous in the rectangle $R:\ \left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$. Then $h=\min\left\{a,\frac{b}{M}\right\}$, $M=\max\limits_{\left(x,y\right)\in R}\left|f\left(x,y\right)\right|$.

> **Theorem 3.6** (First Comparison Theorem)<br>Suppose both functions $f\left(x,y\right)$ and $F\left(x,y\right)$ are continuous in a plane region $G$ and satisfy the inequality $f\left(x,y\right)< F\left(x,y\right)$ ($\left(x,y\right)\in G$); suppose $y=\varphi\left(x\right)$ and $y=\Phi\left(x\right)$ are solutions on the interval $\left(a,b\right)$ of the initial value problems $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ and $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$, respectively, where $\left(x_0,y_0\right)\in G$. Then $\varphi\left(x\right)< \Phi\left(x\right)$ on $\left(x_0,b\right)$, and $\varphi\left(x\right)> \Phi\left(x\right)$ on $\left(a,x_0\right)$. Geometrically: a curve with smaller slope cannot cross from below a curve with larger slope to above as it moves to the right.

> **Minimal and Maximal Solutions**<br>Suppose the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ is continuous in the rectangle $R$. If on the interval $\left[x_0-h,x_0+h\right]$ there are two solutions $y=W\left(x\right)$ and $y=Z\left(x\right)$ such that every solution $y=y\left(x\right)$ of $\left(E\right)$ satisfies $W\left(x\right)\le y\left(x\right)\le Z\left(x\right)$, then $y=W\left(x\right)$ and $y=Z\left(x\right)$ are called the minimal and maximal solutions of $\left(E\right)$, respectively.

> **Theorem 3.7** (Existence of Minimal and Maximal Solutions)<br>There exists a positive number $\delta< h$ such that the initial value problem $\left(E\right)$ has a minimal solution and a maximal solution on the interval $\left[x_0-\delta,x_0+\delta\right]$. Construction: for $\varepsilon> 0$, consider $\left(E_\varepsilon\right):\ \frac{dy}{dx}=f\left(x,y\right)\pm\varepsilon$, take its solutions by **Theorem 3.3** (Peano Existence Theorem), and take the limit using **Ascoli's Lemma** to obtain the minimal and maximal solutions.

> **Theorem 3.8** (Second Comparison Theorem)<br>Suppose both functions $f\left(x,y\right)$ and $F\left(x,y\right)$ are continuous in a plane region $G$ and satisfy $f\left(x,y\right)\le F\left(x,y\right)$; suppose $y=\varphi\left(x\right)$ and $y=\Phi\left(x\right)$ are solutions on $\left(a,b\right)$ of $\left(E_1\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ and $\left(E_2\right):\ \frac{dy}{dx}=F\left(x,y\right),\ y\left(x_0\right)=y_0$, respectively, where $y=\varphi\left(x\right)$ is the rightward minimal and leftward maximal solution of $\left(E_1\right)$, and $y=\Phi\left(x\right)$ is the rightward maximal and leftward minimal solution of $\left(E_2\right)$. Then $\varphi\left(x\right)\le\Phi\left(x\right)$ on $\left[x_0,b\right)$, and $\varphi\left(x\right)\ge\Phi\left(x\right)$ on $\left(a,x_0\right]$.

> **Theorem 3.3** (Peano Existence Theorem)<br>If the function $f\left(x,y\right)$ is continuous in the rectangle $R$, then the initial value problem $\left(E\right):\ \frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ has at least one solution on the interval $\left[x_0-h,x_0+h\right]$.

> **Theorem 3.4** (Extension Theorem for Solutions)<br>If $f\left(x,y\right)$ is continuous in an open region $G$, then the integral curve through any point in $G$ extends to the boundary within $G$.

### Problem 1

(Problem 3-4, Problem 1) Let the initial value problem $\left(E\right)$, the rectangle $R$, and the positive number $h$ be as in **Theorem 3.1** (Picard Existence and Uniqueness Theorem). Prove that between the minimal solution $y=W\left(x\right)$ and the maximal solution $y=Z\left(x\right)$ of $\left(E\right)$ there lie all other solutions of $\left(E\right)$: that is, for any point $\left(x_1,y_1\right)$ with $\left|x_1-x_0\right|\le h,\ W\left(x_1\right)\le y_1\le Z\left(x_1\right)$, there is at least one solution $y=u\left(x\right)$ of $\left(E\right)$ on $\left[x_0-h,x_0+h\right]$ satisfying $u\left(x_1\right)=y_1$.

### Solution to Problem 1

By **Theorem 3.3** (Peano Existence Theorem), the initial value problem with initial value $\left(x_1,y_1\right)$ has a local solution near $x_1$. Then by **Theorem 3.7** (Existence of Minimal and Maximal Solutions), take the maximal solution $y=u\left(x\right)$ through $\left(x_1,y_1\right)$. Below we prove that it lies between $W$ and $Z$ and extends to the whole interval.

First prove the rightward segment $x\in\left[x_1,x_0+h\right]$. We know $u\left(x_1\right)=y_1\le Z\left(x_1\right)$, and $u$ and $Z$ satisfy the same equation $y'=f\left(x,y\right)$. Suppose for contradiction that $u$ exceeds $Z$ at some point; by continuity there is a first contact point $\beta> x_1$ with $u\left(\beta\right)=Z\left(\beta\right)$ and $u< Z$ on $\left(x_1,\beta\right)$. At this contact point the derivatives are equal, i.e. $u'\left(\beta\right)=f\left(\beta,u\left(\beta\right)\right)=f\left(\beta,Z\left(\beta\right)\right)=Z'\left(\beta\right)$, so the curves cannot cross there. This contradicts what **Theorem 3.6** (First Comparison Theorem) reveals: two integral curves of the same right-hand side, once in contact, cannot cross. Hence $u\left(x\right)\le Z\left(x\right)$. Similarly, from $u\left(x_1\right)=y_1\ge W\left(x_1\right)$ we get $u\left(x\right)\ge W\left(x\right)$. Therefore on the rightward segment $W\left(x\right)\le u\left(x\right)\le Z\left(x\right)$.

Since $u$ always stays in the bounded strip $W\le u\le Z$ inside the rectangle $R$, by **Theorem 3.4** (Extension Theorem for Solutions), it can extend to the right to the boundary of $R$, namely $x_0+h$. The leftward segment $x\in\left[x_0-h,x_1\right]$ is entirely analogous, giving $W\left(x\right)\le u\left(x\right)\le Z\left(x\right)$ extending to $x_0-h$.

Thus $y=u\left(x\right)$ is a solution of $\left(E\right)$ on $\left[x_0-h,x_0+h\right]$, with $u\left(x_1\right)=y_1$. $\blacksquare$

### Problem 2

(Problem 3-4, Problem 2) Prove **Theorem 3.8** (Second Comparison Theorem).

### Solution to Problem 2

Let $f\left(x,y\right)\le F\left(x,y\right)$ hold in $G$. The proof is in left and right segments.

First prove the rightward segment $x\in\left[x_0,b\right)$, i.e. prove $\varphi\left(x\right)\le\Phi\left(x\right)$. For any $\varepsilon> 0$, consider the perturbed equation $\left(E_{1,\varepsilon}\right):\ \frac{dy}{dx}=f\left(x,y\right)-\varepsilon,\ y\left(x_0\right)=y_0$. By **Theorem 3.3** (Peano Existence Theorem), it has a solution $u_\varepsilon\left(x\right)$; by **Theorem 3.7** (Existence of Minimal and Maximal Solutions), as $\varepsilon\to0^{+}$, $u_\varepsilon\left(x\right)\to\varphi\left(x\right)$ (since $\varphi$ is the rightward minimal solution of $\left(E_1\right)$). Since $f\left(x,y\right)-\varepsilon< F\left(x,y\right)$ strictly holds, applying **Theorem 3.6** (First Comparison Theorem) to $u_\varepsilon$ and $\Phi$ gives

$$
u_\varepsilon\left(x\right)< \Phi\left(x\right),\quad x\in\left(x_0,b\right).
$$

Letting $\varepsilon\to0^{+}$ and taking the limit by $u_\varepsilon\left(x\right)\to\varphi\left(x\right)$ gives $\varphi\left(x\right)\le\Phi\left(x\right)$ on $\left[x_0,b\right)$.

Next prove the leftward segment $x\in\left(a,x_0\right]$, i.e. prove $\varphi\left(x\right)\ge\Phi\left(x\right)$. Again take the above solution $u_\varepsilon$ corresponding to $\left(E_{1,\varepsilon}\right):\ y'=f\left(x,y\right)-\varepsilon$. By **Theorem 3.7** (Existence of Minimal and Maximal Solutions), $u_\varepsilon$ tends leftward to the leftward maximal solution of $\left(E_1\right)$, i.e. $u_\varepsilon\left(x\right)\to\varphi\left(x\right)$. Since $f\left(x,y\right)-\varepsilon< F\left(x,y\right)$, applying **Theorem 3.6** (First Comparison Theorem) to the leftward segment (its second part gives that the curve with smaller slope lies above the curve with larger slope to the left of $x_0$) gives

$$
u_\varepsilon\left(x\right)> \Phi\left(x\right),\quad x\in\left(a,x_0\right).
$$

Letting $\varepsilon\to0^{+}$ and taking the limit gives $\varphi\left(x\right)\ge\Phi\left(x\right)$ on $\left(a,x_0\right]$.

Combining the two segments, $\varphi\left(x\right)\le\Phi\left(x\right)$ on $\left[x_0,b\right)$ and $\varphi\left(x\right)\ge\Phi\left(x\right)$ on $\left(a,x_0\right]$, and **Theorem 3.8** (Second Comparison Theorem) is proved. $\blacksquare$
