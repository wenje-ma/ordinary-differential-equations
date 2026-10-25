# Assignment 20

> **Theorem 6.1*** (Structure of Solutions of Homogeneous Linear Differential Equations)<br>The homogeneous linear differential equation (6.47) has $n$ linearly independent solutions on the interval $\left(a,b\right)$. If these $n$ linearly independent solutions are $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$, then the general solution of equation (6.47) is $$y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right),$$ where $C_1,C_2,\cdots,C_n$ are arbitrary constants. These $n$ linearly independent solutions are called a fundamental system of solutions.

> **Theorem 6.2*** (Wronskian Criterion for Linear Independence of a Solution Set)<br>The solution set $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ of equation (6.47) is linearly independent if and only if its Wronskian determinant $$W\left(x\right)=\left|\begin{matrix}\varphi_1\left(x\right)&\cdots&\varphi_n\left(x\right)\\\varphi_1'\left(x\right)&\cdots&\varphi_n'\left(x\right)\\\vdots&&\vdots\\\varphi_1^{\left(n-1\right)}\left(x\right)&\cdots&\varphi_n^{\left(n-1\right)}\left(x\right)\end{matrix}\right|$$ never vanishes on the interval $\left(a,b\right)$.

> **Liouville's Formula** (Evolution Formula for the Wronskian Determinant (6.54))<br>If $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ is a solution set of equation (6.47) with Wronskian determinant $W\left(x\right)$, then $$W\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}a_1\left(s\right)ds}\quad\left(a< x< b\right),$$ where $x_0\in\left(a,b\right)$, and $a_1\left(x\right)$ is the coefficient of the $y^{\left(n-1\right)}$ term in equation (6.47). In particular, for the second-order equation $y''+p\left(x\right)y'+q\left(x\right)y=0$, we have $a_1\left(x\right)=p\left(x\right)$.

> **Example 1** (Formula for Constructing the General Solution from One Nonzero Solution (6.56))<br>Suppose $y=\varphi\left(x\right)$ is a nonzero solution of the second-order homogeneous linear equation $y''+p\left(x\right)y'+q\left(x\right)y=0$, where $p\left(x\right)$ and $q\left(x\right)$ are continuous functions on the interval $\left(a,b\right)$. Then on any subinterval where $\varphi\left(x\right)\neq0$, the general solution of the equation is $$y=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2\left(s\right)}e^{-\int_{x_0}^{s}p\left(t\right)dt}ds\right],$$ where $C_1$ and $C_2$ are arbitrary constants.

> **Theorem 6.3*** (General Solution Structure and Variation-of-Parameters Formula for Nonhomogeneous Linear Differential Equations (6.57)(6.58))<br>Suppose $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ is a fundamental system of solutions of the homogeneous linear differential equation (6.47) on the interval $\left(a,b\right)$. Then the general solution of the nonhomogeneous linear differential equation (6.46) is $$y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)+\varphi^*\left(x\right),$$ where $$\varphi^*\left(x\right)=\sum_{k=1}^{n}\varphi_k\left(x\right)\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds$$ is a particular solution of equation (6.46), $W\left(x\right)$ is the Wronskian determinant of the fundamental system, and $W_k\left(x\right)$ is the cofactor of the element in the $n$-th row and $k$-th column of $W\left(x\right)$.

> **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations)<br>The characteristic equation of the constant-coefficient homogeneous linear differential equation $y^{\left(n\right)}+a_1y^{\left(n-1\right)}+\cdots+a_ny=0$ is $$\lambda^n+a_1\lambda^{n-1}+\cdots+a_{n-1}\lambda+a_n=0.$$ Suppose the characteristic equation has $s$ distinct roots $\lambda_1,\cdots,\lambda_s$ in the complex domain, with multiplicities $n_1,\cdots,n_s$ respectively. Then the function set $e^{\lambda_kx},\ xe^{\lambda_kx},\ \cdots,\ x^{n_k-1}e^{\lambda_kx}\ \left(k=1,\cdots,s\right)$ is a fundamental system of solutions. Complex roots occur in conjugate pairs; taking the real and imaginary parts of a complex solution gives the corresponding real solutions.

