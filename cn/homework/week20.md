# 作业 20

> **定理 6.1***(齐次线性微分方程解的结构)<br>齐次线性微分方程 (6.47) 在区间 $\left(a,b\right)$ 上存在 $n$ 个线性无关的解. 如果这 $n$ 个线性无关的解如 $\varphi_1\left(x\right),\varphi_2\left(x\right),\cdots,\varphi_n\left(x\right)$ 所示, 则方程 (6.47) 的通解为 $$y=C_1\varphi_1\left(x\right)+C_2\varphi_2\left(x\right)+\cdots+C_n\varphi_n\left(x\right),$$ 其中 $C_1,C_2,\cdots,C_n$ 为任意常数. 这 $n$ 个线性无关的解称为一个基本解组.

> **定理 6.2***(解组线性无关的朗斯基行列式判据)<br>方程 (6.47) 的解组 $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ 是线性无关的充要条件为它的朗斯基行列式 $$W\left(x\right)=\left|\begin{matrix}\varphi_1\left(x\right)&\cdots&\varphi_n\left(x\right)\\\varphi_1'\left(x\right)&\cdots&\varphi_n'\left(x\right)\\\vdots&&\vdots\\\varphi_1^{\left(n-1\right)}\left(x\right)&\cdots&\varphi_n^{\left(n-1\right)}\left(x\right)\end{matrix}\right|$$ 在区间 $\left(a,b\right)$ 上恒不为零.

> **刘维尔公式**(朗斯基行列式的演化公式 (6.54))<br>若 $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ 是方程 (6.47) 的解组, 其朗斯基行列式为 $W\left(x\right)$, 则 $$W\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}a_1\left(s\right)ds}\quad\left(a< x< b\right),$$ 其中 $x_0\in\left(a,b\right)$, 而 $a_1\left(x\right)$ 是方程 (6.47) 中 $y^{\left(n-1\right)}$ 项的系数. 特别地, 对二阶方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 有 $a_1\left(x\right)=p\left(x\right)$.

> **例 1**(由一个非零解构造通解的公式 (6.56))<br>设 $y=\varphi\left(x\right)$ 是二阶齐次线性微分方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 的一个非零解, 其中 $p\left(x\right)$ 和 $q\left(x\right)$ 是区间 $\left(a,b\right)$ 上的连续函数, 则在 $\varphi\left(x\right)\neq0$ 的子区间上方程的通解为 $$y=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2\left(s\right)}e^{-\int_{x_0}^{s}p\left(t\right)dt}ds\right],$$ 其中 $C_1$ 和 $C_2$ 为任意常数.

> **定理 6.3***(非齐次线性微分方程的通解结构与常数变易公式 (6.57)(6.58))<br>设 $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ 是齐次线性微分方程 (6.47) 在区间 $\left(a,b\right)$ 上的一个基本解组, 则非齐次线性微分方程 (6.46) 的通解为 $$y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)+\varphi^*\left(x\right),$$ 其中 $$\varphi^*\left(x\right)=\sum_{k=1}^{n}\varphi_k\left(x\right)\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds$$ 是方程 (6.46) 的一个特解, $W\left(x\right)$ 是基本解组的朗斯基行列式, 而 $W_k\left(x\right)$ 是 $W\left(x\right)$ 中第 $n$ 行第 $k$ 列元素的代数余子式.

> **定理 6.6***(常系数齐次线性微分方程的特征根解法)<br>常系数齐次线性微分方程 $y^{\left(n\right)}+a_1y^{\left(n-1\right)}+\cdots+a_ny=0$ 的特征方程为 $$\lambda^n+a_1\lambda^{n-1}+\cdots+a_{n-1}\lambda+a_n=0.$$ 设特征方程在复数域中共有 $s$ 个互不相同的根 $\lambda_1,\cdots,\lambda_s$, 相应重数分别为 $n_1,\cdots,n_s$, 则函数组 $e^{\lambda_kx},\ xe^{\lambda_kx},\ \cdots,\ x^{n_k-1}e^{\lambda_kx}\ \left(k=1,\cdots,s\right)$ 是一个基本解组. 复根成对共轭出现, 取复值解的实部和虚部即得相应的实值解.

