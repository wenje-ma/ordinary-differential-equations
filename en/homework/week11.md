# Assignment 11

> **Implicit First-Order Differential Equations**<br>As a supplement to the elementary integration methods of Chapter 2, this section discusses several special solution methods for the implicit first-order equation $$F\left(x,y,\frac{dy}{dx}\right)=0$$. Here "implicit" means that the derivative $\frac{dy}{dx}$ of the unknown function is not explicitly expressed as a function of $x,y$.

> **Differentiation Method**<br>Suppose from the implicit first-order equation one can explicitly solve for the unknown function $$y=f\left(x,p\right),$$ where $p=\frac{dy}{dx}$. Suppose the function $f\left(x,p\right)$ is continuously differentiable with respect to $\left(x,p\right)$; then differentiating the above with respect to $x$ gives $$\left[f_x\left(x,p\right)-p\right]dx+f_p\left(x,p\right)dp=0.$$ This is an explicit first-order differential equation in the variables $x$ and $p$. If one can find its general solution $p=u\left(x,C\right)$, then the general solution of the original equation is $y=f\left(x,u\left(x,C\right)\right)$; if its general solution is conveniently written in the form $x=v\left(p,C\right)$, then the general solution of the original equation can be written as $$\begin{cases}x=v\left(p,C\right),\\y=f\left(v\left(p,C\right),p\right),\end{cases}$$ where $p$ is regarded as a parameter.

> **Parametric Method**<br>Suppose the differential equation does not explicitly contain the independent variable, i.e. $$F\left(y,p\right)=0.$$ As a relation between $y$ and $p$, it generally represents several curves in the $Oyp$ plane. Suppose $$y=g\left(t\right),\quad p=h\left(t\right)$$ is a parametric representation of one of them, where $h\left(t\right)\neq0$. From $dy=p\,dx$ we get $dx=\frac{g'\left(t\right)}{h\left(t\right)}dt$, and integrating gives the general solution of the original equation $$x=\int\frac{g'\left(t\right)}{h\left(t\right)}dt+C,\quad y=g\left(t\right).$$ Similarly, for an equation that does not explicitly contain the unknown function, $F\left(x,p\right)=0$, one can take the parametric representation $x=f\left(t\right),\ p=h\left(t\right)$; then from $dy=p\,dx$ we get $dy=h\left(t\right)f'\left(t\right)dt$, and the general solution is $$y=\int h\left(t\right)f'\left(t\right)dt+C,\quad x=f\left(t\right).$$

### Problem 1

(Problem 4-1, Problem 1(1)) Solve the differential equation $2y=p^2+4px+2x^2$ (where $p=\frac{dy}{dx}$).

### Solution to Problem 1

By the **Differentiation Method**, first solve the equation for $y=f\left(x,p\right)$. The original equation is

$$
y=\frac{1}{2}p^2+2px+x^2.
$$

Differentiating with respect to $x$, noting that $\frac{dy}{dx}=p$, and $f_x=2p+2x,\ f_p=p+2x$, we get

$$
p=\left(2p+2x\right)+\left(p+2x\right)\frac{dp}{dx}.
$$

Rearranging gives

$$
-\left(p+2x\right)=\left(p+2x\right)\frac{dp}{dx}.
$$

Thus either $p+2x=0$, or $\frac{dp}{dx}=-1$.

When $\frac{dp}{dx}=-1$, $p=-x+C$; substituting back into $y=\frac{1}{2}p^2+2px+x^2$ gives the general solution

$$
y=-\frac{1}{2}x^2+Cx+\frac{C^2}{2}.
$$

When $p+2x=0$, i.e. $p=-2x$, substituting back gives the particular solution

$$
y=-x^2.
$$

where the particular solution $y=-x^2$ is not contained in the general solution. $\blacksquare$

### Problem 2

(Problem 4-1, Problem 1(3)) Solve the differential equation $2xp=2\tan y+p^3\cos^2 y$ (where $p=\frac{dy}{dx}$).

### Solution to Problem 2

By the **Differentiation Method**, solve the equation for $x=f\left(y,p\right)$ and regard $y$ as the independent variable, in which case $\frac{dx}{dy}=\frac{1}{p}$. The original equation is

$$
x=\frac{\tan y}{p}+\frac{p^2}{2}\cos^2 y.
$$

Differentiating with respect to $y$, where $\frac{\partial}{\partial y}\left(\frac{\tan y}{p}\right)=\frac{\sec^2 y}{p}$, $\frac{\partial}{\partial y}\left(\frac{p^2}{2}\cos^2 y\right)=-p^2\sin y\cos y$, $\frac{\partial}{\partial p}=-\frac{\tan y}{p^2}+p\cos^2 y$, we get

$$
\frac{1}{p}=\frac{\sec^2 y}{p}-p^2\sin y\cos y+\left(-\frac{\tan y}{p^2}+p\cos^2 y\right)\frac{dp}{dy}.
$$

