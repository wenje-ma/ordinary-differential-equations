# 作业 19

> **命题 1**(矩阵幂级数的绝对收敛性与矩阵指数函数的定义)<br>对 $n$ 阶实常数矩阵 $A$, 矩阵幂级数 $$E+A+\frac{1}{2!}A^2+\cdots+\frac{1}{k!}A^k+\cdots$$ 是绝对收敛的, 其和记为 $$e^A=\sum_{k=0}^{\infty}\frac{1}{k!}A^k,$$ 并称它为矩阵 $A$ 的指数函数, 其中 $E$ 为 $n$ 阶单位矩阵.

> **命题 2**(矩阵指数函数的性质)<br>矩阵指数函数有如下性质: (1) 若矩阵 $A$ 与 $B$ 可交换(即 $AB=BA$), 则 $$e^{A+B}=e^A e^B;$$<br>(2) 对任何矩阵 $A$, 指数函数 $e^A$ 是可逆的, 且 $$\left(e^A\right)^{-1}=e^{-A};$$<br>(3) 若 $P$ 是一个非奇异的 $n$ 阶矩阵, 则 $$e^{PAP^{-1}}=Pe^AP^{-1}.$$

> **定理 6.4**(矩阵指数函数是常系数齐次线性微分方程组的标准基解矩阵)<br>矩阵指数函数 $$\Phi\left(x\right)=e^{xA}$$ 是常系数齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$$ 的一个标准基解矩阵(即基解矩阵 $\Phi\left(x\right)$ 满足 $\Phi\left(0\right)=E$).

> **推论 3**(常系数非齐次线性微分方程组的通解与初值问题解)<br>常系数非齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$$ 在区间 $\left(a,b\right)$ 上的通解为 $$\boldsymbol{y}=e^{xA}\boldsymbol{c}+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,$$ 其中 $c$ 为任意的常数列向量; 而该方程组满足初值条件 $y\left(x_0\right)=y_0$ 的解为 $$\boldsymbol{y}=e^{\left(x-x_0\right)A}\boldsymbol{y}_0+\int_{x_0}^{x}e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds,$$ 其中 $x_0\in\left(a,b\right)$.

> **引理 6.6**(方程组有指数型非零解的充要条件)<br>常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有非零解 $y=e^{\lambda x}r$, 当且仅当 $\lambda$ 是矩阵 $A$ 的特征根, 而 $\boldsymbol{r}$ 是与 $\lambda$ 相应的特征向量, 即 $\boldsymbol{r}$ 满足齐次线性代数方程组 $\left(A-\lambda E\right)\boldsymbol{r}=\boldsymbol{0}$.

> **定理 6.5**($n$ 个互不相同特征根时的基解矩阵)<br>设 $n$ 阶矩阵 $A$ 有 $n$ 个互不相同的特征根 $\lambda_1,\lambda_2,\cdots,\lambda_n$, 则矩阵函数 $$\Phi\left(x\right)=\left(e^{\lambda_1 x}\boldsymbol{r}_1,e^{\lambda_2 x}\boldsymbol{r}_2,\cdots,e^{\lambda_n x}\boldsymbol{r}_n\right)$$ 是方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的一个基解矩阵, 其中 $r_i$ 是 $A$ 的与 $\lambda_i$ 相应的特征向量.

> **引理 6.7**(重特征根时确定向量多项式系数的方法)<br>设 $\lambda_i$ 是矩阵 $A$ 的 $n_i$ 重特征根, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)$$ 的非零解的充要条件是: $r_0$ 是齐次线性代数方程组 $\left(A-\lambda_i E\right)^{n_i}\boldsymbol{r}=\boldsymbol{0}$ 的一个非零解, 而且 $r_1,r_2,\cdots,r_{n_i-1}$ 由下面的关系式逐次确定 $$\boldsymbol{r}_1=\left(A-\lambda_i E\right)\boldsymbol{r}_0,\ \boldsymbol{r}_2=\left(A-\lambda_i E\right)\boldsymbol{r}_1,\ \cdots,\ \boldsymbol{r}_{n_i-1}=\left(A-\lambda_i E\right)\boldsymbol{r}_{n_i-2}.$$

