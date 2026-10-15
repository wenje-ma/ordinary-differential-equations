# Assignment 30

> **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation and Characteristic Curves)<br>The characteristic equation of the first-order quasilinear equation $X\frac{\partial z}{\partial x}+Y\frac{\partial z}{\partial y}=Z$ is $\frac{dx}{X}=\frac{dy}{Y}=\frac{dz}{Z}$; its integral curves are called characteristic curves, and at each point they have the characteristic vector $\left(X,Y,Z\right)$ as their tangent vector. The integral surface $S$ determined by the solution $z=z\left(x,y\right)$ of the partial differential equation is woven from characteristic curves: the characteristic curve through every point on $S$ lies entirely on $S$.

> **Method of Characteristics** (Solution of the Initial Value Problem)<br>Given the initial curve $\Lambda:\ x=\alpha\left(\sigma\right),\ y=\beta\left(\sigma\right),\ z=\gamma\left(\sigma\right)$. Suppose the characteristic equation has two independent first integrals $\varphi=C_1,\ \psi=C_2$. Take a point $M$ on $\Lambda$; the characteristic curve through $M$ is $\varphi=\overline{C}_1,\ \psi=\overline{C}_2$, where $\overline{C}_1=\varphi\left(\alpha,\beta,\gamma\right),\ \overline{C}_2=\psi\left(\alpha,\beta,\gamma\right)$. Eliminating the parameter $\sigma$ gives a relation $E\left(\overline{C}_1,\overline{C}_2\right)=0$ between $\overline{C}_1,\overline{C}_2$; then $E\left(\varphi\left(x,y,z\right),\psi\left(x,y,z\right)\right)=0$ is the desired integral surface.

> **Remark on the Method of Characteristics** (The Solution Is Not Unique When the Initial Curve Is a Characteristic Curve)<br>If the characteristic curves drawn through each point of the initial curve $\Lambda$ intersect $\Lambda$ transversely at the point of intersection, then these characteristic curves form a unique smooth integral surface $z=z\left(x,y\right)$; but if the initial curve $\Lambda$ is itself a characteristic curve, then the characteristic curves through $\Lambda$ are just $\Lambda$ itself and cannot span a surface. In this case, any integral surface containing $\Lambda$ is a solution of the initial value problem, i.e. the solution exists but is not unique.

### Problem 1

(Problem 11-3, Problem 1) Solve the initial value problem $\begin{cases}\sqrt{x}\frac{\partial z}{\partial x}+\sqrt{y}\frac{\partial z}{\partial y}=\sqrt{z},\\ \text{通过初始曲线 }\Lambda:\ x=y=z.\end{cases}$

### Solution to Problem 1

By **Theorem 11.2** (Implicit General Solution of a Quasilinear Partial Differential Equation and Characteristic Curves), first find the characteristic equation

$$
\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}.
$$

From $\frac{dx}{\sqrt{x}}=\frac{dy}{\sqrt{y}}$ we integrate to get $\sqrt{x}-\sqrt{y}=C_1$; from $\frac{dy}{\sqrt{y}}=\frac{dz}{\sqrt{z}}$ we get $\sqrt{y}-\sqrt{z}=C_2$. These are two independent first integrals.

Now consider the initial curve $\Lambda:\ x=y=z$. Parameterize it as $x=y=z=\sigma$ ($\sigma>0$). Substituting into the two first integrals gives

$$
\overline{C}_1=\sqrt{\sigma}-\sqrt{\sigma}=0,\quad\overline{C}_2=\sqrt{\sigma}-\sqrt{\sigma}=0.
$$

No matter what value the parameter $\sigma$ takes, we have $\overline{C}_1=\overline{C}_2=0$, i.e. the initial curve $\Lambda$ is exactly the characteristic curve $\sqrt{x}-\sqrt{y}=0,\ \sqrt{y}-\sqrt{z}=0$ (i.e. $\sqrt{x}=\sqrt{y}=\sqrt{z}$) itself. By the **Remark on the Method of Characteristics** (The Solution Is Not Unique When the Initial Curve Is a Characteristic Curve), when the initial curve is itself a characteristic curve, the characteristic curves through $\Lambda$ are just $\Lambda$ itself and cannot span a surface; in this case, the solution of the initial value problem exists but is not unique.

Specifically, the integral surface of the original equation can be written as $\Phi\left(\sqrt{x}-\sqrt{y},\ \sqrt{y}-\sqrt{z}\right)=0$; to make it contain $\Lambda$, it suffices that $\Phi\left(0,0\right)=0$. There are infinitely many such $\Phi$, and they all give integral surfaces passing through $\Lambda$. Hence this initial value problem has infinitely many solutions, and the solution is not unique. $\blacksquare$
