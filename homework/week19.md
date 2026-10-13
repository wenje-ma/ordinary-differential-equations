# 作业 19

> **命题 1**(矩阵幂级数的绝对收敛性与矩阵指数函数的定义)<br>对 $n$ 阶实常数矩阵 $A$, 矩阵幂级数 $$E+A+\frac{1}{2!}A^2+\cdots+\frac{1}{k!}A^k+\cdots$$ 是绝对收敛的, 其和记为 $$e^A=\sum_{k=0}^{\infty}\frac{1}{k!}A^k,$$ 并称它为矩阵 $A$ 的指数函数, 其中 $E$ 为 $n$ 阶单位矩阵.

> **命题 2**(矩阵指数函数的性质)<br>矩阵指数函数有如下性质: (1) 若矩阵 $A$ 与 $B$ 可交换(即 $AB=BA$), 则 $$e^{A+B}=e^A e^B;$$<br>(2) 对任何矩阵 $A$, 指数函数 $e^A$ 是可逆的, 且 $$(e^A)^{-1}=e^{-A};$$<br>(3) 若 $P$ 是一个非奇异的 $n$ 阶矩阵, 则 $$e^{PAP^{-1}}=Pe^AP^{-1}.$$

> **定理 6.4**(矩阵指数函数是常系数齐次线性微分方程组的标准基解矩阵)<br>矩阵指数函数 $$\Phi(x)=e^{xA}$$ 是常系数齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$$ 的一个标准基解矩阵(即基解矩阵 $\Phi(x)$ 满足 $\Phi(0)=E$).

> **推论 3**(常系数非齐次线性微分方程组的通解与初值问题解)<br>常系数非齐次线性微分方程组 $$\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$$ 在区间 $(a,b)$ 上的通解为 $$\boldsymbol{y}=e^{xA}\boldsymbol{c}+\int_{x_0}^{x}e^{(x-s)A}\boldsymbol{f}(s)\,ds,$$ 其中 $c$ 为任意的常数列向量; 而该方程组满足初值条件 $y(x_0)=y_0$ 的解为 $$\boldsymbol{y}=e^{(x-x_0)A}\boldsymbol{y}_0+\int_{x_0}^{x}e^{(x-s)A}\boldsymbol{f}(s)\,ds,$$ 其中 $x_0\in(a,b)$.

> **引理 6.6**(方程组有指数型非零解的充要条件)<br>常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有非零解 $y=e^{\lambda x}r$, 当且仅当 $\lambda$ 是矩阵 $A$ 的特征根, 而 $\boldsymbol{r}$ 是与 $\lambda$ 相应的特征向量, 即 $\boldsymbol{r}$ 满足齐次线性代数方程组 $(A-\lambda E)\boldsymbol{r}=\boldsymbol{0}$.

> **定理 6.5**($n$ 个互不相同特征根时的基解矩阵)<br>设 $n$ 阶矩阵 $A$ 有 $n$ 个互不相同的特征根 $\lambda_1,\lambda_2,\cdots,\lambda_n$, 则矩阵函数 $$\Phi(x)=\left(e^{\lambda_1 x}\boldsymbol{r}_1,e^{\lambda_2 x}\boldsymbol{r}_2,\cdots,e^{\lambda_n x}\boldsymbol{r}_n\right)$$ 是方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的一个基解矩阵, 其中 $r_i$ 是 $A$ 的与 $\lambda_i$ 相应的特征向量.

> **引理 6.7**(重特征根时确定向量多项式系数的方法)<br>设 $\lambda_i$ 是矩阵 $A$ 的 $n_i$ 重特征根, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{(n_i-1)!}\boldsymbol{r}_{n_i-1}\right)$$ 的非零解的充要条件是: $r_0$ 是齐次线性代数方程组 $(A-\lambda_i E)^{n_i}\boldsymbol{r}=\boldsymbol{0}$ 的一个非零解, 而且 $r_1,r_2,\cdots,r_{n_i-1}$ 由下面的关系式逐次确定 $$\boldsymbol{r}_1=(A-\lambda_i E)\boldsymbol{r}_0,\ \boldsymbol{r}_2=(A-\lambda_i E)\boldsymbol{r}_1,\ \cdots,\ \boldsymbol{r}_{n_i-1}=(A-\lambda_i E)\boldsymbol{r}_{n_i-2}.$$

