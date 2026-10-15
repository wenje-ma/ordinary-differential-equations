# Assignment 19

> **Proposition 1** (Absolute Convergence of Matrix Power Series and Definition of the Matrix Exponential)<br>For an $n$-th order real constant matrix $A$, the matrix power series $$E+A+\frac{1}{2!}A^2+\cdots+\frac{1}{k!}A^k+\cdots$$ is absolutely convergent; its sum is denoted $$e^A=\sum_{k=0}^{\infty}\frac{1}{k!}A^k,$$ and is called the exponential function of the matrix $A$, where $E$ is the $n$-th order identity matrix.

> **Proposition 2** (Properties of the Matrix Exponential)<br>The matrix exponential has the following properties: (1) if the matrices $A$ and $B$ commute (i.e. $AB=BA$), then $$e^{A+B}=e^A e^B;$$<br>(2) for any matrix $A$, the exponential $e^A$ is invertible, and $$\left(e^A\right)^{-1}=e^{-A};$$<br>(3) if $P$ is a nonsingular $n$-th order matrix, then $$e^{PAP^{-1}}=Pe^AP^{-1}.$$

> **Theorem 6.4** (The Matrix Exponential Is a Standard Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System)<br>The matrix exponential $$\Phi\left(x\right)=e^{xA}$$ is a standard fundamental matrix of the constant-coefficient homogeneous linear system $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$$ (i.e. the fundamental matrix $\Phi\left(x\right)$ satisfies $\Phi\left(0\right)=E$).

> **Corollary 3** (General Solution and Initial-Value Solution of a Constant-Coefficient Nonhomogeneous Linear System)<br>The general solution of the constant-coefficient nonhomogeneous linear system $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$$ on the interval $\left(a,b\right)$ is $$\boldsymbol{y}=e^{xA}\boldsymbol{c}+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,$$ where $c$ is an arbitrary constant column vector; the solution satisfying the initial condition $y\left(x_0\right)=y_0$ is $$\boldsymbol{y}=e^{\left(x-x_0\right)A}\boldsymbol{y}_0+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,$$ where $x_0\in\left(a,b\right)$.

> **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution)<br>The constant-coefficient homogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ has a nonzero solution $y=e^{\lambda x}r$ if and only if $\lambda$ is an eigenvalue of the matrix $A$, and $\boldsymbol{r}$ is the eigenvector corresponding to $\lambda$, i.e. $\boldsymbol{r}$ satisfies the homogeneous linear algebraic system $\left(A-\lambda E\right)\boldsymbol{r}=\boldsymbol{0}$.

> **Theorem 6.5** (Fundamental Matrix with $n$ Distinct Eigenvalues)<br>Suppose the $n$-th order matrix $A$ has $n$ distinct eigenvalues $\lambda_1,\lambda_2,\cdots,\lambda_n$. Then the matrix function $$\Phi\left(x\right)=\left(e^{\lambda_1 x}\boldsymbol{r}_1,e^{\lambda_2 x}\boldsymbol{r}_2,\cdots,e^{\lambda_n x}\boldsymbol{r}_n\right)$$ is a fundamental matrix of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$, where $r_i$ is the eigenvector of $A$ corresponding to $\lambda_i$.

> **Lemma 6.7** (Method for Determining Coefficients of the Vector Polynomial in the Case of Repeated Eigenvalues)<br>Suppose $\lambda_i$ is an eigenvalue of multiplicity $n_i$ of the matrix $A$. Then the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ has a nonzero solution of the form $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)$$ if and only if $r_0$ is a nonzero solution of the homogeneous linear algebraic system $\left(A-\lambda_i E\right)^{n_i}\boldsymbol{r}=\boldsymbol{0}$, and $r_1,r_2,\cdots,r_{n_i-1}$ are determined successively by the relations $$\boldsymbol{r}_1=\left(A-\lambda_i E\right)\boldsymbol{r}_0,\ \boldsymbol{r}_2=\left(A-\lambda_i E\right)\boldsymbol{r}_1,\ \cdots,\ \boldsymbol{r}_{n_i-1}=\left(A-\lambda_i E\right)\boldsymbol{r}_{n_i-2}.$$

