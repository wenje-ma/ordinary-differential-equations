# 作业 18

> **存在和唯一性定理**(线性微分方程组初值问题)<br>线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 满足初值条件 $y\left(x_0\right)=y_0$ 的解 $y=y\left(x\right)$ 在区间 $\left(a,b\right)$ 上是存在和唯一的, 其中 $x_0\in\left(a,b\right)$ 和 $y_0\in\mathbb{R}^n$ 是任意给定的.

> **引理 6.1**(齐次线性方程组解的叠加原理)<br>设 $y=y_1\left(x\right)$ 和 $y=y_2\left(x\right)$ 是齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 的解, 则它们的线性组合 $y=C_1y_1\left(x\right)+C_2y_2\left(x\right)$ 也是该方程组的解, 其中 $C_1$ 和 $C_2$ 是任意常数.

> **引理 6.2**(齐次线性方程组解空间的维数)<br>齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 在区间 $\left(a,b\right)$ 上所有解组成的线性空间 $S$ 是 $n$ 维的, 其中 $n$ 是微分方程组的阶数.

> **定理 6.1**(齐次线性微分方程组的通解结构)<br>齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 在区间 $\left(a,b\right)$ 上有 $n$ 个线性无关的解 $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$, 而且它的通解为 $y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right)$, 其中 $C_1,C_2,\cdots,C_n$ 是任意常数. 通常称齐次线性微分方程组的 $n$ 个线性无关的解为一个基本解组.

> **引理 6.3**(朗斯基行列式的刘维尔公式)<br>设 $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ 是齐次线性微分方程组的 $n$ 个解, 其朗斯基行列式为 $W\left(x\right)$, 则 $$W\left(x\right)=W\left(x_0\right)e^{\int_{x_0}^{x}\mathrm{tr}\left[A\left(s\right)\right]ds},$$ 其中 $x_0\in\left(a,b\right)$, 而 $\mathrm{tr}\left[A\left(x\right)\right]$ 表示矩阵 $A\left(x\right)$ 的迹.

> **定理 6.2**(朗斯基行列式判别法)<br>齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y$ 的解组 $y_1\left(x\right),y_2\left(x\right),\cdots,y_n\left(x\right)$ 是线性无关的充要条件为 $W\left(x\right)\neq0\ \left(a< x< b\right)$.

> **推论 2**(基解矩阵的性质)<br>(1) 设 $\Phi\left(x\right)$ 是齐次线性微分方程组的一个基解矩阵, 则对于任一个非奇异的 $n$ 阶常数矩阵 $C$, 矩阵 $\Phi\left(x\right)C$ 也是该方程组的一个基解矩阵; (2) 设 $\Phi\left(x\right)$ 和 $\Psi\left(x\right)$ 都是该方程组的基解矩阵, 则必存在一个非奇异的 $n$ 阶常数矩阵 $C$, 使得 $\Psi\left(x\right)=\Phi\left(x\right)C$.

> **引理 6.4**(非齐次线性方程组解的结构)<br>如果 $\Phi\left(x\right)$ 是与非齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 相应的齐次线性微分方程组的一个基解矩阵, $y^*\left(x\right)$ 是非齐次方程组的一个特解, 则非齐次方程组的任一解 $y=\varphi\left(x\right)$ 可以表示为 $\varphi\left(x\right)=\Phi\left(x\right)c+y^*\left(x\right)$, 其中 $c$ 是一个与 $\varphi\left(x\right)$ 有关的常数列向量.

> **定理 6.3**(非齐次线性微分方程组的通解结构)<br>设 $\Phi\left(x\right)$ 是相应齐次线性微分方程组的一个基解矩阵, 则非齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 在区间 $\left(a,b\right)$ 上的通解可以表示为 $y=\Phi\left(x\right)c+\Phi\left(x\right)\int_{x_0}^{x}\Phi^{-1}\left(s\right)f\left(s\right)ds$, 其中 $c$ 是 $n$ 维的任意常数列向量.

### 习题一

(习题 6-1 题1(1))求出齐次线性微分方程组 $\frac{dy}{dt}=A\left(t\right)y$ 的通解, 其中 $A\left(t\right)=\begin{bmatrix}\frac{1}{t}&0\\0&\frac{1}{t}\end{bmatrix},\ t\neq0$.

### 解答 习题一

该方程组的分量形式为

$$\frac{dy_1}{dt}=\frac{1}{t}y_1,\quad\frac{dy_2}{dt}=\frac{1}{t}y_2.$$