> **定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵)<br>设 $n$ 阶实值常数矩阵 $A$ 在复域中互不相同的特征根是 $\lambda_1,\lambda_2,\cdots,\lambda_s$, 相应的重数分别为 $n_1,n_2,\cdots,n_s$, 则方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的任一解都是形如 $$e^{\lambda_i x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_i-1}}{(n_i-1)!}\boldsymbol{r}_{n_i-1}\right)$$ 的向量函数的线性组合, 其中 $i=1,2,\cdots,s$.

> **附注 2**(从复值解提取实值解的方法)<br>设方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 有一个复值解 $\boldsymbol{y}_1=\boldsymbol{u}(x)+i\boldsymbol{v}(x)$, 其中 $A$ 为实矩阵, 则 $\boldsymbol{y}_1$ 的共轭 $\boldsymbol{y}_2=\boldsymbol{u}(x)-i\boldsymbol{v}(x)$ 也是方程组的复值解, 从而 $\boldsymbol{y}_1$ 的实部 $\boldsymbol{u}(x)$ 和虚部 $\boldsymbol{v}(x)$ 都是方程组的实值解, 即由一对共轭的复值解可以得到两个实值解.

### 习题一

(习题 6-2 题1(2))求常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的通解, 其中矩阵

$$A=\begin{pmatrix}0&a\\-a&0\end{pmatrix},$$

$a$ 为常数.

### 解答 习题一

先求 $A$ 的特征根. 特征方程为

$$\det(A-\lambda E)=\begin{vmatrix}-\lambda&a\\-a&-\lambda\end{vmatrix}=\lambda^2+a^2=0,$$

故 $\lambda=\pm ia$. 以下设 $a\neq0$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 方程组有指数型非零解 $e^{\lambda x}\boldsymbol{r}$ 当且仅当 $\lambda$ 是 $A$ 的特征根. 对 $\lambda=ia$, 解 $(A-iaE)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{pmatrix}-ia&a\\-a&-ia\end{pmatrix}\begin{pmatrix}r_1\\r_2\end{pmatrix}=\boldsymbol{0},$$

由第一行得 $-ir_1+r_2=0$, 取 $\boldsymbol{r}=(1,i)^T$. 于是得到一个复值解

$$\boldsymbol{y}_1=e^{iax}\begin{pmatrix}1\\i\end{pmatrix}.$$

由**附注 2**(从复值解提取实值解的方法), 取 $\boldsymbol{y}_1$ 的实部与虚部即为实值解. 利用 $e^{iax}=\cos ax+i\sin ax$, 展开得

$$\boldsymbol{y}_1=(\cos ax+i\sin ax)\begin{pmatrix}1\\i\end{pmatrix}=\begin{pmatrix}\cos ax+i\sin ax\\i\cos ax-\sin ax\end{pmatrix}.$$

其实部与虚部分别为