> **Theorem 6.6** (Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System with Repeated Eigenvalues)<br>Suppose the $n$-th order real constant matrix $A$ has distinct eigenvalues $\lambda_1,\lambda_2,\cdots,\lambda_s$ in the complex domain, with multiplicities $n_1,n_2,\cdots,n_s$ respectively. Then every solution of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ is a linear combination of vector functions of the form $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)$$ where $i=1,2,\cdots,s$.

> **Remark 2** (Method for Extracting Real Solutions from Complex Solutions)<br>Suppose the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ has a complex solution $\boldsymbol{y}_1=\boldsymbol{u}\left(x\right)+i\boldsymbol{v}\left(x\right)$, where $A$ is a real matrix. Then the conjugate $\boldsymbol{y}_2=\boldsymbol{u}\left(x\right)-i\boldsymbol{v}\left(x\right)$ of $\boldsymbol{y}_1$ is also a complex solution of the system; hence the real part $\boldsymbol{u}\left(x\right)$ and the imaginary part $\boldsymbol{v}\left(x\right)$ of $\boldsymbol{y}_1$ are both real solutions of the system. That is, a pair of conjugate complex solutions yields two real solutions.

### Problem 1

(Problem 6-2, Problem 1(2)) Find the general solution of the constant-coefficient homogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$, where

$$A=\begin{pmatrix}0&a\\-a&0\end{pmatrix},$$

and $a$ is a constant.

### Solution to Problem 1

First find the eigenvalues of $A$. The characteristic equation is

$$\det\left(A-\lambda E\right)=\begin{vmatrix}-\lambda&a\\-a&-\lambda\end{vmatrix}=\lambda^2+a^2=0,$$

so $\lambda=\pm ia$. Below assume $a\neq0$. By **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution), the system has an exponential nonzero solution $e^{\lambda x}\boldsymbol{r}$ if and only if $\lambda$ is an eigenvalue of $A$. For $\lambda=ia$, solve $\left(A-iaE\right)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{pmatrix}-ia&a\\-a&-ia\end{pmatrix}\begin{pmatrix}r_1\\r_2\end{pmatrix}=\boldsymbol{0},$$

From the first row we get $-ir_1+r_2=0$; take $\boldsymbol{r}=\left(1,i\right)^T$. Thus we obtain a complex solution

$$\boldsymbol{y}_1=e^{iax}\begin{pmatrix}1\\i\end{pmatrix}.$$

By **Remark 2** (Method for Extracting Real Solutions from Complex Solutions), taking the real and imaginary parts of $\boldsymbol{y}_1$ gives real solutions. Using $e^{iax}=\cos ax+i\sin ax$, expanding gives

$$\boldsymbol{y}_1=\left(\cos ax+i\sin ax\right)\begin{pmatrix}1\\i\end{pmatrix}=\begin{pmatrix}\cos ax+i\sin ax\\i\cos ax-\sin ax\end{pmatrix}.$$

Its real and imaginary parts are respectively

