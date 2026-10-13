# 作业 13

> **定义 4.2**(包络)<br>设在平面上有一条连续可微的曲线 $\Gamma$. 如果对于任一点 $q\in\Gamma$, 在单参数曲线族 $K(C):V(x,y,C)=0$ 中都有一条曲线 $K(C^*)$ 通过 $q$ 点并在该点与 $\Gamma$ 相切, 而且 $K(C^*)$ 在 $q$ 点的任一邻域内不同于 $\Gamma$, 则称曲线 $\Gamma$ 为该曲线族的一支包络.

> **定理 4.3**(包络是奇解)<br>设微分方程 $F(x,y,\frac{dy}{dx})=0$ 有通积分 $U(x,y,C)=0$, 又设该积分曲线族有包络 $\Gamma:y=\varphi(x)$($x\in J$), 则包络 $y=\varphi(x)$ 是该微分方程的奇解. 因此, 求微分方程的奇解归结到求它的通积分的包络.

> **定理 4.4**(包络满足 $C$-判别式)<br>设 $\Gamma$ 是曲线族 $K(C):V(x,y,C)=0$ 的一支包络, 并且它可表示为参数 $C$ 的光滑曲线, 则它满足 $C$-判别式 $$\begin{cases}V(x,y,C)=0,\\V_C'(x,y,C)=0,\end{cases}$$ 或消去 $C$ 后所得关系式 $\Omega(x,y)=0$.

> **定理 4.5**($C$-判别式是包络的充分条件)<br>设由曲线族 $K(C):V(x,y,C)=0$ 的 $C$-判别式确定一支连续可微且不含于该曲线族的曲线 $$\Lambda:\begin{cases}x=\varphi(C),\\y=\psi(C),\end{cases}\qquad(C\in J),$$ 而且它满足非退化性条件 $$(\varphi'(C),\psi'(C))\neq(0,0),\qquad(V_x',V_y')\neq(0,0),$$ 则 $\Lambda$ 是该曲线族的一支包络.

### 习题一

(习题 4-3 题2)试求一微分方程, 使它有奇解 $y=\sin x$.

### 解答 习题一

由**定理 4.3**(包络是奇解), 只需构造一个单参数曲线族, 使其包络为 $y=\sin x$, 再写出以此曲线族为通积分的微分方程即可.

取 $y=\sin x$ 的全体切线. 在横坐标 $x=a$ 处, 切线方程为

$$
y=\sin a+\cos a\cdot(x-a)=x\cos a+\sin a-a\cos a.
$$

记曲线族为 $V(x,y,a)=y-x\cos a-\sin a+a\cos a=0$. 由**定理 4.4**(包络满足 $C$-判别式), 求其包络: 对参数 $a$ 求偏导, 得

$$
V_a'(x,y,a)=x\sin a-\cos a+\cos a-a\sin a=(x-a)\sin a.
$$

联立 $V=0$ 与 $V_a'=0$. 由 $(x-a)\sin a=0$, 取 $x=a$(此时 $\sin a\neq0$ 的分支), 代入 $V=0$ 得 $y=a\cos a+\sin a-a\cos a=\sin a$. 因 $x=a$, 故包络为 $y=\sin x$. 且该曲线不退化, 满足非退化性条件, 由**定理 4.5**($C$-判别式是包络的充分条件)确认 $y=\sin x$ 确是该曲线族的一支包络.

下面写出以此曲线族为通积分的微分方程. 令 $p=\frac{dy}{dx}=\cos a$, 则 $a=\arccos p$, $\sin a=\sqrt{1-p^2}$. 代入切线方程, 得

$$
y=xp+\sqrt{1-p^2}-p\arccos p.
$$

即所求微分方程为

$$
y=x\frac{dy}{dx}+\sqrt{1-\left(\frac{dy}{dx}\right)^2}-\frac{dy}{dx}\arccos\left(\frac{dy}{dx}\right).
$$

其通积分为 $y=Cx+\sqrt{1-C^2}-C\arccos C$, 而 $y=\sin x$ 是其奇解. 验证: 对 $y=\sin x$ 有 $p=\cos x$, 代入右端得

$$
x\cos x+\sqrt{1-\cos^2 x}-\cos x\cdot\arccos(\cos x)=x\cos x+\sin x-x\cos x=\sin x=y,
$$

故 $y=\sin x$ 确是该方程的解, 且由**定理 4.3**(包络是奇解)知它是奇解. $\blacksquare$
