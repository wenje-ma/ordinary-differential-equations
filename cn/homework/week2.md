# 作业 2

> **恰当方程**(全微分方程)<br>考虑对称形式的一阶微分方程 $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$. 如果存在一个可微函数 $\Phi\left(x,y\right)$, 使得它的全微分为 $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy$, 亦即它的偏导数为 $\frac{\partial\Phi}{\partial x}=P\left(x,y\right),\ \frac{\partial\Phi}{\partial y}=Q\left(x,y\right)$, 则称该式为恰当方程或全微分方程. 当方程为恰当方程时, 可将它改写为全微分的形式 $d\Phi\left(x,y\right)=P\left(x,y\right)dx+Q\left(x,y\right)dy=0$, 从而 $\Phi\left(x,y\right)=C$, 其中 $C$ 为任意常数, 称 $\Phi\left(x,y\right)=C$ 为方程的一个通积分.

> **定理 2.1**(恰当方程的判别与通积分公式)<br>设函数 $P\left(x,y\right)$ 和 $Q\left(x,y\right)$ 在区域 $R:\alpha<x<\beta,\ \gamma<y<\delta$ 上连续, 且有连续的一阶偏导数 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$, 则微分方程 $P\left(x,y\right)dx+Q\left(x,y\right)dy=0$ 是恰当方程的充要条件为恒等式 $$\frac{\partial}{\partial y}P\left(x,y\right)\equiv\frac{\partial}{\partial x}Q\left(x,y\right)$$ 在 $R$ 内成立. 而且当该式成立时, 方程的通积分为 $$\int_{x_0}^{x}P\left(x,y\right)dx+\int_{y_0}^{y}Q\left(x_0,y\right)dy=C,$$ 或者 $$\int_{x_0}^{x}P\left(x,y_0\right)dx+\int_{y_0}^{y}Q\left(x,y\right)dy=C,$$ 其中 $\left(x_0,y_0\right)$ 是 $R$ 中任意取定的一点.

### 习题一

(习题 2-1 题3)判断下列方程是否为恰当方程, 并且对恰当方程求解: $\left(ax+by\right)dx+\left(bx+cy\right)dy=0$($a,b,c$ 为常数).

### 解答 习题一

记 $P\left(x,y\right)=ax+by,\ Q\left(x,y\right)=bx+cy$. 由**定理 2.1**(恰当方程的判别与通积分公式), 只需检查 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$ 是否恒等. 计算得
$$
\frac{\partial P}{\partial y}=b,\quad\frac{\partial Q}{\partial x}=b.
$$

故 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, 方程是恰当方程. 令 $\Phi\left(x,y\right)$ 满足
$$
\frac{\partial\Phi}{\partial x}=ax+by,\quad\frac{\partial\Phi}{\partial y}=bx+cy.
$$

对第一式关于 $x$ 积分, 得
$$
\Phi\left(x,y\right)=\frac{a}{2}x^2+bxy+\psi\left(y\right).
$$

代入第二式, 得 $bx+\psi'\left(y\right)=bx+cy$, 即 $\psi'\left(y\right)=cy$, 故 $\psi\left(y\right)=\frac{c}{2}y^2$(省略积分常数). 因此方程的通积分为
$$
\Phi\left(x,y\right)=\frac{a}{2}x^2+bxy+\frac{c}{2}y^2=C.
$$

$\blacksquare$

### 习题二

(习题 2-1 题6)判断下列方程是否为恰当方程, 并且对恰当方程求解: $\left(ye^x+2e^x+y^2\right)dx+\left(e^x+2xy\right)dy=0$.

### 解答 习题二

记 $P\left(x,y\right)=ye^x+2e^x+y^2,\ Q\left(x,y\right)=e^x+2xy$. 由**定理 2.1**(恰当方程的判别与通积分公式), 只需检查 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$ 是否恒等. 计算得
$$
\frac{\partial P}{\partial y}=e^x+2y,\quad\frac{\partial Q}{\partial x}=e^x+2y.
$$

故 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, 方程是恰当方程. 令 $\Phi\left(x,y\right)$ 满足
$$
\frac{\partial\Phi}{\partial x}=ye^x+2e^x+y^2,\quad\frac{\partial\Phi}{\partial y}=e^x+2xy.
$$

对第一式关于 $x$ 积分, 得
$$
\Phi\left(x,y\right)=ye^x+2e^x+xy^2+\psi\left(y\right).
$$