两个方程相互独立, 分别求解. 对第一个方程分离变量积分, 得 $\ln\left|y_1\right|=\ln\left|t\right|+C_1$, 即 $y_1=C_1t$. 同理 $y_2=C_2t$. 因此通解为

$$y=C_1\begin{bmatrix}t\\0\end{bmatrix}+C_2\begin{bmatrix}0\\t\end{bmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题二

(习题 6-1 题1(3))求出齐次线性微分方程组 $\frac{dy}{dt}=A\left(t\right)y$ 的通解, 其中 $A\left(t\right)=\begin{bmatrix}0&1\\-1&0\end{bmatrix}$.

### 解答 习题二

该方程组的分量形式为

$$\frac{dy_1}{dt}=y_2,\quad\frac{dy_2}{dt}=-y_1.$$

由第一式得 $y_2=\frac{dy_1}{dt}$, 代入第二式, 得二阶方程

$$\frac{d^2y_1}{dt^2}+y_1=0.$$

其特征方程为 $r^2+1=0$, 根为 $r=\pm i$, 故 $y_1=C_1\cos t+C_2\sin t$. 从而 $y_2=\frac{dy_1}{dt}=-C_1\sin t+C_2\cos t$. 因此通解为

$$y=C_1\begin{bmatrix}\cos t\\-\sin t\end{bmatrix}+C_2\begin{bmatrix}\sin t\\\cos t\end{bmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题三

(习题 6-1 题2(2))求解非齐次线性微分方程组的初值问题: $\frac{dx}{dt}=\frac{2t}{1+t^2}x,\ \frac{dy}{dt}=-\frac{1}{t}y+x+t\ \left(t> 0\right),\ x\left(1\right)=0,\ y\left(1\right)=\frac{4}{3}$.

### 解答 习题三

先解关于 $x$ 的方程 $\frac{dx}{dt}=\frac{2t}{1+t^2}x$. 分离变量积分, 得 $\ln\left|x\right|=\ln\left(1+t^2\right)+C$, 即 $x=C\left(1+t^2\right)$. 代入初值 $x\left(1\right)=0$, 得 $C\left(1+1\right)=0$, 故 $C=0$, 从而 $x\left(t\right)\equiv0$.

将 $x\equiv0$ 代入关于 $y$ 的方程, 得一阶线性方程

$$\frac{dy}{dt}+\frac{1}{t}y=t.$$

积分因子为 $\mu\left(t\right)=e^{\int\frac{1}{t}dt}=t$, 乘以方程两端得

$$\frac{d}{dt}\left(ty\right)=t^2.$$

积分得 $ty=\frac{t^3}{3}+C$, 即 $y=\frac{t^2}{3}+\frac{C}{t}$. 代入初值 $y\left(1\right)=\frac{4}{3}$, 得 $\frac{4}{3}=\frac{1}{3}+C$, 故 $C=1$. 因此所求解为

$$x\left(t\right)\equiv0,\quad y\left(t\right)=\frac{t^2}{3}+\frac{1}{t}.$$

$\blacksquare$

### 习题四

(习题 6-1 题3)试证向量函数组 $\begin{bmatrix}1\\0\\0\end{bmatrix},\ \begin{bmatrix}x\\0\\0\end{bmatrix},\ \begin{bmatrix}x^2\\0\\0\end{bmatrix}$ 在任意区间 $\left(a,b\right)$ 上线性无关.

### 解答 习题四

设存在常数 $C_1,C_2,C_3$, 使得对一切 $x\in\left(a,b\right)$ 有

$$C_1\begin{bmatrix}1\\0\\0\end{bmatrix}+C_2\begin{bmatrix}x\\0\\0\end{bmatrix}+C_3\begin{bmatrix}x^2\\0\\0\end{bmatrix}=\begin{bmatrix}0\\0\\0\end{bmatrix}.$$

比较第一分量, 得多项式恒等式

$$C_1+C_2x+C_3x^2=0\quad\left(a< x< b\right).$$

由于非零多项式在任一区间上不可能恒等于零, 故必有 $C_1=C_2=C_3=0$. 由向量函数组线性无关的定义, 该向量函数组在任意区间 $\left(a,b\right)$ 上线性无关. $\blacksquare$

### 习题五

(习题 6-1 题4)试证基解矩阵完全决定齐次线性微分方程组, 即如果方程组 $\frac{dy}{dx}=A\left(x\right)y$ 与 $\frac{dy}{dx}=B\left(x\right)y$ 有一个相同的基解矩阵, 则 $A\left(x\right)\equiv B\left(x\right)$.

### 解答 习题五

设 $\Phi\left(x\right)$ 是两个方程组相同的基解矩阵. 由于 $\Phi\left(x\right)$ 是 $\frac{dy}{dx}=A\left(x\right)y$ 的基解矩阵, 故 $\Phi'\left(x\right)=A\left(x\right)\Phi\left(x\right)$. 又由于 $\Phi\left(x\right)$ 也是 $\frac{dy}{dx}=B\left(x\right)y$ 的基解矩阵, 故 $\Phi'\left(x\right)=B\left(x\right)\Phi\left(x\right)$. 因此

$$A\left(x\right)\Phi\left(x\right)=B\left(x\right)\Phi\left(x\right),$$

即 $\left(A\left(x\right)-B\left(x\right)\right)\Phi\left(x\right)=0$. 由于 $\Phi\left(x\right)$ 是基解矩阵, 由**定理 6.2**(朗斯基行列式判别法), 其朗斯基行列式 $\det\left[\Phi\left(x\right)\right]\neq0$, 故 $\Phi\left(x\right)$ 可逆. 上式两端右乘 $\Phi^{-1}\left(x\right)$, 得

$$A\left(x\right)-B\left(x\right)=0,$$

即 $A\left(x\right)\equiv B\left(x\right)$. $\blacksquare$

### 习题六

(习题 6-1 题6)设当 $a< x< b$ 时, 非齐次线性微分方程组 $\frac{dy}{dx}=A\left(x\right)y+f\left(x\right)$ 中的 $f\left(x\right)$ 不恒为零. 证明: 该方程组有且至多有 $\left(n+1\right)$ 个线性无关解.

### 解答 习题六

先证至多有 $n+1$ 个线性无关解. 设 $y^*\left(x\right)$ 是非齐次方程组的一个特解, $y_1^*\left(x\right),y_2^*\left(x\right),\cdots,y_m^*\left(x\right)$ 是该方程组的任意 $m$ 个解. 由**引理 6.4**(非齐次线性方程组解的结构), 两个非齐次解之差是相应齐次方程组的解, 故 $y_i^*\left(x\right)-y^*\left(x\right)\ \left(i=1,2,\cdots,m\right)$ 都是齐次方程组 $\frac{dy}{dx}=A\left(x\right)y$ 的解. 由**引理 6.2**(齐次线性方程组解空间的维数), 齐次解空间是 $n$ 维的, 故这 $m$ 个齐次解中线性无关的至多 $n$ 个. 从而 $y_1^*,y_2^*,\cdots,y_m^*$ 中线性无关的至多 $n+1$ 个(加上 $y^*$ 本身).

再证存在 $n+1$ 个线性无关解. 由**定理 6.1**(齐次线性微分方程组的通解结构), 取齐次方程组的一个基本解组 $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$. 再由**存在和唯一性定理**(线性微分方程组初值问题), 取非齐次方程组的一个特解 $y^*\left(x\right)$. 考虑 $n+1$ 个解:

$$y^*\left(x\right),\quad y^*\left(x\right)+\varphi_1\left(x\right),\quad\cdots,\quad y^*\left(x\right)+\varphi_n\left(x\right).$$

设存在常数 $C_0,C_1,\cdots,C_n$, 使得

$$C_0y^*\left(x\right)+C_1\left(y^*\left(x\right)+\varphi_1\left(x\right)\right)+\cdots+C_n\left(y^*\left(x\right)+\varphi_n\left(x\right)\right)=0.$$

整理得

$$\left(C_0+C_1+\cdots+C_n\right)y^*\left(x\right)+C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)=0.$$

记 $k=C_0+C_1+\cdots+C_n$. 若 $k\neq0$, 则 $y^*\left(x\right)=-\frac{1}{k}\left(C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)\right)$, 即 $y^*$ 是齐次方程组的解. 但 $y^*$ 是非齐次方程组的特解且 $f\left(x\right)\not\equiv0$, 若 $y^*$ 满足齐次方程, 代入非齐次方程将得 $f\left(x\right)\equiv0$, 矛盾. 故 $k=0$, 即 $C_0+C_1+\cdots+C_n=0$. 此时等式化为

$$C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)=0.$$

由 $\varphi_1,\cdots,\varphi_n$ 是基本解组(线性无关), 得 $C_1=\cdots=C_n=0$. 再由 $C_0+C_1+\cdots+C_n=0$, 得 $C_0=0$. 因此这 $n+1$ 个解线性无关.

综上, 非齐次线性微分方程组恰有 $n+1$ 个线性无关解. $\blacksquare$