$$\boldsymbol{u}(x)=\begin{pmatrix}\cos ax\\-\sin ax\end{pmatrix},\qquad\boldsymbol{v}(x)=\begin{pmatrix}\sin ax\\\cos ax\end{pmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 两个实值解线性无关, 构成一个实基解矩阵, 故通解为

$$\boldsymbol{y}=C_1\begin{pmatrix}\cos ax\\-\sin ax\end{pmatrix}+C_2\begin{pmatrix}\sin ax\\\cos ax\end{pmatrix},$$

其中 $C_1,C_2$ 为任意常数. 当 $a=0$ 时 $A$ 为零矩阵, 方程组退化为 $\frac{d\boldsymbol{y}}{dx}=\boldsymbol{0}$, 通解为常向量 $\boldsymbol{y}=\boldsymbol{C}$. $\blacksquare$

### 习题二

(习题 6-2 题1(4))求常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的通解, 其中矩阵

$$A=\begin{pmatrix}1&\frac{2}{3}&-\frac{2}{3}\\0&\frac{2}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{4}{3}\end{pmatrix}.$$

### 解答 习题二

先求 $A$ 的特征根. 按第一行展开行列式:

$$\det(A-\lambda E)=(1-\lambda)\begin{vmatrix}\frac{2}{3}-\lambda&\frac{1}{3}\\-\frac{1}{3}&\frac{4}{3}-\lambda\end{vmatrix}=(1-\lambda)\left[\left(\frac{2}{3}-\lambda\right)\left(\frac{4}{3}-\lambda\right)+\frac{1}{9}\right].$$

括号内化简为 $(\lambda-1)^2$, 故

$$\det(A-\lambda E)=-(\lambda-1)^3,$$

即 $\lambda=1$ 是三重特征根. 计算 $A-E$:

$$A-E=\begin{pmatrix}0&\frac{2}{3}&-\frac{2}{3}\\0&-\frac{1}{3}&\frac{1}{3}\\0&-\frac{1}{3}&\frac{1}{3}\end{pmatrix}.$$

其秩为 1, 故 $(A-E)\boldsymbol{r}=\boldsymbol{0}$ 的解空间为二维. 由 $(A-E)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_2=r_3$, 取两个线性无关的特征向量

$$\boldsymbol{r}^{(1)}=\begin{pmatrix}1\\0\\0\end{pmatrix},\qquad\boldsymbol{r}^{(2)}=\begin{pmatrix}0\\1\\1\end{pmatrix}.$$

由**引理 6.7**(重特征根时确定向量多项式系数的方法), 还需再取一个满足 $(A-E)^2\boldsymbol{r}_0=O$ 但 $(A-E)\boldsymbol{r}_0\neq\boldsymbol{0}$ 的向量 $\boldsymbol{r}_0$. 直接验算可知

$$(A-E)^2=O,$$

故任取 $\boldsymbol{r}_0^{(3)}=(0,1,0)^T$ 即可, 它不是特征向量. 逐次计算系数:

$$\boldsymbol{r}_1^{(3)}=(A-E)\boldsymbol{r}_0^{(3)}=\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}.$$

于是由**引理 6.7**(重特征根时确定向量多项式系数的方法)所得的第三个解为

$$e^x\left(\boldsymbol{r}_0^{(3)}+x\boldsymbol{r}_1^{(3)}\right)=e^x\left[\begin{pmatrix}0\\1\\0\end{pmatrix}+x\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}\right].$$

三个解在 $x=0$ 处的值分别为 $\boldsymbol{r}^{(1)},\boldsymbol{r}^{(2)}$ 和 $\boldsymbol{r}_0^{(3)}$, 它们线性无关, 由**定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵)知构成基解矩阵, 故通解为

$$\boldsymbol{y}=C_1e^x\begin{pmatrix}1\\0\\0\end{pmatrix}+C_2e^x\begin{pmatrix}0\\1\\1\end{pmatrix}+C_3e^x\left[\begin{pmatrix}0\\1\\0\end{pmatrix}+x\begin{pmatrix}\frac{2}{3}\\-\frac{1}{3}\\-\frac{1}{3}\end{pmatrix}\right],$$

其中 $C_1,C_2,C_3$ 为任意常数. $\blacksquare$

### 习题三

(习题 6-2 题2(2))求常系数非齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$ 的通解, 其中

$$A=\begin{pmatrix}0&-n^2\\-n^2&0\end{pmatrix},\qquad\boldsymbol{f}(x)=\begin{pmatrix}\cos nx\\\sin nx\end{pmatrix}.$$

### 解答 习题三