> **待定系数法**(对特殊非齐次项预先设定特解形式)<br>当非齐次项为 $f\left(x\right)=P_m\left(x\right)e^{\mu x}$(其中 $P_m\left(x\right)$ 是 $m$ 次多项式) 时, 若 $\mu$ 不是特征根, 设特解 $\varphi^*\left(x\right)=Q_m\left(x\right)e^{\mu x}$; 若 $\mu$ 是 $k$ 重特征根, 则设 $$\varphi^*\left(x\right)=x^kQ_m\left(x\right)e^{\mu x},$$ 其中 $Q_m\left(x\right)$ 是系数待定的 $m$ 次多项式. 当非齐次项为 $f\left(x\right)=\left[A_m\left(x\right)\cos\beta x+B_l\left(x\right)\sin\beta x\right]e^{\alpha x}$ 时, 设 $$\varphi^*\left(x\right)=x^k\left[C_n\left(x\right)\cos\beta x+D_n\left(x\right)\sin\beta x\right]e^{\alpha x},$$ 其中 $k$ 是 $\alpha\pm i\beta$ 作为特征根的重数 (不是特征根时取 $k=0$), $n=\max\left\{m,l\right\}$, 多项式 $C_n\left(x\right),D_n\left(x\right)$ 的系数待定.

> **初值问题解的存在唯一性**<br>$n$ 阶线性微分方程满足初值条件 $y\left(x_0\right)=y_0,\ y'\left(x_0\right)=y_0',\ \cdots,\ y^{\left(n-1\right)}\left(x_0\right)=y_0^{\left(n-1\right)}$ 的解在系数与非齐次项的公共连续区间上存在而且唯一. 特别地, 初值条件全取零的初值问题只有零解.

### 习题一

(习题 6-3 题3)考虑微分方程 $y''+q\left(x\right)y=0$. (1) 设 $y=\varphi\left(x\right)$ 与 $y=\psi\left(x\right)$ 是它的任意两个解, 试证 $\varphi\left(x\right)$ 与 $\psi\left(x\right)$ 的朗斯基行列式恒等于一个常数. (2) 已知方程有一个特解为 $y=e^x$, 试求这方程的通解, 并确定 $q\left(x\right)$.

### 解答 习题一

(1) 该方程即 $y''+0\cdot y'+q\left(x\right)y=0$, 其中 $y'$ 项的系数 $a_1\left(x\right)=0$. 由**刘维尔公式**(朗斯基行列式的演化公式 (6.54)), 解组 $\varphi\left(x\right),\psi\left(x\right)$ 的朗斯基行列式为

$$
W\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}a_1\left(s\right)ds}=W\left(x_0\right)e^{-\int_{x_0}^{x}0\,ds}=W\left(x_0\right).
$$

故 $W\left(x\right)\equiv W\left(x_0\right)$ 恒等于一个常数.

(2) 将特解 $y=e^x$ 代入方程 $y''+q\left(x\right)y=0$. 由于 $\left(e^x\right)'=\left(e^x\right)''=e^x$, 故

$$
e^x+q\left(x\right)e^x=0,
$$

由此解出 $q\left(x\right)=-1$. 于是原方程为 $y''-y=0$, 它是二阶常系数齐次线性方程. 由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 其特征方程为 $\lambda^2-1=0$, 即 $\lambda=\pm1$ 为两个单根, 故一个基本解组为 $e^x$ 与 $e^{-x}$, 方程的通解为

$$
y=C_1e^x+C_2e^{-x},
$$

其中 $C_1,C_2$ 为任意常数, 且 $q\left(x\right)=-1$. $\blacksquare$

### 习题二