代入第二式, 得 $e^x+2xy+\psi'\left(y\right)=e^x+2xy$, 即 $\psi'\left(y\right)=0$, 取 $\psi\left(y\right)=0$. 因此方程的通积分为
$$
\Phi\left(x,y\right)=e^x\left(y+2\right)+xy^2=C.
$$

$\blacksquare$

### 习题三

(习题 2-1 题9)判断下列方程是否为恰当方程, 并且对恰当方程求解: $\frac{2s-1}{t}ds+\frac{s-s^2}{t^2}dt=0$.

### 解答 习题三

记 $P\left(s,t\right)=\frac{2s-1}{t},\ Q\left(s,t\right)=\frac{s-s^2}{t^2}$. 由**定理 2.1**(恰当方程的判别与通积分公式), 只需检查 $\frac{\partial P}{\partial t}$ 与 $\frac{\partial Q}{\partial s}$ 是否恒等. 计算得
$$
\frac{\partial P}{\partial t}=-\frac{2s-1}{t^2},\quad\frac{\partial Q}{\partial s}=\frac{1-2s}{t^2}=-\frac{2s-1}{t^2}.
$$

故 $\frac{\partial P}{\partial t}\equiv\frac{\partial Q}{\partial s}$, 方程是恰当方程. 令 $\Phi\left(s,t\right)$ 满足
$$
\frac{\partial\Phi}{\partial s}=\frac{2s-1}{t},\quad\frac{\partial\Phi}{\partial t}=\frac{s-s^2}{t^2}.
$$

对第一式关于 $s$ 积分, 得
$$
\Phi\left(s,t\right)=\frac{s^2-s}{t}+\psi\left(t\right).
$$

代入第二式, 得 $-\frac{s^2-s}{t^2}+\psi'\left(t\right)=\frac{s-s^2}{t^2}$. 由于 $-\left(s^2-s\right)=s-s^2$, 故 $\psi'\left(t\right)=0$, 取 $\psi\left(t\right)=0$. 因此方程的通积分为
$$
\Phi\left(s,t\right)=\frac{s^2-s}{t}=C.
$$

$\blacksquare$

### 习题四

(习题 2-1 题10)判断下列方程是否为恰当方程, 并且对恰当方程求解: $xf\left(x^2+y^2\right)dx+yf\left(x^2+y^2\right)dy=0$, 其中 $f\left(\cdot\right)$ 是连续可微的.

### 解答 习题四

记 $P\left(x,y\right)=xf\left(x^2+y^2\right),\ Q\left(x,y\right)=yf\left(x^2+y^2\right)$. 由**定理 2.1**(恰当方程的判别与通积分公式), 只需检查 $\frac{\partial P}{\partial y}$ 与 $\frac{\partial Q}{\partial x}$ 是否恒等. 由 $f$ 连续可微, 计算得
$$
\frac{\partial P}{\partial y}=2xyf'\left(x^2+y^2\right),\quad\frac{\partial Q}{\partial x}=2xyf'\left(x^2+y^2\right).
$$

故 $\frac{\partial P}{\partial y}\equiv\frac{\partial Q}{\partial x}$, 方程是恰当方程. 设 $F\left(u\right)$ 是 $f\left(u\right)$ 的一个原函数, 即 $F'\left(u\right)=f\left(u\right)$. 令 $\Phi\left(x,y\right)$ 满足
$$
\frac{\partial\Phi}{\partial x}=xf\left(x^2+y^2\right),\quad\frac{\partial\Phi}{\partial y}=yf\left(x^2+y^2\right).
$$

对第一式关于 $x$ 积分, 利用 $\int xf\left(x^2+y^2\right)dx=\frac{1}{2}F\left(x^2+y^2\right)$, 得
$$
\Phi\left(x,y\right)=\frac{1}{2}F\left(x^2+y^2\right)+\psi\left(y\right).
$$

代入第二式, 得 $yf\left(x^2+y^2\right)+\psi'\left(y\right)=yf\left(x^2+y^2\right)$, 即 $\psi'\left(y\right)=0$, 取 $\psi\left(y\right)=0$. 因此方程的通积分为
$$
\Phi\left(x,y\right)=\frac{1}{2}F\left(x^2+y^2\right)=C,
$$

即 $F\left(x^2+y^2\right)=C$, 其中 $F$ 为 $f$ 的原函数. $\blacksquare$