Multiplying both sides by $p$ and rearranging, using $1-\sec^2 y=-\tan^2 y$, gives

$$
-\tan^2 y+p^3\sin y\cos y=\left(-\frac{\tan y}{p}+p^2\cos^2 y\right)\frac{dp}{dy}.
$$

Let $u=p\cos y$; then the left-hand side $=\frac{\sin y}{\cos^2 y}\left(u^3-\sin y\right)$, and the parenthesis on the right $=\frac{u^3-\sin y}{u}$, so the equation becomes

$$
\left(u^3-\sin y\right)\left(\frac{\sin y}{\cos^2 y}-\frac{1}{u}\frac{dp}{dy}\right)=0.
$$

When $\frac{\sin y}{\cos^2 y}=\frac{1}{u}\frac{dp}{dy}$, since $\frac{du}{dy}=\frac{dp}{dy}\cos y-p\sin y=\frac{u\sin y}{\cos y}-\frac{u\sin y}{\cos y}=0$, we get $u=C$, i.e. $p\cos y=C$. Substituting back into $x=\frac{\tan y}{p}+\frac{p^2}{2}\cos^2 y$, we get $\frac{\tan y}{p}=\frac{\sin y}{C}$ and $\frac{p^2}{2}\cos^2 y=\frac{C^2}{2}$, so the general solution is

$$
x=\frac{\sin y}{C}+\frac{C^2}{2},
$$

i.e. $\sin y=Cx-\frac{C^3}{2}$.

When $u^3=\sin y$, i.e. $\left(\sin y\right)^{1/3}=u$, substituting back gives $\frac{\tan y}{p}=\frac{\sin y}{u}=\left(\sin y\right)^{2/3}$ and $\frac{p^2}{2}\cos^2 y=\frac{u^2}{2}=\frac{1}{2}\left(\sin y\right)^{2/3}$, so the particular solution is

$$
x=\frac{3}{2}\left(\sin y\right)^{2/3}.
$$

$\blacksquare$

### Problem 3

(Problem 4-1, Problem 2(2)) Use the parametric method to solve the differential equation $x^2-3\left(\frac{dy}{dx}\right)^2=1$.

### Solution to Problem 3

By the **Parametric Method**, this equation does not explicitly contain the unknown function $y$, so it is of the type $F\left(x,p\right)=0$, where $p=\frac{dy}{dx}$. Take the parametric representation of the curve $x^2-3p^2=1$:

$$
x=\cosh t,\quad p=\frac{1}{\sqrt{3}}\sinh t.
$$

From $dy=p\,dx$, and $\frac{dx}{dt}=\sinh t$, we get

$$
dy=\frac{1}{\sqrt{3}}\sinh t\cdot\sinh t\,dt=\frac{1}{\sqrt{3}}\sinh^2 t\,dt.
$$

Integrating, using $\int\sinh^2 t\,dt=\frac{1}{2}\left(\sinh t\cosh t-t\right)$, gives

$$
y=\frac{1}{2\sqrt{3}}\left(\sinh t\cosh t-t\right)+C.
$$

Hence the general solution of the original equation is in parametric form

$$
\begin{cases}
x=\cosh t,\\
y=\frac{1}{2\sqrt{3}}\left(\sinh t\cosh t-t\right)+C.
\end{cases}
$$

$\blacksquare$

### Problem 4

(Problem 4-1, Problem 2(4)) Use the parametric method to solve the differential equation $x^3+\left(\frac{dy}{dx}\right)^3=4x\frac{dy}{dx}$.

### Solution to Problem 4

By the **Parametric Method**, this equation does not explicitly contain the unknown function $y$, so it is of the type $F\left(x,p\right)=0$, where $p=\frac{dy}{dx}$. For the curve $x^3+p^3=4xp$, take the parameter $p=tx$; substituting gives $x^3\left(1+t^3\right)=4tx^2$, so

$$
x=\frac{4t}{1+t^3},\quad p=\frac{4t^2}{1+t^3}.
$$

From $dy=p\,dx$, and $\frac{dx}{dt}=\frac{4\left(1-2t^3\right)}{\left(1+t^3\right)^2}$, we get

$$
dy=\frac{4t^2}{1+t^3}\cdot\frac{4\left(1-2t^3\right)}{\left(1+t^3\right)^2}dt=\frac{16t^2\left(1-2t^3\right)}{\left(1+t^3\right)^3}dt.
$$

Let $u=1+t^3$; then $du=3t^2dt$ and $1-2t^3=3-2u$, and integrating gives

$$
y=\frac{16}{3}\int\frac{3-2u}{u^3}du+C=-\frac{8}{u^2}+\frac{32}{3u}+C.
$$

Hence the general solution of the original equation is in parametric form

$$
\begin{cases}
x=\frac{4t}{1+t^3},\\
y=-\frac{8}{\left(1+t^3\right)^2}+\frac{32}{3\left(1+t^3\right)}+C.
\end{cases}
$$

$\blacksquare$