$$\boldsymbol{u}\left(x\right)=\begin{pmatrix}\cos ax\\-\sin ax\end{pmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{pmatrix}\sin ax\\\cos ax\end{pmatrix}.$$

By **Theorem 6.5** (Fundamental Matrix with $n$ Distinct Eigenvalues), the two real solutions are linearly independent and form a real fundamental matrix; hence the general solution is

$$\boldsymbol{y}=C_1\begin{pmatrix}\cos ax\\-\sin ax\end{pmatrix}+C_2\begin{pmatrix}\sin ax\\\cos ax\end{pmatrix},$$

where $C_1,C_2$ are arbitrary constants. When $a=0$, $A$ is the zero matrix and the system degenerates to $\frac{d\boldsymbol{y}}{dx}=\boldsymbol{0}$; the general solution is the constant vector $\boldsymbol{y}=\boldsymbol{C}$. $\blacksquare$

### Problem 2

(Problem 6-2, Problem 1(4)) Find the general solution of the constant-coefficient homogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$, where

$$A=\begin{pmatrix}1&\frac{2}{3}&-\frac{2}{3}\\0&\frac{2}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{4}{3}\end{pmatrix}.$$

### Solution to Problem 2

First find the eigenvalues of $A$. Expanding the determinant along the first row:

$$\det\left(A-\lambda E\right)=\left(1-\lambda\right)\begin{vmatrix}\frac{2}{3}-\lambda&\frac{1}{3}\\-\frac{1}{3}&\frac{4}{3}-\lambda\end{vmatrix}=\left(1-\lambda\right)\left[\left(\frac{2}{3}-\lambda\right)\left(\frac{4}{3}-\lambda\right)+\frac{1}{9}\right].$$

Simplifying inside the brackets gives $\left(\lambda-1\right)^2$, so

$$\det\left(A-\lambda E\right)=-\left(\lambda-1\right)^3,$$

i.e. $\lambda=1$ is a triple eigenvalue. Compute $A-E$:

$$A-E=\begin{pmatrix}0&\frac{2}{3}&-\frac{2}{3}\\0&-\frac{1}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{1}{3}\end{pmatrix}.$$

Its rank is 1, so the solution space of $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ is two-dimensional. From $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ we get $r_2=r_3$; take two linearly independent eigenvectors

$$\boldsymbol{r}^{\left(1\right)}=\begin{pmatrix}1\\0\\0\end{pmatrix},\quad\boldsymbol{r}^{\left(2\right)}=\begin{pmatrix}0\\1\\1\end{pmatrix}.$$

By **Lemma 6.7** (Method for Determining Coefficients of the Vector Polynomial in the Case of Repeated Eigenvalues), we also need a vector $\boldsymbol{r}_0$ satisfying $\left(A-E\right)^2\boldsymbol{r}_0=O$ but $\left(A-E\right)\boldsymbol{r}_0\neq\boldsymbol{0}$. Direct verification shows

$$\left(A-E\right)^2=O,$$

so we may simply take $\boldsymbol{r}_0^{\left(3\right)}=\left(0,1,0\right)^T$, which is not an eigenvector. Compute the coefficients successively:

$$\boldsymbol{r}_1^{\left(3\right)}=\left(A-E\right)\boldsymbol{r}_0^{\left(3\right)}=\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}.$$

Thus the third solution obtained by **Lemma 6.7** (Method for Determining Coefficients of the Vector Polynomial in the Case of Repeated Eigenvalues) is

$$e^x\left(\boldsymbol{r}_0^{\left(3\right)}+x\boldsymbol{r}_1^{\left(3\right)}\right)=e^x\left[\begin{pmatrix}0\\1\\0\end{pmatrix}+x\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}\right].$$

The values of the three solutions at $x=0$ are $\boldsymbol{r}^{\left(1\right)},\boldsymbol{r}^{\left(2\right)}$ and $\boldsymbol{r}_0^{\left(3\right)}$, which are linearly independent; by **Theorem 6.6** (Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System with Repeated Eigenvalues) they form a fundamental matrix. Hence the general solution is

$$\boldsymbol{y}=C_1e^x\begin{pmatrix}1\\0\\0\end{pmatrix}+C_2e^x\begin{pmatrix}0\\1\\1\end{pmatrix}+C_3e^x\left[\begin{pmatrix}0\\1\\0\end{pmatrix}+x\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}\right],$$

where $C_1,C_2,C_3$ are arbitrary constants. $\blacksquare$

### Problem 3

(Problem 6-2, Problem 2(2)) Find the general solution of the constant-coefficient nonhomogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$, where

