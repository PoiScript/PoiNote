#解析函数
##I.解析函数的概念
###i.复变函数的导数与微分
####1.导数的定义
设函数 $w=f(z)$, 定义于区域 $D$, $z_0$ 为 $D$ 中的一点, 点 $z_0+\Delta z$ 不出 $D$ 的范围, 如果极限
\[\lim_{\Delta z\to0}\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}\]
存在,那么说 $f(z)$ 在 $z_0$ 可导, 这个极限值称为 $f(z)$ 在 $z_0$ 的导数, 记作:
\[f'(z_0)=\frac{dw}{dz}\mid_{z=z_0}=\lim_{\Delta z\to0}\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}\]
也就是说, 对于任意给定的 $\varepsilon>0$, 相应的有一个 $\delta(\varepsilon)>0$, 使得当 $0<|\Delta z|<\delta$ 时, 有:
\[\left|\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}-f'(z_0)\right|<\varepsilon\]
定义中的 $z_0+\Delta z\to z_0$(即 $\Delta z\to 0$) 的方式是任意的, 比一元实变函数的类似限制的严格得多, 从而使复变可导函数具有许多独特的性质和应用
####2.可导与连续
由在 $z_0$ 可导的定义, 对于仍给的 $\varepsilon>0$, 相应的有一个 $\delta>0$, 使得当 $0<|\Delta z|<\delta$ 时, 有:
\[\left|\frac{f(z_0+\Delta z)-f(z_0)}{\Delta z}-f'(z_0)\right|<\varepsilon\]
\[令\rho(\Delta z)=\frac{f(z_0+\Delta z)-f'(z_0)}{\Delta z}-f'(z_0)\]
\[那么\lim_{\Delta z\to0}\rho(\Delta z)=0\]
\[由此f(z_0+\Delta z)-f(z_0)=f'(z_0)\Delta z+\rho(\Delta z)\Delta z\]
\[所以\lim_{\Delta z\to0}f(z_0+\Delta z)=f(z_0)\]
即 $f(z)$ 在 $z_0$ 连续
####3.求导法则
#####(1).四则运算法则
\[[f(z)\pm g(z)]'=f'(z)\pm g'(z)\]
\[[f(z)g(z)]'=f'(z)g(z)+f(z)g'(z)\]
\[\bigg[\frac{f(z)}{g(z)}\bigg]'=\frac{f'(z)g(z)-f(z)g'(z)}{[g(z)]^2},g(z)\neq0\]
\[(z^n)'=zn^{n-1}\]
#####(2).复合函数的求导法则
\[[f(g(z))]'=f'(g(z))g'(z)\]
#####(3).反函数的求导法则
\[\varphi'(w)=\frac1{f'(z)}|_ {z=\varphi(w)}=\frac1{f'[\varphi(w)]}\]
####4.微分的概念
设函数 $\Delta w=f(z_0+\Delta z)$ 在 $z_0$ 可导, 有:
\[\Delta w=f(z_0+\Delta z)-f(z_0)=f'(z_0)\Delta z+\rho(\Delta z)\Delta z\]
其中 $\displaystyle\lim_{\Delta z\to0}\rho(\Delta z)=0$ 因此 $\left|\rho(\Delta z)\Delta z\right|$ 是 $|\Delta z|$ 的高阶无穷小量 而 $f'(z_0)\Delta z$ 是函数 $w=f(z)$ 的变化量 $\Delta w$ 的线性部分 我们称 $f'(z_0)\Delta z$ 为函数 $w=f(z)$ 在点 $z_0$ 的微分, 记作:
\[dw=f'(z_0)\Delta z\]
###ii.解析函数的概念
如果函数 $f(z)$ 在 $z_0$ 及 $z_0$ 的领域内处处可导, 那么称 $f(z)$ 在$z_0$ 解析, 如果 $f(z)$ 区域 $D$ 内每一点解析, 那么称 $f(z)$ 在 $D$ 内解析, 或称 $f(z)$ 是 $D$ 内的一个解析函数(全纯函数或正则函数)

如果 $f(z)$ 在 $z_0$ 不解析, 那么称 $z_0$ 为 $f(z)$ 的 **奇点**

函数在区域内解析与在区域内可导是等价, 但是, 函数在一点解析和在一点处可导是不等价的概念

1. 解析性与可导性的关系: 在一个点的可导性为一个 **局部概念**，而解析性是一个 **整体概念**；
2. 函数在一个点解析，是指在这个点的某个邻域内可导，因此在这个点可导，反之，在一个点的可导不能得到在这个点解析；
3. 闭区域上的解析函数在包含这个区域的一个更大的区域上解析；
####定理
在区域 $D$ 内解析的两个函数 $f(z)$ 与 $g(z)$ 的和, 差, 积, 商(除去分母为零的点)在 $D$ 内解析

设函数 $h=g(z)$ 在 $z$ 平面上的区域 $D$ 内解析, 函数 $w=f(h)$ 在 $h$ 平面上的区域 $G$ 内解析, 如果对 $D$ 内的每一点 $z$, 函数 $g(z)$ 的对应值 $h$ 都属于 $G$, 那么复合函数 $w=f[g(z)]$ 在 $D$ 内解析

所有的多项式在复平面内处处是解析的, 任何一个有理分式函数 $\frac{P(z)}{Q(z)}$ 在不含分母为零的区域内是解析函数, 是分母为零的点是它的奇点
##II.函数解析的充分条件
###1.柯西-黎曼(Cauchy-Riemann)方程:
\[\frac{\partial u}{\partial x}=\frac{\partial v}{\partial y}\quad\frac{\partial u}{\partial y}=-\frac{\partial v}{\partial x}\]

设函数 $f(z)=u(x,y)+iv(x,y)$ 定义在区域 $D$ 内, 则 $f(z)$ 在 $D$ 内一点 $z=x+iy$ 可导的充要条件是 $u(x,y)$ 与 $v(x,y)$ 在点 $(x,y)$ 可微, 并且在该店满足柯西-黎曼方程

函数 $f(z)=u(x,y)+iv(x,y)$ 在点 $z=x+iy$ 处的导数公式:
\[f'(z)=\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial v}=\frac1i\frac{\partial u}{\partial y}+\frac{\partial u}{\partial y}\]

函数 $f(z)=u(x,y)+iv(x,y)$ 在其定义域 $D$ 内解析的充要条件是 $u(x,y)$ 与 $v(x,y)$ 在 $D$ 内可微, 并且满足柯西-黎曼方程
##III.初等函数
###i.指数函数
定义函数f (z)，满足下列三个条件：
1. $f(z)$在复平面内解析;
2. $f'(z)=f(z)$
3. 当 $\Im(z)=0$ 时, $f(z)=e^x$, 其中 $x=\Re(z)$。
\[f(z)=e^x(\cos y+i\sin y)\\f'(z)=f(z)\quad y=0,f(z)=e^x\]
我们称它为指数函数, 记作
\[\text{exp}z=e^x(\cos y+i\sin y)=e^z\]
####指数函数的基本性质
1. $\left|\text{exp}z\right|=e^x$
2. $\text{Arg}(\text{exp}z)=y+2k\pi$
3. $\text{exp}z\neq0$
4. $\text{exp}z_1\cdot\text{exp}z_2=\text{exp}(z_1+z_2)$
5. $\text{exp}z$ 的周期为 $2k\pi i$

\[f(z)=f(x+iy)=e^xf(iy)\\f(iy)=A(y)+iB(y),f(z)=ie^xB(y)\]
由解析性，我们利用柯西-黎曼条件，有
\[A(y)=B'(y),A'(y)=-B(y)\]
所以
\[A(y)=\cos y,B(y)=\sin y\]
因此
\[e^z=e^x(\cos y+i\sin y)\]
我们也重新得到欧拉公式：
\[e^{iy}=\cos y+i\sin y\]
###ii.对数函数
满足 $e^w=z(z\neq0)$ 的函数 $w=f(z)$ 称为 对数函数, 记作 $w=\text{Ln}z$
注解：由于对数函数是指数函数的反函数，而指数函数是周期为 $2\pi i$ 的周期函数，所以对数函数是多值函数。

令 $w=u+iv,z=re^{i\theta}$，则 $e^{u+iv}=re^{i\theta}$所以 $u=\ln r,v=\theta+2k\pi(k=0,\pm1,\pm2\cdots)$即 $w=\ln|z|+i\text{Arg}z$

由于 $\text{Arg}z$ 为多值函数，所以对数函数 $w=f(z)$ 为多值函数，并且每两个值相差 $2\pi i$ 的整数倍，记作
\[\text{Ln}z=\ln|z|+i\text{Arg}z\]
1. 如果规定上式中的 $\text{Arg}z$ 取主值 $\text{arg}z$，则 $\text{Ln}z$ 为一单值函数，记作 $\ln z$，称为 $\text{Ln}z$ 的 **主值**；因此有
\[\ln z=\ln|z|+i\text{arg}z\]
2. 其余各值可由 $\text{Ln}z=\ln z+2k\pi i(k=\pm1,\pm2)$表示；对于每一个固定的 $k$，上式为一单值函数，称为 $\text{Ln}z$ 的一个 **分支**；
3. 特别地, 当 $z=x>0$ 时, $\text{Ln}z$ 的主值 $\ln z=\ln x$ 就是实变数对数函数。
####三种对数函数的联系与区别:
函数|单值与多值|定义域|注解
:--:|:--:|:--:|:--:
$\ln x$|单|所有正实数|
$\text{Ln}z$|多|所有非零复数|一个单值分支为lnz
$\ln z$|单|所有非零复数|z=x>0时，为lnx
####对数函数的基本性质
1. $\text{Ln}(z_1z_2)=\text{Ln}z_1+\text{Ln}z_2$
1. $\displaystyle\text{Ln}\frac{z_1}{z_2}=\text{Ln}z_1-\text{Ln}z_2$
1. $\require{cancel}\cancel{\text{Ln}z^n=n\text{Ln}z}$
1. $\require{cancel}\cancel{\text{Ln}\sqrt[n]{z}=\frac1n\text{Ln}z}$
1. $\displaystyle\frac{d\ln z}{dz}=\frac1z$
####对数函数的单值化:
相应与幅角函数的单值化，我们也可以将对数函数单值化:

考虑复平面除去负实轴（包括0）而得的区域 $D$。显然，在 $D$ 内，对数函数可以分解为无穷多个单值连续分支。
\[w=\text{Ln}z=\ln|z|+i\text{arg}z+2k\pi i=\ln z+2k\pi i\]
由于对数函数的每个单值连续分支都是解析的，所以我们也将它的连续分支称为解析分支。

我们也称对数函数是一个无穷多值解析函数。

我们称原点和无穷远点是对数函数的无穷阶支点(对数支点) 特点：
1. 当 $z$ 绕它们连续变化一周时，$\text{Ln}z$ 连续变化到其它值；
1. 不论如何沿同一方向变化，永远不会回到同一个值。
###iii.乘幂 $a^b$ 与幂函数
设a为不等于0的一个复数，$b$ 为任意一个复数，定义乘幂 $a^b$ 为 $eb^{\text{Ln}a}$, 即
\[a^b=eb^{\text{Ln}a}\]
由于 $\text{Ln}a=\ln|a|+i(\text{arg}a+2k\pi)$ 是多值的,因而 $a^b$ 也是多值的。

当 $b$ 为整数时, 由于
\[a^b=e^{b\text{Ln}a}=e^{b[\ln|a|+i(\text{arg}a+2k\pi)]}\\=e^{b(\ln|a|+i\text{arg}a)+2kb\pi i}=e^{b\ln a}\]
所以这时 $a^b$ 具有单一的值。

当 $b=p/q$ ($p$ 和 $q$ 为互质的整数, $q>0$) 时, 由于
\[a^b=e^{\frac pq\ln|a|+i\frac pq(\text{arg}a+2k\pi)}\\=e^{\frac pq\ln|a|}\big[\cos\frac pq(\text{arg}a+2k\pi)+i\sin\frac pq(\text{arg}a+2k\pi)\big]\]
$a^b$ 具有 $q$ 个值, 即当 $k=0,1\cdots(q-1)$ 时相应的各个值。

除上述情况外此而外, 一般而论，ab具有无穷多个值
####幂函数的基本性质:
