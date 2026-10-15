# Assignment 27

> **Theorem 10.7** (Global First Integrals and Conservative Systems)<br>For a three-dimensional autonomous system $\frac{dx}{dt}=E,\ \frac{dy}{dt}=F,\ \frac{dz}{dt}=G$, if it has two mutually independent stationary first integrals $\Phi_1=C_1,\ \Phi_2=C_2$ in a global region $\Omega$, then the system is a conservative system in $\Omega$ or is equivalent to one. The derivation is: from the necessary and sufficient condition for first integrals $\frac{\partial\Phi_i}{\partial x}E+\frac{\partial\Phi_i}{\partial y}F+\frac{\partial\Phi_i}{\partial z}G\equiv0$, solve that $\left(E,F,G\right)$ is proportional to the Jacobian quantities $L=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(y,z\right)},\ M=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(z,x\right)},\ N=\frac{D\left(\Phi_1,\Phi_2\right)}{D\left(x,y\right)}$, i.e. $L=\mu E,\ M=\mu F,\ N=\mu G$; then from the identity $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$, we get $\frac{\partial\left(\mu E\right)}{\partial x}+\frac{\partial\left(\mu F\right)}{\partial y}+\frac{\partial\left(\mu G\right)}{\partial z}\equiv0$.

> **Divergence and Conservative Systems**<br>The divergence of the vector field $\left(E,F,G\right)$ is $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}$. When $\mu$ is a constant, the above becomes $\frac{\partial E}{\partial x}+\frac{\partial F}{\partial y}+\frac{\partial G}{\partial z}=0$, i.e. the divergence is zero, and the system is called a conservative system. When $\mu$ is not a constant, $\mu\left(x,y,z\right)$ is called a quasi-integrating factor; in this case the original system, after the parameter transformation $d\tau=\frac{dt}{\mu}$, becomes the equivalent conservative system $\frac{dx}{d\tau}=\mu E,\ \frac{dy}{d\tau}=\mu F,\ \frac{dz}{d\tau}=\mu G$.

> **Theory of Exact Equations and Integrating Factors from Chapter 2**<br>For a first-order equation in symmetric form $Pdx+Qdy=0$, the necessary and sufficient condition for it to be exact (i.e. there exists $\Phi$ such that $d\Phi=Pdx+Qdy$) is $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$; when it is not exact, if there is a factor $\mu\left(x,y\right)$ such that $\mu Pdx+\mu Qdy=0$ is exact, then $\mu$ is called an integrating factor of the equation.

### Problem 1

(Problem 10-4, Problem 1) Establish a theory analogous to Theorem 10.7 for a general autonomous system $\frac{dx_i}{dt}=f_i\left(x_1,\cdots,x_n\right)$ ($i=1,2,\cdots,n,\ n\ge2$); and when $n=2$, show that the above analysis is exactly the global theory of exact equations or integrating factors from Chapter 2.

### Solution to Problem 1

Step 1: generalize **Theorem 10.7** (Global First Integrals and Conservative Systems) to $n$ dimensions. Suppose the $n$-dimensional autonomous system $\frac{dx_i}{dt}=f_i$ ($i=1,\cdots,n$) has $n-1$ mutually independent stationary first integrals $\Phi_1,\cdots,\Phi_{n-1}$ in a region $\Omega$. By the necessary and sufficient condition for first integrals, we have the identity

$$
\sum_{i=1}^n f_i\frac{\partial\Phi_k}{\partial x_i}\equiv0\quad\left(k=1,\cdots,n-1\right).
$$

Since $\Phi_1,\cdots,\Phi_{n-1}$ are mutually independent, these $n-1$ gradients $\nabla\Phi_k$ are linearly independent, and the vector $f=\left(f_1,\cdots,f_n\right)$ is perpendicular to all of them, so $f$ lies in the one-dimensional orthogonal complement. Define the generalized cross product vector

$$
L_i=\left(-1\right)^{i-1}\frac{D\left(\Phi_1,\cdots,\Phi_{n-1}\right)}{D\left(x_1,\cdots,\widehat{x_i},\cdots,x_n\right)}\quad\left(i=1,\cdots,n\right),
$$

where $\widehat{x_i}$ denotes the omission of the variable $x_i$. By Laplace expansion of the determinant, we have $\sum_{i=1}^nL_i\frac{\partial\Phi_k}{\partial x_i}\equiv0$, so $L$ is proportional to $f$:

$$
L_i=\mu f_i\quad\left(i=1,\cdots,n\right).
$$

On the other hand, by the same reasoning as $\frac{\partial L}{\partial x}+\frac{\partial M}{\partial y}+\frac{\partial N}{\partial z}\equiv0$ in three dimensions (requiring each $\Phi_k$ to be twice continuously differentiable), we have

$$
\sum_{i=1}^n\frac{\partial L_i}{\partial x_i}\equiv0.
$$

Substituting $L_i=\mu f_i$, we get

$$
\sum_{i=1}^n\frac{\partial\left(\mu f_i\right)}{\partial x_i}\equiv0.
$$

When $\mu$ is a constant, this is $\sum_{i=1}^n\frac{\partial f_i}{\partial x_i}=0$, the system has zero divergence and is conservative; when $\mu$ is not a constant, $\mu$ is a quasi-integrating factor, and after the parameter transformation $d\tau=\frac{dt}{\mu}$ the system becomes conservative. Thus we obtain the generalized conclusion: if an $n$-dimensional autonomous system has $n-1$ mutually independent stationary first integrals in a global region, then it is conservative or equivalent to a conservative system.

Step 2: take $n=2$. Then the system is $\frac{dx}{dt}=f_1,\ \frac{dy}{dt}=f_2$, and along trajectories $\frac{dy}{dx}=\frac{f_2}{f_1}$. It has only $n-1=1$ first integral $\Phi\left(x,y\right)=C$. By the above generalized cross product, taking $i=1,2$:

$$
L_1=\frac{D\left(\Phi\right)}{D\left(y\right)}=\frac{\partial\Phi}{\partial y},\quad L_2=-\frac{D\left(\Phi\right)}{D\left(x\right)}=-\frac{\partial\Phi}{\partial x},
$$

so $L_i=\mu f_i$ becomes $\frac{\partial\Phi}{\partial y}=\mu f_1,\ -\frac{\partial\Phi}{\partial x}=\mu f_2$. The generalized divergence identity becomes

$$
\frac{\partial L_1}{\partial x}+\frac{\partial L_2}{\partial y}
=\frac{\partial\left(\mu f_1\right)}{\partial x}+\frac{\partial\left(\mu f_2\right)}{\partial y}\equiv0.
$$

Along the first integral solution, $d\Phi=\frac{\partial\Phi}{\partial x}dx+\frac{\partial\Phi}{\partial y}dy=-\mu f_2\,dx+\mu f_1\,dy=0$, i.e. the symmetric form $Pdx+Qdy=0$ where $P=-\mu f_2,\ Q=\mu f_1$. By **Theorem 2.1** (Criterion and General Integral Formula for Exact Equations), its exactness condition $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$ is exactly

$$
-\frac{\partial\left(\mu f_2\right)}{\partial y}=\frac{\partial\left(\mu f_1\right)}{\partial x},
$$

which is completely consistent with the divergence identity above. Therefore when $n=2$, the $\mu$ here is exactly the integrating factor from Chapter 2: when $\mu$ is a constant, the original equation is already exact; when $\mu$ is not a constant, it is the integrating factor that converts the original equation into an exact one. Hence the above global analysis is exactly the global theory of exact equations and integrating factors from Chapter 2. $\blacksquare$