$$A=\begin{pmatrix}0&-n^2\\-n^2&0\end{pmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{pmatrix}\cos nx\\\sin nx\end{pmatrix}.$$

### Solution to Problem 3

First find the general solution of the corresponding homogeneous system. The characteristic equation is

$$\det\left(A-\lambda E\right)=\lambda^2-n^4=0,$$

so $\lambda=\pm n^2$. By **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution), find the eigenvectors separately: for $\lambda=n^2$, solving $\left(A-n^2E\right)\boldsymbol{r}=\boldsymbol{0}$ gives $r_1+r_2=0$, take $\left(1,-1\right)^T$; for $\lambda=-n^2$, solving $\left(A+n^2E\right)\boldsymbol{r}=\boldsymbol{0}$ gives $r_1-r_2=0$, take $\left(1,1\right)^T$. Hence the homogeneous general solution is

$$\boldsymbol{y}_h=C_1e^{n^2x}\begin{pmatrix}1\\-1\end{pmatrix}+C_2e^{-n^2x}\begin{pmatrix}1\\1\end{pmatrix}.$$

Next find a particular solution. The nonhomogeneous term is $\cos nx$ and $\sin nx$, which are not in resonance with the eigenvalues $\pm n^2$, so assume a particular solution of the form

$$\boldsymbol{y}_p=\begin{pmatrix}a_1\cos nx+b_1\sin nx\\a_2\cos nx+b_2\sin nx\end{pmatrix}.$$

Substituting into the system $y_1'=-n^2y_2+\cos nx,\ y_2'=-n^2y_1+\sin nx$, and comparing coefficients of $\cos nx$ and $\sin nx$, gives $a_1=0,\ b_2=0$, and

$$nb_1=1-n^2a_2,\quad -na_2=1-n^2b_1.$$

Solving simultaneously gives

$$a_2=\frac{n-1}{n\left(1+n^2\right)},\quad b_1=\frac{n+1}{n\left(1+n^2\right)}.$$

Hence a particular solution is

$$\boldsymbol{y}_p=\begin{pmatrix}\frac{n+1}{n\left(1+n^2\right)}\sin nx\\[2pt\right]\frac{n-1}{n\left(1+n^2\right)}\cos nx\end{pmatrix}.$$

By **Corollary 3** (General Solution and Initial-Value Solution of a Constant-Coefficient Nonhomogeneous Linear System), the nonhomogeneous general solution is the homogeneous general solution plus a particular solution:

$$\boldsymbol{y}=C_1e^{n^2x}\begin{pmatrix}1\\-1\end{pmatrix}+C_2e^{-n^2x}\begin{pmatrix}1\\1\end{pmatrix}+\begin{pmatrix}\frac{n+1}{n\left(1+n^2\right)}\sin nx\\[2pt\right]\frac{n-1}{n\left(1+n^2\right)}\cos nx\end{pmatrix},$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$

### Problem 4

(Problem 6-2, Problem 2(4)) Find the general solution of the constant-coefficient nonhomogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$, where

$$A=\begin{pmatrix}2&1&-2\\-1&0&0\\1&1&-1\end{pmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{pmatrix}2-x\\0\\1-x\end{pmatrix}.$$

### Solution to Problem 4

First find the general solution of the corresponding homogeneous system. Compute the characteristic polynomial:

$$\det\left(A-\lambda E\right)=\left(2-\lambda\right)\left(\lambda+\lambda^2\right)-\left(1+\lambda\right)-2\left(\lambda-1\right)=-\left(\lambda-1\right)\left(\lambda^2+1\right).$$

Hence the eigenvalues are $\lambda=1,\ \lambda=\pm i$. For $\lambda=1$, solving $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ gives the eigenvector $\boldsymbol{r}^{\left(1\right)}=\left(-1,1,0\right)^T$. For $\lambda=i$, solving $\left(A-iE\right)\boldsymbol{r}=\boldsymbol{0}$ gives the complex eigenvector $\boldsymbol{r}=\left(-i,1,-i\right)^T$, corresponding to the complex solution $e^{ix}\left(-i,1,-i\right)^T$. By **Remark 2** (Method for Extracting Real Solutions from Complex Solutions), using $e^{ix}=\cos x+i\sin x$ and taking real and imaginary parts, gives

$$\boldsymbol{u}\left(x\right)=\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}.$$