(习题 6-3 题4)考虑微分方程 $y''+p\left(x\right)y'+q\left(x\right)y=0\ \left(6.76\right)$, 其中 $p\left(x\right)$ 和 $q\left(x\right)$ 是区间 $I=\left(a,b\right)$ 上的连续函数. (1) 设 $y=\varphi\left(x\right)$ 是方程 (6.76) 在区间 $I$ 上的一个非零解 (即 $\varphi\left(x\right)$ 在区间 $I$ 上不恒等于零), 试证 $\varphi\left(x\right)$ 在区间 $I$ 上只有简单零点 (即: 如果存在 $x_0\in I$, 使得 $\varphi\left(x_0\right)=0$, 那么必有 $\varphi'\left(x_0\right)\neq0$), 并由此进一步证明, $\varphi\left(x\right)$ 在任意有限闭区间上至多有有限个零点, 从而每一个零点都是孤立的. (2) 在例 1 中, 对一般的情形证明相应的结论.

### 解答 习题二

(1) 先证简单零点. 反设存在 $x_0\in I$ 使 $\varphi\left(x_0\right)=0$ 且 $\varphi'\left(x_0\right)=0$. 由**初值问题解的存在唯一性**, 以 $\varphi\left(x_0\right)=0,\ \varphi'\left(x_0\right)=0$ 为初值的初值问题只有零解 $y\equiv0$, 因此 $\varphi\left(x\right)\equiv0$ 在 $I$ 上成立, 与 $\varphi\left(x\right)$ 为非零解矛盾. 故若 $\varphi\left(x_0\right)=0$, 必有 $\varphi'\left(x_0\right)\neq0$, 即 $\varphi\left(x\right)$ 的零点都是简单零点.

再证零点孤立. 由于 $\varphi\left(x\right)$ 是方程 (6.76) 的解, 而 $p\left(x\right),q\left(x\right)$ 连续, 故 $\varphi'\left(x\right)$ 连续. 对任一零点 $x_0$, 由 $\varphi'\left(x_0\right)\neq0$ 及 $\varphi'$ 的连续性, 存在 $x_0$ 的邻域, 在该邻域内 $\varphi'\left(x\right)$ 保持非零且同号, 从而 $\varphi\left(x\right)$ 严格单调, 于是 $x_0$ 是该邻域内唯一的零点, 即每个零点都是孤立的.

最后证有限闭区间上零点有限. 任取有限闭区间 $\left[c,d\right]\subset I$, 反设 $\varphi\left(x\right)$ 在 $\left[c,d\right]$ 上有无穷多个零点. 由有界无穷点集必有聚点的维尔斯特拉斯聚点原理, 这些零点在 $\left[c,d\right]$ 内存在聚点 $x_*$. 由 $\varphi$ 的连续性得 $\varphi\left(x_*\right)=0$, 即 $x_*$ 本身也是零点. 但由上一段, $x_*$ 是孤立零点, 与它是零点列的聚点矛盾. 故 $\varphi\left(x\right)$ 在 $\left[c,d\right]$ 上至多有有限个零点.

(2) 例 1 为简单起见曾假定 $\varphi\left(x\right)$ 在区间上恒不为零; 一般情形即 $\varphi\left(x\right)$ 允许有零点的情形. 由 (1), $\varphi\left(x\right)$ 的零点都是孤立的简单零点, 因此可在 $I$ 内任取一个不含 $\varphi$ 零点的开区间 $J$, 并取定 $x_0\in J$. 设 $y\left(x\right)$ 是方程 (6.55) 的任一解. 对解组 $\varphi\left(x\right),y\left(x\right)$ 用**刘维尔公式**(朗斯基行列式的演化公式 (6.54)), 其朗斯基行列式为

$$
W\left(x\right)=\left|\begin{matrix}\varphi\left(x\right)&y\left(x\right)\\\varphi'\left(x\right)&y'\left(x\right)\end{matrix}\right|=\varphi\left(x\right)y'\left(x\right)-\varphi'\left(x\right)y\left(x\right)=W\left(x_0\right)e^{-\int_{x_0}^{x}p\left(s\right)ds}.
$$

记 $C=W\left(x_0\right)$. 在 $J$ 上 $\varphi\left(x\right)\neq0$, 以 $\frac{1}{\varphi^2\left(x\right)}$ 乘上式两端, 得

