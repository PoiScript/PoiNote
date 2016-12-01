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
\[\mathrm{exp}z=e^x(\cos y+i\sin y)=e^z\]
####指数函数的基本性质
1. $\left|\mathrm{exp}z\right|=e^x$
2. $\mathrm{Arg}(\mathrm{exp}z)=y+2k\pi$
3. $\mathrm{exp}z\neq0$
4. $\mathrm{exp}z_1\cdot\mathrm{exp}z_2=\mathrm{exp}(z_1+z_2)$
5. $\mathrm{exp}z$ 的周期为 $2k\pi i$

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
满足 $e^w=z(z\neq0)$ 的函数 $w=f(z)$ 称为 对数函数, 记作 $w=\mathrm{Ln}z$
注解：由于对数函数是指数函数的反函数，而指数函数是周期为 $2\pi i$ 的周期函数，所以对数函数是多值函数。

令 $w=u+iv,z=re^{i\theta}$，则 $e^{u+iv}=re^{i\theta}$所以 $u=\ln r,v=\theta+2k\pi(k=0,\pm1,\pm2\cdots)$即 $w=\ln|z|+i\mathrm{Arg}z$

由于 $\mathrm{Arg}z$ 为多值函数，所以对数函数 $w=f(z)$ 为多值函数，并且每两个值相差 $2\pi i$ 的整数倍，记作
\[\mathrm{Ln}z=\ln|z|+i\mathrm{Arg}z\]
1. 如果规定上式中的 $\mathrm{Arg}z$ 取主值 $\mathrm{arg}z$，则 $\mathrm{Ln}z$ 为一单值函数，记作 $\ln z$，称为 $\mathrm{Ln}z$ 的 **主值**；因此有
\[\ln z=\ln|z|+i\mathrm{arg}z\]
2. 其余各值可由 $\mathrm{Ln}z=\ln z+2k\pi i(k=\pm1,\pm2)$表示；对于每一个固定的 $k$，上式为一单值函数，称为 $\mathrm{Ln}z$ 的一个 **分支**；
3. 特别地, 当 $z=x>0$ 时, $\mathrm{Ln}z$ 的主值 $\ln z=\ln x$ 就是实变数对数函数。
####三种对数函数的联系与区别:
函数|单值与多值|定义域|注解
:--:|:--:|:--:|:--:
$\ln x$|单|所有正实数|
$\mathrm{Ln}z$|多|所有非零复数|一个单值分支为lnz
$\ln z$|单|所有非零复数|z=x>0时，为lnx
####对数函数的基本性质
1. $\mathrm{Ln}(z_1z_2)=\mathrm{Ln}z_1+\mathrm{Ln}z_2$
1. $\displaystyle\mathrm{Ln}\frac{z_1}{z_2}=\mathrm{Ln}z_1-\mathrm{Ln}z_2$
1. $\require{cancel}\cancel{\mathrm{Ln}z^n=n\mathrm{Ln}z}$
1. $\require{cancel}\cancel{\mathrm{Ln}\sqrt[n]{z}=\frac1n\mathrm{Ln}z}$
1. $\displaystyle\frac{d\ln z}{dz}=\frac1z$
####对数函数的单值化:
相应与幅角函数的单值化，我们也可以将对数函数单值化:

考虑复平面除去负实轴（包括0）而得的区域 $D$。显然，在 $D$ 内，对数函数可以分解为无穷多个单值连续分支。
\[w=\mathrm{Ln}z=\ln|z|+i\mathrm{arg}z+2k\pi i=\ln z+2k\pi i\]
由于对数函数的每个单值连续分支都是解析的，所以我们也将它的连续分支称为解析分支。

我们也称对数函数是一个无穷多值解析函数。

