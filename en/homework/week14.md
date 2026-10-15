# Assignment 14

> **Autonomous (Stationary) Differential Equations**<br>There is a class of differential equations that do not explicitly contain the independent variable; these are called autonomous (or stationary) differential equations. They can be reduced in order. For example, for a second-order autonomous equation $y''=f\left(y,y'\right)$, set $z=\frac{dy}{dx}$; then $y''=\frac{dz}{dx}=\frac{dz}{dy}\cdot\frac{dy}{dx}=z\frac{dz}{dy}$, reducing it to the first-order equation in $z=z\left(y\right)$: $z\frac{dz}{dy}=f\left(y,z\right)$.

> **First Integral**<br>A relation obtained by integrating a higher-order differential equation once (and hence containing one arbitrary constant) is called a first integral. For example, for the autonomous equation $y''=f\left(y,y'\right)$, multiplying the equation by $y'$, the left-hand side is exactly the total differential $\frac{d}{dx}\left[\frac{1}{2}\left(y'\right)^2-F\left(y\right)\right]$, where $F'\left(y\right)=-f\left(y,0\right)$ is a corresponding antiderivative; integrating directly gives a first integral.

> **Phase Plane, Orbits, and Phase Portrait**<br>For the second-order autonomous equation $\frac{d^2x}{dt^2}=f\left(x,\frac{dx}{dt}\right)$, in the phase plane $O\left(x,v\right)$ ($v=\frac{dx}{dt}$), the curve determined by the first integral $\frac{1}{2}v^2+V\left(x\right)=E$ is called an orbit; the distribution of orbits in the phase plane is called the phase portrait. Stationary points correspond to zero (trivial) solutions of the equation, and closed orbits represent periodic motion.

> **The Pendulum Equation and the Linear Pendulum Equation**<br>The equation of motion of a pendulum is $\frac{d^2\theta}{dt^2}+a^2\sin\theta=0$, where the constant $a=\sqrt{\frac{g}{l}}$, $g$ is the magnitude of gravitational acceleration, and $l$ is the pendulum length. Taking the first-order approximation of $\sin\theta$, $\sin\theta\approx\theta$, gives the linear pendulum equation $\frac{d^2\theta}{dt^2}+a^2\theta=0$, whose general solution is $\theta=A\sin\left(at+D\right)$, where $A,D$ are arbitrary constants, and the period of oscillation is $T=\frac{2\pi}{a}=2\pi\sqrt{\frac{l}{g}}$.

### Problem 1

(Problem 5-1, Problem 1) Use the linear pendulum equation to estimate the magnitude of gravitational acceleration $g$ at the reader's location.

### Solution to Problem 1

By **The Pendulum Equation and the Linear Pendulum Equation**, the linearized pendulum equation is $\theta''+a^2\theta=0$, where $a=\sqrt{\frac{g}{l}}$, and its general solution is $\theta=A\sin\left(at+D\right)$; hence the period of small oscillations of the pendulum is

$$
T=\frac{2\pi}{a}=2\pi\sqrt{\frac{l}{g}}.
$$

Solving for the magnitude of gravitational acceleration gives

$$
g=\frac{4\pi^2l}{T^2}.
$$

In practice, suspend a small weight by a thin string to make a pendulum, measure the length $l$ from the suspension point to the center of mass of the weight as the pendulum length; let it swing freely at small angle, use a stopwatch to measure the total time $t_N$ for $N$ complete oscillations, and average to get the period $T=\frac{t_N}{N}$ (measuring several times and averaging reduces error); substitute into the above to get the magnitude of gravitational acceleration $g$ at the location.

$\blacksquare$

### Problem 2

(Problem 5-1, Problem 2) If in the nonlinear pendulum equation one takes the third-order approximation of $\sin x$, i.e. $\sin x\approx x-\frac{1}{6}x^3$, then one obtains the third-order approximate pendulum equation $\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)=0$. Use this to prove that pendulum oscillations are not isochronous, and that its phase portrait shows that precession can occur.

### Solution to Problem 2

By the **First Integral**, multiply the equation $\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)=0$ by $\frac{dx}{dt}$ to get

$$
\frac{dx}{dt}\cdot\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)\frac{dx}{dt}=0.
$$

The left-hand side is a total differential; integrating directly gives the first integral

$$
\frac{1}{2}\left(\frac{dx}{dt}\right)^2+\frac{a^2}{2}x^2-\frac{a^2}{24}x^4=E,
$$

where $E$ is an arbitrary constant. Let $v=\frac{dx}{dt}$; then the orbit equation in the phase plane $O\left(x,v\right)$ is

$$
v^2=2E-a^2x^2+\frac{a^2}{12}x^4.
$$

First find the stationary points. From $v=0$ and $x''=-a^2\left(x-\frac{1}{6}x^3\right)=0$, we get $x=0$ or $x=\pm\sqrt{6}$. Linearizing near $x=0$ gives $x''+a^2x=0$, so $\left(0,0\right)$ is a center (closed orbits surround it, corresponding to oscillation); linearizing near $x=\pm\sqrt{6}$ gives $u''-2a^2u=0$, so $\left(\pm\sqrt{6},0\right)$ are saddle points. At the saddle points, the energy is $E_*=\frac{a^2}{2}\cdot 6-\frac{a^2}{24}\cdot 36=\frac{3}{2}a^2$, and the orbit through the saddle point is the separatrix.

(1) Prove that oscillations are not isochronous. Consider a closed orbit with amplitude $A$ ($0<A<\sqrt{6}$); it turns around at $x=A$ (i.e. $v=0$), so $E=\frac{a^2}{2}A^2-\frac{a^2}{24}A^4$. The period of oscillation is

$$
T\left(A\right)=4\int_0^A\frac{dx}{\sqrt{2\left[E-\left(\frac{a^2}{2}x^2-\frac{a^2}{24}x^4\right)\right]}}.
$$

Simplifying the integrand gives

$$
2\left[E-\left(\frac{a^2}{2}x^2-\frac{a^2}{24}x^4\right)\right]=a^2\left(A^2-x^2\right)\left[1-\frac{A^2+x^2}{12}\right].
$$

Make the substitution $x=A\sin\varphi$; then $dx=A\cos\varphi\,d\varphi$, and $\sqrt{A^2-x^2}=A\cos\varphi$, so

$$
T\left(A\right)=\frac{4}{a}\int_0^{\frac{\pi}{2}}\frac{d\varphi}{\sqrt{1-\frac{A^2}{12}\left(1+\sin^2\varphi\right)}}.
$$

When $A\to 0$, $T\left(A\right)\to\frac{4}{a}\cdot\frac{\pi}{2}=\frac{2\pi}{a}$, the period of the linear pendulum. When $0<A<\sqrt{6}$, the denominator of the integrand is $<1$, so the integrand is $>1$, and hence $T\left(A\right)>\frac{2\pi}{a}$; moreover, the larger $A$, the smaller the denominator and the larger $T\left(A\right)$. Therefore the period $T$ varies with the amplitude $A$, i.e. pendulum oscillations are not isochronous. Also, when $A\to\sqrt{6}^{-}$, the denominator tends to zero at $\varphi=\frac{\pi}{2}$, and the period $T\left(A\right)\to+\infty$.

(2) Show that precession can occur on the phase portrait. When the energy $E>\frac{3}{2}a^2$, the right-hand side of the first integral $2E-a^2x^2+\frac{a^2}{12}x^4\to+\infty$ ($\left|x\right|\to\infty$), so $v=\frac{dx}{dt}$ is never zero and does not change sign: when $v>0$, $x\left(t\right)$ increases monotonically; when $v<0$, $x\left(t\right)$ decreases monotonically. The orbit no longer turns around and closes, but bypasses the two saddle points $\left(\pm\sqrt{6},0\right)$ and extends in the direction of increasing $\left|x\right|$. On the phase portrait these are the upper and lower orbits outside the separatrix, corresponding to the pendulum rotating continuously past its highest point, i.e. precession occurs.

$\blacksquare$