By **Theorem 6.5** (Fundamental Matrix with $n$ Distinct Eigenvalues), the homogeneous general solution is

$$\boldsymbol{y}_h=C_1e^x\begin{pmatrix}-1\\1\\0\end{pmatrix}+C_2\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix}+C_3\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}.$$

Next find a particular solution. The nonhomogeneous term is linear in $x$; assume a particular solution $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, where $\boldsymbol{a},\boldsymbol{b}$ are constant vectors. Substituting into the system and comparing constant and $x$ coefficients gives

$$A\boldsymbol{b}=\begin{pmatrix}1\\0\\1\end{pmatrix},\quad\boldsymbol{b}=A\boldsymbol{a}+\begin{pmatrix}2\\0\\1\end{pmatrix}.$$

From the first equation solve $\boldsymbol{b}=\left(0,1,0\right)^T$; substituting into the second gives $A\boldsymbol{a}=\left(-2,1,-1\right)^T$, solving gives $\boldsymbol{a}=\left(-1,0,0\right)^T$. Hence a particular solution is

$$\boldsymbol{y}_p=\begin{pmatrix}-1\\x\\0\end{pmatrix}.$$

By **Corollary 3** (General Solution and Initial-Value Solution of a Constant-Coefficient Nonhomogeneous Linear System), the general solution is

$$\boldsymbol{y}=C_1e^x\begin{pmatrix}-1\\1\\0\end{pmatrix}+C_2\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix}+C_3\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}+\begin{pmatrix}-1\\x\\0\end{pmatrix},$$

where $C_1,C_2,C_3$ are arbitrary constants. $\blacksquare$

### Problem 5

(Problem 6-2, Problem 3(2)) Find the solution of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ satisfying the initial condition $\boldsymbol{y}\left(0\right)=\boldsymbol{\eta}$, where

$$A=\begin{pmatrix}0&-2\\2&0\end{pmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{pmatrix}3x\\4\end{pmatrix},\quad\boldsymbol{\eta}=\begin{pmatrix}2\\3\end{pmatrix}.$$

### Solution to Problem 5

First find the general solution of the corresponding homogeneous system. The characteristic equation is

$$\det\left(A-\lambda E\right)=\lambda^2+4=0,$$

so $\lambda=\pm2i$. For $\lambda=2i$, solving $\left(A-2iE\right)\boldsymbol{r}=\boldsymbol{0}$ gives $\boldsymbol{r}=\left(1,-i\right)^T$, corresponding to the complex solution $e^{2ix}\left(1,-i\right)^T$. By **Remark 2** (Method for Extracting Real Solutions from Complex Solutions), using $e^{2ix}=\cos 2x+i\sin 2x$ and taking real and imaginary parts, gives two real solutions

$$\boldsymbol{u}\left(x\right)=\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}.$$

Next find a particular solution. The nonhomogeneous term is linear; assume $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, substitute and compare coefficients:

$$A\boldsymbol{b}=\begin{pmatrix}-3\\0\end{pmatrix},\quad\boldsymbol{b}=A\boldsymbol{a}+\begin{pmatrix}0\\4\end{pmatrix}.$$

From the first equation get $\boldsymbol{b}=\left(0,\frac{3}{2}\right)^T$; substituting gives $\boldsymbol{a}=\left(-\frac{5}{4},0\right)^T$. Hence a particular solution is

$$\boldsymbol{y}_p=\begin{pmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{pmatrix}.$$

By **Corollary 3** (General Solution and Initial-Value Solution of a Constant-Coefficient Nonhomogeneous Linear System), the general solution is

$$\boldsymbol{y}=C_1\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix}+C_2\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{pmatrix}.$$

Substitute the initial condition $\boldsymbol{y}\left(0\right)=\left(2,3\right)$:

$$C_1\begin{pmatrix}1\\0\end{pmatrix}+C_2\begin{pmatrix}0\\-1\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\0\end{pmatrix}=\begin{pmatrix}2\\3\end{pmatrix},$$