> **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms)<br>When the nonhomogeneous term is $f\left(x\right)=P_m\left(x\right)e^{\mu x}$ (where $P_m\left(x\right)$ is a polynomial of degree $m$), if $\mu$ is not a characteristic root, assume a particular solution $\varphi^*\left(x\right)=Q_m\left(x\right)e^{\mu x}$; if $\mu$ is a root of multiplicity $k$, then assume $$\varphi^*\left(x\right)=x^kQ_m\left(x\right)e^{\mu x},$$ where $Q_m\left(x\right)$ is a polynomial of degree $m$ with undetermined coefficients. When the nonhomogeneous term is $f\left(x\right)=\left[A_m\left(x\right)\cos\beta x+B_l\left(x\right)\sin\beta x\right]e^{\alpha x}$, assume $$\varphi^*\left(x\right)=x^k\left[C_n\left(x\right)\cos\beta x+D_n\left(x\right)\sin\beta x\right]e^{\alpha x},$$ where $k$ is the multiplicity of $\alpha\pm i\beta$ as a characteristic root (take $k=0$ if it is not a root), $n=\max\left\{m,l\right\}$, and the coefficients of the polynomials $C_n\left(x\right),D_n\left(x\right)$ are undetermined.

> **Existence and Uniqueness of the Solution to an Initial Value Problem**<br>The solution of an $n$-th order linear differential equation satisfying the initial condition $y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$ exists and is unique on the common interval of continuity of the coefficients and the nonhomogeneous term. In particular, the initial value problem with all zero initial conditions has only the zero solution.

### Problem 1

(Problem 6-3, Problem 3) Consider the differential equation $y''+q\left(x\right)y=0$. (1) Suppose $y=\varphi\left(x\right)$ and $y=\psi\left(x\right)$ are any two of its solutions. Prove that the Wronskian determinant of $\varphi\left(x\right)$ and $\psi\left(x\right)$ is identically a constant. (2) Given that the equation has a particular solution $y=e^x$, find the general solution and determine $q\left(x\right)$.

### Solution to Problem 1

(1) The equation is $y''+0\cdot y'+q\left(x\right)y=0$, where the coefficient of the $y'$ term is $a_1\left(x\right)=0$. By **Liouville's Formula** (Evolution Formula for the Wronskian Determinant (6.54)), the Wronskian determinant of the solution set $\varphi\left(x\right),\psi\left(x\right)$ is

$$
W\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}a_1\left(s\right)ds}=W\left(x_0\right)e^{-\int_{x_0}^{x}0\,ds}=W\left(x_0\right).
$$

Hence $W\left(x\right)\equiv W\left(x_0\right)$ is identically a constant.

(2) Substitute the particular solution $y=e^x$ into the equation $y''+q\left(x\right)y=0$. Since $\left(e^x\right)'=\left(e^x\right)''=e^x$, we have

$$
e^x+q\left(x\right)e^x=0,
$$

from which we solve $q\left(x\right)=-1$. Thus the original equation is $y''-y=0$, which is a second-order constant-coefficient homogeneous linear equation. By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), its characteristic equation is $\lambda^2-1=0$, i.e. $\lambda=\pm1$ are two simple roots; hence a fundamental system of solutions is $e^x$ and $e^{-x}$, and the general solution is

$$
y=C_1e^x+C_2e^{-x},
$$

where $C_1,C_2$ are arbitrary constants, and $q\left(x\right)=-1$. $\blacksquare$

### Problem 2