先求相应齐次方程组的通解. 特征方程为

$$\det(A-\lambda E)=\lambda^2-n^4=0,$$

故 $\lambda=\pm n^2$. 由**引理 6.6**(方程组有指数型非零解的充要条件)分别求特征向量: 对 $\lambda=n^2$ 解 $(A-n^2E)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_1+r_2=0$, 取 $(1,-1)^T$; 对 $\lambda=-n^2$ 解 $(A+n^2E)\boldsymbol{r}=\boldsymbol{0}$ 得 $r_1-r_2=0$, 取 $(1,1)^T$. 故齐次通解为

$$\boldsymbol{y}_h=C_1e^{n^2x}\begin{pmatrix}1\\-1\end{pmatrix}+C_2e^{-n^2x}\begin{pmatrix}1\\1\end{pmatrix}.$$

再求一个特解. 非齐次项为 $\cos nx$ 与 $\sin nx$, 与特征根 $\pm n^2$ 不共振, 故设特解形如

$$\boldsymbol{y}_p=\begin{pmatrix}a_1\cos nx+b_1\sin nx\\a_2\cos nx+b_2\sin nx\end{pmatrix}.$$

代入方程组 $y_1'=-n^2y_2+\cos nx,\ y_2'=-n^2y_1+\sin nx$, 比较 $\cos nx$ 与 $\sin nx$ 的系数, 得 $a_1=0,\ b_2=0$, 以及

$$nb_1=1-n^2a_2,\qquad -na_2=1-n^2b_1.$$

联立解得

$$a_2=\frac{n-1}{n(1+n^2)},\qquad b_1=\frac{n+1}{n(1+n^2)}.$$

故一个特解为

$$\boldsymbol{y}_p=\begin{pmatrix}\frac{n+1}{n(1+n^2)}\sin nx\\[2pt]\frac{n-1}{n(1+n^2)}\cos nx\end{pmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 非齐次通解为齐次通解加上一个特解, 即

$$\boldsymbol{y}=C_1e^{n^2x}\begin{pmatrix}1\\-1\end{pmatrix}+C_2e^{-n^2x}\begin{pmatrix}1\\1\end{pmatrix}+\begin{pmatrix}\frac{n+1}{n(1+n^2)}\sin nx\\[2pt]\frac{n-1}{n(1+n^2)}\cos nx\end{pmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题四

(习题 6-2 题2(4))求常系数非齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$ 的通解, 其中

$$A=\begin{pmatrix}2&1&-2\\-1&0&0\\1&1&-1\end{pmatrix},\qquad\boldsymbol{f}(x)=\begin{pmatrix}2-x\\0\\1-x\end{pmatrix}.$$

### 解答 习题四

先求相应齐次方程组的通解. 计算特征多项式:

$$\det(A-\lambda E)=(2-\lambda)(\lambda+\lambda^2)-(1+\lambda)-2(\lambda-1)=-(\lambda-1)(\lambda^2+1).$$

故特征根为 $\lambda=1,\ \lambda=\pm i$. 对 $\lambda=1$, 解 $(A-E)\boldsymbol{r}=\boldsymbol{0}$ 得特征向量 $\boldsymbol{r}^{(1)}=(-1,1,0)^T$. 对 $\lambda=i$, 解 $(A-iE)\boldsymbol{r}=\boldsymbol{0}$ 得复特征向量 $\boldsymbol{r}=(-i,1,-i)^T$, 对应复值解 $e^{ix}(-i,1,-i)^T$. 由**附注 2**(从复值解提取实值解的方法), 利用 $e^{ix}=\cos x+i\sin x$ 取实部与虚部, 得

$$\boldsymbol{u}(x)=\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix},\qquad\boldsymbol{v}(x)=\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 齐次通解为

$$\boldsymbol{y}_h=C_1e^x\begin{pmatrix}-1\\1\\0\end{pmatrix}+C_2\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix}+C_3\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}.$$

