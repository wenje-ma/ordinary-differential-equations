# 作业 5

> **齐次方程**<br>若一阶微分方程 $$P\left(x,y\right)dx+Q\left(x,y\right)dy=0$$ 中的 $P\left(x,y\right)$ 与 $Q\left(x,y\right)$ 是同次齐次函数, 即 $P\left(tx,ty\right)=t^mP\left(x,y\right),\ Q\left(tx,ty\right)=t^mQ\left(x,y\right)$, 则称它为齐次方程. 作变量替换 $y=ux$($u$ 为新未知函数), 方程化为关于 $u$ 与 $x$ 的变量分离方程.

> **可化为齐次的方程**<br>对方程 $$\frac{dy}{dx}=\frac{ax+by+c}{mx+ny+l},$$ 当 $c,l$ 不全为零时, 若 $\Delta=an-bm\neq0$, 可由线性方程组 $a\alpha+b\beta+c=0,\ m\alpha+n\beta+l=0$ 定出 $\alpha,\beta$, 作平移变换 $x=\xi+\alpha,\ y=\eta+\beta$, 方程化为齐次方程 $\frac{d\eta}{d\xi}=\frac{a\xi+b\eta}{m\xi+n\eta}$; 再令 $\eta=u\xi$ 即化为变量分离方程.

> **伯努利方程**<br>形如 $$\frac{dy}{dx}+p\left(x\right)y=q\left(x\right)y^n$$ 的方程称为伯努利方程, 其中常数 $n\neq0,1$. 以 $\left(1-n\right)y^{-n}$ 乘方程两端, 再令 $z=y^{1-n}$, 方程化为关于 $z$ 的一阶线性方程 $$\frac{dz}{dx}+\left(1-n\right)p\left(x\right)z=\left(1-n\right)q\left(x\right).$$

> **里卡蒂方程**<br>若一阶方程 $\frac{dy}{dx}=f\left(x,y\right)$ 的右端是关于 $y$ 的二次多项式, 即写成 $$\frac{dy}{dx}=p\left(x\right)y^2+q\left(x\right)y+r\left(x\right),$$ 则称它为里卡蒂方程, 其中 $p\left(x\right),q\left(x\right),r\left(x\right)$ 在区间上连续且 $p\left(x\right)$ 不恒为零.

### 习题一

(习题 2-4 题1(2))求解微分方程 $y'=\frac{2y-x+5}{2x-y-4}$.

### 解答 习题一

这是**可化为齐次的方程**. 解方程组 $2y-x+5=0,\ 2x-y-4=0$, 得 $x=1,\ y=-2$. 作平移变换 $x=\xi+1,\ y=\eta-2$, 则
$$
2y-x+5=2\eta-\xi,\quad2x-y-4=2\xi-\eta.
$$

方程化为齐次方程 $\frac{d\eta}{d\xi}=\frac{2\eta-\xi}{2\xi-\eta}$. 令 $\eta=u\xi$, 由**齐次方程**, 得
$$
u+\xi\frac{du}{d\xi}=\frac{2u-1}{2-u}.
$$

整理得 $\xi\frac{du}{d\xi}=\frac{u^2-1}{2-u}$, 分离变量:
$$
\frac{2-u}{u^2-1}du=\frac{d\xi}{\xi}.
$$

将左端分项 $\frac{2-u}{u^2-1}=\frac{1/2}{u-1}-\frac{3/2}{u+1}$, 积分得
$$
\frac{1}{2}\ln\left|u-1\right|-\frac{3}{2}\ln\left|u+1\right|=\ln\left|\xi\right|+C.
$$

即 $\frac{u-1}{\left(u+1\right)^3}=C\xi^2$. 以 $u=\frac{\eta}{\xi}$ 代回, 化简得 $\frac{\eta-\xi}{\left(\eta+\xi\right)^3}=C$. 再代回 $\xi=x-1,\ \eta=y+2$, 通积分为
$$
y-x+3=C\left(x+y+1\right)^3.
$$

$\blacksquare$

### 习题二

(习题 2-4 题1(4))求解微分方程 $y'=x^3y^3-xy$.

### 解答 习题二

原方程即 $\frac{dy}{dx}+xy=x^3y^3$, 这是 $n=3$ 的**伯努利方程**. 以 $\left(1-n\right)y^{-n}=-2y^{-3}$ 乘方程两端, 并令 $z=y^{-2}$, 则 $z'=-2y^{-3}y'$, 方程化为一阶线性方程
$$
z'-2xz=-2x^3.
$$

由一阶线性方程的积分因子法, 积分因子为 $e^{\int-2x\,dx}=e^{-x^2}$. 于是
$$
\frac{d}{dx}\left(ze^{-x^2}\right)=-2x^3e^{-x^2}.
$$

右端积分 $\int-2x^3e^{-x^2}dx=\left(x^2+1\right)e^{-x^2}$, 故
$$
ze^{-x^2}=\left(x^2+1\right)e^{-x^2}+C.
$$

