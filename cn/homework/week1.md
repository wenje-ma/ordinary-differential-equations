# week1

> **基础知识: 初值问题 (柯西问题)**<br>对 $n$ 阶微分方程, 初值条件为 $y\left(x_0\right)=y_0$, $y'\left(x_0\right)=y_0'$, $\cdots$, $y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$.

> **基础知识: 微分方程的求解与积分运算**<br>微分方程的求解与一定的积分运算相联系. $n$ 阶微分方程的通解应包含 $n$ 个任意常数.

> **定义 1.2 (解)**<br>若 $y=\varphi\left(x\right)$ 及其各阶导数代入方程后得到恒等式, 则称 $y=\varphi\left(x\right)$ 为该微分方程在区间 $J$ 上的一个解.

---

## 1-1 题1(4)

验证 $y=\begin{cases}-\frac14\left(x-C_1\right)^2,&x< C_1\\ 0,&C_1\le x\le C_2\\ \frac14\left(x-C_2\right)^2,&x> C_2\end{cases}$ 是 $y'=\sqrt{|y|}$ 的解.

### 解答 1-1 题1(4)

由**定义 1.2 (解)**, 分三段验证: (1) $x< C_1$ 时 $y'=-\frac12\left(x-C_1\right)=\frac12\left(C_1-x\right)=\sqrt{|y|}$; (2) $C_1\le x\le C_2$ 时 $y'=0=\sqrt{|y|}$; (3) $x> C_2$ 时 $y'=\frac12\left(x-C_2\right)=\sqrt{|y|}$. 故 $y$ 是解. $\blacksquare$

---

## 1-2 题2(3)

求初值问题 $\frac{\mathrm dR}{\mathrm dt}=-aR$, $R\left(0\right)=1$ 的解.

### 解答 1-2 题2(3)

由**基础知识: 微分方程的求解与积分运算**, 分离变量积分得 $R=Ce^{-at}$. 代入初值 $R\left(0\right)=1$, 得 $C=1$. 故 $R\left(t\right)=e^{-at}$. $\blacksquare$

---

## 1-2 题2(4)

求初值问题 $\frac{\mathrm dy}{\mathrm dx}=1+y^2$, $y\left(x_0\right)=y_0$ 的解.

### 解答 1-2 题2(4)

分离变量积分得 $\arctan y=x+C$. 代入初值, 得 $C=\arctan y_0-x_0$. 故 $y=\tan\left(x+\arctan y_0-x_0\right)$. $\blacksquare$