我们称原点和无穷远点是对数函数的无穷阶支点(对数支点) 特点：
1. 当 $z$ 绕它们连续变化一周时，$\mathrm{Ln}z$ 连续变化到其它值；
1. 不论如何沿同一方向变化，永远不会回到同一个值。
###iii.乘幂 $a^b$ 与幂函数
设a为不等于0的一个复数，$b$ 为任意一个复数，定义乘幂 $a^b$ 为 $eb^{\mathrm{Ln}a}$, 即
\[a^b=eb^{\mathrm{Ln}a}\]
由于 $\mathrm{Ln}a=\ln|a|+i(\mathrm{arg}a+2k\pi)$ 是多值的,因而 $a^b$ 也是多值的。

当 $b$ 为整数时, 由于
\[a^b=e^{b\mathrm{Ln}a}=e^{b[\ln|a|+i(\mathrm{arg}a+2k\pi)]}\\=e^{b(\ln|a|+i\mathrm{arg}a)+2kb\pi i}=e^{b\ln a}\]
所以这时 $a^b$ 具有单一的值。

当 $b=p/q$ ($p$ 和 $q$ 为互质的整数, $q>0$) 时, 由于
\[a^b=e^{\frac pq\ln|a|+i\frac pq(\mathrm{arg}a+2k\pi)}\\=e^{\frac pq\ln|a|}\big[\cos\frac pq(\mathrm{arg}a+2k\pi)+i\sin\frac pq(\mathrm{arg}a+2k\pi)\big]\]
$a^b$ 具有 $q$ 个值, 即当 $k=0,1\cdots(q-1)$ 时相应的各个值。

除上述情况外此而外, 一般而论，$a^b$ 具有无穷多个值
1. 当 $b$ 为正整数时 $n$ 根据定义: $a^n=e^{n\mathrm{Ln}a}=e^{\mathrm{Ln}a+\cdots+\mathrm{Ln}a}=e^{\mathrm{Ln}a}\cdots e^{\mathrm{Ln}a}=a\cdots a$
2. 当 $b$ 为分数 $\displaystyle\frac1n$ 时, 有 $\displaystyle a^\frac1n=e^{\frac1n\mathrm{Ln}a}=e^{\frac1n\ln|a|}(\cos\frac{\mathrm{arg}a+2k\pi}n+i\sin\frac{\mathrm{arg}+2k\pi}n)\\\displaystyle=|a|^{\left|\frac1n\right|}(\cos\frac{\mathrm{arg}a+2k\pi}n+i\sin\frac{\mathrm{arg}+2k\pi}n)=\sqrt[n]a,其中k=1,2\cdots(n-1)$

所以, 如果 $a=z$ 为一复变数, 就得到一般的幂函数 $w=z^b$; 当 $b=n与\frac1n$ 时, 就分别得到通常的幂函数 $w=z^n$ 及 $z=w^n$ 的反函数 $w=z^\frac1n=\sqrt[n]z$