(Problem 6-3, Problem 4) Consider the differential equation $y''+p\left(x\right)y'+q\left(x\right)y=0\ \left(6.76\right)$, where $p\left(x\right)$ and $q\left(x\right)$ are continuous functions on the interval $I=\left(a,b\right)$. (1) Suppose $y=\varphi\left(x\right)$ is a nonzero solution of equation (6.76) on the interval $I$ (i.e. $\varphi\left(x\right)$ is not identically zero on $I$). Prove that $\varphi\left(x\right)$ has only simple zeros on $I$ (i.e. if there exists $x_0\in I$ such that $\varphi\left(x_0\right)=0$, then necessarily $\varphi'\left(x_0\right)\neq0$), and further prove that $\varphi\left(x\right)$ has at most finitely many zeros on any finite closed interval, so every zero is isolated. (2) In Example 1, prove the corresponding conclusion for the general case.

### Solution to Problem 2

(1) First prove simple zeros. Suppose for contradiction that there exists $x_0\in I$ such that $\varphi\left(x_0\right)=0$ and $\varphi'\left(x_0\right)=0$. By **Existence and Uniqueness of the Solution to an Initial Value Problem**, the initial value problem with $\varphi\left(x_0\right)=0,\ \varphi'\left(x_0\right)=0$ as initial conditions has only the zero solution $y\equiv0$; hence $\varphi\left(x\right)\equiv0$ on $I$, contradicting that $\varphi\left(x\right)$ is a nonzero solution. Therefore if $\varphi\left(x_0\right)=0$, necessarily $\varphi'\left(x_0\right)\neq0$, i.e. all zeros of $\varphi\left(x\right)$ are simple.

Next prove that zeros are isolated. Since $\varphi\left(x\right)$ is a solution of equation (6.76), and $p\left(x\right),q\left(x\right)$ are continuous, $\varphi'\left(x\right)$ is continuous. For any zero $x_0$, since $\varphi'\left(x_0\right)\neq0$ and $\varphi'$ is continuous, there exists a neighborhood of $x_0$ in which $\varphi'\left(x\right)$ remains nonzero and of the same sign, so $\varphi\left(x\right)$ is strictly monotone; hence $x_0$ is the unique zero in that neighborhood, i.e. every zero is isolated.

Finally prove that there are finitely many zeros on a finite closed interval. Take any finite closed interval $\left[c,d\right]\subset I$; suppose for contradiction that $\varphi\left(x\right)$ has infinitely many zeros on $\left[c,d\right]$. By the Bolzano-Weierstrass accumulation principle (a bounded infinite set has an accumulation point), these zeros have an accumulation point $x_*$ within $\left[c,d\right]$. By continuity of $\varphi$, $\varphi\left(x_*\right)=0$, i.e. $x_*$ itself is also a zero. But by the previous paragraph, $x_*$ is an isolated zero, contradicting that it is the accumulation point of a sequence of zeros. Hence $\varphi\left(x\right)$ has at most finitely many zeros on $\left[c,d\right]$.

(2) For simplicity, Example 1 assumed $\varphi\left(x\right)$ never vanishes on the interval; the general case allows $\varphi\left(x\right)$ to have zeros. By part (1), the zeros of $\varphi\left(x\right)$ are all isolated simple zeros; therefore we may take any open interval $J$ within $I$ that contains no zero of $\varphi$, and fix $x_0\in J$. Let $y\left(x\right)$ be any solution of equation (6.55). Applying **Liouville's Formula** (Evolution Formula for the Wronskian Determinant (6.54)) to the solution set $\varphi\left(x\right),y\left(x\right)$, its Wronskian determinant is

$$
W\left(x\right)=\left|\begin{matrix}\varphi\left(x\right)&y\left(x\right)\\\varphi'\left(x\right)&y'\left(x\right)\end{matrix}\right|=\varphi\left(x\right)y'\left(x\right)-\varphi'\left(x\right)y\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}p\left(s\right)ds}.
$$

Denote $C=W\left(x_0\right)$. On $J$, $\varphi\left(x\right)\neq0$; multiplying both sides by $\frac{1}{\varphi^2\left(x\right)}$, we get

$$
\frac{d}{dx}\left(\frac{y}{\varphi}\right)=\frac{\varphi y'-\varphi'y}{\varphi^2}=\frac{C}{\varphi^2\left(x\right)}e^{-\int_{x_0}^{x}p\left(s\right)ds}.
$$