再求一个特解. 非齐次项是 $x$ 的一次式, 设特解 $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, 其中 $\boldsymbol{a},\boldsymbol{b}$ 为常向量. 代入方程组, 比较常数项与 $x$ 的系数, 得

$$A\boldsymbol{b}=\begin{pmatrix}1\\0\\1\end{pmatrix},\qquad\boldsymbol{b}=A\boldsymbol{a}+\begin{pmatrix}2\\0\\1\end{pmatrix}.$$

由前式解出 $\boldsymbol{b}=(0,1,0)^T$, 再代入后式得 $A\boldsymbol{a}=(-2,1,-1)^T$, 解得 $\boldsymbol{a}=(-1,0,0)^T$. 故一个特解为

$$\boldsymbol{y}_p=\begin{pmatrix}-1\\x\\0\end{pmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 通解为

$$\boldsymbol{y}=C_1e^x\begin{pmatrix}-1\\1\\0\end{pmatrix}+C_2\begin{pmatrix}\sin x\\\cos x\\\sin x\end{pmatrix}+C_3\begin{pmatrix}-\cos x\\\sin x\\-\cos x\end{pmatrix}+\begin{pmatrix}-1\\x\\0\end{pmatrix},$$

其中 $C_1,C_2,C_3$ 为任意常数. $\blacksquare$

### 习题五

(习题 6-2 题3(2))求微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$ 满足初值条件 $\boldsymbol{y}(0)=\boldsymbol{\eta}$ 的解, 其中

$$A=\begin{pmatrix}0&-2\\2&0\end{pmatrix},\qquad\boldsymbol{f}(x)=\begin{pmatrix}3x\\4\end{pmatrix},\qquad\boldsymbol{\eta}=\begin{pmatrix}2\\3\end{pmatrix}.$$

### 解答 习题五

先求相应齐次方程组的通解. 特征方程为

$$\det(A-\lambda E)=\lambda^2+4=0,$$

故 $\lambda=\pm2i$. 对 $\lambda=2i$, 解 $(A-2iE)\boldsymbol{r}=\boldsymbol{0}$ 得 $\boldsymbol{r}=(1,-i)^T$, 对应复值解 $e^{2ix}(1,-i)^T$. 由**附注 2**(从复值解提取实值解的方法), 利用 $e^{2ix}=\cos 2x+i\sin 2x$ 取实部与虚部, 得两个实值解

$$\boldsymbol{u}(x)=\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix},\qquad\boldsymbol{v}(x)=\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}.$$

再求一个特解. 非齐次项为一次式, 设 $\boldsymbol{y}_p=\boldsymbol{a}+\boldsymbol{b}x$, 代入方程组比较系数, 得

$$A\boldsymbol{b}=\begin{pmatrix}-3\\0\end{pmatrix},\qquad\boldsymbol{b}=A\boldsymbol{a}+\begin{pmatrix}0\\4\end{pmatrix}.$$

由前式得 $\boldsymbol{b}=(0,\frac{3}{2})^T$, 再代入得 $\boldsymbol{a}=(-\frac{5}{4},0)^T$. 故一个特解为

$$\boldsymbol{y}_p=\begin{pmatrix}-\frac{5}{4}\\[2pt]\frac{3}{2}x\end{pmatrix}.$$

由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 通解为

$$\boldsymbol{y}=C_1\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix}+C_2\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\[2pt]\frac{3}{2}x\end{pmatrix}.$$

代入初值条件 $\boldsymbol{y}(0)=(2,3)$:

$$C_1\begin{pmatrix}1\\0\end{pmatrix}+C_2\begin{pmatrix}0\\-1\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\0\end{pmatrix}=\begin{pmatrix}2\\3\end{pmatrix},$$

解得 $C_1=\frac{13}{4},\ C_2=-3$. 故所求初值问题的解为

