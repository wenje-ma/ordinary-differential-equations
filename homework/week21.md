# 作业 21

> **优级数与优函数**<br>假设有两个幂级数 $\sum_{i,j=0}^{\infty}a_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j$ 和 $\sum_{i,j=0}^{\infty}A_{ij}\left(x-x_0\right)^i\left(y-y_0\right)^j\ \left(A_{ij}\ge0\right)$, 其中系数 $a_{ij}$ 和 $A_{ij}$ 满足不等式 $\left|a_{ij}\right|\le A_{ij}\ \left(i,j=0,1,2,\cdots\right)$, 则称第二个幂级数是第一个的一个优级数(或强级数). 如果该优级数在区域 $D:\left|x-x_0\right|<\alpha,\ \left|y-y_0\right|<\beta$ 内又是收敛的, 则它的和函数 $F\left(x,y\right)$ 叫作原幂级数在 $D$ 内的一个优函数(或强函数).

> **定理 7.1**(柯西定理)<br>如果函数 $f\left(x,y\right)$ 在矩形区域 $R:\left|x-x_0\right|<\alpha,\ \left|y-y_0\right|<\beta$ 上可以展开成 $\left(x-x_0\right)$ 和 $\left(y-y_0\right)$ 的一个收敛的幂级数, 则初值问题 $\frac{dy}{dx}=f\left(x,y\right),\ y\left(x_0\right)=y_0$ 在 $x_0$ 点的邻域 $\left(x_0-\rho,x_0+\rho\right)$ 内有一个解析解 $y=y\left(x\right)$, 而且它是唯一的. 此处形式解的系数 $C_n=\frac{1}{n!}y^{\left(n\right)}\left(x_0\right)=P_n\left(a_{00},a_{01},a_{10},\cdots,a_{n-1,0}\right)$, 其中 $P_n$ 是关于各系数的正系数多项式, 只与标号 $n$ 有关而与函数 $f$ 无关.

> **附注 3**(优级数方法对微分方程组的应用)<br>优级数方法可以应用于微分方程组的情形. 考虑微分方程组的初值问题 $\frac{dy_k}{dx}=f_k\left(x,y_1,\cdots,y_n\right),\ y_k\left(0\right)=0\ \left(k=1,2,\cdots,n\right)$. 假设右端函数在区域 $\left|x\right|\le\alpha,\ \left|y_1\right|\le\beta,\ \cdots,\ \left|y_n\right|\le\beta$ 内可以展成收敛的幂级数, 则与引理 7.1 类似可证存在优函数, 再用与定理 7.1 同样的推理可知该初值问题在 $x=0$ 的某邻域内有收敛的幂级数解.

### 习题一

(习题 7-1 题2)设初值问题 $\left(E\right):\ y''+p\left(x\right)y'+q\left(x\right)y=0,\ y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0'$, 其中 $p\left(x\right)$ 和 $q\left(x\right)$ 在区间 $\left(x_0-a,x_0+a\right)$ 内可以展成 $\left(x-x_0\right)$ 的收敛的幂级数, 则 $\left(E\right)$ 的解析解 $y=y\left(x\right)$ 在 $\left(x_0-a,x_0+a\right)$ 内存在且唯一.

### 解答 习题一

将二阶方程化为一阶方程组. 令 $y_1=y,\ y_2=y'$, 则原方程等价于

$$
\begin{cases}\frac{dy_1}{dx}=y_2,\\\frac{dy_2}{dx}=-q\left(x\right)y_1-p\left(x\right)y_2,\end{cases}
$$

初值条件为 $y_1\left(x_0\right)=y_0,\ y_2\left(x_0\right)=y_0'$.

记右端函数 $f_1\left(x,y_1,y_2\right)=y_2,\ f_2\left(x,y_1,y_2\right)=-q\left(x\right)y_1-p\left(x\right)y_2$. 由于 $p\left(x\right)$ 和 $q\left(x\right)$ 在 $\left(x_0-a,x_0+a\right)$ 内可展成 $\left(x-x_0\right)$ 的收敛幂级数, 而 $f_1=y_2$ 是关于 $y_2$ 的一次式(天然解析), $f_2$ 是 $p\left(x\right),q\left(x\right)$ 与 $y_1,y_2$ 的乘积之和, 故 $f_1$ 和 $f_2$ 在 $x_0$ 附近关于 $\left(x,y_1,y_2\right)$ 是解析的.