Integrating both sides from $x_0$ to $x$ ($x\in J$), gives

$$
y\left(x\right)=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2\left(s\right)}e^{-\int_{x_0}^{s}p\left(t\right)dt}ds\right],
$$

where $C_1=\frac{y\left(x_0\right)}{\varphi\left(x_0\right)},\ C_2=C$ are arbitrary constants. This is exactly formula (6.56). Since open intervals containing no zeros can be chosen to cover the region between any two adjacent zeros in $I$ (and neighborhoods of the interval endpoints), the general solution formula of Example 1 still holds on the corresponding subintervals in the general case. $\blacksquare$

### Problem 3

(Problem 6-3, Problem 5) Suppose the functions $u\left(x\right)$ and $v\left(x\right)$ form a fundamental system of solutions of equation (6.76). Prove: (1) the coefficient functions $p\left(x\right)$ and $q\left(x\right)$ of the equation are uniquely determined by this fundamental system. (2) $u\left(x\right)$ and $v\left(x\right)$ have no common zeros.

### Solution to Problem 3

(1) Since $u\left(x\right),v\left(x\right)$ are solutions of equation (6.76), they satisfy

$$
u''+p\left(x\right)u'+q\left(x\right)u=0,\quad v''+p\left(x\right)v'+q\left(x\right)v=0.
$$

Treating $p\left(x\right),q\left(x\right)$ as unknowns, this is a linear algebraic system with coefficients $u'\left(x\right),u\left(x\right)$ and $v'\left(x\right),v\left(x\right)$:

$$
\left\{\begin{matrix}u'\left(x\right)p\left(x\right)+u\left(x\right)q\left(x\right)=-u''\left(x\right),\\v'\left(x\right)p\left(x\right)+v\left(x\right)q\left(x\right)=-v''\left(x\right).\end{matrix}\right.
$$

Its coefficient determinant is

$$
\Delta\left(x\right)=u'\left(x\right)v\left(x\right)-u\left(x\right)v'\left(x\right)=-\left[u\left(x\right)v'\left(x\right)-u'\left(x\right)v\left(x\right)\right]=-W\left(x\right),
$$

where $W\left(x\right)$ is the Wronskian determinant of the fundamental system $u,v$. By **Theorem 6.2*** (Wronskian Criterion for Linear Independence of a Solution Set), $u,v$ being a fundamental system implies $W\left(x\right)\neq0$ on all of $I$, so $\Delta\left(x\right)\neq0$, and the above linear system has a unique solution. By Cramer's rule,

$$
p\left(x\right)=\frac{u''\left(x\right)v\left(x\right)-u\left(x\right)v''\left(x\right)}{W\left(x\right)},\quad q\left(x\right)=\frac{u'\left(x\right)v''\left(x\right)-u''\left(x\right)v'\left(x\right)}{W\left(x\right)}.
$$

Therefore $p\left(x\right),q\left(x\right)$ are uniquely determined by the fundamental system $u,v$.

(2) Suppose for contradiction that $u\left(x\right),v\left(x\right)$ have a common zero $x_0\in I$, i.e. $u\left(x_0\right)=v\left(x_0\right)=0$. Then

$$
W\left(x_0\right)=u\left(x_0\right)v'\left(x_0\right)-u'\left(x_0\right)v\left(x_0\right)=0.
$$

But $u,v$ are a fundamental system, and by **Theorem 6.2*** (Wronskian Criterion for Linear Independence of a Solution Set), $W\left(x\right)$ never vanishes on $I$, a contradiction. Hence $u\left(x\right)$ and $v\left(x\right)$ have no common zeros. $\blacksquare$

### Problem 4

(Problem 6-3, Problem 6) Use the method of variation of parameters to prove Theorem 6.3*.

### Solution to Problem 4

Suppose $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ is a fundamental system of solutions of the homogeneous linear differential equation (6.47). By **Theorem 6.1*** (Structure of Solutions of Homogeneous Linear Differential Equations), the general solution of the homogeneous equation is $y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)$. The idea of variation of parameters is to vary the constants $C_k$ into functions of $x$, and assume the nonhomogeneous equation (6.46) has a solution of the form