> **定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵)<br>设 $n$ 阶实值常数矩阵 $A$ 在复域中互不相同的特征根是 $\lambda_1,\lambda_2,\cdots,\lambda_s$, 相应的重数分别为 $n_1,n_2,\cdots,n_s$, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的任一解都是形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{\left(n_i-1\right)!}\boldsymbol{r}_{n_i-1}\right)$$ 的向量函数的线性组合, 其中 $i=1,2,\cdots,s$.

> **附注 2**(从复值解提取实值解的方法)<br>设方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有一个复值解 $\boldsymbol{y}_1=\boldsymbol{u}\left(x\right)+i\boldsymbol{v}\left(x\right)$, 其中 $A$ 为实矩阵, 则 $\boldsymbol{y}_1$ 的共轭 $\boldsymbol{y}_2=\boldsymbol{u}\left(x\right)-i\boldsymbol{v}\left(x\right)$ 也是方程组的复值解, 从而 $\boldsymbol{y}_1$ 的实部 $\boldsymbol{u}\left(x\right)$ 和虚部 $\boldsymbol{v}\left(x\right)$ 都是方程组的实值解, 即由一对共轭的复值解可以得到两个实值解.

### 习题一

(习题 6-2 题1(2))求常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的通解, 其中矩阵

$$A=\begin{bmatrix}0&a\\-a&0\end{bmatrix},$$

$a$ 为常数.

### 解答 习题一

先求 $A$ 的特征根. 特征方程为

$$\det\left(A-\lambda E\right)=\begin{vmatrix}-\lambda&a\\-a&-\lambda\end{vmatrix}=\lambda^2+a^2=0,$$

故 $\lambda=\pm ia$. 以下设 $a\neq0$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 方程组有指数型非零解 $e^{\lambda x}\boldsymbol{r}$ 当且仅当 $\lambda$ 是 $A$ 的特征根. 对 $\lambda=ia$, 解 $\left(A-iaE\right)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{bmatrix}-ia&a\\-a&-ia\end{bmatrix}\begin{bmatrix}r_1\\r_2\end{bmatrix}=\boldsymbol{0},$$

由第一行得 $-ir_1+r_2=0$, 取 $\boldsymbol{r}=\left(1,i\right)^\top$. 于是得到一个复值解

$$\boldsymbol{y}_1=e^{iax}\begin{bmatrix}1\\i\end{bmatrix}.$$

由**附注 2**(从复值解提取实值解的方法), 取 $\boldsymbol{y}_1$ 的实部与虚部即为实值解. 利用 $e^{iax}=\cos ax+i\sin ax$, 展开得

$$\boldsymbol{y}_1=\left(\cos ax+i\sin ax\right)\begin{bmatrix}1\\i\end{bmatrix}=\begin{bmatrix}\cos ax+i\sin ax\\i\cos ax-\sin ax\end{bmatrix}.$$

其实部与虚部分别为