Solving gives $C_1=\frac{13}{4},\ C_2=-3$. Hence the solution of the initial value problem is

$$\boldsymbol{y}=\frac{13}{4}\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix}-3\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{pmatrix}.$$

$\blacksquare$

### Problem 6

(Problem 6-2, Problem 3(4)) Find the solution of the system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ satisfying the initial condition $\boldsymbol{y}\left(0\right)=\boldsymbol{\eta}$, where

$$A=\begin{pmatrix}16&14&38\\-9&-7&-18\\-4&-4&-11\end{pmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{pmatrix}-2e^{-x}\\-3e^{-x}\\2e^{-x}\end{pmatrix},\quad\boldsymbol{\eta}=\begin{pmatrix}0\\0\\0\end{pmatrix}.$$

### Solution to Problem 6

First find the eigenvalues of $A$. Compute the characteristic polynomial:

$$\det\left(A-\lambda E\right)=-\left(\lambda-2\right)\left(\lambda+1\right)\left(\lambda+3\right),$$

so the eigenvalues are $\lambda=2,\ \lambda=-1,\ \lambda=-3$. By **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution), find the corresponding eigenvectors:

$$\boldsymbol{r}^{\left(2\right)}=\begin{pmatrix}-1\\1\\0\end{pmatrix},\quad\boldsymbol{r}^{\left(-1\right)}=\begin{pmatrix}2\\3\\-2\end{pmatrix},\quad\boldsymbol{r}^{\left(-3\right)}=\begin{pmatrix}-2\\0\\1\end{pmatrix}.$$

Note that the nonhomogeneous term is exactly

$$\boldsymbol{f}\left(x\right)=e^{-x}\begin{pmatrix}-2\\-3\\2\end{pmatrix}=-e^{-x}\boldsymbol{r}^{\left(-1\right)},$$

i.e. the nonhomogeneous vector is in resonance with the eigenvalue $\lambda=-1$. By **Corollary 3** (General Solution and Initial-Value Solution of a Constant-Coefficient Nonhomogeneous Linear System), taking $x_0=0,\ \boldsymbol{y}_0=\boldsymbol{0}$, the solution of the initial value problem is

$$\boldsymbol{y}\left(x\right)=\int_0^x e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds.$$

Since $\boldsymbol{r}^{\left(-1\right)}$ is the eigenvector for $\lambda=-1$, we have $e^{\left(x-s\right)A}\boldsymbol{r}^{\left(-1\right)}=e^{-\left(x-s\right)}\boldsymbol{r}^{\left(-1\right)}$, so

$$\boldsymbol{y}\left(x\right)=-\boldsymbol{r}^{\left(-1\right)}\int_0^x e^{-\left(x-s\right)}e^{-s}\,ds=-\boldsymbol{r}^{\left(-1\right)}e^{-x}\int_0^x 1\,ds=-xe^{-x}\boldsymbol{r}^{\left(-1\right)}.$$

Substituting $\boldsymbol{r}^{\left(-1\right)}=\left(2,3,-2\right)^T$, the solution is

$$\boldsymbol{y}\left(x\right)=xe^{-x}\begin{pmatrix}-2\\-3\\2\end{pmatrix}.$$

$\blacksquare$

### Problem 7

(Problem 6-2, Problem 4) Solve the system

$$\frac{d}{dt}\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}a&-b\\b&a\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix},$$

where $a$ and $b$ are real constants and $b\neq0$.

### Solution to Problem 7

Denote $A=\begin{pmatrix}a&-b\\b&a\end{pmatrix}$. First find the eigenvalues. The characteristic equation is

$$\det\left(A-\lambda E\right)=\left(a-\lambda\right)^2+b^2=0,$$

so $\lambda=a\pm ib$. For $\lambda=a+ib$, solve $\left(A-\left(a+ib\right)E\right)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{pmatrix}-ib&-b\\b&-ib\end{pmatrix}\begin{pmatrix}r_1\\r_2\end{pmatrix}=\boldsymbol{0},$$