$$
y=C_1\left(x\right)\varphi_1\left(x\right)+\cdots+C_n\left(x\right)\varphi_n\left(x\right)
$$

Differentiate successively, and set the combinations of the derivatives of the varied constants in each order to zero, i.e. set

$$
\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(j\right)}\left(x\right)=0\quad\left(j=0,1,\cdots,n-2\right),
$$

then we have $y^{\left(j\right)}\left(x\right)=\sum_{k=1}^{n}C_k\left(x\right)\varphi_k^{\left(j\right)}\left(x\right)\ \left(j=0,1,\cdots,n-1\right)$. Differentiate once more to get

$$
y^{\left(n\right)}\left(x\right)=\sum_{k=1}^{n}C_k\left(x\right)\varphi_k^{\left(n\right)}\left(x\right)+\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right).
$$

Substitute $y,y',\cdots,y^{\left(n\right)}$ into equation (6.46); noting that each $\varphi_k$ satisfies the homogeneous equation, all terms containing $C_k\left(x\right)$ cancel, leaving

$$
\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right)=f\left(x\right).
$$

Thus $C_1'\left(x\right),\cdots,C_n'\left(x\right)$ satisfy the linear system

$$
\left\{\begin{matrix}\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k\left(x\right)=0,\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k'\left(x\right)=0,\\\quad\vdots\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-2\right)}\left(x\right)=0,\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right)=f\left(x\right).\end{matrix}\right.
$$

Its coefficient determinant is exactly the Wronskian determinant $W\left(x\right)$ of the fundamental system. By **Theorem 6.2*** (Wronskian Criterion for Linear Independence of a Solution Set), $W\left(x\right)\neq0$; hence by Cramer's rule, $C_k'\left(x\right)$ equals the determinant obtained by replacing the $k$-th column of $W\left(x\right)$ with the right-hand side vector $\left(0,\cdots,0,f\left(x\right)\right)^T$, divided by $W\left(x\right)$. Expanding that determinant along the $k$-th column, only $f\left(x\right)$ in the last row contributes, so

$$
C_k'\left(x\right)=\frac{W_k\left(x\right)}{W\left(x\right)}f\left(x\right),
$$

where $W_k\left(x\right)$ is the cofactor of the element in the $n$-th row and $k$-th column of $W\left(x\right)$. Taking the integration constants to be zero to obtain a particular solution, and integrating, gives

$$
C_k\left(x\right)=\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds\quad\left(k=1,\cdots,n\right).
$$

Substituting back into the assumed solution form gives a particular solution of equation (6.46)

$$
\varphi^*\left(x\right)=\sum_{k=1}^{n}\varphi_k\left(x\right)\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds.
$$

Adding the arbitrary constants $C_1,\cdots,C_n$ from the homogeneous general solution gives the general solution of equation (6.46)

$$
y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)+\varphi^*\left(x\right),
$$

which is exactly formulas (6.57)(6.58). **Theorem 6.3*** (General Solution Structure and Variation-of-Parameters Formula for Nonhomogeneous Linear Differential Equations (6.57)(6.58)) is proved. $\blacksquare$

### Problem 5

(Problem 6-3, Problem 7) Consider the Euler equation $x^ny^{\left(n\right)}+a_1x^{n-1}y^{\left(n-1\right)}+\cdots+a_{n-1}xy'+a_ny=0$, where $a_1,a_2,\cdots,a_n$ are all constants and $x> 0$. Use an appropriate change of variable to convert it into a constant-coefficient homogeneous linear differential equation.

### Solution to Problem 5

Make the change of independent variable $x=e^t$, i.e. $t=\ln x\ \left(x> 0\right)$. Denote $D=\frac{d}{dt}$; then $\frac{d}{dx}=\frac{1}{x}\frac{d}{dt}$, i.e.

$$
x\frac{d}{dx}=D.
$$