$$\boldsymbol{u}\left(x\right)=\begin{bmatrix}\cos ax\\-\sin ax\end{bmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{bmatrix}\sin ax\\\cos ax\end{bmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 两个实值解线性无关, 构成一个实基解矩阵, 故通解为

$$\boldsymbol{y}=C_1\begin{bmatrix}\cos ax\\-\sin ax\end{bmatrix}+C_2\begin{bmatrix}\sin ax\\\cos ax\end{bmatrix},$$

其中 $C_1,C_2$ 为任意常数. 当 $a=0$ 时 $A$ 为零矩阵, 方程组退化为 $\frac{d\boldsymbol{y}}{dx}=\boldsymbol{0}$, 通解为常向量 $\boldsymbol{y}=\boldsymbol{C}$. $\blacksquare$

### 习题二

(习题 6-2 题1(4))求常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的通解, 其中矩阵

$$A=\begin{bmatrix}1&\frac{2}{3}&-\frac{2}{3}\\0&\frac{2}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{4}{3}\end{bmatrix}.$$

### 解答 习题二

先求 $A$ 的特征根. 按第一行展开行列式:

$$\det\left(A-\lambda E\right)=\left(1-\lambda\right)\begin{vmatrix}\frac{2}{3}-\lambda&\frac{1}{3}\\-\frac{1}{3}&\frac{4}{3}-\lambda\end{vmatrix}=\left(1-\lambda\right)\left[\left(\frac{2}{3}-\lambda\right)\left(\frac{4}{3}-\lambda\right)+\frac{1}{9}\right].$$

括号内化简为 $\left(\lambda-1\right)^2$, 故

$$\det\left(A-\lambda E\right)=-\left(\lambda-1\right)^3,$$

即 $\lambda=1$ 是三重特征根. 计算 $A-E$:

$$A-E=\begin{bmatrix}0&\frac{2}{3}&-\frac{2}{3}\\0&-\frac{1}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{1}{3}\end{bmatrix}.$$

其秩为 1, 故 $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ 的解空间为二维. 由 $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_2=r_3$, 取两个线性无关的特征向量

$$\boldsymbol{r}^{\left(1\right)}=\begin{bmatrix}1\\0\\0\end{bmatrix},\quad\boldsymbol{r}^{\left(2\right)}=\begin{bmatrix}0\\1\\1\end{bmatrix}.$$

由**引理 6.7**(重特征根时确定向量多项式系数的方法), 还需再取一个满足 $\left(A-E\right)^2\boldsymbol{r}_0=O$ 但 $\left(A-E\right)\boldsymbol{r}_0\neq\boldsymbol{0}$ 的向量 $\boldsymbol{r}_0$. 直接验算可知

$$\left(A-E\right)^2=O,$$

故任取 $\boldsymbol{r}_0^{\left(3\right)}=\left(0,1,0\right)^\top$ 即可, 它不是特征向量. 逐次计算系数:

$$\boldsymbol{r}_1^{\left(3\right)}=\left(A-E\right)\boldsymbol{r}_0^{\left(3\right)}=\begin{bmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{bmatrix}.$$

于是由**引理 6.7**(重特征根时确定向量多项式系数的方法)所得的第三个解为

$$e^x\left(\boldsymbol{r}_0^{\left(3\right)}+x\boldsymbol{r}_1^{\left(3\right)}\right)=e^x\left[\begin{bmatrix}0\\1\\0\end{bmatrix}+x\begin{bmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{bmatrix}\right].$$

三个解在 $x=0$ 处的值分别为 $\boldsymbol{r}^{\left(1\right)},\boldsymbol{r}^{\left(2\right)}$ 和 $\boldsymbol{r}_0^{\left(3\right)}$, 它们线性无关, 由**定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵)知构成基解矩阵, 故通解为

$$\boldsymbol{y}=C_1e^x\begin{bmatrix}1\\0\\0\end{bmatrix}+C_2e^x\begin{bmatrix}0\\1\\1\end{bmatrix}+C_3e^x\left[\begin{bmatrix}0\\1\\0\end{bmatrix}+x\begin{bmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{bmatrix}\right],$$

其中 $C_1,C_2,C_3$ 为任意常数. $\blacksquare$

### 习题三

(习题 6-2 题2(2))求常系数非齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ 的通解, 其中

$$A=\begin{bmatrix}0&-n^2\\-n^2&0\end{bmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{bmatrix}\cos nx\\\sin nx\end{bmatrix}.$$

### 解答 习题三

先求相应齐次方程组的通解. 特征方程为

$$\det\left(A-\lambda E\right)=\lambda^2-n^4=0,$$

故 $\lambda=\pm n^2$. 由**引理 6.6**(方程组有指数型非零解的充要条件)分别求特征向量: 对 $\lambda=n^2$ 解 $\left(A-n^2E\right)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_1+r_2=0$, 取 $\left(1,-1\right)^\top$; 对 $\lambda=-n^2$ 解 $\left(A+n^2E\right)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_1-r_2=0$, 取 $\left(1,1\right)^\top$. 故齐次通解为

$$\boldsymbol{y}_h=C_1e^{n^2x}\begin{bmatrix}1\\-1\end{bmatrix}+C_2e^{-n^2x}\begin{bmatrix}1\\1\end{bmatrix}.$$

再求一个特解. 非齐次项为 $\cos nx$ 与 $\sin nx$, 与特征根 $\pm n^2$ 不共振, 故设特解形如

$$\boldsymbol{y}_p=\begin{bmatrix}a_1\cos nx+b_1\sin nx\\a_2\cos nx+b_2\sin nx\end{bmatrix}.$$

代入方程组 $y_1'=-n^2y_2+\cos nx,\ y_2'=-n^2y_1+\sin nx$, 比较 $\cos nx$ 与 $\sin nx$ 的系数, 得 $a_1=0,\ b_2=0$, 以及

$$nb_1=1-n^2a_2,\quad -na_2=1-n^2b_1.$$

联立解得

$$a_2=\frac{n-1}{n\left(1+n^2\right)},\quad b_1=\frac{n+1}{n\left(1+n^2\right)}.$$

故一个特解为

$$\boldsymbol{y}_p=\begin{bmatrix}\frac{n+1}{n\left(1+n^2\right)}\sin nx\\[2pt\right]\frac{n-1}{n\left(1+n^2\right)}\cos nx\end{bmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 非齐次通解为齐次通解加上一个特解, 即

$$\boldsymbol{y}=C_1e^{n^2x}\begin{bmatrix}1\\-1\end{bmatrix}+C_2e^{-n^2x}\begin{bmatrix}1\\1\end{bmatrix}+\begin{bmatrix}\frac{n+1}{n\left(1+n^2\right)}\sin nx\\[2pt\right]\frac{n-1}{n\left(1+n^2\right)}\cos nx\end{bmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题四

(习题 6-2 题2(4))求常系数非齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ 的通解, 其中

$$A=\begin{bmatrix}2&1&-2\\-1&0&0\\1&1&-1\end{bmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{bmatrix}2-x\\0\\1-x\end{bmatrix}.$$

### 解答 习题四

先求相应齐次方程组的通解. 计算特征多项式:

$$\det\left(A-\lambda E\right)=\left(2-\lambda\right)\left(\lambda+\lambda^2\right)-\left(1+\lambda\right)-2\left(\lambda-1\right)=-\left(\lambda-1\right)\left(\lambda^2+1\right).$$

故特征根为 $\lambda=1,\ \lambda=\pm i$. 对 $\lambda=1$, 解 $\left(A-E\right)\boldsymbol{r}=\boldsymbol{0}$ 得特征向量 $\boldsymbol{r}^{\left(1\right)}=\left(-1,1,0\right)^\top$. 对 $\lambda=i$, 解 $\left(A-iE\right)\boldsymbol{r}=\boldsymbol{0}$ 得复特征向量 $\boldsymbol{r}=\left(-i,1,-i\right)^\top$, 对应复值解 $e^{ix}\left(-i,1,-i\right)^\top$. 由**附注 2**(从复值解提取实值解的方法), 利用 $e^{ix}=\cos x+i\sin x$ 取实部与虚部, 得

$$\boldsymbol{u}\left(x\right)=\begin{bmatrix}\sin x\\\cos x\\\sin x\end{bmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{bmatrix}-\cos x\\\sin x\\-\cos x\end{bmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 齐次通解为

$$\boldsymbol{y}_h=C_1e^x\begin{bmatrix}-1\\1\\0\end{bmatrix}+C_2\begin{bmatrix}\sin x\\\cos x\\\sin x\end{bmatrix}+C_3\begin{bmatrix}-\cos x\\\sin x\\-\cos x\end{bmatrix}.$$

再求一个特解. 非齐次项是 $x$ 的一次式, 设特解 $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, 其中 $\boldsymbol{a},\boldsymbol{b}$ 为常向量. 代入方程组, 比较常数项与 $x$ 的系数, 得

$$A\boldsymbol{b}=\begin{bmatrix}1\\0\\1\end{bmatrix},\quad\boldsymbol{b}=A\boldsymbol{a}+\begin{bmatrix}2\\0\\1\end{bmatrix}.$$

由前式解出 $\boldsymbol{b}=\left(0,1,0\right)^\top$, 再代入后式得 $A\boldsymbol{a}=\left(-2,1,-1\right)^\top$, 解得 $\boldsymbol{a}=\left(-1,0,0\right)^\top$. 故一个特解为

$$\boldsymbol{y}_p=\begin{bmatrix}-1\\x\\0\end{bmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 通解为

$$\boldsymbol{y}=C_1e^x\begin{bmatrix}-1\\1\\0\end{bmatrix}+C_2\begin{bmatrix}\sin x\\\cos x\\\sin x\end{bmatrix}+C_3\begin{bmatrix}-\cos x\\\sin x\\-\cos x\end{bmatrix}+\begin{bmatrix}-1\\x\\0\end{bmatrix},$$

其中 $C_1,C_2,C_3$ 为任意常数. $\blacksquare$

### 习题五

(习题 6-2 题3(2))求微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ 满足初值条件 $\boldsymbol{y}\left(0\right)=\boldsymbol{\eta}$ 的解, 其中

$$A=\begin{bmatrix}0&-2\\2&0\end{bmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{bmatrix}3x\\4\end{bmatrix},\quad\boldsymbol{\eta}=\begin{bmatrix}2\\3\end{bmatrix}.$$

### 解答 习题五

先求相应齐次方程组的通解. 特征方程为

$$\det\left(A-\lambda E\right)=\lambda^2+4=0,$$

故 $\lambda=\pm2i$. 对 $\lambda=2i$, 解 $\left(A-2iE\right)\boldsymbol{r}=\boldsymbol{0}$ 得 $\boldsymbol{r}=\left(1,-i\right)^\top$, 对应复值解 $e^{2ix}\left(1,-i\right)^\top$. 由**附注 2**(从复值解提取实值解的方法), 利用 $e^{2ix}=\cos 2x+i\sin 2x$ 取实部与虚部, 得两个实值解

$$\boldsymbol{u}\left(x\right)=\begin{bmatrix}\cos 2x\\\sin 2x\end{bmatrix},\quad\boldsymbol{v}\left(x\right)=\begin{bmatrix}\sin 2x\\-\cos 2x\end{bmatrix}.$$

再求一个特解. 非齐次项为一次式, 设 $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, 代入方程组比较系数, 得

$$A\boldsymbol{b}=\begin{bmatrix}-3\\0\end{bmatrix},\quad\boldsymbol{b}=A\boldsymbol{a}+\begin{bmatrix}0\\4\end{bmatrix}.$$

由前式得 $\boldsymbol{b}=\left(0,\frac{3}{2}\right)^\top$, 再代入得 $\boldsymbol{a}=\left(-\frac{5}{4},0\right)^\top$. 故一个特解为

$$\boldsymbol{y}_p=\begin{bmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{bmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 通解为

$$\boldsymbol{y}=C_1\begin{bmatrix}\cos 2x\\\sin 2x\end{bmatrix}+C_2\begin{bmatrix}\sin 2x\\-\cos 2x\end{bmatrix}+\begin{bmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{bmatrix}.$$

代入初值条件 $\boldsymbol{y}\left(0\right)=\left(2,3\right)$:

$$C_1\begin{bmatrix}1\\0\end{bmatrix}+C_2\begin{bmatrix}0\\-1\end{bmatrix}+\begin{bmatrix}-\frac{5}{4}\\0\end{bmatrix}=\begin{bmatrix}2\\3\end{bmatrix},$$

解得 $C_1=\frac{13}{4},\ C_2=-3$. 故所求初值问题的解为

$$\boldsymbol{y}=\frac{13}{4}\begin{bmatrix}\cos 2x\\\sin 2x\end{bmatrix}-3\begin{bmatrix}\sin 2x\\-\cos 2x\end{bmatrix}+\begin{bmatrix}-\frac{5}{4}\\[2pt\right]\frac{3}{2}x\end{bmatrix}.$$

$\blacksquare$

### 习题六

(习题 6-2 题3(4))求微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}\left(x\right)$ 满足初值条件 $\boldsymbol{y}\left(0\right)=\boldsymbol{\eta}$ 的解, 其中

$$A=\begin{bmatrix}16&14&38\\-9&-7&-18\\-4&-4&-11\end{bmatrix},\quad\boldsymbol{f}\left(x\right)=\begin{bmatrix}-2e^{-x}\\-3e^{-x}\\2e^{-x}\end{bmatrix},\quad\boldsymbol{\eta}=\begin{bmatrix}0\\0\\0\end{bmatrix}.$$

### 解答 习题六

先求 $A$ 的特征根. 计算特征多项式:

$$\det\left(A-\lambda E\right)=-\left(\lambda-2\right)\left(\lambda+1\right)\left(\lambda+3\right),$$

故特征根为 $\lambda=2,\ \lambda=-1,\ \lambda=-3$. 由**引理 6.6**(方程组有指数型非零解的充要条件)分别求对应的特征向量, 得

$$\boldsymbol{r}^{\left(2\right)}=\begin{bmatrix}-1\\1\\0\end{bmatrix},\quad\boldsymbol{r}^{\left(-1\right)}=\begin{bmatrix}2\\3\\-2\end{bmatrix},\quad\boldsymbol{r}^{\left(-3\right)}=\begin{bmatrix}-2\\0\\1\end{bmatrix}.$$

注意到非齐次项恰为

$$\boldsymbol{f}\left(x\right)=e^{-x}\begin{bmatrix}-2\\-3\\2\end{bmatrix}=-e^{-x}\boldsymbol{r}^{\left(-1\right)},$$

即非齐次向量共振于特征根 $\lambda=-1$. 由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 取 $x_0=0,\ \boldsymbol{y}_0=\boldsymbol{0}$, 初值问题的解为

$$\boldsymbol{y}\left(x\right)=\int_0^x e^{\left(x-s\right)A}\boldsymbol{f}\left(s\right)\,ds.$$

由于 $\boldsymbol{r}^{\left(-1\right)}$ 是 $\lambda=-1$ 的特征向量, 有 $e^{\left(x-s\right)A}\boldsymbol{r}^{\left(-1\right)}=e^{-\left(x-s\right)}\boldsymbol{r}^{\left(-1\right)}$, 故

$$\boldsymbol{y}\left(x\right)=-\boldsymbol{r}^{\left(-1\right)}\int_0^x e^{-\left(x-s\right)}e^{-s}\,ds=-\boldsymbol{r}^{\left(-1\right)}e^{-x}\int_0^x 1\,ds=-xe^{-x}\boldsymbol{r}^{\left(-1\right)}.$$

代入 $\boldsymbol{r}^{\left(-1\right)}=\left(2,3,-2\right)^\top$, 所求解为

$$\boldsymbol{y}\left(x\right)=xe^{-x}\begin{bmatrix}-2\\-3\\2\end{bmatrix}.$$

$\blacksquare$

### 习题七

(习题 6-2 题4)求解微分方程组

$$\frac{d}{dt}\begin{bmatrix}x\\y\end{bmatrix}=\begin{bmatrix}a&-b\\b&a\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix},$$

其中 $a$ 和 $b$ 为实常数, 而且 $b\neq0$.

### 解答 习题七

记 $A=\begin{bmatrix}a&-b\\b&a\end{bmatrix}$. 先求特征根. 特征方程为

$$\det\left(A-\lambda E\right)=\left(a-\lambda\right)^2+b^2=0,$$

故 $\lambda=a\pm ib$. 对 $\lambda=a+ib$, 解 $\left(A-\left(a+ib\right)E\right)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{bmatrix}-ib&-b\\b&-ib\end{bmatrix}\begin{bmatrix}r_1\\r_2\end{bmatrix}=\boldsymbol{0},$$

由第一行得 $-ir_1-r_2=0$, 取 $\boldsymbol{r}=\left(1,-i\right)^\top$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 得复值解

$$\boldsymbol{y}_1=e^{\left(a+ib\right)t}\begin{bmatrix}1\\-i\end{bmatrix}.$$

由**附注 2**(从复值解提取实值解的方法), 利用 $e^{\left(a+ib\right)t}=e^{at}\left(\cos bt+i\sin bt\right)$ 取实部与虚部, 得

$$\boldsymbol{u}\left(t\right)=e^{at}\begin{bmatrix}\cos bt\\\sin bt\end{bmatrix},\quad\boldsymbol{v}\left(t\right)=e^{at}\begin{bmatrix}\sin bt\\-\cos bt\end{bmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 通解为

$$\begin{bmatrix}x\\y\end{bmatrix}=C_1e^{at}\begin{bmatrix}\cos bt\\\sin bt\end{bmatrix}+C_2e^{at}\begin{bmatrix}\sin bt\\-\cos bt\end{bmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题八

(习题 6-2 题5)证明: 常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的任何解当 $x\to+\infty$ 时都趋于零, 当且仅当它的系数矩阵 $A$ 的所有特征根都具有负的实部.

### 解答 习题八

由**定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵), 方程组的任一解都是形如

$$e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_\lambda-1}}{\left(n_\lambda-1\right)!}\boldsymbol{r}_{n_\lambda-1}\right)$$

的向量函数的线性组合, 其中 $\lambda$ 为 $A$ 的特征根. 记 $\alpha=\mathrm{Re}\,\lambda$, 则上述函数的模满足估计

$$\left|e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots\right)\right|\le e^{\alpha x}\left(M_0+M_1x+\cdots+M_{n_\lambda-1}x^{n_\lambda-1}\right),$$

其中 $M_k$ 为常数.

先证充分性. 设 $A$ 的所有特征根的实部均为负, 即对每个特征根 $\lambda$ 都有 $\alpha=\mathrm{Re}\,\lambda< 0$. 由于多项式函数增长慢于指数函数的衰减, 对任意 $k\ge0$ 都有 $x^ke^{\alpha x}\to0\ \left(x\to+\infty\right)$, 故上式右端趋于零, 从而方程组的每一个解都趋于零.

再证必要性. 反设 $A$ 有某个特征根 $\lambda_j$ 满足 $\alpha_j=\mathrm{Re}\,\lambda_j\ge0$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 取与 $\lambda_j$ 相应的特征向量 $\boldsymbol{r}_j\neq\boldsymbol{0}$, 则 $\boldsymbol{y}=e^{\lambda_j x}\boldsymbol{r}_j$ 是方程组的一个非零解. 当 $\alpha_j> 0$ 时, $\left\|\boldsymbol{y}\right\|=e^{\alpha_j x}\left\|\boldsymbol{r}_j\right\|\to+\infty$; 当 $\alpha_j=0$ 时, 若 $\lambda_j=0$ 则 $\boldsymbol{y}=\boldsymbol{r}_j$ 为非零常向量, 若 $\lambda_j=i\beta\ \left(\beta\neq0\right)$ 则 $\boldsymbol{y}=e^{i\beta x}\boldsymbol{r}_j$ 的模恒为 $\left\|\boldsymbol{r}_j\right\|$ 而不趋于零. 这些都与题设结论矛盾. 故 $A$ 的所有特征根都必须具有负的实部. $\blacksquare$