即 $z=x^2+1+Ce^{x^2}$. 以 $z=y^{-2}$ 代回, 通积分为
$$
\frac{1}{y^2}=x^2+1+Ce^{x^2},
$$

此外还应补上分离时丢失的特解 $y\equiv0$. $\blacksquare$

### 习题三

(习题 2-4 题2(2))利用适当的变换, 求解方程 $\left(3uv+v^2\right)du+\left(u^2+uv\right)dv=0$.

### 解答 习题三

记 $P\left(u,v\right)=3uv+v^2,\ Q\left(u,v\right)=u^2+uv$, 二者均为二次齐次函数, 故这是**齐次方程**. 令 $v=wu$($w$ 为新未知函数), 则 $\frac{dv}{du}=w+u\frac{dw}{du}$, 原方程化为
$$
\frac{dv}{du}=-\frac{3uv+v^2}{u^2+uv}=-\frac{3w+w^2}{1+w}.
$$

于是
$$
u\frac{dw}{du}=-\frac{3w+w^2}{1+w}-w=-\frac{2w\left(2+w\right)}{1+w}.
$$

分离变量:
$$
\frac{1+w}{w\left(2+w\right)}dw=-\frac{2\,du}{u}.
$$

将左端分项 $\frac{1+w}{w\left(2+w\right)}=\frac{1/2}{w}+\frac{1/2}{w+2}$, 积分得
$$
\frac{1}{2}\ln\left|w\right|+\frac{1}{2}\ln\left|w+2\right|=-2\ln\left|u\right|+C.
$$

即 $w\left(w+2\right)=Cu^{-4}$. 以 $w=\frac{v}{u}$ 代回, 并整理, 通积分为
$$
u^2v\left(v+2u\right)=C.
$$

其中 $C=0$ 已包含特解 $v=0$ 与 $v=-2u$. $\blacksquare$

### 习题四

(习题 2-4 题2(4))利用适当的变换, 求解方程 $\frac{dy}{dx}=\frac{2x^3+3xy^2-7x}{3x^2y+2y^3-8y}$.

### 解答 习题四

右端可写为 $\frac{x\left(2x^2+3y^2-7\right)}{y\left(3x^2+2y^2-8\right)}$. 作变换 $u=x^2,\ v=y^2$, 则 $\frac{dv}{du}=\frac{2y\,dy/dx}{2x}=\frac{y}{x}\frac{dy}{dx}$, 代入得
$$
\frac{dv}{du}=\frac{2u+3v-7}{3u+2v-8}.
$$

这是**可化为齐次的方程**. 解方程组 $2u+3v-7=0,\ 3u+2v-8=0$, 得 $u=2,\ v=1$. 作平移变换 $u=\xi+2,\ v=\eta+1$, 则
$$
2u+3v-7=2\xi+3\eta,\quad3u+2v-8=3\xi+2\eta.
$$

方程化为 $\frac{d\eta}{d\xi}=\frac{2\xi+3\eta}{3\xi+2\eta}$. 令 $\eta=w\xi$, 由**齐次方程**, 得
$$
\xi\frac{dw}{d\xi}=\frac{2+3w}{3+2w}-w=\frac{2\left(1-w^2\right)}{3+2w}.
$$

分离变量:
$$
\frac{3+2w}{1-w^2}dw=\frac{2\,d\xi}{\xi}.
$$

将左端分项 $\frac{3+2w}{1-w^2}=\frac{5/2}{1-w}+\frac{1/2}{1+w}$, 积分得
$$
-\frac{5}{2}\ln\left|1-w\right|+\frac{1}{2}\ln\left|1+w\right|=2\ln\left|\xi\right|+C.
$$

即 $\frac{1+w}{\left(1-w\right)^5}=C\xi^4$. 以 $w=\frac{\eta}{\xi}$ 代回, 化简得 $\frac{\xi+\eta}{\left(\xi-\eta\right)^5}=C$. 再代回 $\xi=x^2-2,\ \eta=y^2-1$, 通积分为
$$
x^2+y^2-3=C\left(x^2-y^2-1\right)^5.
$$

$\blacksquare$

### 习题五

(习题 2-4 题4)试把二阶微分方程 $y''+p\left(x\right)y'+q\left(x\right)y=0$ 化成一个里卡蒂方程.

### 解答 习题五

作对数导数变换 $y'=yz$, 即 $z=\frac{y'}{y}$($y\neq0$ 时), 其中 $z$ 为新未知函数. 对 $y'=yz$ 再求导, 得
$$
y''=y'z+yz'=yz^2+yz'.
$$

代入原二阶方程, 得
$$
yz^2+yz'+p\left(x\right)yz+q\left(x\right)y=0.
$$

约去非零因子 $y$, 整理得
$$
z'=-z^2-p\left(x\right)z-q\left(x\right).
$$

这正是**里卡蒂方程** $\frac{dz}{dx}=P\left(x\right)z^2+Q\left(x\right)z+R\left(x\right)$ 的形式, 其中 $P\left(x\right)=-1,\ Q\left(x\right)=-p\left(x\right),\ R\left(x\right)=-q\left(x\right)$. $\blacksquare$