We prove by induction that

$$
x^ky^{\left(k\right)}=D\left(D-1\right)\cdots\left(D-k+1\right)y\quad\left(k=1,2,\cdots,n\right).
$$

For $k=1$, $xy'=Dy$, which is clearly true. Assume the formula holds for $k$; then for $k+1$,

$$
x^{k+1}y^{\left(k+1\right)}=x\frac{d}{dx}\left(x^ky^{\left(k\right)}\right)-kx^ky^{\left(k\right)}=D\Big[D\left(D-1\right)\cdots\left(D-k+1\right)y\Big]-k\Big[D\left(D-1\right)\cdots\left(D-k+1\right)y\Big],
$$

i.e.

$$
x^{k+1}y^{\left(k+1\right)}=D\left(D-1\right)\cdots\left(D-k+1\right)\left(D-k\right)y.
$$

The induction is complete. Substituting this into the Euler equation gives

$$
\left[D\left(D-1\right)\cdots\left(D-n+1\right)+a_1D\left(D-1\right)\cdots\left(D-n+2\right)+\cdots+a_{n-1}D+a_n\right]y=0.
$$

The left-hand side is a constant-coefficient polynomial operator in $D=\frac{d}{dt}$, so the above is a constant-coefficient homogeneous linear differential equation for the unknown function $y=y\left(t\right)$. $\blacksquare$

### Problem 6

(Problem 6-3, Problem 9) Solve the forced vibration equation of a spring oscillator without damping: $m\frac{d^2x}{dt^2}+kx=p\cos\omega t$, where $m,k,p$ and $\omega$ are all positive constants. Also, for the two cases $\omega\neq\omega_0$ and $\omega=\omega_0$, explain the physical meaning of the solution, where $\omega_0=\sqrt{\frac{k}{m}}$ is the natural frequency of the spring oscillator.

### Solution to Problem 6

First solve the corresponding homogeneous equation $mx''+kx=0$, i.e. $x''+\omega_0^2x=0$. By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), the characteristic equation is $\lambda^2+\omega_0^2=0$, giving the conjugate complex roots $\lambda=\pm i\omega_0$; taking real and imaginary parts gives the fundamental system $\cos\omega_0t,\ \sin\omega_0t$, so the homogeneous general solution is

$$
x_h\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t.
$$

(1) When $\omega\neq\omega_0$, $\pm i\omega$ is not a characteristic root. By **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms), assume a particular solution $x^*\left(t\right)=A\cos\omega t+B\sin\omega t$. Substitute into the original equation:

$$
m\left(-A\omega^2\cos\omega t-B\omega^2\sin\omega t\right)+k\left(A\cos\omega t+B\sin\omega t\right)=p\cos\omega t.
$$

Comparing coefficients gives $\left(k-m\omega^2\right)A=p,\ \left(k-m\omega^2\right)B=0$, so $A=\frac{p}{k-m\omega^2}=\frac{p}{m\left(\omega_0^2-\omega^2\right)},\ B=0$. The general solution is

$$
x\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t+\frac{p}{m\left(\omega_0^2-\omega^2\right)}\cos\omega t.
$$

Physical meaning: the solution is a superposition of free vibration at the natural frequency $\omega_0$ and forced vibration at the driving frequency $\omega$; in general the motion is non-periodic. When $\omega$ is close to $\omega_0$, the superposition of the two harmonic motions produces a "beat" phenomenon, with the amplitude periodically increasing and decreasing over time.

(2) When $\omega=\omega_0$, $\pm i\omega_0$ is a simple characteristic root. By **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms), we should assume a particular solution $x^*\left(t\right)=t\big(A\cos\omega_0t+B\sin\omega_0t\big)$. Differentiating gives

$$
x^{*''}\left(t\right)=-2A\omega_0\sin\omega_0t+2B\omega_0\cos\omega_0t-\omega_0^2t\big(A\cos\omega_0t+B\sin\omega_0t\big).
$$