$$\boldsymbol{y}=\frac{13}{4}\begin{pmatrix}\cos 2x\\\sin 2x\end{pmatrix}-3\begin{pmatrix}\sin 2x\\-\cos 2x\end{pmatrix}+\begin{pmatrix}-\frac{5}{4}\\[2pt]\frac{3}{2}x\end{pmatrix}.$$

$\blacksquare$

### 习题六

(习题 6-2 题3(4))求微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}+\boldsymbol{f}(x)$ 满足初值条件 $\boldsymbol{y}(0)=\boldsymbol{\eta}$ 的解, 其中

$$A=\begin{pmatrix}16&14&38\\-9&-7&-18\\-4&-4&-11\end{pmatrix},\qquad\boldsymbol{f}(x)=\begin{pmatrix}-2e^{-x}\\-3e^{-x}\\2e^{-x}\end{pmatrix},\qquad\boldsymbol{\eta}=\begin{pmatrix}0\\0\\0\end{pmatrix}.$$

### 解答 习题六

先求 $A$ 的特征根. 计算特征多项式:

$$\det(A-\lambda E)=-(\lambda-2)(\lambda+1)(\lambda+3),$$

故特征根为 $\lambda=2,\ \lambda=-1,\ \lambda=-3$. 由**引理 6.6**(方程组有指数型非零解的充要条件)分别求对应的特征向量, 得

$$\boldsymbol{r}^{(2)}=\begin{pmatrix}-1\\1\\0\end{pmatrix},\qquad\boldsymbol{r}^{(-1)}=\begin{pmatrix}2\\3\\-2\end{pmatrix},\qquad\boldsymbol{r}^{(-3)}=\begin{pmatrix}-2\\0\\1\end{pmatrix}.$$

注意到非齐次项恰为

$$\boldsymbol{f}(x)=e^{-x}\begin{pmatrix}-2\\-3\\2\end{pmatrix}=-e^{-x}\boldsymbol{r}^{(-1)},$$

即非齐次向量共振于特征根 $\lambda=-1$. 由**推论 3**(常系数非齐次线性微分方程组的通解与初值问题解), 取 $x_0=0,\ \boldsymbol{y}_0=\boldsymbol{0}$, 初值问题的解为

$$\boldsymbol{y}(x)=\int_0^x e^{(x-s)A}\boldsymbol{f}(s)\,ds.$$

由于 $\boldsymbol{r}^{(-1)}$ 是 $\lambda=-1$ 的特征向量, 有 $e^{(x-s)A}\boldsymbol{r}^{(-1)}=e^{-(x-s)}\boldsymbol{r}^{(-1)}$, 故

$$\boldsymbol{y}(x)=-\boldsymbol{r}^{(-1)}\int_0^x e^{-(x-s)}e^{-s}\,ds=-\boldsymbol{r}^{(-1)}e^{-x}\int_0^x 1\,ds=-xe^{-x}\boldsymbol{r}^{(-1)}.$$

代入 $\boldsymbol{r}^{(-1)}=(2,3,-2)^T$, 所求解为

$$\boldsymbol{y}(x)=xe^{-x}\begin{pmatrix}-2\\-3\\2\end{pmatrix}.$$

$\blacksquare$

### 习题七

(习题 6-2 题4)求解微分方程组

$$\frac{d}{dt}\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}a&-b\\b&a\end{pmatrix}\begin{pmatrix}x\\y\end{pmatrix},$$

其中 $a$ 和 $b$ 为实常数, 而且 $b\neq0$.

### 解答 习题七

记 $A=\begin{pmatrix}a&-b\\b&a\end{pmatrix}$. 先求特征根. 特征方程为

$$\det(A-\lambda E)=(a-\lambda)^2+b^2=0,$$

故 $\lambda=a\pm ib$. 对 $\lambda=a+ib$, 解 $(A-(a+ib)E)\boldsymbol{r}=\boldsymbol{0}$:

$$\begin{pmatrix}-ib&-b\\b&-ib\end{pmatrix}\begin{pmatrix}r_1\\r_2\end{pmatrix}=\boldsymbol{0},$$