From the first row we get $-ir_1-r_2=0$; take $\boldsymbol{r}=\left(1,-i\right)^T$. By **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution), we get the complex solution

$$\boldsymbol{y}_1=e^{\left(a+ib\right)t}\begin{pmatrix}1\\-i\end{pmatrix}.$$

By **Remark 2** (Method for Extracting Real Solutions from Complex Solutions), using $e^{\left(a+ib\right)t}=e^{at}\left(\cos bt+i\sin bt\right)$ and taking real and imaginary parts, gives

$$\boldsymbol{u}\left(t\right)=e^{at}\begin{pmatrix}\cos bt\\\sin bt\end{pmatrix},\quad\boldsymbol{v}\left(t\right)=e^{at}\begin{pmatrix}\sin bt\\-\cos bt\end{pmatrix}.$$

By **Theorem 6.5** (Fundamental Matrix with $n$ Distinct Eigenvalues), the general solution is

$$\begin{pmatrix}x\\y\end{pmatrix}=C_1e^{at}\begin{pmatrix}\cos bt\\\sin bt\end{pmatrix}+C_2e^{at}\begin{pmatrix}\sin bt\\-\cos bt\end{pmatrix},$$

where $C_1,C_2$ are arbitrary constants. $\blacksquare$

### Problem 8

(Problem 6-2, Problem 5) Prove: every solution of the constant-coefficient homogeneous linear system $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ tends to zero as $x\to+\infty$ if and only if all eigenvalues of the coefficient matrix $A$ have negative real part.

### Solution to Problem 8

By **Theorem 6.6** (Fundamental Matrix of a Constant-Coefficient Homogeneous Linear System with Repeated Eigenvalues), every solution of the system is a linear combination of vector functions of the form

$$e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_\lambda-1}}{\left(n_\lambda-1\right)!}\boldsymbol{r}_{n_\lambda-1}\right)$$

where $\lambda$ is an eigenvalue of $A$. Denote $\alpha=\mathrm{Re}\,\lambda$; then the norm of the above function satisfies the estimate

$$\left|e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots\right)\right|\le e^{\alpha x}\left(M_0+M_1x+\cdots+M_{n_\lambda-1}x^{n_\lambda-1}\right),$$

where $M_k$ are constants.

First prove sufficiency. Suppose all eigenvalues of $A$ have negative real part, i.e. for each eigenvalue $\lambda$, $\alpha=\mathrm{Re}\,\lambda<0$. Since polynomial functions grow slower than the decay of the exponential, for any $k\ge0$ we have $x^ke^{\alpha x}\to0\ \left(x\to+\infty\right)$; hence the right-hand side tends to zero, and every solution of the system tends to zero.

Next prove necessity. Suppose for contradiction that $A$ has some eigenvalue $\lambda_j$ with $\alpha_j=\mathrm{Re}\,\lambda_j\ge0$. By **Lemma 6.6** (Necessary and Sufficient Condition for a System to Have an Exponential Nonzero Solution), take the eigenvector $\boldsymbol{r}_j\neq\boldsymbol{0}$ corresponding to $\lambda_j$; then $\boldsymbol{y}=e^{\lambda_j x}\boldsymbol{r}_j$ is a nonzero solution of the system. When $\alpha_j>0$, $\left\|\boldsymbol{y}\right\|=e^{\alpha_j x}\left\|\boldsymbol{r}_j\right\|\to+\infty$; when $\alpha_j=0$, if $\lambda_j=0$ then $\boldsymbol{y}=\boldsymbol{r}_j$ is a nonzero constant vector, and if $\lambda_j=i\beta\ \left(\beta\neq0\right)$ then the norm of $\boldsymbol{y}=e^{i\beta x}\boldsymbol{r}_j$ is constantly $\left\|\boldsymbol{r}_j\right\|$ and does not tend to zero. All these contradict the stated conclusion. Hence all eigenvalues of $A$ must have negative real part. $\blacksquare$