Substituting into $mx''+kx$, the terms containing $t$ cancel because $k=m\omega_0^2$, leaving

$$
-2mA\omega_0\sin\omega_0t+2mB\omega_0\cos\omega_0t=p\cos\omega_0t.
$$

Comparing coefficients gives $A=0,\ B=\frac{p}{2m\omega_0}$. The general solution is

$$
x\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t+\frac{p}{2m\omega_0}\,t\sin\omega_0t.
$$

Physical meaning: this is undamped resonance. The amplitude of the particular solution term $\frac{p}{2m\omega_0}t\sin\omega_0t$ grows linearly with time $t$, and the vibration amplitude tends to infinity; resonance occurs when the driving frequency equals the natural frequency. $\blacksquare$

### Problem 7

(Problem 6-3, Problem 10(3)) Solve the constant-coefficient linear differential equation $y''+2y'=3+4\sin2x$.

### Solution to Problem 7

First solve the homogeneous equation $y''+2y'=0$. By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), the characteristic equation is $\lambda^2+2\lambda=\lambda\left(\lambda+2\right)=0$, giving the simple roots $\lambda=0,\ -2$; hence the homogeneous general solution is

$$
y_h=C_1+C_2e^{-2x}.
$$

Split the nonhomogeneous term $3+4\sin2x$ into two parts, find particular solutions separately, and superpose.

For the constant term $3=3e^{0\cdot x}$, $\mu=0$ is a simple characteristic root. By **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms), assume a particular solution $y_1^*=Ax$. Substituting gives $\left(Ax\right)''+2\left(Ax\right)'=2A=3$, so $A=\frac{3}{2}$, i.e. $y_1^*=\frac{3}{2}x$.

For $4\sin2x$, $\pm2i$ is not a characteristic root. Assume a particular solution $y_2^*=B\cos2x+D\sin2x$. Differentiating gives $y_2^{*'}=-2B\sin2x+2D\cos2x,\ y_2^{*''}=-4B\cos2x-4D\sin2x$. Substituting into the equation:

$$
y_2^{*''}+2y_2^{*'}=\left(-4B+4D\right)\cos2x+\left(-4D-4B\right)\sin2x=4\sin2x.
$$

Comparing coefficients gives $-4B+4D=0,\ -4D-4B=4$, solving gives $B=D=-\frac{1}{2}$. Hence $y_2^*=-\frac{1}{2}\cos2x-\frac{1}{2}\sin2x$.

The general solution is

$$
y=C_1+C_2e^{-2x}+\frac{3}{2}x-\frac{1}{2}\left(\cos2x+\sin2x\right),
$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$

### Problem 8

(Problem 6-3, Problem 10(6)) Solve the constant-coefficient linear differential equation $y'''-3ay''+3a^2y'-a^3y=0$.

### Solution to Problem 8

By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), the characteristic equation is

$$
\lambda^3-3a\lambda^2+3a^2\lambda-a^3=\left(\lambda-a\right)^3=0,
$$

i.e. $\lambda=a$ is a triple characteristic root. The corresponding fundamental system is $e^{ax},\ xe^{ax},\ x^2e^{ax}$, so the general solution is

$$
y=\left(C_1+C_2x+C_3x^2\right)e^{ax},
$$

where $C_1,C_2,C_3$ are arbitrary constants. $\blacksquare$

### Problem 9

(Problem 6-3, Problem 10(9)) Solve the constant-coefficient linear differential equation $y^{\left(4\right)}+2y''+y=\sin x,\ y\left(0\right)=1,\ y'\left(0\right)=-2,\ y''\left(0\right)=3,\ y'''\left(0\right)=0$.

### Solution to Problem 9

By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), the characteristic equation is

$$
\lambda^4+2\lambda^2+1=\left(\lambda^2+1\right)^2=0,
$$

i.e. $\lambda=\pm i$ are both double characteristic roots. Taking the real and imaginary parts of the complex solutions gives the fundamental system $\cos x,\ x\cos x,\ \sin x,\ x\sin x$, so the homogeneous general solution is

$$
y_h=\left(C_1+C_2x\right)\cos x+\left(C_3+C_4x\right)\sin x.
$$

The nonhomogeneous term is $\sin x$, and $\pm i$ is a double characteristic root. By **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms), assume a particular solution $y^*=x^2\left(A\cos x+B\sin x\right)$. Denote $D=\frac{d}{dx}$; the original equation is $\left(D^2+1\right)^2y=\sin x$. Direct differentiation gives