幂函数 $z^\frac1n=\sqrt[n]z$ 是一个多值函数, 具有 $n$ 个分支, 由于对数函数 $\mathrm{Ln}z$ 的各个分支在除去原点和复实轴的复平面内是解析的 因而不难看出它的各个分支在除去原点和负实轴的复平面内也是解析的 而且:
\[(z^\frac1n)'=(\sqrt[n]z)'=(e^{\frac1n\mathrm{Ln}z})'=\frac1nz^{\frac1n-1}\]
幂函数 $w=z^b$ (除去 $b=n$ 与 $\frac1n$ 两种情况外) 也是一个多值函数, 当 $b$ 为无理数或复数时, 是无穷多值, 同样的道理, 它的各个分支在去除原点和负实轴的复平面内也是解析的, 并且有 $(z^b)'=bz^{n-1}$
####幂函数的基本性质:
###vi.三角函数和双曲函数
由 **欧拉公式** 有
\[e^{iy}=\cos y+i\sin y\quad e^{-iy}=\cos y-i\sin y\]
将这两式相加与相减, 分别得到
\[\cos y=\frac{e^{iy}+e^{-iy}}2\quad\sin y=\frac{e^{iy}-e^{-iy}}{2i}\]
现将其推广到自变数取复值的情形, 定义
\[\cos z=\frac{e^{iz}+e^{-iz}}2\quad\sin z=\frac{e^{iz}-e^{-iz}}{2i}\]
当 $z$ 为实数时, 显然这与上式完全一致。
####三角函数的性质
#####(1).周期性
由于 $e^z$ 是以 $2\pi i$ 为周期的周期函数,因此 $\cos z$ 和 $\sin z$ 以 $2\pi$ 为周期, 即
\[\cos(z+2\pi)=\frac{e^{i(z+2\pi)}+e^{-i(z+2\pi)}}2=\cos z\]
\[\sin(z+2\pi)=\frac{e^{i(z+2\pi)}-e^{-i(z+2\pi)}}2=\sin z\]
#####(2).奇偶性
$\cos z$ 是偶函数, $\sin z$ 是奇函数
\[\cos(-z)=\cos z\quad\sin(-z)=-\sin z\]
#####(3).求导
\[(\cos z)'=-\sin z\quad(\sin z)'=\cos z\]
#####(4).欧拉公式
\[e^{iz}=\cos z+i\sin z\]
普遍正确, 即对于复数, 欧拉公式仍然成立。
#####(5).加法定理
由定义和指数函数的加法定理，成立：
\[\begin{cases}\cos(z_1+z_2)=\cos z_1\cos z_2-\sin z_1\sin z_2\\
\sin(z_1+z_2)=\sin z_1\cos z_2+\cos z_1\sin z_2\\
\sin^2 z+\cos^2 z=1\end{cases}\]
由此得
\[\cos(x+iy)=\cos x\cos iy-\sin x\sin iy\]
\[\sin(x+iy)=\sin x\cos iy+\cos x\sin iy\]
当 $z$ 为纯虚数 $iy$ 时, 有
\[\begin{cases}\cos iy=\displaystyle\frac{e^{-y}+e^y}2=\cosh y
\\\sin iy=\displaystyle\frac{e^{-y}-e^y}{2i}=i\sinh y\end{cases}\]
所以
\[\cos(x+iy)=\cos x\cosh y-i\sin x\sinh y\\\sin(x+iy)=\sin x\cosh y+i\cos x\sinh y\]
这两个公式对于计算 $\cos z$ 与 $\sin z$ 的值有用。

当 $y\to\infty$ 时， $|\sin iy|$ 和 $|\cos iy|$ 都趋于无穷大，因此，$|\sin z|\leq1$ 和 $|\cos z|\leq1$ 在复数范围内不再成立。

其它复变数三角函数的定义如下:
\[\tan z=\frac{\sin z}{\cos z}\quad\cot z=\frac{\cos z}{\sin z}\\
\sec z=\frac1{\cos z}\quad\csc z=\frac1{\sin z}\]
与三角函数密切相关的是 **双曲函数**, 定义
\[\cosh z=\frac{e^z+e^{-z}}2\quad\sinh z=\frac{e^z-e^{-z}}2\tanh z=\frac{e^z-e^{-z}}{e^z+e^{-z}}\]
分别称为 **双曲余弦**, **正弦和正切函数**。

$\cosh z$ 和 $\sinh z$ 都是以 $2\pi i$ 为周期的函数，$\cosh z$ 偶函数，$\sinh z$ 为奇函数。他们都是复平面内的解析函数。

导数分别为:
\[(\cosh z)'=\sinh z\quad(\sinh z)'=\cosh z\]
不难证明
\[\cosh iy=\cos y,\sinh iy=i\sin y\]
及
\[\cosh(x+iy)=\cosh x\cos y+i\sinh x\sin y\\\sinh(x+iy)=\sinh x\cos y+i\cosh x\sin y\]
###v.反三角函数与反双曲函数
反三角函数定义为三角函数的反函数, 设 $z=\cos w$ 则称 $w$ 为 $z$ 的反余弦函数, 记作:
\[w=\mathrm{Arccos}z\]
由 $z=\cos w=\displaystyle\frac12(e^{iw}+e^{-iw})$, 得二次方程 $e^{2iw}-2ze^{iw}+1=0$, 它的根为 $e^{iw}=z+\sqrt{z^2+1}$ 应理解为 **双值函数**。两端取对数得:
\[\mathrm{Arccos}z=-i\mathrm{Ln}(z+\sqrt{z^2-1})\]
显然 $\mathrm{Arccos}z$ 是一个多值函数，它的多值性正是 $\cos w$ 的偶性和周期性的反映。

用同样的方法可以定义反正弦和反正切函数:
\[\begin{cases}\mathrm{Arcsin}z=-i\mathrm{Ln}(iz+\sqrt{1-z^2})\\\mathrm{Arctan}z=-\displaystyle\frac i2\mathrm{Ln}\frac{1+iz}{1-iz}\end{cases}\]
反双曲函数定义为双曲函数的反函数。用与推导反三角函数表达式完全类似的步骤, 可以得到各反双曲函数的表达式：
\[\begin{cases}\mathrm{Arsinh}z=\mathrm{Ln}(z+\sqrt{z^2+1})&反双曲正弦\\\mathrm{Arcosh}z=\mathrm{Ln}(z+\sqrt{z^2-1})&反双曲余弦\\\mathrm{Artanh}z=\displaystyle\frac12\mathrm{Ln}\frac{1+z}{1-z}&反双曲正切\end{cases}\]
它们都是多值函数。

多值函数导引：幅角函数:
因为初等复变多值函数的多值性是由于辐角的多值性引起的，所以我们先研究辐角函数:
\[w=\mathrm{Arg}z(z\in C\setminus\{0\})\]
它本身不是一般意义下的初等函数。$w=\mathrm{Arg}z$ 函数有无穷个不同的值:
\[w=\mathrm{Arg}z=\mathrm{arg}z+2k\pi(k\in Z),z\neq0\]
其中 $\mathrm{arg}z$ 表示 $\mathrm{Arg}z$ 的主值:(我们也把 $\mathrm{Arg}z$ 的任意一个确定的值记为 $\mathrm{arg}z$)
\[-\pi<\mathrm{arg}z\leq\pi\]
为了研究方便起见，我们把幅角函数在某些区域内分解为一些单值连续函数，每一个单值连续函数称为幅角函数在这区域内的一个单值连续分支。

考虑复平面除去负实轴（包括0）而得的区域 $D$。显然，在 $D$ 内，$\mathrm{Arg}z$ 的主值 $\mathrm{arg}z$ 是一个单值连续函数。

对一个固定的整数 $k$，$\mathrm{arg}z+2k\pi$ 也是一个单值连续函数 。

因此，$w=\mathrm{Arg}z$ 在区域 $D$ 内可以分解成无穷多个单值连续函数，它们都是 $w=\mathrm{Arg}z$ 在 $D$ 内的单值连续分支。

**结论**: 因此，对于幅角函数 $w=\mathrm{Arg}z$，0和无穷远点是特殊的两点。

在复平面上，取连接0和无穷远点的一条无界简单连续曲线 $L$ 作为割线，得到一个区域 $D$，其边界就是曲线 $L$。则可以将 $\mathrm{arg}z$ 分解成一些连续分支：
1. 当 $L$ 为负实轴时，幅角函数可以分解成无穷个单值连续分支；
2. 一般区域见下图：

因此，对于幅角函数 $w=\mathrm{Arg}z$ 可以分解成无穷个单值连续分支 $\mathrm{arg}+2k\pi(\mathrm{z_1}=\theta_1)$

$\mathrm{Arg}z$ 在 $C$ 内上任一点（非原点）的各值之间的联系：通过作一条简单连续曲线围绕0或无穷远点，让 $z$ 从某点按一定方向沿曲线连续变动若干周后，回到该点时，$\mathrm{Arg}z$ 相应地可从幅角函数的一值连续变动到它在预先指定的其它任一值，即从 $\mathrm{Arg}z$ 的一个单值连续分支在该点的值，连续变动到预先指定的其它单值连续分支在该点的值。