$$
\frac{d}{dx}\left(\frac{y}{\varphi}\right)=\frac{\varphi y'-\varphi'y}{\varphi^2}=\frac{C}{\varphi^2\left(x\right)}e^{-\int_{x_0}^{x}p\left(s\right)ds}.
$$

两端从 $x_0$ 到 $x$ ($x\in J$) 积分, 得

$$
y\left(x\right)=\varphi\left(x\right)\left[C_1+C_2\int_{x_0}^{x}\frac{1}{\varphi^2\left(s\right)}e^{-\int_{x_0}^{s}p\left(t\right)dt}ds\right],
$$

其中 $C_1=\frac{y\left(x_0\right)}{\varphi\left(x_0\right)},\ C_2=C$ 为任意常数. 这正是 (6.56) 式. 由于不含零点的开区间可取遍 $I$ 内任意两个相邻零点之间的部分 (以及区间端点邻域), 故一般情形下例 1 的通解公式仍在相应子区间上成立. $\blacksquare$

### 习题三

(习题 6-3 题5)设函数 $u\left(x\right)$ 和 $v\left(x\right)$ 是方程 (6.76) 的一个基本解组, 试证: (1) 方程的系数函数 $p\left(x\right)$ 和 $q\left(x\right)$ 能由这个基本解组唯一地确定. (2) $u\left(x\right)$ 和 $v\left(x\right)$ 没有共同的零点.

### 解答 习题三

(1) 由于 $u\left(x\right),v\left(x\right)$ 是方程 (6.76) 的解, 它们满足

$$
u''+p\left(x\right)u'+q\left(x\right)u=0,\quad v''+p\left(x\right)v'+q\left(x\right)v=0.
$$

将 $p\left(x\right),q\left(x\right)$ 视为未知量, 这是以 $u'\left(x\right),u\left(x\right)$ 和 $v'\left(x\right),v\left(x\right)$ 为系数的线性代数方程组:

$$
\left\{\begin{matrix}u'\left(x\right)p\left(x\right)+u\left(x\right)q\left(x\right)=-u''\left(x\right),\\v'\left(x\right)p\left(x\right)+v\left(x\right)q\left(x\right)=-v''\left(x\right).\end{matrix}\right.
$$

其系数行列式为

$$
\Delta\left(x\right)=u'\left(x\right)v\left(x\right)-u\left(x\right)v'\left(x\right)=-\left[u\left(x\right)v'\left(x\right)-u'\left(x\right)v\left(x\right)\right]=-W\left(x\right),
$$

其中 $W\left(x\right)$ 是基本解组 $u,v$ 的朗斯基行列式. 由**定理 6.2***(解组线性无关的朗斯基行列式判据), $u,v$ 为基本解组蕴含 $W\left(x\right)\neq0$ 在 $I$ 上恒成立, 故 $\Delta\left(x\right)\neq0$, 上述线性方程组有唯一解. 由克莱姆法则解得

$$
p\left(x\right)=\frac{u''\left(x\right)v\left(x\right)-u\left(x\right)v''\left(x\right)}{W\left(x\right)},\quad q\left(x\right)=\frac{u'\left(x\right)v''\left(x\right)-u''\left(x\right)v'\left(x\right)}{W\left(x\right)}.
$$

因此 $p\left(x\right),q\left(x\right)$ 被基本解组 $u,v$ 唯一地确定.

(2) 反设 $u\left(x\right),v\left(x\right)$ 有共同零点 $x_0\in I$, 即 $u\left(x_0\right)=v\left(x_0\right)=0$. 则

$$
W\left(x_0\right)=u\left(x_0\right)v'\left(x_0\right)-u'\left(x_0\right)v\left(x_0\right)=0.
$$

但 $u,v$ 是基本解组, 由**定理 6.2***(解组线性无关的朗斯基行列式判据), $W\left(x\right)$ 在 $I$ 上恒不为零, 矛盾. 故 $u\left(x\right)$ 与 $v\left(x\right)$ 没有共同的零点. $\blacksquare$

### 习题四

(习题 6-3 题6)试用常数变易法证明定理 6.3*.

### 解答 习题四

设 $\varphi_1\left(x\right),\cdots,\varphi_n\left(x\right)$ 是齐次线性微分方程 (6.47) 的一个基本解组. 由**定理 6.1***(齐次线性微分方程解的结构), 齐次方程的通解为 $y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)$. 常数变易法的思想是把常数 $C_k$ 变易为 $x$ 的函数, 设非齐次方程 (6.46) 有形如

