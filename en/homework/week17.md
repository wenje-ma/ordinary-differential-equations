# Assignment 17

> **Theorem 5.3** (Continuous Differentiability of Solutions with Respect to a Parameter)<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y,\lambda\right)$ is continuous on the region $G:\left|x\right|\le a,\ \left|y\right|\le b,\ \left|\lambda-\lambda_0\right|\le c$ and has continuous partial derivatives with respect to $y$ and $\lambda$. Then the solution $y=\varphi\left(x,\lambda\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(0\right)=0$ is continuously differentiable on the region $D:\left|x\right|\le h,\ \left|\lambda-\lambda_0\right|\le c$, where $h=\min\left\{a,\frac{b}{M}\right\}$, and $M$ is an upper bound of $\left|f\left(x,y,\lambda\right)\right|$ on $G$.

> **Corollary to Theorem 5.3** (Continuous Differentiability of Solutions with Respect to Initial Values)<br>Suppose the $n$-dimensional vector-valued function $f\left(x,y\right)$ is continuous on the region $R:\left|x-x_0\right|\le a,\ \left|y-y_0\right|\le b$ and has a continuous partial derivative $f_y\left(x,y\right)$ with respect to $y$. Then the solution $y=\varphi\left(x,\eta\right)$ of the initial value problem $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=\eta$ is continuously differentiable on the region $D:\left|x-x_0\right|\le\frac{h}{2},\ \left|\eta-y_0\right|\le\frac{b}{2}$.

> **Variational Equation**<br>Suppose $y=\varphi\left(x;x_0,y_0,\lambda\right)$ is the solution of $\frac{dy}{dx}=f\left(x,y,\lambda\right),\ y\left(x_0\right)=y_0$. The integral equation equivalent to the Cauchy problem is $\varphi\left(x;x_0,y_0,\lambda\right)=y_0+\displaystyle\int_{x_0}^{x}f\left(s,\varphi\left(s;x_0,y_0,\lambda\right),\lambda\right)ds$. Denote $A\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial y}\left(x,\varphi,\lambda\right)$, $B\left(x,x_0,y_0,\lambda\right)=\frac{\partial f}{\partial\lambda}\left(x,\varphi,\lambda\right)$. Then $z=\frac{\partial\varphi}{\partial\lambda}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z+B\left(x,x_0,y_0,\lambda\right)$, $z\left(x_0\right)=0$; $z=\frac{\partial\varphi}{\partial y_0}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=1$; $z=\frac{\partial\varphi}{\partial x_0}$ satisfies $\frac{dz}{dx}=A\left(x,x_0,y_0,\lambda\right)z$, $z\left(x_0\right)=-f\left(x_0,y_0,\lambda\right)$. These equations are collectively called the variational equations of the original equation with respect to initial values and parameters.

> **Jacobian Matrix**<br>The Jacobian matrix of the vector-valued function $f\left(x,y,\lambda\right)=\left(f_1,\cdots,f_n\right)^T$ with respect to $y=\left(y_1,\cdots,y_n\right)^T$ is $f_y=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$, and with respect to the parameter $\lambda=\left(\lambda_1,\cdots,\lambda_m\right)^T$ is $f_\lambda=\left(\frac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. Differentiation of composite functions is performed by matrix multiplication: $\frac{\partial f\left(x,\varphi,\lambda\right)}{\partial\lambda_k}=\displaystyle\sum_{j=1}^{n}\frac{\partial f}{\partial y_j}\frac{\partial\varphi_j}{\partial\lambda_k}+\frac{\partial f}{\partial\lambda_k}$.

### Problem 1

(Problem 5-4, Problem 1) Using **Theorem 5.3** (Continuous Differentiability of Solutions with Respect to a Parameter) (in the case where $y$ is a column vector), prove that $z=\frac{\partial\varphi}{\partial\lambda}\left(x,\lambda\right)=\left(\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)\right)_{n\times m}$ satisfies the linear (variational) equation $\frac{dz}{dx}=A\left(x,\lambda\right)z+B\left(x,\lambda\right)$ and the initial condition $z\left(x_0,\lambda\right)=0$, where $A\left(x,\lambda\right)=f_y'\left(x,\varphi\left(x,\lambda\right),\lambda\right)=\left(\frac{\partial f_i}{\partial y_j}\right)_{n\times n}$, $B\left(x,\lambda\right)=f_\lambda'\left(x,\varphi\left(x,\lambda\right),\lambda\right)=\left(\frac{\partial f_i}{\partial\lambda_k}\right)_{n\times m}$. Also consider the corresponding variational equation in the case where $y$ is a row vector.

### Solution to Problem 1

Consider the Cauchy problem

$$
\frac{dy}{dx}=f\left(x,y,\lambda\right),\quad y\left(x_0\right)=y_0,
$$

where the initial value $y_0$ is fixed (independent of $\lambda$), $\lambda\in K\subset R^m$. By **Theorem 5.3** (Continuous Differentiability of Solutions with Respect to a Parameter), its solution $y=\varphi\left(x,\lambda\right)$ is continuously differentiable, so the partial derivative $z=\frac{\partial\varphi}{\partial\lambda}$ exists and is continuous.