$$
\left(D^2+1\right)^2\left(x^2\cos x\right)=-8\cos x,\quad\left(D^2+1\right)^2\left(x^2\sin x\right)=-8\sin x.
$$

Substituting gives

$$
\left(D^2+1\right)^2y^*=-8A\cos x-8B\sin x=\sin x,
$$

Comparing coefficients gives $A=0,\ B=-\frac{1}{8}$, so $y^*=-\frac{1}{8}x^2\sin x$. The general solution is

$$
y=\left(C_1+C_2x\right)\cos x+\left(C_3+C_4x\right)\sin x-\frac{1}{8}x^2\sin x.
$$

By **Existence and Uniqueness of the Solution to an Initial Value Problem**, any given initial condition uniquely determines a set of constants. Compute the values of the derivatives at $x=0$: $y\left(0\right)=C_1$; from $y'=C_2\cos x-\left(C_1+C_2x\right)\sin x+C_4\sin x+\left(C_3+C_4x\right)\cos x-\frac{1}{8}\left(2x\sin x+x^2\cos x\right)$, we get $y'\left(0\right)=C_2+C_3$; direct computation gives $y''\left(0\right)=-C_1+2C_4,\ y'''\left(0\right)=-3C_2-C_3-\frac{3}{4}$. Substituting the initial conditions:

$$
C_1=1,\quad C_2+C_3=-2,\quad-C_1+2C_4=3,\quad-3C_2-C_3-\frac{3}{4}=0.
$$

Solving gives $C_1=1,\ C_2=\frac{5}{8},\ C_3=-\frac{21}{8},\ C_4=2$. Hence the desired particular solution is

$$
y=\left(1+\frac{5}{8}x\right)\cos x+\left(2x-\frac{21}{8}-\frac{1}{8}x^2\right)\sin x.
$$

$\blacksquare$

### Problem 10

(Problem 6-3, Problem 10(12)) Solve the constant-coefficient linear differential equation $y''-5y'+6y=\left(12x-7\right)e^{-x}$.

### Solution to Problem 10

By **Theorem 6.6*** (Characteristic-Root Method for Constant-Coefficient Homogeneous Linear Differential Equations), the characteristic equation is

$$
\lambda^2-5\lambda+6=\left(\lambda-2\right)\left(\lambda-3\right)=0,
$$

giving the simple roots $\lambda=2,\ 3$, so the homogeneous general solution is

$$
y_h=C_1e^{2x}+C_2e^{3x}.
$$

The nonhomogeneous term is $\left(12x-7\right)e^{-x}$, where $\mu=-1$ is not a characteristic root. By **Method of Undetermined Coefficients** (Presetting the Form of a Particular Solution for Special Nonhomogeneous Terms), assume a particular solution $y^*=\left(Ax+B\right)e^{-x}$. Differentiating gives

$$
y^{*'}=\left(A-Ax-B\right)e^{-x},\quad y^{*''}=\left(Ax+B-2A\right)e^{-x}.
$$

Substituting into the equation:

$$
y^{*''}-5y^{*'}+6y^*=\big[Ax+B-2A-5\left(A-Ax-B\right)+6\left(Ax+B\right)\big]e^{-x}=\left(12Ax+12B-7A\right)e^{-x}.
$$

Comparing coefficients with $\left(12x-7\right)e^{-x}$ gives $12A=12,\ 12B-7A=-7$, solving gives $A=1,\ B=0$, i.e. $y^*=xe^{-x}$. The general solution is

$$
y=C_1e^{2x}+C_2e^{3x}+xe^{-x},
$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$