$$
y=C_1\left(x\right)\varphi_1\left(x\right)+\cdots+C_n\left(x\right)\varphi_n\left(x\right)
$$

的解. 逐次求导, 并依次令各阶导数中变易常数导数的组合为零, 即令

$$
\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(j\right)}\left(x\right)=0\quad\left(j=0,1,\cdots,n-2\right),
$$

则有 $y^{\left(j\right)}\left(x\right)=\sum_{k=1}^{n}C_k\left(x\right)\varphi_k^{\left(j\right)}\left(x\right)\ \left(j=0,1,\cdots,n-1\right)$. 再求一次导数, 得

$$
y^{\left(n\right)}\left(x\right)=\sum_{k=1}^{n}C_k\left(x\right)\varphi_k^{\left(n\right)}\left(x\right)+\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right).
$$

将 $y,y',\cdots,y^{\left(n\right)}$ 代入方程 (6.46), 注意到每个 $\varphi_k$ 满足齐次方程, 含 $C_k\left(x\right)$ 的项全部抵消, 剩下

$$
\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right)=f\left(x\right).
$$

于是 $C_1'\left(x\right),\cdots,C_n'\left(x\right)$ 满足线性方程组

$$
\left\{\begin{matrix}\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k\left(x\right)=0,\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k'\left(x\right)=0,\\\quad\vdots\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-2\right)}\left(x\right)=0,\\\sum_{k=1}^{n}C_k'\left(x\right)\varphi_k^{\left(n-1\right)}\left(x\right)=f\left(x\right).\end{matrix}\right.
$$

其系数行列式恰为基本解组的朗斯基行列式 $W\left(x\right)$. 由**定理 6.2***(解组线性无关的朗斯基行列式判据), $W\left(x\right)\neq0$, 故由克莱姆法则, $C_k'\left(x\right)$ 等于把 $W\left(x\right)$ 的第 $k$ 列换成右端向量 $\left(0,\cdots,0,f\left(x\right)\right)^T$ 所得行列式除以 $W\left(x\right)$. 按第 $k$ 列展开该行列式, 只有最后一行的 $f\left(x\right)$ 贡献, 故

$$
C_k'\left(x\right)=\frac{W_k\left(x\right)}{W\left(x\right)}f\left(x\right),
$$

其中 $W_k\left(x\right)$ 是 $W\left(x\right)$ 中第 $n$ 行第 $k$ 列元素的代数余子式. 取积分常数为零以得到一个特解, 积分得

$$
C_k\left(x\right)=\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds\quad\left(k=1,\cdots,n\right).
$$

代回所设解的形式, 得方程 (6.46) 的一个特解

$$
\varphi^*\left(x\right)=\sum_{k=1}^{n}\varphi_k\left(x\right)\int_{x_0}^{x}\frac{W_k\left(s\right)}{W\left(s\right)}f\left(s\right)ds.
$$

再叠加上齐次通解中任意常数 $C_1,\cdots,C_n$, 即得方程 (6.46) 的通解

$$
y=C_1\varphi_1\left(x\right)+\cdots+C_n\varphi_n\left(x\right)+\varphi^*\left(x\right),
$$

正是公式 (6.57)(6.58). **定理 6.3***(非齐次线性微分方程的通解结构与常数变易公式 (6.57)(6.58)) 证完. $\blacksquare$

### 习题五

(习题 6-3 题7)设欧拉方程 $x^ny^{\left(n\right)}+a_1x^{n-1}y^{\left(n-1\right)}+\cdots+a_{n-1}xy'+a_ny=0$, 其中 $a_1,a_2,\cdots,a_n$ 都是常数, $x> 0$. 试利用适当的变换把它化成常系数齐次线性微分方程.

### 解答 习题五

作自变量变换 $x=e^t$, 即 $t=\ln x\ \left(x> 0\right)$. 记 $D=\frac{d}{dt}$, 则 $\frac{d}{dx}=\frac{1}{x}\frac{d}{dt}$, 即

$$
x\frac{d}{dx}=D.
$$

下面归纳证明

$$
x^ky^{\left(k\right)}=D\left(D-1\right)\cdots\left(D-k+1\right)y\quad\left(k=1,2,\cdots,n\right).
$$

$k=1$ 时 $xy'=Dy$, 显然成立. 设上式对 $k$ 成立, 则对 $k+1$ 有

$$
x^{k+1}y^{\left(k+1\right)}=x\frac{d}{dx}\left(x^ky^{\left(k\right)}\right)-kx^ky^{\left(k\right)}=D\Big[D\left(D-1\right)\cdots\left(D-k+1\right)y\Big]-k\Big[D\left(D-1\right)\cdots\left(D-k+1\right)y\Big],
$$

即

$$
x^{k+1}y^{\left(k+1\right)}=D\left(D-1\right)\cdots\left(D-k+1\right)\left(D-k\right)y.
$$

归纳完成. 将此式代入欧拉方程, 得

$$
\left[D\left(D-1\right)\cdots\left(D-n+1\right)+a_1D\left(D-1\right)\cdots\left(D-n+2\right)+\cdots+a_{n-1}D+a_n\right]y=0.
$$

左端是 $D=\frac{d}{dt}$ 的常系数多项式算子, 故上式是关于未知函数 $y=y\left(t\right)$ 的常系数齐次线性微分方程. $\blacksquare$

### 习题六

(习题 6-3 题9)求解弹簧振子在无阻尼下的强迫振动方程 $m\frac{d^2x}{dt^2}+kx=p\cos\omega t$, 其中 $m,k,p$ 和 $\omega$ 都是正的常数. 并对外加频率 $\omega\neq\omega_0$ 和 $\omega=\omega_0$ 两种不同的情况, 说明解的物理意义, 这里 $\omega_0=\sqrt{\frac{k}{m}}$ 是弹簧振子的固有频率.

### 解答 习题六

先解相应的齐次方程 $mx''+kx=0$, 即 $x''+\omega_0^2x=0$. 由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 特征方程为 $\lambda^2+\omega_0^2=0$, 得共轭复根 $\lambda=\pm i\omega_0$, 取实部虚部得基本解组 $\cos\omega_0t,\ \sin\omega_0t$, 故齐次通解为

$$
x_h\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t.
$$

(1) 当 $\omega\neq\omega_0$ 时, $\pm i\omega$ 不是特征根. 由**待定系数法**(对特殊非齐次项预先设定特解形式), 设特解 $x^*\left(t\right)=A\cos\omega t+B\sin\omega t$. 代入原方程:

$$
m\left(-A\omega^2\cos\omega t-B\omega^2\sin\omega t\right)+k\left(A\cos\omega t+B\sin\omega t\right)=p\cos\omega t.
$$

比较系数得 $\left(k-m\omega^2\right)A=p,\ \left(k-m\omega^2\right)B=0$, 故 $A=\frac{p}{k-m\omega^2}=\frac{p}{m\left(\omega_0^2-\omega^2\right)},\ B=0$. 通解为

$$
x\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t+\frac{p}{m\left(\omega_0^2-\omega^2\right)}\cos\omega t.
$$

其物理意义: 解由频率为固有频率 $\omega_0$ 的自由振动与频率为外加频率 $\omega$ 的强迫振动叠加而成, 一般为非周期运动; 当 $\omega$ 接近 $\omega_0$ 时, 两种简谐运动叠加产生"拍"现象, 振幅随时间周期性地增减.

(2) 当 $\omega=\omega_0$ 时, $\pm i\omega_0$ 是单特征根. 由**待定系数法**(对特殊非齐次项预先设定特解形式), 应设特解 $x^*\left(t\right)=t\big(A\cos\omega_0t+B\sin\omega_0t\big)$. 求导得

$$
x^{*''}\left(t\right)=-2A\omega_0\sin\omega_0t+2B\omega_0\cos\omega_0t-\omega_0^2t\big(A\cos\omega_0t+B\sin\omega_0t\big).
$$

代入 $mx''+kx$, 含 $t$ 的项因 $k=m\omega_0^2$ 抵消, 剩下

$$
-2mA\omega_0\sin\omega_0t+2mB\omega_0\cos\omega_0t=p\cos\omega_0t.
$$

比较系数得 $A=0,\ B=\frac{p}{2m\omega_0}$. 通解为

$$
x\left(t\right)=C_1\cos\omega_0t+C_2\sin\omega_0t+\frac{p}{2m\omega_0}\,t\sin\omega_0t.
$$

其物理意义: 这是无阻尼共振现象. 特解项 $\frac{p}{2m\omega_0}t\sin\omega_0t$ 的振幅随时间 $t$ 线性增长, 振动的幅值趋于无穷, 即外加频率等于固有频率时发生共振. $\blacksquare$

### 习题七

(习题 6-3 题10(3))求解常系数线性微分方程 $y''+2y'=3+4\sin2x$.

### 解答 习题七

先解齐次方程 $y''+2y'=0$. 由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 特征方程为 $\lambda^2+2\lambda=\lambda\left(\lambda+2\right)=0$, 得单根 $\lambda=0,\ -2$, 故齐次通解为

$$
y_h=C_1+C_2e^{-2x}.
$$

非齐次项 $3+4\sin2x$ 分为两部分, 分别求特解再叠加.

对常数项 $3=3e^{0\cdot x}$, $\mu=0$ 是单特征根. 由**待定系数法**(对特殊非齐次项预先设定特解形式), 设特解 $y_1^*=Ax$. 代入得 $\left(Ax\right)''+2\left(Ax\right)'=2A=3$, 故 $A=\frac{3}{2}$, 即 $y_1^*=\frac{3}{2}x$.

对 $4\sin2x$, $\pm2i$ 不是特征根. 设特解 $y_2^*=B\cos2x+D\sin2x$. 求导得 $y_2^{*'}=-2B\sin2x+2D\cos2x,\ y_2^{*''}=-4B\cos2x-4D\sin2x$. 代入方程:

$$
y_2^{*''}+2y_2^{*'}=\left(-4B+4D\right)\cos2x+\left(-4D-4B\right)\sin2x=4\sin2x.
$$

比较系数得 $-4B+4D=0,\ -4D-4B=4$, 解得 $B=D=-\frac{1}{2}$. 故 $y_2^*=-\frac{1}{2}\cos2x-\frac{1}{2}\sin2x$.

通解为

$$
y=C_1+C_2e^{-2x}+\frac{3}{2}x-\frac{1}{2}\left(\cos2x+\sin2x\right),
$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$

### 习题八

(习题 6-3 题10(6))求解常系数线性微分方程 $y'''-3ay''+3a^2y'-a^3y=0$.

### 解答 习题八

由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 特征方程为

$$
\lambda^3-3a\lambda^2+3a^2\lambda-a^3=\left(\lambda-a\right)^3=0,
$$

即 $\lambda=a$ 是三重特征根. 相应的基本解组为 $e^{ax},\ xe^{ax},\ x^2e^{ax}$, 故通解为

$$
y=\left(C_1+C_2x+C_3x^2\right)e^{ax},
$$

其中 $C_1,C_2,C_3$ 为任意常数. $\blacksquare$

### 习题九

(习题 6-3 题10(9))求解常系数线性微分方程 $y^{\left(4\right)}+2y''+y=\sin x,\ y\left(0\right)=1,\ y'\left(0\right)=-2,\ y''\left(0\right)=3,\ y'''\left(0\right)=0$.

### 解答 习题九

由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 特征方程为

$$
\lambda^4+2\lambda^2+1=\left(\lambda^2+1\right)^2=0,
$$

即 $\lambda=\pm i$ 均为二重特征根. 取复值解的实部虚部, 得基本解组 $\cos x,\ x\cos x,\ \sin x,\ x\sin x$, 故齐次通解为

$$
y_h=\left(C_1+C_2x\right)\cos x+\left(C_3+C_4x\right)\sin x.
$$

非齐次项为 $\sin x$, 而 $\pm i$ 是二重特征根. 由**待定系数法**(对特殊非齐次项预先设定特解形式), 设特解 $y^*=x^2\left(A\cos x+B\sin x\right)$. 记 $D=\frac{d}{dx}$, 原方程为 $\left(D^2+1\right)^2y=\sin x$. 直接求导可算得

$$
\left(D^2+1\right)^2\left(x^2\cos x\right)=-8\cos x,\quad\left(D^2+1\right)^2\left(x^2\sin x\right)=-8\sin x.
$$

代入得

$$
\left(D^2+1\right)^2y^*=-8A\cos x-8B\sin x=\sin x,
$$

比较系数得 $A=0,\ B=-\frac{1}{8}$, 故 $y^*=-\frac{1}{8}x^2\sin x$. 通解为

$$
y=\left(C_1+C_2x\right)\cos x+\left(C_3+C_4x\right)\sin x-\frac{1}{8}x^2\sin x.
$$

由**初值问题解的存在唯一性**, 任意给定的初值条件唯一确定一组常数. 计算各阶导数在 $x=0$ 的值: $y\left(0\right)=C_1$; 由 $y'=C_2\cos x-\left(C_1+C_2x\right)\sin x+C_4\sin x+\left(C_3+C_4x\right)\cos x-\frac{1}{8}\left(2x\sin x+x^2\cos x\right)$, 得 $y'\left(0\right)=C_2+C_3$; 直接算得 $y''\left(0\right)=-C_1+2C_4,\ y'''\left(0\right)=-3C_2-C_3-\frac{3}{4}$. 代入初值条件:

$$
C_1=1,\quad C_2+C_3=-2,\quad-C_1+2C_4=3,\quad-3C_2-C_3-\frac{3}{4}=0.
$$

解得 $C_1=1,\ C_2=\frac{5}{8},\ C_3=-\frac{21}{8},\ C_4=2$. 故所求特解为

$$
y=\left(1+\frac{5}{8}x\right)\cos x+\left(2x-\frac{21}{8}-\frac{1}{8}x^2\right)\sin x.
$$

$\blacksquare$

### 习题十

(习题 6-3 题10(12))求解常系数线性微分方程 $y''-5y'+6y=\left(12x-7\right)e^{-x}$.

### 解答 习题十

由**定理 6.6***(常系数齐次线性微分方程的特征根解法), 特征方程为

$$
\lambda^2-5\lambda+6=\left(\lambda-2\right)\left(\lambda-3\right)=0,
$$

得单根 $\lambda=2,\ 3$, 故齐次通解为

$$
y_h=C_1e^{2x}+C_2e^{3x}.
$$

非齐次项为 $\left(12x-7\right)e^{-x}$, 其中 $\mu=-1$ 不是特征根. 由**待定系数法**(对特殊非齐次项预先设定特解形式), 设特解 $y^*=\left(Ax+B\right)e^{-x}$. 求导得

$$
y^{*'}=\left(A-Ax-B\right)e^{-x},\quad y^{*''}=\left(Ax+B-2A\right)e^{-x}.
$$

代入方程:

$$
y^{*''}-5y^{*'}+6y^*=\big[Ax+B-2A-5\left(A-Ax-B\right)+6\left(Ax+B\right)\big]e^{-x}=\left(12Ax+12B-7A\right)e^{-x}.
$$

与 $\left(12x-7\right)e^{-x}$ 比较系数, 得 $12A=12,\ 12B-7A=-7$, 解得 $A=1,\ B=0$, 即 $y^*=xe^{-x}$. 通解为

$$
y=C_1e^{2x}+C_2e^{3x}+xe^{-x},
$$

其中 $C_1,C_2$ 为任意常数. $\blacksquare$