由第一行得 $-ir_1-r_2=0$, 取 $\boldsymbol{r}=(1,-i)^T$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 得复值解

$$\boldsymbol{y}_1=e^{(a+ib)t}\begin{pmatrix}1\\-i\end{pmatrix}.$$

由**附注 2**(从复值解提取实值解的方法), 利用 $e^{(a+ib)t}=e^{at}(\cos bt+i\sin bt)$ 取实部与虚部, 得

$$\boldsymbol{u}(t)=e^{at}\begin{pmatrix}\cos bt\\\sin bt\end{pmatrix},\qquad\boldsymbol{v}(t)=e^{at}\begin{pmatrix}\sin bt\\-\cos bt\end{pmatrix}.$$

由**定理 6.5**($n$ 个互不相同特征根时的基解矩阵), 通解为

$$\begin{pmatrix}x\\y\end{pmatrix}=C_1e^{at}\begin{pmatrix}\cos bt\\\sin bt\end{pmatrix}+C_2e^{at}\begin{pmatrix}\sin bt\\-\cos bt\end{pmatrix},$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题八

(习题 6-2 题5)证明: 常系数齐次线性微分方程组 $\frac{d\boldsymbol{y}}{dx}=A\boldsymbol{y}$ 的任何解当 $x\to+\infty$ 时都趋于零, 当且仅当它的系数矩阵 $A$ 的所有特征根都具有负的实部.

### 解答 习题八

由**定理 6.6**(有重特征根时常系数齐次线性微分方程组的基解矩阵), 方程组的任一解都是形如

$$e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots+\frac{x^{n_\lambda-1}}{(n_\lambda-1)!}\boldsymbol{r}_{n_\lambda-1}\right)$$

的向量函数的线性组合, 其中 $\lambda$ 为 $A$ 的特征根. 记 $\alpha=\mathrm{Re}\,\lambda$, 则上述函数的模满足估计

$$\left|e^{\lambda x}\left(\boldsymbol{r}_0+\frac{x}{1!}\boldsymbol{r}_1+\cdots\right)\right|\le e^{\alpha x}\left(M_0+M_1x+\cdots+M_{n_\lambda-1}x^{n_\lambda-1}\right),$$

其中 $M_k$ 为常数.

先证充分性. 设 $A$ 的所有特征根的实部均为负, 即对每个特征根 $\lambda$ 都有 $\alpha=\mathrm{Re}\,\lambda<0$. 由于多项式函数增长慢于指数函数的衰减, 对任意 $k\ge0$ 都有 $x^ke^{\alpha x}\to0\ (x\to+\infty)$, 故上式右端趋于零, 从而方程组的每一个解都趋于零.

再证必要性. 反设 $A$ 有某个特征根 $\lambda_j$ 满足 $\alpha_j=\mathrm{Re}\,\lambda_j\ge0$. 由**引理 6.6**(方程组有指数型非零解的充要条件), 取与 $\lambda_j$ 相应的特征向量 $\boldsymbol{r}_j\neq\boldsymbol{0}$, 则 $\boldsymbol{y}=e^{\lambda_j x}\boldsymbol{r}_j$ 是方程组的一个非零解. 当 $\alpha_j>0$ 时, $\|\boldsymbol{y}\|=e^{\alpha_j x}\|\boldsymbol{r}_j\|\to+\infty$; 当 $\alpha_j=0$ 时, 若 $\lambda_j=0$ 则 $\boldsymbol{y}=\boldsymbol{r}_j$ 为非零常向量, 若 $\lambda_j=i\beta\ (\beta\neq0)$ 则 $\boldsymbol{y}=e^{i\beta x}\boldsymbol{r}_j$ 的模恒为 $\|\boldsymbol{r}_j\|$ 而不趋于零. 这些都与题设结论矛盾. 故 $A$ 的所有特征根都必须具有负的实部. $\blacksquare$