由**附注 3**(优级数方法对微分方程组的应用), 该一阶方程组在 $x_0$ 的某邻域内存在唯一的收敛幂级数解 $\left(y_1\left(x\right),y_2\left(x\right)\right)$. 因此 $y=y_1\left(x\right)$ 在 $x_0$ 附近可展成 $\left(x-x_0\right)$ 的收敛幂级数, 即解析解存在且唯一.

进一步, 由于 $p\left(x\right)$ 和 $q\left(x\right)$ 的幂级数在整个区间 $\left(x_0-a,x_0+a\right)$ 内收敛, 在该区间内任取一点 $x^*$, 已得的解析解在 $x^*$ 处取有限值 $y\left(x^*\right),\ y'\left(x^*\right)$, 而 $p,q$ 在 $x^*$ 附近仍解析, 故可在 $x^*$ 处重新施用上述结论, 将解析解延拓. 由区间的连通性, 解析解在整个 $\left(x_0-a,x_0+a\right)$ 内存在且唯一. $\blacksquare$

### 习题二

(习题 7-1 题3)叙述并证明解析的微分方程的解关于初值和参数的解析性定理.

### 解答 习题二

**定理(解关于初值和参数的解析性). ** 设初值问题

$$
\frac{dy}{dx}=f\left(x,y,\lambda\right),\quad y\left(x_0\right)=y_0
$$

中 $f\left(x,y,\lambda\right)$ 在 $\left(x_0,y_0,\lambda_0\right)$ 的某邻域内关于 $\left(x,y,\lambda\right)$ 是解析的, 则解 $y=y\left(x,x_0,y_0,\lambda\right)$ 在 $\left(x_0,y_0,\lambda_0\right)$ 附近关于所有变量 $\left(x,x_0,y_0,\lambda\right)$ 是解析的.

**证明. ** 将 $x$ 平移, 令 $t=x-x_0$, 则方程变为

$$
\frac{dy}{dt}=f\left(t+x_0,y,\lambda\right),\quad y\left(0\right)=y_0.
$$

把 $x_0$ 和 $\lambda$ 视为附加的未知函数, 满足 $\frac{dx_0}{dt}=0$ 和 $\frac{d\lambda}{dt}=0$, 则得到方程组

$$
\begin{cases}\frac{dy}{dt}=f\left(t+x_0,y,\lambda\right),\\\frac{dx_0}{dt}=0,\\\frac{d\lambda}{dt}=0.\end{cases}
$$

右端函数 $f\left(t+x_0,y,\lambda\right)$ 关于 $\left(t,x_0,y,\lambda\right)$ 解析, 其余右端恒为零亦解析. 由**附注 3**(优级数方法对微分方程组的应用), 该方程组在 $t=0$ 附近有唯一的收敛幂级数解. 由于 $x_0\left(t\right)\equiv a,\ \lambda\left(t\right)\equiv b$ 为常数, 故 $y=y\left(t,a,y_0,b\right)$ 是 $t$ 的解析函数.

为说明 $y$ 关于 $\left(a,y_0,b\right)$ 的解析性, 注意形式幂级数 $y=\sum_{n=0}^{\infty}c_n\left(a,y_0,b\right)t^n$ 中的系数 $c_n$ 是 $f$ 在 $\left(a,y_0,b\right)$ 处各阶偏导数的多项式(由**定理 7.1**(柯西定理)证明中形式解系数的递推性质可知), 因而 $c_n$ 关于 $\left(a,y_0,b\right)$ 是解析的. 优级数法保证了幂级数在 $\left(a,y_0,b\right)$ 附近一致收敛, 故 $y$ 关于 $\left(a,y_0,b\right)$ 亦是解析的. $\blacksquare$