By the integral-equation equivalent form in the **Variational Equation**, we have

$$
\varphi\left(x,\lambda\right)=y_0+\int_{x_0}^{x}f\left(s,\varphi\left(s,\lambda\right),\lambda\right)ds.
$$

Differentiate both sides with respect to $\lambda_k$. The left-hand side is $\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)=z_{ik}$. By the chain rule for **Jacobian Matrix**, the right-hand side is

$$
\frac{\partial\varphi_i}{\partial\lambda_k}\left(x,\lambda\right)=\int_{x_0}^{x}\left[\sum_{j=1}^{n}\frac{\partial f_i}{\partial y_j}\left(s,\varphi,\lambda\right)\frac{\partial\varphi_j}{\partial\lambda_k}\left(s,\lambda\right)+\frac{\partial f_i}{\partial\lambda_k}\left(s,\varphi,\lambda\right)\right]ds.
$$

Note that $\frac{\partial\varphi_j}{\partial\lambda_k}=z_{jk}$. Differentiating both sides with respect to $x$ gives

$$
\frac{\partial z_{ik}}{\partial x}=\sum_{j=1}^{n}A_{ij}\left(x,\lambda\right)z_{jk}\left(x,\lambda\right)+B_{ik}\left(x,\lambda\right),
$$

where $A_{ij}=\frac{\partial f_i}{\partial y_j}$, $B_{ik}=\frac{\partial f_i}{\partial\lambda_k}$. In matrix form,

$$
\frac{dz}{dx}=A\left(x,\lambda\right)z+B\left(x,\lambda\right).
$$

Initial condition: since $\varphi\left(x_0,\lambda\right)=y_0$ is independent of $\lambda$, $\frac{\partial\varphi}{\partial\lambda}\left(x_0,\lambda\right)=0$, so

$$
z\left(x_0,\lambda\right)=0.
$$

This proves the column vector case.

Row vector case: if $y$ is taken as a row vector (i.e. $y$ is a $1\times n$ row, and the system is written as $\frac{dy}{dx}=yA_{\text{行}}\left(x,\lambda\right)+e\left(x,\lambda\right)$), then the component differentiation formula $\frac{\partial z_{ik}}{\partial x}=\displaystyle\sum_{j=1}^{n}\frac{\partial f_i}{\partial y_j}z_{jk}+\frac{\partial f_i}{\partial\lambda_k}$ is unchanged, but the Jacobian matrix is multiplied on the right under the row-vector convention, and the variational equation is written as

$$
\frac{dz}{dx}=z\,A\left(x,\lambda\right)+B\left(x,\lambda\right),
$$

where $z=\frac{\partial\varphi}{\partial\lambda}$ and $B$ take the corresponding transposed arrangement (of order $m\times n$), and the initial condition remains $z\left(x_0,\lambda\right)=0$.

$\blacksquare$

### Problem 2

(Problem 5-4, Problem 2) In the corollary at the end of this section (i.e. **Corollary to Theorem 5.3** (Continuous Differentiability of Solutions with Respect to Initial Values)), find the differential equation and initial condition satisfied by $z=\frac{\partial\varphi}{\partial\eta}\left(x,\eta\right)$. (Only formal computation is required.)

### Solution to Problem 2

In **Corollary to Theorem 5.3** (Continuous Differentiability of Solutions with Respect to Initial Values), the Cauchy problem is

$$
\frac{dy}{dx}=f\left(x,y\right),\quad y\left(x_0\right)=\eta,
$$

where $f\left(x,y\right)$ is continuous and has a continuous partial derivative $f_y\left(x,y\right)$ with respect to $y$, and the solution is $y=\varphi\left(x,\eta\right)$.

By the integral-equation equivalent form in the **Variational Equation**, we have

$$
\varphi\left(x,\eta\right)=\eta+\int_{x_0}^{x}f\left(s,\varphi\left(s,\eta\right)\right)ds.
$$

Differentiating both sides with respect to $\eta$ (denote $z=\frac{\partial\varphi}{\partial\eta}$, an $n\times n$ matrix), by the chain rule for the **Jacobian Matrix**, gives

$$
z\left(x,\eta\right)=I_n+\int_{x_0}^{x}f_y\left(s,\varphi\left(s,\eta\right)\right)z\left(s,\eta\right)ds,
$$

where $I_n$ is the identity matrix of order $n$. Differentiating both sides with respect to $x$ gives the differential equation

$$
\frac{dz}{dx}=f_y\left(x,\varphi\left(x,\eta\right)\right)\,z\left(x,\eta\right).
$$

Initial condition: setting $x=x_0$ in the integral equation gives $\varphi\left(x_0,\eta\right)=\eta$, and differentiating with respect to $\eta$ gives

$$
z\left(x_0,\eta\right)=I_n.
$$

In the one-dimensional (scalar) case, this reduces to $\frac{dz}{dx}=f_y\left(x,\varphi\left(x,\eta\right)\right)z$, $z\left(x_0,\eta\right)=1$. This is the variational equation for the solution with respect to the initial value $\eta$ in the corollary.

$\blacksquare$
