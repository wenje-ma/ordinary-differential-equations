# 作业 14

> **自治(驻定)微分方程**<br>有一类微分方程不明显包含自变量, 这类方程叫作自治(或驻定)的微分方程. 对它们可以进行降阶. 例如对二阶自治方程 $y''=f\left(y,y'\right)$, 令 $z=\frac{dy}{dx}$, 则有 $y''=\frac{dz}{dx}=\frac{dz}{dy}\cdot\frac{dy}{dx}=z\frac{dz}{dy}$, 从而降为关于 $z=z\left(y\right)$ 的一阶方程 $z\frac{dz}{dy}=f\left(y,z\right)$.

> **首次积分**<br>由高阶微分方程积分一次(因而包含一个任意常数)所得的关系式称为首次积分. 例如对自治方程 $y''=f\left(y,y'\right)$, 以 $y'$ 乘方程后左端恰为全微分 $\frac{d}{dx}\left[\frac{1}{2}\left(y'\right)^2-F\left(y\right)\right]$, 其中 $F'\left(y\right)=-f\left(y,0\right)$ 的相应原函数, 直接积分即得首次积分.

> **相平面, 轨线与相图**<br>对于二阶自治方程 $\frac{d^2x}{dt^2}=f\left(x,\frac{dx}{dt}\right)$, 在相平面 $O\left(x,v\right)$($v=\frac{dx}{dt}$)上, 由首次积分 $\frac{1}{2}v^2+V\left(x\right)=E$ 确定的曲线称为轨线; 轨线在相平面上的分布图称为相图. 静止点对应于方程的零解(平凡解), 封闭轨线表示周期运动.

> **单摆方程与线性单摆方程**<br>单摆的运动方程为 $\frac{d^2\theta}{dt^2}+a^2\sin\theta=0$, 其中常数 $a=\sqrt{\frac{g}{l}}$, $g$ 为重力加速度大小, $l$ 为摆长. 取 $\sin\theta$ 的一次近似 $\sin\theta\approx\theta$, 得线性单摆方程 $\frac{d^2\theta}{dt^2}+a^2\theta=0$, 其通解为 $\theta=A\sin\left(at+D\right)$, 其中 $A,D$ 为任意常数, 振动周期为 $T=\frac{2\pi}{a}=2\pi\sqrt{\frac{l}{g}}$.

### 习题一

(习题 5-1 题1)利用线性单摆方程估计读者所在地的重力加速度大小 $g$.

### 解答 习题一

由**单摆方程与线性单摆方程**, 线性化后的单摆方程为 $\theta''+a^2\theta=0$, 其中 $a=\sqrt{\frac{g}{l}}$, 其通解为 $\theta=A\sin\left(at+D\right)$, 故单摆小振动的周期为

$$
T=\frac{2\pi}{a}=2\pi\sqrt{\frac{l}{g}}.
$$

由此反解出重力加速度大小

$$
g=\frac{4\pi^2l}{T^2}.
$$

实际测量时, 用细线拴一小重锤制成单摆, 量出悬点到重锤质心的长度 $l$ 作为摆长; 让小角度自由摆动, 用秒表测出完成 $N$ 次全振动所用的总时间 $t_N$, 取平均得周期 $T=\frac{t_N}{N}$(多测几次取平均可减小误差); 代入上式即得所在地的重力加速度大小 $g$.

$\blacksquare$

### 习题二

(习题 5-1 题2)如果在非线性单摆方程中取 $\sin x$ 的三次近似, 即 $\sin x\approx x-\frac{1}{6}x^3$, 则有单摆的三次近似方程 $\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)=0$. 由此证明单摆振动是不等时的, 而且它的相图表明可以发生进动.

### 解答 习题二

由**首次积分**, 以 $\frac{dx}{dt}$ 乘方程 $\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)=0$, 得

$$
\frac{dx}{dt}\cdot\frac{d^2x}{dt^2}+a^2\left(x-\frac{1}{6}x^3\right)\frac{dx}{dt}=0.
$$

左端为全微分, 直接积分得首次积分

$$
\frac{1}{2}\left(\frac{dx}{dt}\right)^2+\frac{a^2}{2}x^2-\frac{a^2}{24}x^4=E,
$$

其中 $E$ 为任意常数. 记 $v=\frac{dx}{dt}$, 则相平面 $O\left(x,v\right)$ 上的轨线方程为

$$
v^2=2E-a^2x^2+\frac{a^2}{12}x^4.
$$

先找静止点. 由 $v=0$ 与 $x''=-a^2\left(x-\frac{1}{6}x^3\right)=0$, 得 $x=0$ 或 $x=\pm\sqrt{6}$. 在 $x=0$ 附近线性化得 $x''+a^2x=0$, 故 $\left(0,0\right)$ 为中心(封闭轨线包围它, 对应振动); 在 $x=\pm\sqrt{6}$ 附近线性化得 $u''-2a^2u=0$, 故 $\left(\pm\sqrt{6},0\right)$ 为鞍点. 鞍点处能量为 $E_*=\frac{a^2}{2}\cdot 6-\frac{a^2}{24}\cdot 36=\frac{3}{2}a^2$, 过鞍点的轨线为分界线.

(1) 证明振动不等时. 考虑振幅为 $A$($0<A<\sqrt{6}$) 的封闭轨线, 它在 $x=A$ 处掉头(即 $v=0$), 故 $E=\frac{a^2}{2}A^2-\frac{a^2}{24}A^4$. 振动周期为

$$
T\left(A\right)=4\int_0^A\frac{dx}{\sqrt{2\left[E-\left(\frac{a^2}{2}x^2-\frac{a^2}{24}x^4\right)\right]}}.
$$

化简被积函数, 得

$$
2\left[E-\left(\frac{a^2}{2}x^2-\frac{a^2}{24}x^4\right)\right]=a^2\left(A^2-x^2\right)\left[1-\frac{A^2+x^2}{12}\right].
$$

作代换 $x=A\sin\varphi$, 则 $dx=A\cos\varphi\,d\varphi$, 且 $\sqrt{A^2-x^2}=A\cos\varphi$, 于是

$$
T\left(A\right)=\frac{4}{a}\int_0^{\frac{\pi}{2}}\frac{d\varphi}{\sqrt{1-\frac{A^2}{12}\left(1+\sin^2\varphi\right)}}.
$$

当 $A\to 0$ 时, $T\left(A\right)\to\frac{4}{a}\cdot\frac{\pi}{2}=\frac{2\pi}{a}$, 即线性单摆的周期. 而当 $0<A<\sqrt{6}$ 时, 被积函数的分母 $<1$, 故被积函数 $>1$, 从而 $T\left(A\right)>\frac{2\pi}{a}$; 并且 $A$ 越大分母越小, $T\left(A\right)$ 越大. 因此周期 $T$ 随振幅 $A$ 变化, 即单摆振动是不等时的. 又当 $A\to\sqrt{6}^{-}$ 时, 在 $\varphi=\frac{\pi}{2}$ 处分母趋于零, 周期 $T\left(A\right)\to+\infty$.

(2) 说明相图上可以发生进动. 当能量 $E>\frac{3}{2}a^2$ 时, 首次积分右端 $2E-a^2x^2+\frac{a^2}{12}x^4\to+\infty$($\left|x\right|\to\infty$), 故 $v=\frac{dx}{dt}$ 恒不为零且不变号: $v>0$ 时 $x\left(t\right)$ 单调增加, $v<0$ 时 $x\left(t\right)$ 单调减少, 轨线不再掉头封闭, 而是绕过两个鞍点 $\left(\pm\sqrt{6},0\right)$ 向 $\left|x\right|$ 增大的方向延伸. 在相图上这就是分界线之外的上, 下两支轨线, 对应单摆越过最高点持续转动, 即发生进动.

$\blacksquare$
